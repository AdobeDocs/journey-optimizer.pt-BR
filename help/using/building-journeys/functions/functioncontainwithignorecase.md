---
product: adobe campaign
title: containIgnoreCase
description: Saiba mais sobre a função containIgnoreCase
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 26074584-a215-4515-8a61-7460bd9d4447
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
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
