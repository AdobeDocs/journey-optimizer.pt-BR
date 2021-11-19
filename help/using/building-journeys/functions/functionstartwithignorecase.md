---
product: adobe campaign
title: startWithIgnoreCase
description: Saiba mais sobre a função startWithIgnoreCase
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 25%

---

# startWithIgnoreCase {#startWithIgnoreCase}

Retorna true se o segundo parâmetro for um prefixo do primeiro sem considerar um caso.

## Categoria

String

## Sintaxe da função

`startWithIgnoreCase(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|-------------|--------|
| string | string |
| prefixo | string |

## Assinatura e tipo retornado

`startWithIgnoreCase(<string>,<string>)`

Retorne um booleano.

## Exemplo

`startWithIgnoreCase("rowing is great", "RO")`

Retorna true.
