---
product: adobe campaign
title: count
description: Saiba mais sobre a contagem de funções
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: d786f3d42515d65a6574f51b6cff4b85063a0126
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 30%

---

# count {#count}

Conta os elementos da lista que não consideram os valores nulos.

## Categoria

Agregação

## Sintaxe da função

`count(<listAny>)`

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

## Assinaturas e tipo retornado

`count(<listAny>)`

Retorna um número inteiro.

## Exemplo

`count([10,2,10,null])`

Retorna 3.
