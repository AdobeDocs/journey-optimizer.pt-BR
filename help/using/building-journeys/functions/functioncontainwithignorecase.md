---
product: adobe campaign
title: containIgnoreCase
description: Saiba mais sobre a função containIgnoreCase
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

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
