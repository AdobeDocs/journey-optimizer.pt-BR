---
product: adobe campaign
title: min
description: Saiba mais sobre o min da função
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 1c425d1d-08b4-446b-83ce-db376b2bf39f
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 6%

---

# min {#min}

Retorna o valor mínimo entre um conjunto de expressões, considerando como uma lista ou duas expressões. Valores nulos são ignorados.

## Categoria

Agregação

## Sintaxe da função

`min(<parameters>)`

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

`min(<listDuration>)`

Retorna uma duração.

`min(<listInteger>)`

Retorna uma duração.

`min(<listDateTimeOnly>)`

Retorna um datetime sem considerar o fuso horário.

`min(<listDateTime>)`

Retorna um datetime.

`min(<listDateOnly>)`

Retorna uma data.

`min(<listDecimal>)`

Retorna um decimal.

`min(<decimal>,<decimal>)`

Retorna um decimal.

`min(<duration>,<duration>)`

Retorna uma duração.

`min(<dateTime>,<dateTime>)`

Retorna um datetime.

`min(<dateTimeOnly>,<dateTimeOnly>)`

Retorna um datetime sem considerar o fuso horário.

`min(<integer>,<integer>)`

Retorna um número inteiro.

## Exemplos

`min(@{BarBeacon.inventory},5)`

`min([10,3,8])`

Retorna 3.

`min([10,null,8])`

Retorna 8.
