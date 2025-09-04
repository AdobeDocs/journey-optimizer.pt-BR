---
product: journey optimizer
title: countOnlyNull
description: Saiba mais sobre a função countOnlyNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countOnlyNull, função, expressão, jornada
exl-id: d06fc594-33dd-48ce-8c62-2f2892a867da
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 14%

---

# countOnlyNull {#countOnlyNull}

Conta o número de valores nulos na lista.

Observe que o parâmetro `<listObject>` não tem suporte nessa função.

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
