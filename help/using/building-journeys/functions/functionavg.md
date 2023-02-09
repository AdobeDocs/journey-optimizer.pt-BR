---
product: journey optimizer
title: avg
description: Saiba mais sobre o avg da função
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: avg, função, expressão, jornada
exl-id: cc70f90c-2d12-42a0-829f-5f28c3c29cad
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 13%

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
* inteiro

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
