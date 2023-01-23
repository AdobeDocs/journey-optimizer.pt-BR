---
product: journey optimizer
title: inLastDays
description: Saiba mais sobre a função emLastDays
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastDays, função, expressão, jornada
exl-id: 1b150568-17c2-454d-847e-17bac3d0b35d
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 16%

---

# inLastDays {#inLastDays}

Retorna true se uma determinada data ou dateTime estiver entre agora e agora - dias delta.

## Categoria

Data

## Sintaxe da função

`inLastDays(<dateTime>,<delta>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| data e hora | dateTime |
| delta | integer |

## Assinaturas e tipo retornado

`inLastDays(<dateTime>,<integer>)`

Retorna um booleano.

## Exemplos

`inLastDays(toDateTime('2019-12-12T01:11:00Z'), 4)`

Retorna true.
