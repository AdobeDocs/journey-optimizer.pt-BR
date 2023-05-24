---
product: journey optimizer
title: startWithIgnoreCase
description: Saiba mais sobre a função startWithIgnoreCase
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: startWithIgnoreCase, função, expressão, jornada
exl-id: b6bd9f77-272f-4c2b-b085-20ab5f043793
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 22%

---

# startWithIgnoreCase {#startWithIgnoreCase}

Retornará true se o segundo parâmetro for um prefixo do primeiro sem considerar letras maiúsculas e minúsculas.

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

Retornar um booleano.

## Exemplo

`startWithIgnoreCase("rowing is great", "RO")`

Retorna verdadeiro.
