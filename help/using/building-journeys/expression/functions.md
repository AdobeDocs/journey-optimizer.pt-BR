---
solution: Journey Optimizer
product: journey optimizer
title: Funções
description: Saiba mais sobre funções
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: função, expressões, editor, jornada
exl-id: 5b978eef-7d3e-41fe-bb08-0cf37c3b125d
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
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
| Agregação | [avg](../functions/functionavg.md) |
| Agregação | [count](../functions/functioncount.md) |
| Agregação | [countOnlyNull](../functions/functioncountonlynull.md) |
| Agregação | [countWithNull](../functions/functioncountwithnull.md) |
| Agregação | [distinctCount](../functions/functiondistinctcount.md) |
| Agregação | [distinctCountWithNull](../functions/functiondistinctcountwithnull.md) |
| Agregação | [max](../functions/functionmax.md) |
| Agregação | [min](../functions/functionmin.md) |
| Agregação | [sum](../functions/functionsum.md) |
| Conversão | [toBool](../functions/functiontobool.md) |
| Conversão | [toDateOnly](../functions/functiontodateonly.md) |
| Conversão | [toDateTime](../functions/functiontodatetime.md) |
| Conversão | [toDateTimeOnly](../functions/functiontodatetimeonly.md) |
| Conversão | [toDecimal](../functions/functiontodecimal.md) |
| Conversão | [toDuration](../functions/functiontoduration.md) |
| Conversão | [toInteger](../functions/functiontointeger.md) |
| Conversão | [toString](../functions/functiontostring.md) |
| Data | [currentTimeInMillis](../functions/functioncurrenttimeinmillis.md) |
| Data | [inLastDays](../functions/functioninlastdays.md) |
| Data | [inLastHours](../functions/functioninlasthours.md) |
| Data | [inLastMonths](../functions/functioninlastmonths.md) |
| Data | [inLastYears](../functions/functioninlastyears.md) |
| Data | [inNextDays](../functions/functioninnextdays.md) |
| Data | [inNextHours](../functions/functioninnexthours.md) |
| Data | [inNextMonths](../functions/functioninnextmonths.md) |
| Data | [inNextYears](../functions/functioninnextyears.md) |
| Data | [now](../functions/functionnow.md) |
| Data | [nowWithDelta](../functions/functionnowwithdelta.md) |
| Data | [setHours](../functions/functionsethours.md) |
| Data | [setDays](../functions/functionsetdays.md) |
| Data | [updateTimeZone](../functions/functionupdatetimezone.md) |
| Lista | [distinct](../functions/functiondistinct.md) |
| Lista | [distinctWithNull](../functions/functiondistinctwithnull.md) |
| Lista | [filtro](../functions/functionfilter.md) |
| Lista | [getListItem](../functions/functiongetlistitem.md) |
| Lista | [in](../functions/functionin.md) |
| Lista | [interseção](../functions/functionintersect.md) |
| Lista | [limite](../functions/functionlimit.md) |
| Lista | [listSize](../functions/functionlistsize.md) |
| Lista | [serializeList](../functions/functionserializelist.md) |
| Lista | [sort](../functions/functionsort.md) |
| Matemática | [random](../functions/functionrandom.md) |
| Matemática | [round](../functions/functionround.md) |
| String | [concat](../functions/functionconcat.md) |
| String | [contain](../functions/functioncontain.md) |
| String | [containIgnoreCase](../functions/functioncontainwithignorecase.md) |
| String | [endWith](../functions/functionendwith.md) |
| String | [endWithIgnoreCase](../functions/functionendwithignorecase.md) |
| String | [equalIgnoreCase](../functions/functionequalignorecase.md) |
| String | [indexOf](../functions/functionindexof.md) |
| String | [isEmpty](../functions/functionisempty.md) |
| String | [isNotEmpty](../functions/functionisnotempty.md) |
| String | [lastIndexOf](../functions/functionlastindexof.md) |
| String | [length](../functions/functionlength.md) |
| String | [lower](../functions/functionlower.md) |
| String | [matchRegExp](../functions/functionmatchregexp.md) |
| String | [notEqualIgnoreCase](../functions/functionnotequalignorecase.md) |
| String | [replace](../functions/functionreplace.md) |
| String | [replaceAll](../functions/functionreplaceall.md) |
| String | [split](../functions/functionsplit.md) |
| String | [startWith](../functions/functionstartwith.md) |
| String | [startWithIgnoreCase](../functions/functionstartwithignorecase.md) |
| String | [substr](../functions/functionsubstr.md) |
| String | [trim](../functions/functiontrim.md) |
| String | [upper](../functions/functionupper.md) |
| String | [uuid](../functions/functionuuid.md) |
