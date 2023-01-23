---
product: journey optimizer
title: containIgnoreCase
description: Saiba mais sobre a função containIgnoreCase
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: containIgnoreCase, função, expressão, jornada
exl-id: 26074584-a215-4515-8a61-7460bd9d4447
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 21%

---

# containIgnoreCase {#containIgnoreCase}

Verifica se a segunda string de argumento está contida na primeira string de argumento, sem considerar o caso.

## Categoria

String

## Sintaxe da função

`containIgnoreCase(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| string | string |
| string pesquisada | string |

## Assinatura e tipo retornado

`containIgnoreCase(<string>,<string>)`

Retorna um booleano.

## Exemplo

`containIgnoreCase("rowing is great", "GREAT")`

Retorna true.
