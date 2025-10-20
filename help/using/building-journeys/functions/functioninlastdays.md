---
product: journey optimizer
title: inLastDays
description: Saiba mais sobre a função em LastDays
feature: Journeys
role: Engineer
level: Experienced
keywords: inLastDays, função, expressão, jornada
exl-id: 1b150568-17c2-454d-847e-17bac3d0b35d
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
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
