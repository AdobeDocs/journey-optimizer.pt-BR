---
product: journey optimizer
title: inLastHours
description: Saiba mais sobre a função em Últimas horas
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastHours, função, expressão, jornada
exl-id: c648d711-c81b-403b-9adb-792c7e79e4e2
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 16%

---

# inLastHours {#inLastHours}

Retorna verdadeiro se a data e hora especificadas estiverem entre agora e agora - delta horas.

## Categoria

Data

## Sintaxe da função

`inLastHours(<dateTime>,<delta>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| data e hora | dateTime |
| delta | inteiro |

## Assinaturas e tipo retornado

`inLastHours(<dateTime>,<integer>)`

Retorna um valor booleano.

## Exemplos

`inLastHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Retorna verdadeiro.

`inLastHours(@event{MyEvent.timestamp}, 4)`

Retorna verdadeiro.
