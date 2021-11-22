---
product: adobe campaign
title: inLastHours
description: Saiba mais sobre a função emLastHours
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: c648d711-c81b-403b-9adb-792c7e79e4e2
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 17%

---

# inLastHours {#inLastHours}

Retorna verdadeiro se a hora da data especificada estiver entre agora e agora - horas delta.

## Categoria

Data 

## Sintaxe da função

`inLastHours(<dateTime>,<delta>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| data e hora | dateTime |
| delta | integer |

## Assinaturas e tipo retornado

`inLastHours(<dateTime>,<integer>)`

Retorna um booleano.

## Exemplos

`inLastHours(toDateTime('2019-12-12T01:11:00Z'), 4)`

Retorna true.

`inLastHours(@{MyEvent.timestamp}, 4)`

Retorna true.
