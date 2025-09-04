---
product: journey optimizer
title: endWithIgnoreCase
description: Saiba mais sobre a função endWithIgnoreCase
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: endWithIgnoreCase, função, expressão, jornada
exl-id: 278ef1a4-571c-4b5f-b4de-0cfc644ac7d7
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 17%

---

# endWithIgnoreCase {#endWithIgnoreCase}

Verifica se a primeira sequência de argumento termina com uma sequência específica (segunda sequência de argumento), sem levar em conta maiúsculas e minúsculas.

## Categoria

String

## Sintaxe da função

`endWithIgnoreCase(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| sequência de caracteres | sequência de caracteres |
| sufixo | sequência de caracteres |

## Assinatura e tipo retornado

`endWithIgnoreCase(<string>,<string>)`

Retorna um valor booleano.

## Exemplo

`endWithIgnoreCase("rowing is great", "AT")`

Retorna verdadeiro.
