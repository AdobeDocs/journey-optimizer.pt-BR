---
product: journey optimizer
title: setHours
description: Saiba mais sobre a função setHours
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: setHours, função, expressão, jornada
exl-id: ed78c2a9-d83a-4fac-a2e9-7383da131a1f
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '109'
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

`setHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Retorna 2023-12-12T04:11:00Z.

`setHours(nowWithDelta(1, "days"), 20)`

Retorna amanhã às 20h00, sendo XY os minutos no momento da avaliação de hora atual. :XY Se a avaliação ocorrer às 2:45 AM, a hora retornada será 20:45 PM.
