---
product: journey optimizer
title: matchRegExp
description: Saiba mais sobre a função matchRegExp
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: matchRegExp, função, expressão, jornada
exl-id: 24cf362c-f390-4bb1-be82-a079bc27fa1f
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 19%

---

# matchRegExp {#matchRegExp}

Retornará true se a cadeia de caracteres no primeiro parâmetro corresponder à expressão regular no segundo parâmetro. Para obter mais informações, consulte [esta página](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html).

## Categoria

String

## Sintaxe da função

`matchRegExp(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|--- |--- |
| sequência de caracteres | sequência de caracteres |
| regexp | sequência de caracteres |

## Assinatura e tipo retornado

`matchRegExp(<string>,<string>)`

Retorna um valor booleano.

## Exemplo

`matchRegExp("username@adobe.com", "*adobe")`

Retorna verdadeiro.
