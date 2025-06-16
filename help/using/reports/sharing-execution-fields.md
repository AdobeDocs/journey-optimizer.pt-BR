---
solution: Journey Optimizer
product: journey optimizer
title: campos de execução de ação de eventos journeyStep
description: campos de execução de ação de eventos journeyStep
feature: Journeys, Reporting
topic: Content Management
role: Data Engineer, Data Architect, Admin
level: Experienced
exl-id: 273cda84-0261-4c5b-b5f4-0202e8874d05
source-git-commit: 91835d5b8b1f129c83c79613df30d9413db98ffe
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 4%

---

# campos de execução de ação de eventos journeyStep {#sharing-execution-fields}

Este grupo de campos será compartilhado por journeyStepEvent e journeyStepProfileEvent.

Se a etapa tiver uma ação a ser processada, esses campos serão adicionados à carga do evento.

## actionID {#actionid-field}

ID da ação que está sendo executada.

Tipo: sequência de caracteres

## actionName {#actionname-field}

Nome da ação. Se nenhum nome tiver sido definido, stepName será usado.

Tipo: sequência de caracteres

## actionType {#actionType-field}

Tipo de ação.

Tipo: sequência de caracteres

## actionParameterized {#actionparameterized-field}

Indica se a ação tem ou não parâmetros.

Tipo: booleano

## actionExecutionTime {#actionexecutiontime-field}

O tempo (em milissegundos) necessário para executar uma ação atual.

Tipo: longo

O campo `actionExecutionTime` representa o tempo total (em milissegundos) necessário para executar a ação, incluindo o tempo que a solicitação gastou aguardando na fila (se a limitação estiver configurada e o limite de taxa for atingido) e o tempo de execução real (incluindo a latência de rede para o ponto de extremidade externo).

O campo `Timestamp` indica a hora de término da execução da ação. Para determinar quando o perfil entrou no nó de ação personalizada, subtraia `actionExecutionTime` de `Timestamp`.

Por exemplo, se `Timestamp` for &quot;2025-02-04 09:39:03 UTC&quot; e `actionExecutionTime` for 1.813.227 ms (~31 minutos), o perfil entrou no nó em aproximadamente &quot;2025-02-04 09:08:32 UTC&quot;.




## actionExecutionError {#actionexecutionerror-field}

Tipo de erro que ocorre quando a ação é chamada.

Tipo: sequência de caracteres

Valores:
* http
* limite
* timeout
* erro

## actionExecutionErrorCode {#actionexecutionerrorcode-field}

Código do erro de execução da ação. Presente se o erro tiver um código, como um HTTP.

Tipo: sequência de caracteres

## actionExecutionOriginError {#actionexecutionoriginerror-field}

Um tempo limite pode ocorrer, em dois casos:

* na primeira tentativa, uma ação é executada. Nesse caso, a execução não é concluída, portanto, não há erro subjacente
* em uma tentativa: nesse caso, actionExecOrigError/actionExecOrigErrorCode descreve o erro encontrado na tentativa antes da tentativa.

Por exemplo, um email está sendo enviado e um erro HTTP 500 é retornado na primeira tentativa. A busca é repetida, mas a duração das 2 tentativas excede o tempo limite. Em seguida, a execução da ação é marcada como tempo limite. A parte da ação será semelhante a:

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

Código de erro do actionExecOrigError.

Tipo: sequência de caracteres

## actionBusinessType {#actionbusinesstype-field}

Indica o tipo de ação.

Valores:

* interno
* Email do ACS
* SMS DO ACS
* ACS Push
* cliente
* Épsilon
* ...

Tipo: sequência de caracteres

## deliveryJobID {#deliveryjobid-field}

Isso descreve a ID da tarefa de entrega para a Jornada em lote.

Tipo: sequência de caracteres

## batchDeliveryID {#batchdeliveryid-field}

Isso descreve a Id de delivery da Jornada em lote.

Tipo: sequência de caracteres

## fromSegmentTrigger {#fromsegmenttrigger-field}

Descreve se a Jornada em lote é acionada a partir do segmento do público-alvo.

Tipo: booleano

## actionSchedulerCount {#actionschedulercount-field}

Contagem de solicitações de notificação do agendador enviadas ao serviço do agendador durante o processamento da etapa.

Tipo: longo
