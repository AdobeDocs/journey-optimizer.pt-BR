---
product: adobe campaign
title: split
description: Saiba mais sobre a divisão de funções
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 37bcdf98-203c-4f82-8d8a-be2b2c45c4e7
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 19%

---

# split {#split}

Divida a primeira string de argumento por uma string separadora (segunda string de argumento, que pode ser uma expressão regular) para produzir uma lista de strings (tokens).

## Categoria

String

## Sintaxe da função

`split(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| string de entrada | string |
| sequência separadora | string |

## Assinaturas e tipo retornado

`split(<input string>, <separator string>)`

Retorna listString.

## Exemplo

`split(["A_B_C"], "_")`

Devoluções `["A","B","C"]`

Exemplo com um campo de evento &#39;event.appVersion&#39; com o valor: &quot;20.45.2.3434&quot;

`split(@{event.appVersion}, "\\.")`

Devoluções `["20", "45", "2", "3434"]`
