---
product: journey optimizer
title: substr
description: Saiba mais sobre a função substr
feature: Journeys
role: Engineer
level: Experienced
keywords: substr, função, expressão, jornada
exl-id: 58a3107a-b4f3-43da-b454-5ce597515847
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 17%

---

# substr {#substr}

Retorna a subcadeia de caracteres da expressão de cadeia de caracteres entre o índice inicial e o índice final. Se o índice final não estiver definido, ele será entre o índice inicial e o final.

## Categoria

String

## Sintaxe da função

`substr(<parameters>)`

## Parâmetros

| Parâmetro | tipo |
|-------------|----------|
| sequência de caracteres | sequência de caracteres |
| beginIndex | inteiro |
| endIndex | inteiro |

## Assinatura e tipo retornado

`substr(<string>,<beginIndex>)`

`substr(<string>,<beginIndex>,<endIndex>)`

Retorna uma string.

## Exemplo

`substr("Hello World",6)`

Retorna &quot;Mundo&quot;.

`substr("Hello World", 0, 5)`

Retorna &quot;Olá&quot;.
