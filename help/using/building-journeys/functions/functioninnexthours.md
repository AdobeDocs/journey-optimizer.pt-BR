---
product: journey optimizer
title: inNextHours
description: Saiba mais sobre a função em NextHours
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextHours, função, expressão, jornada
exl-id: 079a91b6-49c5-4e68-a240-358ed0cded92
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 16%

---

# inNextHours {#inNextHours}

Retorna verdadeiro se uma determinada data ou dateTime estiver entre agora e agora + horas delta.

## Categoria

Data

## Sintaxe da função

`inNextHours(<dateTime>,<delta>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| data e hora | dateTime |
| delta | inteiro |

## Assinaturas e tipo retornado

`inNextHours(<dateTime>,<integer>)`

Retorna um valor booleano.

## Exemplos

`inNextHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Retorna verdadeiro.
