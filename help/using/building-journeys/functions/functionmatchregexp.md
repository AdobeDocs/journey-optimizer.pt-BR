---
product: adobe campaign
title: matchRegExp
description: Saiba mais sobre a função matchRegExp
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 4695c88b4372a0f2a804bef268ae6f2d39eb2f0b
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 18%

---

# matchRegExp {#matchRegExp}

Retorna true se a string no primeiro parâmetro corresponder à expressão regular no segundo parâmetro. Para obter mais informações, consulte [esta página](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html).

## Categoria

String

## Sintaxe da função

`matchRegExp(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|--- |--- |
| string | string |
| regexp | string |

## Assinatura e tipo retornado

`matchRegExp(<string>,<string>)`

Retorna um booleano.

## Exemplo

`matchRegExp("username@adobe.com", "*adobe")`

Retorna true.
