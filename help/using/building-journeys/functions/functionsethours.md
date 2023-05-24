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
ht-degree: 9%

---

# setHours {#setHours}

Define apenas as horas de uma data e hora ou data e hora. Por exemplo, se você quiser aguardar até uma determinada hora amanhã, poderá forçar a hora.

## Categoria

Data

## Sintaxe da função

`setHours(<parameter>)`

## Parâmetros

| Parâmetro | Tipo |
|--- |--- |
| data e hora | dateTime |
| data hora sem considerar o fuso horário | dateTimeOnly |
| horas | inteiro |

## Assinaturas e tipo retornado

`setHours(<dateTime>,<hours>)`

Retorna um datetime.

`setHours(<dateTimeOnly>,<hours>)`

Retorna uma data e hora sem considerar o fuso horário.

## Exemplos

`setHours(toDateTime('2010-12-12T01:11:00Z'), 4)`

Devoluções 2010-12-12T04:11:00Z

`setHours(nowWithDelta(1, "days"), 20)`

Retorna amanhã às 20:XY, sendo XY os minutos no momento da avaliação de hora atual. Se a avaliação ocorrer às 2h45, o horário retornado será às 20h45.
