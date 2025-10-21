---
product: journey optimizer
title: max
description: Saiba mais sobre o máximo da função
feature: Journeys
role: Developer
level: Experienced
keywords: max, função, expressão, jornada
exl-id: 5c792d33-32b9-4b1b-ab99-3ebfac391678
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 7%

---

# max{#max}

Retorna o valor máximo entre um conjunto de expressões, fornecido como uma lista ou duas expressões. Valores nulos são ignorados.

## Categoria

Agregação

## Sintaxe da função

`max(<parameter>)`

## Parâmetros

* listDuration
* listInteger
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* duração
* inteiro
* decimal
* dateTime
* dateTimeOnly

## Assinaturas e tipos retornados

`max(<listDuration>)`

Retorna uma duração.

`max(<listInteger>)`

Retorna uma duração.

`max(<listDateTimeOnly>)`

Retorna uma data e hora sem considerar o fuso horário.

`max(<listDateTime>)`

Retorna um datetime.

`max(<listDateOnly>)`

Retorna uma data.

`max(<listDecimal>)`

Retorna um decimal.

`max(<decimal>,<decimal>)`

Retorna um decimal.

`max(<duration>,<duration>)`

Retorna uma duração.

`max(<dateTime>,<dateTime>)`

Retorna um datetime.

`max(<dateTimeOnly>,<dateTimeOnly>)`

Retorna uma data e hora sem considerar o fuso horário.

`max(<integer>,<integer>)`

Retorna um inteiro.

## Exemplos

`max(@event{BarBeacon.inventory},5)`

`max([10,3,8])`

Retorna 10.

`max([10,null,8])`

Retorna 10.
