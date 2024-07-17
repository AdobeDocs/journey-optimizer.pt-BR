---
product: journey optimizer
title: endWith
description: Saiba mais sobre a função endWith
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: endWith, função, expressão, jornada
exl-id: ae54c127-9de2-42fd-942c-664d2cfe66d2
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 23%

---

# endWith {#endWith}

Retornará true se o segundo parâmetro for um sufixo do primeiro.

## Categoria

String

## Sintaxe da função

`endWith(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| sequência de caracteres | sequência de caracteres |
| sufixo | sequência de caracteres |

## Assinatura e tipo retornado

`endWith(<string>,<string>)`

Retorna um valor booleano.

## Exemplo

`endWith("Hello World", "World")`

Retorna verdadeiro.

`endWith("Hello World", "Hello")`

Retorna falso.
