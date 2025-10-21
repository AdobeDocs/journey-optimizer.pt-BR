---
product: journey optimizer
title: replaceAll
description: Saiba mais sobre a função replaceAll
feature: Journeys
role: Developer
level: Experienced
keywords: replaceAll, função, expressão, jornada
exl-id: 5543e123-a5f4-4153-8709-97eeb9be83ba
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 10%

---

# replaceAll {#replaceAll}

Substitui todas as ocorrências correspondentes à cadeia de caracteres de destino pela cadeia de caracteres de substituição na cadeia de caracteres base.

A substituição continua do início da string até o fim. Por exemplo, substituir &quot;aa&quot; por &quot;b&quot; na string &quot;aaa&quot; resultará em &quot;ba&quot; em vez de &quot;ab&quot;.

## Categoria

String

## Sintaxe da função

`replaceAll(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|--------------|
| base | sequência de caracteres |
| destino | string (RegExp) |
| substituição | sequência de caracteres |

## Assinatura e tipo retornado

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

Retorna uma string.

## Exemplo{#example}

`replaceAll("Hello World", "l", "x")`

Retorna &quot;Hexxo Worxd&quot;.

Como o parâmetro de destino é um RegExp, dependendo da cadeia de caracteres que você deseja substituir, talvez seja necessário usar escape em alguns caracteres. Consulte o exemplo em [esta página](../functions/functionreplace.md#example_2).
