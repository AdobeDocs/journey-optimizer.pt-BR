---
solution: Journey Optimizer
product: journey optimizer
title: campos de busca de dados de eventos journeyStep
description: campos de busca de dados de eventos journeyStep
feature: Journeys, Reporting
topic: Content Management
role: Data Engineer, Data Architect, Admin
level: Experienced
exl-id: 948fe843-47cf-4b20-976a-48069eb9cf5c
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

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
* erro

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

O código de erro fornecido pelo sistema [!DNL Journey Optimizer] O está consultando. Por exemplo, pode ser um 404, 500, etc.

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
