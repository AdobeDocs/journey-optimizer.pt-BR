---
solution: Journey Optimizer
product: journey optimizer
title: campos de busca de dados de eventos journeyStep
description: campos de busca de dados de eventos journeyStep
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 948fe843-47cf-4b20-976a-48069eb9cf5c
TQID: https://experienceleague.adobe.com/obaiLWD6yq0dZ5ZhE69q-iLHzI99ll7XJnMNlOpJp1A
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a9f73820-6899-47c2-a597-3fec28ab756aid: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2: id: d145add9-d5b9-481b-aa8a-e15e6bb7f813id: a7289281-9ae4-47b1-b8cf-4028b98af776id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 377
ht-degree: 4%

---

# campos de busca de dados de eventos journeyStep {#sharing-fetch-fields}

Este grupo de campos será compartilhado por journeyStepEvent e journeyStepProfileEvent.

Durante um processamento de etapa, podemos ter N busca de dados em grupos de campos.

## fetchTotalTime {#fetchtotaltime-field}

Tempo total gasto na busca de dados em milissegundos durante o processamento da etapa.

Tipo: longo

## fetchTypeInError {#fetchtypeinerror-field}

Define se a busca com erro está no Adobe Experience Platform ou em uma fonte de dados personalizada.

Tipo: sequência de caracteres

Valores:

* aep
* personalizado

## fetchError {#fetcherror-field}

Tipo de erro que ocorre quando a busca de dados é processada.

Tipo: sequência de caracteres

Valores:

* http
* limite
* tempo limite
* error

## fetchErrorCode {#fetcherrorcode-field}

Código do erro de busca. Presente se o erro tiver um código, como um HTTP. Por exemplo, se actionExecError for http, o código 404 representará o erro HTTP 404.

Tipo: sequência de caracteres

## fetchOriginError {#fetchoriginerror-field}

Um tempo limite pode ocorrer, em dois casos:

* na primeira tentativa, a ação é executada. Nesse caso, a execução não é concluída, portanto, não há erro subjacente
* em uma tentativa: nesse caso, actionExecOrigError/actionExecOrigErrorCode descreve o erro encontrado na tentativa antes da tentativa.

Por exemplo, os dados estão sendo obtidos do Unified Profile Service e um erro HTTP 500 é retornado na primeira tentativa. A busca é repetida, mas a duração das 2 tentativas excede o tempo limite. Em seguida, a execução da ação é marcada como tempo limite. A parte da ação será semelhante a:

```
    ...
    "fetchTypeInError": "aep",
    "fieldgroupIdInError": "MyProfileFieldgroup",
    "fetchError": "timedout",
    "fetchOrigError": "http",
    "fetchOrigErrorCode": "500"
```

Tipo: sequência de caracteres

## fetchOriginErrorCode {#fetchoriginerrorcode-field}

O código de Erro fornecido pelo sistema [!DNL Journey Optimizer] está consultando. Por exemplo, pode ser um 404, 500, etc.

Tipo: sequência de caracteres

## fetchCount {#fetchcount-field}

Quantas vezes os dados são obtidos, independentemente do tipo de fonte.

Tipo: longo

## fetchPlatformTotalTime {#fetchplatformtotaltime-field}

A quantidade total de tempo gasto para buscar os dados do Adobe Experience Platform em milhões. Observação: este período é calculado a partir do momento em que o mecanismo envia o evento de enriquecimento ao serviço de enriquecimento e recebe a resposta.

Tipo: longo

## fetchPlatformCount {#fetchplatformcount-field}

Quantas vezes os dados são obtidos do Adobe Experience Platform.

Tipo: longo

## fetchCustomTotalTime {#fetchcustomtotaltime-field}

Tempo para buscar os dados personalizados em milissegundos. Observação: este período é calculado a partir do momento em que o mecanismo envia o evento de enriquecimento ao serviço de enriquecimento e recebe a resposta

Tipo: longo

## fetchCustomCount {#fetchcustomcount-field}

Quantas vezes os dados personalizados são obtidos de sistemas externos.

Tipo: longo
