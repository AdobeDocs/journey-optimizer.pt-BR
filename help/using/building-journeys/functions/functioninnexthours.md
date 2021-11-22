---
product: adobe campaign
title: inNextHours
description: Saiba mais sobre a função em NextHours
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 079a91b6-49c5-4e68-a240-358ed0cded92
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 18%

---

# inNextHours {#inNextHours}

Retorna true se uma determinada data ou dateTime estiver entre agora e agora + horas delta.

## Categoria

Data 

## Sintaxe da função

`inNextHours(<dateTime>,<delta>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| data e hora | dateTime |
| delta | integer |

## Assinaturas e tipo retornado

`inNextHours(<dateTime>,<integer>)`

Retorna um booleano.

## Exemplos

`inNextHours(toDateTime('2010-12-12T01:11:00Z'), 4)`

Retorna true.
