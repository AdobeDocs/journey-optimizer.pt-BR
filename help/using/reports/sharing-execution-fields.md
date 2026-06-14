---
solution: Journey Optimizer
product: journey optimizer
title: campos de execução de ação de eventos journeyStep
description: campos de execução de ação de eventos journeyStep
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 273cda84-0261-4c5b-b5f4-0202e8874d05
TQID: https://experienceleague.adobe.com/wX-aqOHlSWGU0gTqyv0nEuSVFL8sstvCMxgiqeFDWIo
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a9f73820-6899-47c2-a597-3fec28ab756a
  - id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2:
  - id: d145add9-d5b9-481b-aa8a-e15e6bb7f813
  - id: a7289281-9ae4-47b1-b8cf-4028b98af776
  - id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 7f28f19b11ead867b0851943fdd997dcc3af170b
workflow-type: tm+mt
source-wordcount: 685
ht-degree: 2%

---

# campos de execução de ação de eventos journeyStep {#sharing-execution-fields}

>[!BEGINSHADEBOX]

**Nesta página:** Faça referência aos campos de execução de ação adicionados aos eventos de etapa de jornada quando uma etapa processar uma ação personalizada.

>[!ENDSHADEBOX]

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
* error

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

## actionOriginEndpoint {#actionoriginendpoint}

URI do ponto de extremidade de ação personalizada usado na ação.

Tipo: sequência de caracteres

## actionOriginMethod {#actionoriginmethod}

Isso descreve o método usado na solicitação HTTP (GET ou POST).

Tipo: sequência de caracteres

## actionOriginIsMTLS {#actionoriginismtls}

Descreve se o MTLS está habilitado para o endpoint.

Tipo: booleano

## actionIsProxy {#actionisproxy}

Descreve se um proxy HTTP com intervalo de endereços IP definido é usado para a chamada.

Tipo: booleano

## actionExecutionOriginStartTime {#actionexecutionoriginstarttime}

Descreve o carimbo de data e hora em que a solicitação HTTP é iniciada. No caso de uma nova tentativa, esse é o carimbo de data e hora em que a nova tentativa final é iniciada. O carimbo de data e hora usa o formato ISO8601 no fuso horário UTC.

Observe que esse carimbo de data e hora normalmente será exibido um pouco depois que o perfil entrar no nó de ação personalizada ou significativamente depois de entrar no nó, em caso de limitação.

Tipo: carimbo de data e hora

## actionExecutionOriginTime {#actionexecutionorigintime}

Descreve o tempo de resposta da chamada HTTP. Em caso de nova tentativa, esse é o tempo gasto pela tentativa final. Ele mede o tempo entre o início da solicitação HTTP e o retorno da resposta completa do servidor. Observe que isso exclui qualquer tempo gasto aguardando na fila em caso de limitação.

Tipo: longo

## actionIsThrottled {#actionisthrottled}

Descreve se a limitação está habilitada para o endpoint.

Tipo: booleano

## actionWaitTime {#actionwaittime}

Descreve quando o limite de taxa configurado é atingido para um endpoint limitado, as chamadas são enfileiradas e processadas na taxa configurada. Este campo relata o tempo que a chamada gastou aguardando na fila antes de ser executada. Especificado somente se actionIsThrottled == true.

Tipo: longo

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
