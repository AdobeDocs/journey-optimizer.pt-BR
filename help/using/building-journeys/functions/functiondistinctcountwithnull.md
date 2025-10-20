---
product: journey optimizer
title: distinctCountWithNull
description: Saiba mais sobre a função distinctCountWithNull
feature: Journeys
role: Engineer
level: Experienced
keywords: distinctCountWithNull, função, expressão, jornada
exl-id: 2c3f629f-2220-44a4-9b0c-8aa602301098
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 14%

---

# distinctCountWithNull {#distinctCountWithNull}

Conta o número de valores diferentes, incluindo os valores nulos.

Observe que o parâmetro `<listObject>` não tem suporte nessa função.

## Categoria

Agregação

## Sintaxe da função

`distinctCountWithNull(<listAny>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

## Assinatura e tipo retornado

`distinctCountWithNull(<listAny>)`

Retorna um inteiro.

## Exemplo

`distinctCountWithNull([10,2,10,null])`

Retorna 3.
