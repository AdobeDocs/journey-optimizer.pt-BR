---
product: journey optimizer
title: now
description: Saiba mais sobre a função agora
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 16dcc772-e48d-4f10-be75-62dd39473556
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 18%

---

# now {#now}

Retorna a data atual no formato de data/hora. Para obter mais informações sobre tipos de dados, consulte [esta página](../expression/data-types.md).

## Categoria

Data

## Sintaxe da função

`now(<parameter>)`

## Parâmetros

| Parâmetro | Descrição |
|--- |--- |
| string |  |

## Assinaturas e tipo retornado

`now()`

`now("<timeZone id>")`

Retorna dateTime.

## Exemplos

`now()`

Retorna 2019-06-03T06:30Z.

`toString(now())`

Retorna &quot;2019-06-03T06:30Z&quot;

`now("Europe/Paris")`

Retorna 2019-06-03T08:30+02:00.
