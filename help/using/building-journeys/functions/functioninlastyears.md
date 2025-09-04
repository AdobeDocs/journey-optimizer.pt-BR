---
product: journey optimizer
title: inLastYears
description: Saiba mais sobre a função inLastYears
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastYears, função, expressão, jornada
exl-id: cdf653d2-967e-4a1b-92e5-37dd22f379f9
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inLastYears {#inLastYears}

Retorna verdadeiro se uma determinada data ou dateTime estiver entre agora e agora - anos delta.

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

Retorna um valor booleano.

## Exemplos

`inLastYears(toDateTime('2023-12-12T01:11:00Z'), 4)`

Retorna verdadeiro.
