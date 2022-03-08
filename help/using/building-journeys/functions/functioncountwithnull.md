---
product: adobe campaign
title: countWithNull
description: Saiba mais sobre a função countWithNull
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 8d53b6d8-f00f-4d1a-b6df-951f84a15430
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
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
