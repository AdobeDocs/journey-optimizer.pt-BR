---
product: journey optimizer
title: endWithIgnoreCase
description: Saiba mais sobre a função endWithIgnoreCase
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: endWithIgnoreCase, função, expressão, jornada
exl-id: 278ef1a4-571c-4b5f-b4de-0cfc644ac7d7
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 17%

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
