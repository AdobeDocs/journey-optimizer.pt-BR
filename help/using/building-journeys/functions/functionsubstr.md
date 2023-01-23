---
product: journey optimizer
title: substr
description: Saiba mais sobre a função substr
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: substr, função, expressão, jornada
exl-id: 58a3107a-b4f3-43da-b454-5ce597515847
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 14%

---

# substr {#substr}

Retorna a substring da expressão da string entre o índice begin e o índice end. Se o índice final não estiver definido, ele estará entre o índice inicial e o final.

## Categoria

String

## Sintaxe da função

`substr(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|-------------|----------|
| string | string |
| beginIndex | integer |
| endIndex | integer |

## Assinatura e tipo retornado

`substr(<string>,<beginIndex>)`

`substr(<string>,<beginIndex>,<endIndex>)`

Retorne uma string.

## Exemplo

`substr("Hello World",6)`

Retorna &quot;Mundo&quot;.

`substr("Hello World", 0, 5)`

Retorna &quot;Hello&quot;.
