---
product: journey optimizer
title: split
description: Saiba mais sobre a divisão de função
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: split, função, expressão, jornada
exl-id: 37bcdf98-203c-4f82-8d8a-be2b2c45c4e7
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 13%

---

# split {#split}

Divide a primeira sequência de argumento com uma sequência de separador (segunda sequência de argumento, que pode ser uma expressão regular) para produzir uma lista de sequências de caracteres (tokens).

## Categoria

String

## Sintaxe da função

`split(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| string de entrada | sequência de caracteres |
| sequência de caracteres separadora | sequência de caracteres |

## Assinaturas e tipo retornado

`split(<input string>, <separator string>)`

Retorna uma listString.

## Exemplo

`split("A_B_C", "_")`

Devoluções `["A","B","C"]`

Exemplo com um campo de evento &quot;event.appVersion&quot; com valor: &quot;20.45.2.3434&quot;

`split(@event{event.appVersion}, "\\.")`

Devoluções `["20", "45", "2", "3434"]`
