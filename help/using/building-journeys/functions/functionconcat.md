---
product: adobe campaign
title: concat
description: Saiba mais sobre a função concat
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 690c8aa9-f754-4720-b4ed-a338e5d3b79d
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '40'
ht-degree: 27%

---

# concat {#concat}

Concatena dois parâmetros de string ou uma lista de strings.

## Categoria

String

## Sintaxe da função

`concat(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| Lista | listString |
| string | string |

## Assinatura e tipo retornado

`concat(<string>,<string>)`

`concat(<listString>)`

Retorna uma string.

## Exemplo

`concat("Hello","World")`

Retorna &quot;HelloWorld&quot;.

`concat(["Hello"," ","World"])`

Retorna &quot;Hello World&quot;.
