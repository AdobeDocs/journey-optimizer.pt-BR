---
product: journey optimizer
title: matchRegExp
description: Saiba mais sobre a função matchRegExp
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 24cf362c-f390-4bb1-be82-a079bc27fa1f
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
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
