---
product: adobe campaign
title: endWithIgnoreCase
description: Saiba mais sobre a função endWithIgnoreCase
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# endWithIgnoreCase {#endWithIgnoreCase}

Verifica se a primeira string de argumento termina com uma string específica (segunda string de argumento), não considerando o caso.

## Categoria

String

## Sintaxe da função

`endWithIgnoreCase(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| string | string |
| sufixo | string |

## Assinatura e tipo retornado

`endWithIgnoreCase(<string>,<string>)`

Retorna um booleano.

## Exemplo

`endWithIgnoreCase("rowing is great", "AT")`

Retorna true.
