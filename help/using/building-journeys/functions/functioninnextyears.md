---
product: journey optimizer
title: inNextYears
description: Saiba mais sobre a função em NextYears
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: e4597772-d53c-4e15-8237-b2460ce31170
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 18%

---

# inNextYears {#inNextYears}

Retorna true se uma determinada data ou dateTime estiver entre agora e agora + anos delta.

## Categoria

Data

## Sintaxe da função

`inNextYears(<dateTime>,<delta>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| data e hora | dateTime |
| delta | integer |

## Assinaturas e tipo retornado

`inNextYears(<dateTime>,<integer>)`

Retorna um booleano.

## Exemplos

`inNextYears(toDateTime('2021-12-12T01:11:00Z'), 4)`

Retorna true.
