---
solution: Journey Optimizer
product: journey optimizer
title: Instrução condicional (if, then, else)
description: Saiba mais sobre instrução condicional
feature: Journeys
role: Developer
level: Experienced
keywords: avançado, condição, ação, jornada
exl-id: 5a5b35a7-e3b5-4dc0-8a87-e985956b04a4
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/SObpEvgu0D-pcoLVaKM7iRffLTSP1stp1zcg4Ygs-vQ
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: cce82f05-fc3c-4af7-85ff-8bba603861a7id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 168
ht-degree: 0%

---

# Instrução condicional (if, then, else) {#conditional-instruction}

A instrução condicional (if, then, else) é compatível com o editor avançado. Ele permite definir expressões mais complexas. Ele é composto pelos seguintes elementos:

* **[!UICONTROL if]**: a condição a ser avaliada primeiro.
* **[!UICONTROL then]**: a expressão a ser avaliada caso o resultado da avaliação da condição seja verdadeiro.
* **[!UICONTROL else]**: a expressão a ser avaliada caso o resultado da avaliação da condição seja falso.

>[!NOTE]
>
>São necessários parênteses em todas as expressões.

```json
if  (<expression1>)
then
   (<expression2>)
else
   (<expression3>)
```

`<expression1>` deve retornar um **booleano**.

`<expression2>` e `<expression3>` devem ter o mesmo tipo ou tipos compatíveis. As assinaturas compatíveis e os tipos retornados são:

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

A instrução condicional permite otimizar o workflow de jornada reduzindo o número de atividades de condição. Por exemplo, na mesma atividade de ação, é possível especificar duas alternativas para uma definição de campo usando apenas uma expressão de condição.

Exemplo de uma atividade de ação (para um campo que espera uma string como o resultado da instrução condicional):

```json
if (startWithIgnoreCase(@event{eventiOSPushPermissionAllowed.device.model}, 'iPad') or startWithIgnoreCase(@event{eventiOSPushPermissionAllowed.device.model}, 'iOS'))
then
   ('apns')
else
   ('fcm')
```
