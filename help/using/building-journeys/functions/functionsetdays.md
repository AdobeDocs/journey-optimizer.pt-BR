---
product: journey optimizer
title: setDays
description: Saiba mais sobre a função setDays
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: setDays, função, expressão, jornada
exl-id: c2757e41-8206-44f7-9dbb-1fa79c0ba6e6
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 11%

---

# setDays {#setDays}

Define apenas o dia de uma data e hora ou data e hora. Por exemplo, se você quiser aguardar até um determinado dia do mês, poderá forçar o dia.

## Categoria

Data

## Sintaxe da função

`setDays(<parameter>)`

## Parâmetros

| Parâmetro | Tipo |
|--- |--- |
| data e hora | dateTime |
| data hora sem considerar o fuso horário | dateTimeOnly |
| dias | inteiro |

## Assinaturas e tipo retornado

`setDays(<dateTime>,<days>)`

Retorna um datetime.

`setDays(<dateTimeOnly>,<days>)`

Retorna uma data e hora sem considerar o fuso horário.

## Exemplos

`setDays(toDateTime('2010-12-12T01:11:00Z'), 25)`

Retorna 2010-12-25T01:11:00Z

`setDays(toDateTimeOnly(@event{MyEvent.registrationDate}), 1)`
