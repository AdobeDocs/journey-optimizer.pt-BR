---
product: journey optimizer
title: setHours
description: Saiba mais sobre a função setHours
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: setHours, função, expressão, jornada
exl-id: ed78c2a9-d83a-4fac-a2e9-7383da131a1f
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 8%

---

# setHours {#setHours}

Define somente as horas de uma data ou hora de data. Por exemplo, se você quiser esperar até uma determinada hora amanhã, você pode forçar a hora.

## Categoria

Data

## Sintaxe da função

`setHours(<parameter>)`

## Parâmetros

| Parâmetro | Tipo |
|--- |--- |
| data e hora | dateTime |
| data e hora sem considerar fuso horário | dateTimeOnly |
| horas | integer |

## Assinaturas e tipo retornado

`setHours(<dateTime>,<hours>)`

Retorna um datetime.

`setHours(<dateTimeOnly>,<hours>)`

Retorna um datetime sem considerar o fuso horário.

## Exemplos

`setHours(toDateTime('2010-12-12T01:11:00Z'), 4)`

Retorna 2010-12-12T04:11:00Z.

`setHours(nowWithDelta(1, "days"), 20)`

Retorna amanhã às 8hXY PM, sendo XY os minutos no momento da avaliação atual. Se a avaliação ocorrer às 2:45 da manhã, o horário retornado será 20:45.
