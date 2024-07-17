---
product: journey optimizer
title: inLastDays
description: Saiba mais sobre a função em LastDays
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastDays, função, expressão, jornada
exl-id: 1b150568-17c2-454d-847e-17bac3d0b35d
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inLastDays {#inLastDays}

Retorna verdadeiro se uma determinada data ou dateTime estiver entre agora e agora - dias delta.

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
