---
product: adobe campaign
title: setDays
description: Saiba mais sobre a função setDays
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: c2757e41-8206-44f7-9dbb-1fa79c0ba6e6
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 12%

---

# setDays {#setDays}

Define somente o dia de uma data ou hora. Por exemplo, se você quiser esperar até um determinado dia do mês, é possível forçar o dia.

## Categoria

Data

## Sintaxe da função

`setDays(<parameter>)`

## Parâmetros

| Parâmetro | Tipo |
|--- |--- |
| data e hora | dateTime |
| data e hora sem considerar fuso horário | dateTimeOnly |
| dias | integer |

## Assinaturas e tipo retornado

`setDays(<dateTime>,<days>)`

Retorna um datetime.

`setDays(<dateTimeOnly>,<days>)`

Retorna um datetime sem considerar o fuso horário.

## Exemplos

`setDays(toDateTime('2010-12-12T01:11:00Z'), 25)`

Retorna 2010-12-25T01:11:00Z.

`setDays(toDateTimeOnly(@{MyEvent.registrationDate}), 1)`
