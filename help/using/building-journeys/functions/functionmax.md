---
product: adobe campaign
title: max
description: Saiba mais sobre o máximo da função
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 5c792d33-32b9-4b1b-ab99-3ebfac391678
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 6%

---

# max{#max}

Retorna o valor máximo entre um conjunto de expressões, considerando como uma lista ou duas expressões. Valores nulos são ignorados.

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
* duration
* integer
* decimal
* dateTime
* dateTimeOnly

## Assinaturas e tipos retornados

`max(<listDuration>)`

Retorna uma duração.

`max(<listInteger>)`

Retorna uma duração.

`max(<listDateTimeOnly>)`

Retorna um datetime sem considerar o fuso horário.

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

Retorna um datetime sem considerar o fuso horário.

`max(<integer>,<integer>)`

Retorna um número inteiro.

## Exemplos

`max(@{BarBeacon.inventory},5)`

`max([10,3,8])`

Retorna 10.

`max([10,null,8])`

Retorna 10.
