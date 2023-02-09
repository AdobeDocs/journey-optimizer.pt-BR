---
product: journey optimizer
title: max
description: Saiba mais sobre o máximo da função
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: max, função, expressão, jornada
exl-id: 5c792d33-32b9-4b1b-ab99-3ebfac391678
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 7%

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
