---
product: journey optimizer
title: countWithNull
description: Saiba mais sobre a função countWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countWithNull, função, expressão, jornada
exl-id: 8d53b6d8-f00f-4d1a-b6df-951f84a15430
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 14%

---

# countWithNull {#countWithNull}

Conta todos os elementos da lista, incluindo valores nulos.

Observe que o parâmetro `<listObject>` não tem suporte nessa função.

## Categoria

Agregação

## Sintaxe da função

`countWithNull(<listAny>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

## Assinatura e tipo retornado

`countWithNull(<listAny>)`

Retorna um inteiro.

## Exemplo

`countWithNull([10,2,10,null])`

Retorna 4.
