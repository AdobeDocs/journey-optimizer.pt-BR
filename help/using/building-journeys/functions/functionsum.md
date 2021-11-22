---
product: adobe campaign
title: sum
description: Saiba mais sobre a soma de funções
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: a9085f4d-6434-4bc5-8e5d-3f2b6033defc
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 11%

---

# sum {#sum}

Retorna a soma dos valores de um conjunto de expressões. Valores nulos são ignorados.

## Categoria

Agregação

## Sintaxe da função

`sum(<parameters>)`

## Parâmetros

* listInteger
* listDecimal
* duration
* integer
* decimal

## Assinaturas e tipos retornados

`sum(<listDecimal>)`

Retorna um decimal.

`sum(<listInteger>)`

Retorna um número inteiro.

`sum(<integer>,<integer>)`

Retorna um número inteiro.

`sum(<decimal>,<decimal>)`

Retorna um decimal.

## Exemplos

`sum(@{BarBeacon.inventory},5)`

`sum([10,3,8])`

Retorna 21.

`sum([10.5,null,8.1])`

Retorna 18.6.
