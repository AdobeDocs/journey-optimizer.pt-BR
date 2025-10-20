---
product: journey optimizer
title: startWith
description: Saiba mais sobre a função startWith
feature: Journeys
role: Engineer
level: Experienced
keywords: startWith, função, expressão, jornada
exl-id: 1abdf947-2873-4e45-a26c-cb895980e76a
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 23%

---

# startWith {#startWith}

Retornará true se o segundo parâmetro for um prefixo do primeiro.

## Categoria

String

## Sintaxe da função

`startWith(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|-------------|--------|
| sequência de caracteres | sequência de caracteres |
| prefixo | sequência de caracteres |

## Assinatura e tipo retornado

`startWith(<string>,<string>)`

Retornar um booleano.

## Exemplo

`startWith("Hello World", "Hello")`

Retorna verdadeiro.

`startWith("Hello World", "World")`

Retorna falso.
