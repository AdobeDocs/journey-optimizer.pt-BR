---
product: journey optimizer
title: inNextDays
description: Saiba mais sobre a função em NextDays
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextDays, função, expressão, jornada
exl-id: 0cb3e0db-dc5b-4d4e-a057-af030d9bdb21
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextDays {#inNextDays}

Retorna verdadeiro se uma determinada data ou dateTime estiver entre agora e agora + dias delta.

## Categoria

Data

## Sintaxe da função

`inNextDays(<dateTime>,<delta>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| data e hora | dateTime |
| delta | inteiro |

## Assinaturas e tipo retornado

`inNextDays(<dateTime>,<integer>)`

Retorna um valor booleano.

## Exemplos

`inNextDays(toDateTime('2010-12-12T01:11:00Z'), 4)`

Retorna verdadeiro.
