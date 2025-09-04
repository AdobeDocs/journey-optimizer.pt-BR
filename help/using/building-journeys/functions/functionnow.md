---
product: journey optimizer
title: now
description: Saiba mais sobre a função agora
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: agora, função, expressão, jornada
exl-id: 16dcc772-e48d-4f10-be75-62dd39473556
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 15%

---

# now {#now}

Retorna a data atual no formato de data e hora. Para obter mais informações sobre tipos de dados, consulte [esta página](../expression/data-types.md).

## Categoria

Data

## Sintaxe da função

`now(<parameter>)`

## Parâmetros

| Parâmetro | Descrição |
|--- |--- |
| sequência de caracteres |  |

## Assinaturas e tipo retornado

`now()`

`now("<timeZone id>")`

Retorna dateTime.

## Exemplos

`now()`

Retorna 2023-06-03T06:30Z.

`toString(now())`

Retorna &quot;2023-06-03T06:30Z&quot;

`now("Europe/Paris")`

Retorna 2023-06-03T08:30+02:00.
