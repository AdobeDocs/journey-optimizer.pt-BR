---
solution: Journey Optimizer
product: journey optimizer
title: campos de execução de ação de eventos journeyStep
description: campos de execução de ação de eventos journeyStep
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 273cda84-0261-4c5b-b5f4-0202e8874d05
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 13%

---

# campos de execução de ação de eventos journeyStep {#sharing-execution-fields}

Esse grupo de campos será compartilhado por journeyStepEvent e journeyStepProfileEvent.

Se a etapa tiver uma ação a ser processada, esses campos serão adicionados ao payload do evento.

## actionID {#actionid-field}

ID da ação que está sendo executada.

Tipo: sequência de caracteres

## actionName {#actionname-field}

Nome da ação. Se nenhum nome tiver sido definido, o stepName será executado.

Tipo: sequência de caracteres

## actionType {#actionType-field}

Tipo da ação.

Tipo: sequência de caracteres

## actionParameterized {#actionparameterized-field}

Indica se a ação está parametrizada ou não.

Tipo: booleano

## actionExecutionTime {#actionexecutiontime-field}

O tempo (em milissegundos) necessário para executar uma ação atual.

Tipo: long

## actionExecutionError {#actionexecutionerror-field}

Tipo de erro que ocorre quando a ação é chamada.

Tipo: sequência de caracteres

Valores:
* http
* limite
* timeout
* error

## actionExecutionErrorCode {#actionexecutionerrorcode-field}

Código para erro de execução de ação. Apresentar se o erro tiver um código, como um HTTP.

Tipo: sequência de caracteres

## actionExecutionOriginError {#actionexecutionoriginerror-field}

Um tempo limite pode ocorrer, em dois casos:

* na primeira tentativa, uma ação é executada. Nesse caso, a execução não está concluída, portanto, não há erro subjacente
* em uma nova tentativa: nesse caso, o actionExecOrigError/actionExecOrigErrorCode descreve o erro encontrado na tentativa antes da nova tentativa.

Por exemplo, um email está sendo enviado e um erro HTTP 500 é retornado na primeira tentativa. A busca é repetida, mas a duração das 2 tentativas excede o tempo limite. Em seguida, a execução da ação é marcada como tempo limite. A parte de ação terá a seguinte aparência:

```
    ...
    "actionId": "myActionId",
    "actionName": "My mail sending",
    "actionType": "acsRestAction",
    "actionParameterized": true,
    "actionExecError": "timedout",
    "actionExecOrigError": "http",
    "actionExecOrigErrorCode": "500"
```

Tipo: sequência de caracteres

## actionExecutionOriginCode {#actionexecutionorigincode-field}

Código de erro de actionExecOrigError.

Tipo: sequência de caracteres

## actionBusinessType {#actionbusinesstype-field}

Indica o tipo de ação.

Valores:

* construção
* Email ACS
* SMS ACS
* Envio ACS
* cliente
* Epsilon
* ...

Tipo: sequência de caracteres

## deliveryJobID {#deliveryjobid-field}

Este artigo descreve a ID de trabalho de delivery para a Jornada em lote.

Tipo: sequência de caracteres

## batchDeliveryID {#batchdeliveryid-field}

Este artigo descreve a ID de delivery da Jornada em lote.

Tipo: sequência de caracteres

## fromSegmentTrigger {#fromsegmenttrigger-field}

Isso descreve se a Jornada em lote é acionada pelo Segmento do público-alvo.

Tipo: booleano

## actionSchedulerCount {#actionschedulercount-field}

Contagem de solicitações de notificação do programador enviadas ao serviço do programador durante o processamento da etapa.

Tipo: long
