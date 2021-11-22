---
product: adobe campaign
title: startWithIgnoreCase
description: Saiba mais sobre a função startWithIgnoreCase
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: b6bd9f77-272f-4c2b-b085-20ab5f043793
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
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
