---
product: adobe campaign
title: countWithNull
description: Saiba mais sobre a função countWithNull
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: d786f3d42515d65a6574f51b6cff4b85063a0126
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 32%

---

# countWithNull {#countWithNull}

Conta todos os elementos da lista, incluindo valores nulos.

## Categoria

Agregação

## Sintaxe da função

`countWithNull(<listAny>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| Lista | listString |
| Lista | listBoolean |
| Lista | listInteger |
| Lista | listDecimal |
| Lista | listDuration |
| Lista | listDateTime |
| Lista | listDateTimeOnly |
| Lista | listDateOnly |

## Assinatura e tipo retornado

`countWithNull(<listAny>)`

Retorna um número inteiro.

## Exemplo

`countWithNull([10,2,10,null])`

Retorna 4.
