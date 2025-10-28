---
solution: Journey Optimizer
product: journey optimizer
title: Integrar o Journey Optimizer a sistemas externos
description: Conheça as práticas recomendadas ao integrar o Journey Optimizer com sistemas externos
feature: Integrations
role: User
level: Beginner
keywords: external, API, otimizer, capping
exl-id: 27859689-dc61-4f7a-b942-431cdf244455
source-git-commit: cef105e55f3353c616e18be84faa0ee774aeac06
workflow-type: tm+mt
source-wordcount: '1654'
ht-degree: 19%

---

# Integrar a sistemas externos {#external-systems}

Esta página apresenta as diferentes medidas de proteção fornecidas pelo Journey Optimizer ao integrar um sistema externo, bem como as práticas recomendadas: como otimizar a proteção do sistema externo usando a API de limite, como configurar o tempo limite do jornada e como as tentativas funcionam.

O Journey Optimizer permite configurar conexões com sistemas externos por meio de fontes de dados personalizadas e ações personalizadas. Isso permite, por exemplo, enriquecer suas jornadas com dados provenientes de um sistema de reservas externo ou enviar mensagens usando um sistema de terceiros, como Epsilon ou Facebook.

Ao integrar um sistema externo, você pode encontrar vários problemas, o sistema pode ficar lento, pode parar de responder ou pode não ser capaz de lidar com um grande volume. A Journey Optimizer oferece várias medidas de proteção para proteger seu sistema contra sobrecarga.

Todos os sistemas externos são diferentes em termos de desempenho. Você precisa adaptar a configuração aos seus casos de uso.

Quando o Journey Optimizer executa uma chamada para uma API externa, as medidas de proteção técnica são executadas da seguinte maneira:

1. As regras de limitação ou limitação são aplicadas: se a taxa máxima for atingida, as chamadas restantes serão descartadas ou colocadas em fila.

1. Tempo limite e tentativa de repetição: se a regra de limitação ou limitação for atendida, o Journey Optimizer tentará executar a chamada até que o final da duração do tempo limite seja atingido.

>[!TIP]
>
>Recomendamos deixar pelo menos um buffer de um minuto entre o período de expiração do token da API externa e a configuração [`cacheDuration` do Journey Optimizer &#x200B;](../datasource/external-data-sources.md#custom-authentication-access-token), especialmente em cargas de trabalho pesadas, para evitar incompatibilidades de expiração e erros 401.

## APIs de limitação e limitação {#capping}

### Sobre APIs de limitação e limitação

Ao configurar uma fonte de dados ou uma ação, você estabelece uma conexão com um sistema para recuperar informações adicionais e usar em suas jornadas ou enviar mensagens ou chamadas de API.

As APIs de jornadas comportam até 5.000 eventos por segundo, mas alguns sistemas externos ou APIs podem não ter uma taxa de transferência equivalente. Para evitar sobrecarga desses sistemas, você pode usar as APIs **Limite** e **Limitação** para limitar o número de eventos enviados por segundo.

Toda vez que uma chamada de API é executada pelas jornadas, ela passa pelo mecanismo da API. Se o limite definido na API for atingido, a chamada será rejeitada se você estiver usando a API de limitação ou colocada em fila por até 6 horas e processada assim que possível na ordem em que foi recebida se você estiver usando a API de limitação.

Por exemplo, digamos que você tenha definido uma regra de limitação ou limitação de 200 chamadas por segundo para o sistema externo. Seu sistema é chamado por uma ação personalizada em 10 jornadas diferentes. Se uma jornada receber 300 chamadas por segundo, ela usará os 200 slots disponíveis e descartará ou colocará em fila os 100 slots restantes. Como a taxa máxima foi excedida, não restará nenhum slot para as outras 9 jornadas. Essa granularidade ajuda a proteger o sistema externo contra sobrecarga e falhas.

>[!IMPORTANT]
>
>**As regras de limitação** são configuradas no nível da sandbox para um terminal específico (a URL chamada), mas global para todas as jornadas dessa sandbox. O limite está disponível em fontes de dados e ações personalizadas.
>
>As **regras de limitação** são configuradas apenas em sandboxes de produção para um ponto de acesso específico, porém, são globais para todas as jornadas em todas as sandboxes. Você pode ter apenas uma configuração de limitação por organização. A limitação só está disponível em ações personalizadas.
>
>O valor **maxCallsCount** deve ser maior que 1.

Para obter mais informações sobre como trabalhar com as APIs, consulte estas seções:

* [API de limite](capping.md)
* [API de limitação](throttling.md)

Uma descrição detalhada das APIs está disponível na [documentação das APIs do Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/journeys/)

### Capacidade de ações personalizadas e fontes de dados {#capacity}

Para **fontes de dados externas**, o número máximo de chamadas por segundo é limitado a 15. Se esse limite for excedido, as chamadas adicionais serão descartadas ou enfileiradas, dependendo da API utilizada. É possível aumentar esse limite para fontes de dados externas privadas entrando em contato com a Adobe para incluir o ponto de acesso na lista de permissões, mas essa não é uma opção para fontes de dados externas públicas. * [Saiba como configurar fontes de dados](../datasource/about-data-sources.md).

>[!NOTE]
>
>Se uma fonte de dados usar uma autenticação personalizada com um ponto de acesso diferente daquele usado para a fonte de dados, também será necessário entrar em contato com a Adobe para incluir esse ponto de acesso na lista de permissões.

Para **ações personalizadas**, é necessário avaliar a capacidade de sua API externa. Por exemplo, se o Journey Optimizer enviar 1000 chamadas por segundo e seu sistema suportar apenas 200 chamadas por segundo, será necessário definir uma configuração de limitação para que seu sistema não fique saturado. [Saiba como configurar ações](../action/action.md)

>[!NOTE]
>
>Como as respostas agora são compatíveis, você deve usar ações personalizadas em vez de fontes de dados para casos de uso de fontes de dados externas. Para obter mais informações sobre respostas, consulte esta [seção](../action/action-response.md)

## Endpoints com tempo de resposta lento {#response-time}

Quando um ponto de extremidade tem um tempo de resposta superior a 0,75 segundos, suas chamadas de ação personalizadas são roteadas por um **serviço de ação personalizada lenta** dedicado em vez do serviço padrão.

Esse serviço de ação personalizada lenta aplica um limite de 150.000 chamadas a cada 30 segundos. O limite é aplicado usando uma janela deslizante, que pode começar a qualquer milissegundo dentro desse período de 30 segundos. Quando a janela estiver cheia, as chamadas adicionais serão rejeitadas com erros de limite. O sistema não espera pelo próximo intervalo fixo, mas começa a limitar imediatamente depois que o limite de 30 segundos é atingido.

Como endpoints lentos podem causar atrasos em todas as ações em fila no pipeline, é recomendável não configurar ações personalizadas com endpoints com tempos de resposta lentos. O roteamento dessas ações para o serviço lento ajuda a proteger o desempenho geral do sistema e impede a latência adicional de outras ações personalizadas.

## Tempo limite e tentativas {#timeout}

Se a regra de limitação ou limitação for atendida, a regra de tempo limite será aplicada.

Em cada jornada, é possível definir uma duração de tempo limite. Isso permite definir uma duração máxima ao chamar um sistema externo. A duração do tempo limite é configurada nas propriedades de uma jornada. Consulte [esta página](../building-journeys/journey-properties.md#timeout_and_error).

Esse tempo limite é global para todas as chamadas externas (chamadas de API externas em ações personalizadas e fontes de dados personalizadas). Por padrão, é definido como 30 segundos.

Durante o tempo limite definido, o Journey Optimizer tenta chamar o sistema externo. Após a primeira chamada, um máximo de três tentativas pode ser executado até que a duração do tempo limite seja atingida. O número de tentativas não pode ser alterado.

Cada tentativa usa um slot. Se você tiver um limite de 100 chamadas por segundo e cada uma das chamadas exigir duas tentativas, a taxa cai para 30 chamadas por segundo (cada chamada usa 3 slots: a primeira chamada e duas tentativas).

O valor de duração do tempo limite depende do caso de uso. Se você quiser enviar a mensagem rapidamente, por exemplo, quando o cliente entrar na loja, não desejará configurar um tempo limite longo. Além disso, quanto maior for o tempo limite, mais itens serão colocados na fila. Isso pode afetar muito o desempenho. Se o Journey Optimizer realizar 1.000 chamadas por segundo, manter 5 ou 15 segundos de dados pode sobrecarregar rapidamente o sistema.

Vamos ver um exemplo para um tempo limite de 5 segundos.

* A primeira chamada dura menos de 5 segundos: a chamada é bem-sucedida, não há nova tentativa.
* A primeira chamada dura mais de 5 segundos: a chamada é cancelada e não há nenhuma tentativa. É contado como um erro de tempo limite no relatório.
* A primeira chamada falha após 2 segundos (o sistema externo retorna um erro): restam 3 segundos para tentativas, se os slots de limite estiverem disponíveis.
   * Se uma das três tentativas for bem-sucedida antes do final dos 5 segundos, a chamada será executada e não haverá erro.
   * Se o fim da duração do tempo limite for atingido durante as tentativas, a chamada será cancelada e contada como um erro de tempo limite no relatório.

## Perguntas frequentes {#faq}

Você encontrará abaixo perguntas frequentes sobre a integração do Journey Optimizer com sistemas externos.

Precisa de mais detalhes? Use as opções de feedback na parte inferior desta página para fazer sua pergunta ou conecte-se com a [comunidade Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=pt){target="_blank"}.

+++ Como posso configurar uma regra de limitação ou limitação? Há uma regra padrão?

Para criar regras de limitação ou limitação, consulte [esta seção](../configuration/external-systems.md#capping). Por padrão, não há regra de limitação, mas um limite de 300.000 chamadas em um minuto definido para todas as ações personalizadas, por host e por sandbox. Esse limite foi definido com base no uso pelos clientes, para proteger pontos de acesso externos direcionados por ações personalizadas. Se necessário, é possível substituir essa configuração definindo um limite máximo ou limite maior por meio das APIs de Limite/Limitação.

+++

+++ Quantas tentativas são executadas? Posso alterar o número de tentativas ou definir um período mínimo de espera entre tentativas?

Para uma determinada chamada, um máximo de três tentativas pode ser executado após a primeira chamada, até que a duração do tempo limite seja atingida. O número de tentativas e o tempo entre cada nova tentativa não podem ser alterados. Consulte [esta seção](../configuration/external-systems.md#timeout).

+++

+++ Onde posso configurar o tempo limite? Há um valor máximo?

Em cada jornada, é possível definir uma duração de tempo limite. A duração do tempo limite é configurada nas propriedades de uma jornada. A duração do tempo limite deve estar entre 1 segundo e 30 segundos. Consulte [esta seção](../configuration/external-systems.md#timeout) e [esta página](../building-journeys/journey-properties.md#timeout_and_error).

+++

+++ Qual é o número máximo de conexões abertas pelo Journey Optimizer quando ações personalizadas são usadas?

Com o proxy IP habilitado e uma configuração de limitação definida no endpoint de destino, o número de conexões é baseado na taxa (que são estimativas, números não garantidos):

* entre 200 e 2000 c/s: 50 conexões
* entre 2000 e 3000: 75 conexões
* entre 3000 e 4000: 100 conexões
* entre 4000 e 5000: 125 conexões

Se nenhuma configuração de limitação for definida em um endpoint, o mecanismo da Journey Optimizer será dimensionado para aumentar e chegar a um número alto de conexões (mais de 2.000). Para obter um número limitado de conexões, os clientes precisam usar uma configuração de limitação.

+++
