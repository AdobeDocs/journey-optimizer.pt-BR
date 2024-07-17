---
product: journey optimizer
title: concat
description: Saiba mais sobre a função concat
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: concat, função, expressão, jornada
exl-id: 690c8aa9-f754-4720-b4ed-a338e5d3b79d
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 25%

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
| sequência de caracteres | sequência de caracteres |

## Assinatura e tipo retornado

`concat(<string>,<string>)`

`concat(<listString>)`

Retorna uma string.

## Exemplo

`concat("Hello","World")`

Retorna &quot;HelloWorld&quot;.

`concat(["Hello"," ","World"])`

Retorna &quot;Olá, Mundo&quot;.
