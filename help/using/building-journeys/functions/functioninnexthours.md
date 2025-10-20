---
product: journey optimizer
title: inNextHours
description: Saiba mais sobre a função em NextHours
feature: Journeys
role: Engineer
level: Experienced
keywords: inNextHours, função, expressão, jornada
exl-id: 079a91b6-49c5-4e68-a240-358ed0cded92
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextHours {#inNextHours}

Retorna verdadeiro se uma determinada data ou dateTime estiver entre agora e agora + horas delta.

## Categoria

Data

## Sintaxe da função

`inNextHours(<dateTime>,<delta>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| data e hora | dateTime |
| delta | inteiro |

## Assinaturas e tipo retornado

`inNextHours(<dateTime>,<integer>)`

Retorna um valor booleano.

## Exemplos

`inNextHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Retorna verdadeiro.
