---
product: adobe campaign
title: inLastYears
description: Saiba mais sobre a função emLastYears
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: cdf653d2-967e-4a1b-92e5-37dd22f379f9
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 18%

---

# inLastYears {#inLastYears}

Retorna true se uma determinada data ou dateTime estiver entre agora e agora - anos delta.

## Categoria

Data

## Sintaxe da função

`inLastYears(<dateTime>,<delta>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| data e hora | dateTime |
| delta | integer |

## Assinaturas e tipo retornado

`inLastYears(<dateTime>,<integer>)`

Retorna um booleano.

## Exemplos

`inLastYears(toDateTime('2010-12-12T01:11:00Z'), 4)`

Retorna true.
