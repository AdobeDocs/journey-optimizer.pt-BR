---
product: adobe campaign
title: avg
description: Saiba mais sobre o avg da função
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 12%

---

# avg {#avg}

Retorna o valor médio entre um conjunto de expressões, considerando como uma lista ou duas expressões. Valores nulos são ignorados.


## Categoria

Agregação

## Sintaxe da função

`avg(<parameter>)`

## Parâmetros

Tipos compatíveis:

* listInteger
* listDecimal
* decimal
* integer

## Assinaturas e tipo retornado

`avg(<listInteger>)`

`avg(<listDecimal>)`

`avg(<decimal>,<decimal>)`

`avg(<decimal>,<integer>)`

`avg(<integer>,<decimal>)`

`avg(<integer>,<integer>)`

Retorna um decimal.

## Exemplos

`avg(@{BarBeacon.inventory},5)`

`avg([10,3,8])`

Retorna 7.0.

`avg(10.2, 3)`

Retorna 6.6.
