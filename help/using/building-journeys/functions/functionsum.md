---
product: journey optimizer
title: sum
description: Saiba mais sobre a soma das funções
feature: Journeys
role: Engineer
level: Experienced
keywords: soma, função, expressão, jornada
exl-id: a9085f4d-6434-4bc5-8e5d-3f2b6033defc
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 12%

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
* duração
* inteiro
* decimal

## Assinaturas e tipos retornados

`sum(<listDecimal>)`

Retorna um decimal.

`sum(<listInteger>)`

Retorna um inteiro.

`sum(<integer>,<integer>)`

Retorna um inteiro.

`sum(<decimal>,<decimal>)`

Retorna um decimal.

## Exemplos

`sum(@event{BarBeacon.inventory},5)`

`sum([10,3,8])`

Retorna 21.

`sum([10.5,null,8.1])`

Retorna 18,6.
