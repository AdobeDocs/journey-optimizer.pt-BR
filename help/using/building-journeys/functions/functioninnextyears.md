---
product: journey optimizer
title: inNextYears
description: Saiba mais sobre a função em NextYears
feature: Journeys
role: Engineer
level: Experienced
keywords: inNextYears, função, expressão, jornada
exl-id: e4597772-d53c-4e15-8237-b2460ce31170
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextYears {#inNextYears}

Retorna verdadeiro se uma determinada data ou dateTime estiver entre agora e agora + anos delta.

## Categoria

Data

## Sintaxe da função

`inNextYears(<dateTime>,<delta>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| data e hora | dateTime |
| delta | inteiro |

## Assinaturas e tipo retornado

`inNextYears(<dateTime>,<integer>)`

Retorna um valor booleano.

## Exemplos

`inNextYears(toDateTime('2021-12-12T01:11:00Z'), 4)`

Retorna verdadeiro.
