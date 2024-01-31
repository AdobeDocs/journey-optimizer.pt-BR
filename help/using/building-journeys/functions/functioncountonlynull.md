---
product: journey optimizer
title: countOnlyNull
description: Saiba mais sobre a função countOnlyNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countOnlyNull, função, expressão, jornada
exl-id: d06fc594-33dd-48ce-8c62-2f2892a867da
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 14%

---

# countOnlyNull {#countOnlyNull}

Conta o número de valores nulos na lista.

Observe que o parâmetro `<listObject>` não é compatível com esta função.

## Categoria

Agregação

## Sintaxe da função

`countOnlyNull(<listAny>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

## Assinatura e tipo retornado

`countOnlyNull(<listAny>)`

Retorna um inteiro.

## Exemplo

`countOnlyNull([10,2,10,null])`

Retorna 1.
