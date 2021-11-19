---
product: adobe campaign
title: startWith
description: Saiba mais sobre a função startWith
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '43'
ht-degree: 25%

---

# startWith {#startWith}

Retorna true se o segundo parâmetro for um prefixo do primeiro.

## Categoria

String

## Sintaxe da função

`startWith(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|-------------|--------|
| string | string |
| prefixo | string |

## Assinatura e tipo retornado

`startWith(<string>,<string>)`

Retorne um booleano.

## Exemplo

`startWith("Hello World", "Hello")`

Retorna true.

`startWith("Hello World", "World")`

Retorna false.
