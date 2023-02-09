---
product: journey optimizer
title: inNextMonths
description: Saiba mais sobre a função em NextMonths
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextMonths, função, expressão, jornada
exl-id: e2e520ec-ae9e-4ed6-b50d-606fc6861d56
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextMonths {#inNextMonths}

Retorna true se uma determinada data ou dateTime estiver entre agora e agora + meses delta.

## Categoria

Data

## Sintaxe da função

`inNextMonths(<dateTime>,<delta>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| data e hora | dateTime |
| delta | inteiro |

## Assinaturas e tipo retornado

`inNextMonths(<dateTime>,<integer>)`

Retorna um booleano.

## Exemplos

`inNextMonths(toDateTime('2020-01-12T01:11:00Z'), 4)`

Retorna true.
