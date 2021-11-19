---
product: adobe campaign
title: inNextYears
description: Saiba mais sobre a função em NextYears
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
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
