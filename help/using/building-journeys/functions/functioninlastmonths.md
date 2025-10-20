---
product: journey optimizer
title: inLastMonths
description: Saiba mais sobre a função inLastMonths
feature: Journeys
role: Engineer
level: Experienced
keywords: inLastMonths, função, expressão, jornada
exl-id: 4933ef43-66b8-462d-867c-03edd4c34947
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inLastMonths {#inLastMonths}

Retorna verdadeiro se uma determinada data ou dateTime estiver entre agora e agora - meses delta.

## Categoria

Data

## Sintaxe da função

`inLastMonths(<dateTime>,<delta>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| data e hora | dateTime |
| delta | inteiro |

## Assinaturas e tipo retornado

`inLastMonths(<dateTime>,<integer>)`

Retorna um valor booleano.

## Exemplos

`inLastMonths(toDateTime('2023-12-12T01:11:00Z'), 4)`

Retorna verdadeiro.
