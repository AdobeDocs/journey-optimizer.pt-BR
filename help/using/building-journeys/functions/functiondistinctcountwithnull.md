---
product: journey optimizer
title: distinctCountWithNull
description: Saiba mais sobre a função distinctCountWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctCountWithNull, função, expressão, jornada
exl-id: 2c3f629f-2220-44a4-9b0c-8aa602301098
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 12%

---

# distinctCountWithNull {#distinctCountWithNull}

Conta o número de valores diferentes, incluindo os valores nulos.

Observe que o parâmetro `<listObject>` não é compatível com esta função.

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
