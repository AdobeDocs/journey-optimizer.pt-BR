---
product: journey optimizer
title: updateTimeZone
description: Saiba mais sobre a função updateTimeZone
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: updateTimeZone, função, expressão, jornada
exl-id: 1bf4662e-55d0-4631-af93-1430ec7ed7e2
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 9%

---

# updateTimeZone {#updateTimeZone}

Retorna uma nova data e hora, com um novo fuso horário no mesmo instante.

## Categoria

Data

## Sintaxe da função

`updateTimeZone(<parameters>)`

## Parâmetros

* id do fuso horário: string
* dateTime

## Assinatura e tipo retornado

`updateTimeZone(<dateTime>,<timeZone id>)`

Retorna um datetime.

## Exemplos

`updateTimeZone( toDateTime("2019-08-28T08:15:30.123-07:00"), "Europe/Paris"))`

Devoluções em 28/08/2019:15:30.123+02:00.

<!--`updateTimeZone( toDateTime("2019-08-28T08:15:30.123-07:00"), toTimeZone("Europe/Paris")))`
Returns "2019-08-28T17:15:30.123+02:00".-->

`updateTimeZone(@event{MyExpEvent.timestamp}, "Australia/Sydney")`

Se o valor do campo de carimbo de data e hora for `2021-11-16T16:55:12.939318+01:00`, a função retornará `2021-11-17T02:55:12.942115+11:00`.
