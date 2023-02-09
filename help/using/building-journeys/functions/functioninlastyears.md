---
product: journey optimizer
title: inLastYears
description: Saiba mais sobre a função emLastYears
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastYears, função, expressão, jornada
exl-id: cdf653d2-967e-4a1b-92e5-37dd22f379f9
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
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
| delta | inteiro |

## Assinaturas e tipo retornado

`inLastYears(<dateTime>,<integer>)`

Retorna um booleano.

## Exemplos

`inLastYears(toDateTime('2010-12-12T01:11:00Z'), 4)`

Retorna true.
