---
product: journey optimizer
title: inLastDays
description: Saiba mais sobre a função em LastDays
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastDays, função, expressão, jornada
exl-id: 1b150568-17c2-454d-847e-17bac3d0b35d
source-git-commit: e0a942f4dc84b41882b3c12dd47f5931a8a34a2b
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 19%

---

# inLastDays {#inLastDays}

Retorna verdadeiro se um determinado dateTime estiver entre agora e agora - dias delta.

## Categoria

Data

## Sintaxe da função

`inLastDays(<dateTime>,<delta>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| data e hora | dateTime |
| delta | inteiro |

## Assinaturas e tipo retornado

`inLastDays(<dateTime>,<integer>)`

Retorna um valor booleano.

## Exemplos

`inLastDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

Retorna verdadeiro.
