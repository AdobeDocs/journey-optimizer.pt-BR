---
product: journey optimizer
title: sum
description: Saiba mais sobre a soma de funções
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: soma, função, expressão, jornada
exl-id: a9085f4d-6434-4bc5-8e5d-3f2b6033defc
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '55'
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
* duration
* inteiro
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
