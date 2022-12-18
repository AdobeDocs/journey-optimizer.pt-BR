---
solution: Journey Optimizer
product: journey optimizer
title: Instrução condicional (if, then, else)
description: Saiba mais sobre instrução condicional
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 5a5b35a7-e3b5-4dc0-8a87-e985956b04a4
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---

# Instrução condicional (if, then, else) {#conditional-instruction}

A instrução condicional (if, then, else) é compatível no editor avançado. Ela permite definir expressões mais complexas. Ele é composto pelos seguintes elementos:

* **[!UICONTROL if]**: a condição a ser avaliada primeiro.
* **[!UICONTROL then]**: a expressão a ser avaliada caso o resultado da avaliação de condição seja true.
* **[!UICONTROL else]**: a expressão a ser avaliada caso o resultado da avaliação de condição seja false.

>[!NOTE]
>
>Os parênteses são necessários em todas as expressões.

```json
if  (<expression1>)
then
   (<expression2>)
else
   (<expression3>)
```

`<expression1>` deve retornar um **booleano**.

`<expression2>` e `<expression3>` deve ter o mesmo tipo ou tipos compatíveis. As assinaturas compatíveis e os tipos retornados são:

```json
boolean,boolean : boolean
dateTime,dateTime : dateTime
dateTimeOnly,dateTimeOnly : dateTimeOnly
decimal,integer : decimal
integer,decimal : integer
integer,decimal : decimal
duration,duration : duration
string,string : string
listBoolean,listBoolean : listBoolean
listDateTime,listDateTime : listDateTime
listDateTimeOnly,listDateTimeOnly : listDateTimeOnly
listDateOnly,listDateOnly : listDateOnly
listDecimal,listDecimal : listDecimal
listInteger,listInteger : listInteger
listString,listString : listString
```

**Uso**

A instrução condicional permite otimizar o workflow do jornada, reduzindo o número de atividades de condição. Por exemplo, na mesma atividade de ação, é possível especificar duas alternativas para uma definição de campo usando apenas uma expressão de condição.

Exemplo para uma atividade de ação (para um campo que espera uma string como resultado da instrução condicional):

```json
if (startWithIgnoreCase(@{eventiOSPushPermissionAllowed.device.model}, 'iPad') or startWithIgnoreCase(@{eventiOSPushPermissionAllowed.device.model}, 'iOS'))
then
   ('apns')
else
   ('fcm')
```
