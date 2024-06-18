---
product: journey optimizer
title: avg
description: Saiba mais sobre a função avg
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: avg, função, expressão, jornada
exl-id: cc70f90c-2d12-42a0-829f-5f28c3c29cad
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 10%

---

# avg {#avg}

Retorna o valor médio entre um conjunto de expressões, fornecido como uma lista ou duas expressões. Valores nulos são ignorados.


## Categoria

Agregação

## Sintaxe da função

`avg(<parameter>)`

## Parâmetros

Tipos suportados:

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

`avg(@event{BarBeacon.inventory},5)`

`avg([10,3,8])`

Retorna 7.0.

`avg(10.2, 3)`

Retorna 6.6.
