---
solution: Journey Optimizer
product: journey optimizer
title: Funções
description: Saiba mais sobre funções
feature: Journeys
role: Developer
level: Experienced
keywords: função, expressões, editor, jornada
exl-id: 5b978eef-7d3e-41fe-bb08-0cf37c3b125d
version: Journey Orchestration
source-git-commit: d58319d687d113ce680c415524fdea0400cb38f0
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 69%

---

# Funções {#functions}

Uma função pode ter diferentes assinaturas (um conjunto diferente de parâmetros ordenados). Uma assinatura de função pode ter expressões 0-N como parâmetros ordenados.

`<function name>`(`<expression as param 1>`, `<expression as param 2>`, ... ,`<expression as param N>`)

Cada função tem um tipo retornado específico.

Esta é a lista de funções compatíveis.

## Funções principais

| Categoria | Função |
|-------------|-----------------------|
| Adobe Experience Platform | [inAudience](../functions/functioninaudience.md) |
| Agregação | [avg](../functions/aggregation-functions.md#avg) |
| Agregação | [count](../functions/aggregation-functions.md#count) |
| Agregação | [countOnlyNull](../functions/aggregation-functions.md#countOnlyNull) |
| Agregação | [countWithNull](../functions/aggregation-functions.md#countWithNull) |
| Agregação | [distinctCount](../functions/aggregation-functions.md#distinctCount) |
| Agregação | [distinctCountWithNull](../functions/aggregation-functions.md#distinctCountWithNull) |
| Agregação | [max](../functions/aggregation-functions.md#max) |
| Agregação | [min](../functions/aggregation-functions.md#min) |
| Agregação | [sum](../functions/aggregation-functions.md#sum) |
| Conversão | [toBool](../functions/conversion-functions.md#toBool) |
| Conversão | [toDateOnly](../functions/conversion-functions.md#toDateOnly) |
| Conversão | [toDateTime](../functions/conversion-functions.md#toDateTime) |
| Conversão | [toDateTimeOnly](../functions/conversion-functions.md#toDateTimeOnly) |
| Conversão | [toDecimal](../functions/conversion-functions.md#toDecimal) |
| Conversão | [toDuration](../functions/conversion-functions.md#toDuration) |
| Conversão | [toInteger](../functions/conversion-functions.md#toInteger) |
| Conversão | [toString](../functions/conversion-functions.md#toString) |
| Data | [currentTimeInMillis](../functions/date-functions.md#currentTimeInMillis) |
| Data | [inLastDays](../functions/date-functions.md#inLastDays) |
| Data | [inLastHours](../functions/date-functions.md#inLastHours) |
| Data | [inLastMonths](../functions/date-functions.md#inLastMonths) |
| Data | [inLastYears](../functions/date-functions.md#inLastYears) |
| Data | [inNextDays](../functions/date-functions.md#inNextDays) |
| Data | [inNextHours](../functions/date-functions.md#inNextHours) |
| Data | [inNextMonths](../functions/date-functions.md#inNextMonths) |
| Data | [inNextYears](../functions/date-functions.md#inNextYears) |
| Data | [now](../functions/date-functions.md#now) |
| Data | [nowWithDelta](../functions/date-functions.md#nowWithDelta) |
| Data | [setHours](../functions/date-functions.md#setHours) |
| Data | [setDays](../functions/date-functions.md#setDays) |
| Data | [updateTimeZone](../functions/date-functions.md#updateTimeZone) |
| Lista | [distinct](../functions/list-functions.md#distinct) |
| Lista | [distinctWithNull](../functions/list-functions.md#distinctWithNull) |
| Lista | [filtro](../functions/list-functions.md#filter) |
| Lista | [getListItem](../functions/list-functions.md#getListItem) |
| Lista | [in](../functions/list-functions.md#in) |
| Lista | [interseção](../functions/list-functions.md#intersect) |
| Lista | [limite](../functions/list-functions.md#limit) |
| Lista | [listSize](../functions/list-functions.md#listSize) |
| Lista | [serializeList](../functions/list-functions.md#serializeList) |
| Lista | [sort](../functions/list-functions.md#sort) |
| Matemática | [random](../functions/functionrandom.md) |
| Matemática | [round](../functions/functionround.md) |
| String | [concat](../functions/string-functions.md#concat) |
| String | [contain](../functions/string-functions.md#contain) |
| String | [containIgnoreCase](../functions/string-functions.md#containIgnoreCase) |
| String | [endWith](../functions/string-functions.md#endWith) |
| String | [endWithIgnoreCase](../functions/string-functions.md#endWithIgnoreCase) |
| String | [equalIgnoreCase](../functions/string-functions.md#equalIgnoreCase) |
| String | [indexOf](../functions/string-functions.md#indexOf) |
| String | [isEmpty](../functions/string-functions.md#isEmpty) |
| String | [isNotEmpty](../functions/string-functions.md#isNotEmpty) |
| String | [lastIndexOf](../functions/string-functions.md#lastIndexOf) |
| String | [length](../functions/string-functions.md#length) |
| String | [lower](../functions/string-functions.md#lower) |
| String | [matchRegExp](../functions/string-functions.md#matchRegExp) |
| String | [notEqualIgnoreCase](../functions/string-functions.md#notEqualIgnoreCase) |
| String | [replace](../functions/string-functions.md#replace) |
| String | [replaceAll](../functions/string-functions.md#replaceAll) |
| String | [split](../functions/string-functions.md#split) |
| String | [startWith](../functions/string-functions.md#startWith) |
| String | [startWithIgnoreCase](../functions/string-functions.md#startWithIgnoreCase) |
| String | [substr](../functions/string-functions.md#substr) |
| String | [trim](../functions/string-functions.md#trim) |
| String | [upper](../functions/string-functions.md#upper) |
| String | [uuid](../functions/string-functions.md#uuid) |
