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
source-git-commit: d4ecfecdc74c26890658d68d352c36b75f7c9039
workflow-type: tm+mt
source-wordcount: '1219'
ht-degree: 32%

---

# Integrar a sistemas externos {#external-systems}

Esta página apresenta as diferentes medidas de proteção fornecidas pelo Journey Optimizer ao integrar um sistema externo, bem como as práticas recomendadas: como otimizar a proteção do sistema externo usando a API de limite, como configurar o tempo limite do jornada e como as tentativas funcionam.

O Journey Optimizer permite configurar conexões com sistemas externos por meio de fontes de dados personalizadas e ações personalizadas. Isso permite, por exemplo, enriquecer suas jornadas com dados provenientes de um sistema de reservas externo ou enviar mensagens usando um sistema de terceiros, como Epsilon ou Facebook.

Ao integrar um sistema externo, você pode encontrar vários problemas, o sistema pode ficar lento, pode parar de responder ou pode não ser capaz de lidar com um grande volume. A Journey Optimizer oferece várias medidas de proteção para proteger seu sistema contra sobrecarga.

Todos os sistemas externos são diferentes em termos de desempenho. Você precisa adaptar a configuração aos seus casos de uso.

Quando o Journey Optimizer executa uma chamada para uma API externa, as medidas de proteção técnica são executadas da seguinte maneira:

1. As regras de limitação ou limitação são aplicadas: se a taxa máxima for atingida, as chamadas restantes serão descartadas ou colocadas em fila.

2. Tempo limite e tentativa de repetição: se a regra de limitação ou limitação for atendida, o Journey Optimizer tentará executar a chamada até que o final da duração do tempo limite seja atingido.

## APIs de limitação e limitação {#capping}

### Sobre APIs de limitação e limitação

Ao configurar uma fonte de dados ou uma ação, você estabelece uma conexão com um sistema para recuperar informações adicionais e usar em suas jornadas ou enviar mensagens ou chamadas de API.

As APIs de jornadas comportam até 5000 eventos por segundo, mas alguns sistemas externos ou APIs podem não ter uma taxa de transferência equivalente. Para evitar sobrecarga desses sistemas, você pode usar o **Limite** e **Limitação** APIs para limitar o número de eventos enviados por segundo.

Toda vez que uma chamada de API é executada pelas jornadas, ela passa pelo mecanismo da API. Se o limite definido na API for atingido, a chamada será rejeitada se você estiver usando a API de limitação ou colocada em fila por até 6 horas e processada assim que possível na ordem em que foi recebida se você estiver usando a API de limitação.

Por exemplo, digamos que você tenha definido uma regra de limite ou limitação de 100 chamadas por segundo para seu sistema externo. Seu sistema é chamado por uma ação personalizada em 10 jornadas diferentes. Se uma jornada receber 200 chamadas por segundo, ela usará os 100 slots disponíveis e descartará ou colocará em fila os 100 slots restantes. Como a taxa máxima foi excedida, não restará nenhum slot para as outras 9 jornadas. Essa granularidade ajuda a proteger o sistema externo contra sobrecarga e falhas.

>[!IMPORTANT]
>
>As **regras de limite** são configuradas no nível da sandbox para um ponto de acesso específico (o URL chamado), porém, são globais para todas as jornadas dessa sandbox. O limite está disponível em fontes de dados e ações personalizadas.
>
>As **regras de limitação** são configuradas apenas em sandboxes de produção para um ponto de acesso específico, porém, são globais para todas as jornadas em todas as sandboxes. Você pode ter apenas uma configuração de limitação por organização. A limitação só está disponível em ações personalizadas.

Para obter mais informações sobre como trabalhar com as APIs, consulte estas seções:

* [API de limite](capping.md)
* [API de limitação](throttling.md)

Uma descrição detalhada das APIs está disponível em [Documentação das APIs do Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/journeys/)

### Capacidade de ações personalizadas e fontes de dados {#capacity}

Para **fontes de dados externas**, o número máximo de chamadas por segundo é limitado a 15. Se esse limite for excedido, as chamadas adicionais serão descartadas ou enfileiradas, dependendo da API utilizada. É possível aumentar esse limite para fontes de dados externas privadas entrando em contato com a Adobe para incluir o ponto de acesso na lista de permissões, mas essa não é uma opção para fontes de dados externas públicas. * [Saiba como configurar fontes de dados](../datasource/about-data-sources.md).

>[!NOTE]
>
>Se uma fonte de dados usar uma autenticação personalizada com um ponto de acesso diferente daquele usado para a fonte de dados, também será necessário entrar em contato com a Adobe para incluir esse ponto de acesso na lista de permissões.

Para **ações personalizadas**, é necessário avaliar a capacidade de sua API externa. Por exemplo, se o Journey Optimizer envia 1000 chamadas por segundo e o sistema permite apenas 100 chamadas por segundo, é necessário definir uma configuração de limite ou limitação para não sobrecarregar o sistema. [Saiba como configurar ações](../action/action.md)

## Tempo limite e tentativas{#timeout}

Se a regra de limitação ou limitação for atendida, a regra de tempo limite será aplicada.

Em cada jornada, é possível definir uma duração de tempo limite. Isso permite definir uma duração máxima ao chamar um sistema externo. A duração do tempo limite é configurada nas propriedades de uma jornada. Consulte [esta página](../building-journeys/journey-gs.md#timeout_and_error).

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

## Perguntas frequentes{#faq}

**Como posso configurar uma regra de limitação ou limitação? Há uma regra padrão?**

Por padrão, não há regra de limitação. As regras são definidas no nível da sandbox para um endpoint específico (o URL chamado), usando a API de limitação ou limitação. Consulte [esta seção](../configuration/external-systems.md#capping).

**Quantas tentativas são executadas? Posso alterar o número de tentativas ou definir um período mínimo de espera entre tentativas?**

Para uma determinada chamada, um máximo de três tentativas pode ser executado após a primeira chamada, até que a duração do tempo limite seja atingida. O número de tentativas e o tempo entre cada nova tentativa não podem ser alterados. Consulte [esta seção](../configuration/external-systems.md#timeout).

**Onde posso configurar o tempo limite? Há um valor máximo?**

Em cada jornada, é possível definir uma duração de tempo limite. A duração do tempo limite é configurada nas propriedades de uma jornada. A duração do tempo limite deve estar entre 1 segundo e 30 segundos. Consulte [nesta seção](../configuration/external-systems.md#timeout) e [esta página](../building-journeys/journey-gs.md#timeout_and_error).