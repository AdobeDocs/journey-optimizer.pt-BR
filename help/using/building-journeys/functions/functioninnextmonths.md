---
product: journey optimizer
title: inNextMonths
description: Saiba mais sobre a função inNextMonths
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextMonths, função, expressão, jornada
exl-id: e2e520ec-ae9e-4ed6-b50d-606fc6861d56
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 16%

---

# inNextMonths {#inNextMonths}

Retorna verdadeiro se uma determinada data ou dateTime estiver entre agora e agora + meses delta.

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

Retorna um valor booleano.

## Exemplos

`inNextMonths(toDateTime('2023-01-12T01:11:00Z'), 4)`

Retorna verdadeiro.
