---
solution: Journey Optimizer
product: journey optimizer
title: Integrar o Journey Optimizer a sistemas externos
description: Conheça as práticas recomendadas ao integrar o Journey Optimizer a sistemas externos
role: User
level: Beginner
keywords: externo, API, otimizador, limitação
exl-id: 27859689-dc61-4f7a-b942-431cdf244455
source-git-commit: 40afc1c0e0ae55dfbec45ff0b22170d6345a8e46
workflow-type: tm+mt
source-wordcount: '1201'
ht-degree: 2%

---

# Integrar a sistemas externos {#external-systems}

Esta página apresenta as diferentes medidas de proteção fornecidas pela Journey Optimizer ao integrar um sistema externo, bem como as práticas recomendadas: como otimizar a proteção do sistema externo usando a API de limitação, como configurar o tempo limite da jornada e como as tentativas funcionam.

O Journey Optimizer permite configurar conexões com sistemas externos por meio de fontes de dados personalizadas e ações personalizadas. Isso permite, por exemplo, enriquecer suas jornadas com dados provenientes de um sistema de reservas externo ou enviar mensagens usando um sistema de terceiros, como Epsilon ou Facebook.

Ao integrar um sistema externo, você pode encontrar vários problemas, o sistema pode estar lento, pode parar de responder ou pode não ser capaz de lidar com um grande volume. A Journey Optimizer oferece várias medidas de proteção para proteger seu sistema contra sobrecarga.

Todos os sistemas externos são diferentes em termos de desempenho. Você precisa adaptar a configuração aos seus casos de uso.

Quando o Journey Optimizer executa uma chamada para uma API externa, as medidas de proteção técnicas são executadas da seguinte maneira:

1. As regras de limitação ou limitação são aplicadas: se a taxa máxima for atingida, as chamadas restantes serão descartadas ou enfileiradas.

2. Tempo limite e tentativa: se a regra de limitação for cumprida, o Journey Optimizer tentará executar a chamada até que o fim do tempo limite seja atingido.

## Limitação e limitação de APIs {#capping}

### Sobre APIs de limitação e limitação

Ao configurar uma fonte de dados ou uma ação, você estabelece uma conexão com um sistema para recuperar informações adicionais para usar em suas jornadas ou enviar mensagens ou chamadas de API.

As APIs do Jornada suportam até 5000 eventos por segundo, mas alguns sistemas externos ou APIs podem não ter uma taxa de transferência equivalente. Para evitar sobrecarga desses sistemas, você pode usar o **Limitação** e **Limitação** APIs para limitar o número de eventos enviados por segundo.

Toda vez que uma chamada de API é executada pelo jornada, ela passa pelo mecanismo de API. Se o limite definido na API for atingido, a chamada será rejeitada se você estiver usando a API de limitação ou colocada em fila por até 6 horas e processada o mais rápido possível na ordem em que foi recebida se estiver usando a API de limitação.

Por exemplo, digamos que você tenha definido uma regra de limitação ou limitação de 100 chamadas por segundo para seu sistema externo. Seu sistema é chamado por uma ação personalizada em 10 jornadas diferentes. Se uma jornada receber 200 chamadas por segundo, ela usará os 100 slots disponíveis e descartará ou colocará em fila os 100 slots restantes. Como a taxa máxima foi excedida, as outras 9 jornadas não terão mais nenhum slot. Essa granularidade ajuda a proteger o sistema externo contra sobrecarga e falha.

>[!IMPORTANT]
>
>**Regras de limitação** são configuradas no nível da sandbox, para um endpoint específico (o URL chamado), mas globais para todas as jornadas da sandbox.
>
>**Regras de limitação** são configuradas apenas em sandboxes de produção, para um endpoint específico, mas globais para todas as jornadas em todas as sandboxes. Você pode ter apenas uma configuração de limitação por organização.

Para obter mais informações sobre como trabalhar com as APIs, consulte estas seções:

* [Limitação da API](capping.md)
* [API de limitação](throttling.md)

Uma descrição detalhada das APIs está disponível em [Documentação das APIs do Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/journeys/)

### Fontes de dados e capacidade de ações personalizadas {#capacity}

Para **fontes de dados externas**, o número máximo de chamadas por segundo é limitado a 15. Se esse limite for excedido, as chamadas adicionais serão descartadas ou enfileiradas, dependendo da API em uso. É possível aumentar esse limite para fontes de dados externas privadas entrando em contato com o Adobe para incluir o endpoint na  de lista de permissões, mas essa não é uma opção para fontes de dados externas públicas. * [Saiba como configurar fontes de dados](../datasource/about-data-sources.md).

>[!NOTE]
>
>Se uma fonte de dados usar uma autenticação personalizada com um terminal diferente daquele usado para a fonte de dados, será necessário entrar em contato com o Adobe para também incluir esse terminal na  de lista de permissões.

Para **ações personalizadas**, é necessário avaliar a capacidade da API externa do . Por exemplo, se o Journey Optimizer enviar 1000 chamadas por segundo e o sistema suportar apenas 100 chamadas por segundo, é necessário definir uma configuração de limitação ou limitação para que o sistema não fique saturado. [Saiba como configurar ações](../action/action.md)

## Tempo limite e tentativas{#timeout}

Se a regra de limitação ou limitação for cumprida, a regra de tempo limite será aplicada.

Em cada jornada, é possível definir uma duração de tempo limite. Isso permite definir uma duração máxima ao chamar um sistema externo. A duração do tempo limite é configurada nas propriedades de uma jornada. Consulte [esta página](../building-journeys/journey-gs.md#timeout_and_error).

Esse tempo limite é global para todas as chamadas externas (chamadas de API externas em ações personalizadas e fontes de dados personalizadas). Por padrão, é definido como 30 segundos.

Durante o tempo limite definido, a Journey Optimizer tenta chamar o sistema externo. Após a primeira chamada, um máximo de três tentativas pode ser executado até que o fim do tempo limite seja atingido. Não é possível alterar o número de tentativas.

Cada tentativa usa um slot. Se você tiver um limite de 100 chamadas por segundo e cada uma delas exigir duas tentativas, a taxa cairá para 30 chamadas por segundo (cada chamada usa 3 slots: a primeira chamada e duas tentativas).

O valor da duração do tempo limite depende do caso de uso. Se desejar enviar a mensagem rapidamente, por exemplo, quando o cliente entra na loja, você não quer definir um tempo limite longo. Além disso, quanto mais tempo limite for definido, mais itens serão colocados na fila. Isso pode afetar muito o desempenho. Se o Journey Optimizer executar 1000 chamadas por segundo, manter 5 ou 15 segundos de dados pode dominar rapidamente o sistema.

Vamos tomar um exemplo por um tempo limite de 5 segundos.

* A primeira chamada dura menos de 5 segundos: se a chamada for bem-sucedida, nenhuma tentativa será executada.
* A primeira chamada dura mais de 5 segundos: a chamada é cancelada e não há nova tentativa. Ele é contado como um erro de tempo limite no relatório.
* A primeira chamada falha após 2 segundos (o sistema externo retorna um erro): Restam 3 segundos para tentativas, se os slots de limitação estiverem disponíveis.
   * Se uma das três tentativas for bem-sucedida antes do final dos 5 segundos, a chamada será executada e não haverá erro.
   * Se o fim da duração do tempo limite for atingido durante as tentativas, a chamada será cancelada e contada como um erro de tempo limite no relatório.

## Perguntas frequentes{#faq}

**Como posso configurar uma regra de limitação ou limitação? Existe uma regra padrão?**

Por padrão, não há regra de limitação ou limitação. As regras são definidas no nível da sandbox para um endpoint específico (o URL chamado), usando a API de limitação ou limitação. Consulte [esta seção](../configuration/external-systems.md#capping).

**Quantas tentativas são executadas? Posso alterar o número de tentativas ou definir um período mínimo de espera entre as tentativas?**

Para uma chamada específica, é possível executar no máximo três tentativas após a primeira chamada, até que o tempo limite seja atingido. Não é possível alterar o número de tentativas e o tempo entre cada nova tentativa. Consulte [esta seção](../configuration/external-systems.md#timeout).

**Onde posso configurar o tempo limite? Existe um valor máximo?**

Em cada jornada, é possível definir uma duração de tempo limite. A duração do tempo limite é configurada nas propriedades de uma jornada. A duração do tempo limite deve estar entre 1 segundo e 30 segundos. Consulte [esta seção](../configuration/external-systems.md#timeout) e [esta página](../building-journeys/journey-gs.md#timeout_and_error).