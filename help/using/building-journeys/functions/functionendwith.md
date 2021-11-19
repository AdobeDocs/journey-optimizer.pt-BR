---
product: adobe campaign
title: endWith
description: Saiba mais sobre a função endWith
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '43'
ht-degree: 25%

---

# endWith {#endWith}

Retorna true se o segundo parâmetro for um sufixo do primeiro.

## Categoria

String

## Sintaxe da função

`endWith(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| string | string |
| sufixo | string |

## Assinatura e tipo retornado

`endWith(<string>,<string>)`

Retorna um booleano.

## Exemplo

`endWith("Hello World", "World")`

Retorna true.

`endWith("Hello World", "Hello")`

Retorna false.
