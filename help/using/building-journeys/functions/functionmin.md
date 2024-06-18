---
product: journey optimizer
title: min
description: Saiba mais sobre a função principal
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: min, função, expressão, jornada
exl-id: 1c425d1d-08b4-446b-83ce-db376b2bf39f
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 6%

---

# min {#min}

Retorna o valor mínimo entre um conjunto de expressões, fornecido como uma lista ou duas expressões. Valores nulos são ignorados.

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
* duração
* inteiro
* decimal
* dateTime
* dateTimeOnly

## Assinaturas e tipos retornados

`min(<listDuration>)`

Retorna uma duração.

`min(<listInteger>)`

Retorna uma duração.

`min(<listDateTimeOnly>)`

Retorna uma data e hora sem considerar o fuso horário.

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

Retorna uma data e hora sem considerar o fuso horário.

`min(<integer>,<integer>)`

Retorna um inteiro.

## Exemplos

`min(@event{BarBeacon.inventory},5)`

`min([10,3,8])`

Retorna 3.

`min([10,null,8])`

Retorna 8.
