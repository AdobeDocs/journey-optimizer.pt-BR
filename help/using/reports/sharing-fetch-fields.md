---
solution: Journey Optimizer
product: journey optimizer
title: campos de busca de dados de eventos journeyStep
description: campos de busca de dados de eventos journeyStep
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 948fe843-47cf-4b20-976a-48069eb9cf5c
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---

# campos de busca de dados de eventos journeyStep {#sharing-fetch-fields}

Esse grupo de campos será compartilhado por journeyStepEvent e journeyStepProfileEvent.

Durante o processamento de uma etapa, podemos ter N busca de dados em grupos de campos.

## fetchTotalTime {#fetchtotaltime-field}

Tempo total gasto na busca de dados em milis durante o processamento da etapa.

Tipo: long

## fetchTypeInError {#fetchtypeinerror-field}

Define se a busca com erro está na Adobe Experience Platform ou em uma fonte de dados personalizada.

Tipo: string

Valores:
* aep
* custom

## fetchError {#fetcherror-field}

Tipo de erro que ocorre quando a busca de dados é processada.

Tipo: string

Valores:
* http
* limite
* tempo
* erro

## fetchErrorCode {#fetcherrorcode-field}

Código para erro de busca. Apresentar se o erro tiver um código, como um HTTP. Por exemplo, se actionExecError for http, o código 404 representa o erro HTTP 404.

Tipo: string

## fetchOriginError {#fetchoriginerror-field}

Um tempo limite pode ocorrer, em dois casos:

* na primeira tentativa, a ação é executada. Nesse caso, a execução não está concluída, portanto, não há erro subjacente
* em uma nova tentativa: nesse caso, o actionExecOrigError/actionExecOrigErrorCode descreve o erro encontrado na tentativa antes da nova tentativa.

Por exemplo, os dados estão sendo buscados no Serviço de perfil unificado e um erro HTTP 500 é retornado na primeira tentativa. A busca é repetida, mas a duração das 2 tentativas excede o tempo limite. Em seguida, a execução da ação é marcada como tempo limite. A parte de ação terá a seguinte aparência:

```
    ...
    "fetchTypeInError": "aep",
    "fieldgroupIdInError": "MyProfileFieldgroup",
    "fetchError": "timedout",
    "fetchOrigError": "http",
    "fetchOrigErrorCode": "500"
```

Tipo: string

## fetchOriginErrorCode {#fetchoriginerrorcode-field}

O código de erro fornecido pelo sistema [!DNL Journey Optimizer] O está consultando o . Por exemplo, pode ser 404, 500 etc.

Tipo: string

## fetchCount {#fetchcount-field}

Quantas vezes os dados são buscados, independentemente do tipo de fonte.

Tipo: long

## fetchPlatformTotalTime {#fetchplatformtotaltime-field}

O tempo total necessário para buscar os dados da Adobe Experience Platform em millis. Observação: esse tempo é calculado a partir do momento em que o mecanismo envia o evento de enriquecimento ao serviço de enriquecimento e recebe a resposta.

Tipo: long

## fetchPlatformCount {#fetchplatformcount-field}

Quantas vezes os dados são buscados na Adobe Experience Platform.

Tipo: long

## fetchCustomTotalTime {#fetchcustomtotaltime-field}

Quantidade de tempo para buscar os dados personalizados em millis. Observação: esse período é calculado a partir do momento em que o mecanismo envia o evento de enriquecimento ao serviço de enriquecimento e recebe a resposta

Tipo: long

## fetchCustomCount {#fetchcustomcount-field}

Quantas vezes os dados personalizados são buscados em sistemas externos.

Tipo: long
