---
product: journey optimizer
title: startWith
description: Saiba mais sobre a função startWith
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: startWith, função, expressão, jornada
exl-id: 1abdf947-2873-4e45-a26c-cb895980e76a
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
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
| string | string |
| prefixo | string |

## Assinatura e tipo retornado

`startWith(<string>,<string>)`

Retornar um booleano.

## Exemplo

`startWith("Hello World", "Hello")`

Retorna verdadeiro.

`startWith("Hello World", "World")`

Retorna falso.
