---
product: journey optimizer
title: endWith
description: Saiba mais sobre a função endWith
feature: Journeys
role: Engineer
level: Experienced
keywords: endWith, função, expressão, jornada
exl-id: ae54c127-9de2-42fd-942c-664d2cfe66d2
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 23%

---

# endWith {#endWith}

Retornará true se o segundo parâmetro for um sufixo do primeiro.

## Categoria

String

## Sintaxe da função

`endWith(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| sequência de caracteres | sequência de caracteres |
| sufixo | sequência de caracteres |

## Assinatura e tipo retornado

`endWith(<string>,<string>)`

Retorna um valor booleano.

## Exemplo

`endWith("Hello World", "World")`

Retorna verdadeiro.

`endWith("Hello World", "Hello")`

Retorna falso.
