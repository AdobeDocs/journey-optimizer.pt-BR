---
title: campos de busca de dados de eventos journeyStep
description: campos de busca de dados de eventos journeyStep
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 7%

---

# campos de busca de dados de eventos journeyStep {#sharing-fetch-fields}

![](../assets/do-not-localize/badge.png)

Esse mixin será compartilhado por journeyStepEvent e journeyStepProfileEvent.

Durante o processamento de uma etapa, podemos ter N busca de dados em grupos de campos.

## fetchTotalTime

Tempo total gasto na busca de dados em milis durante o processamento da etapa.

Tipo: long

## fetchTypeInError

Define se a busca com erro está no Adobe Experience Platform ou em uma fonte de dados personalizada.

Tipo: sequência de caracteres

Valores:
* aep
* custom

## fetchError

Tipo de erro que ocorre quando a busca de dados é processada.

Tipo: sequência de caracteres

Valores:
* http
* limite
* tempo
* error

## fetchErrorCode

Código para erro de busca. Apresentar se o erro tiver um código, como um HTTP. Por exemplo, se actionExecError for http, o código 404 representa o erro HTTP 404.

Tipo: sequência de caracteres

## fetchOriginError

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

Tipo: sequência de caracteres

## fetchOriginErrorCode

O código de erro fornecido pelo sistema [!DNL Journey Orchestration] está consultando. Por exemplo, pode ser 404, 500 etc.

Tipo: sequência de caracteres

## fetchCount

Quantas vezes os dados são buscados, independentemente do tipo de fonte.

Tipo: long

## fetchPlatformTotalTime

O tempo total necessário para buscar os dados do Adobe Experience Platform em millis. Observação: esse tempo é calculado a partir do momento em que o mecanismo envia o evento de enriquecimento ao serviço de enriquecimento e recebe a resposta.

Tipo: long

## fetchPlatformCount

Quantas vezes os dados são buscados no Adobe Experience Platform.

Tipo: long

## fetchCustomTotalTime

Quantidade de tempo para buscar os dados personalizados em millis. Observação: esse período é calculado a partir do momento em que o mecanismo envia o evento de enriquecimento ao serviço de enriquecimento e recebe a resposta

Tipo: long

## fetchCustomCount

Quantas vezes os dados personalizados são buscados em sistemas externos.

Tipo: long
