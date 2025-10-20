---
product: journey optimizer
title: containIgnoreCase
description: Saiba mais sobre a função containIgnoreCase
feature: Journeys
role: Engineer
level: Experienced
keywords: containIgnoreCase, função, expressão, jornada
exl-id: 26074584-a215-4515-8a61-7460bd9d4447
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 21%

---

# containIgnoreCase {#containIgnoreCase}

Verifica se a segunda cadeia de caracteres do argumento está contida na primeira cadeia de caracteres do argumento, sem levar em conta maiúsculas e minúsculas.

## Categoria

String

## Sintaxe da função

`containIgnoreCase(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| sequência de caracteres | sequência de caracteres |
| sequência de caracteres pesquisada | sequência de caracteres |

## Assinatura e tipo retornado

`containIgnoreCase(<string>,<string>)`

Retorna um valor booleano.

## Exemplo

`containIgnoreCase("rowing is great", "GREAT")`

Retorna verdadeiro.
