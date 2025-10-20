---
product: journey optimizer
title: serializeList
description: Saiba mais sobre a função serializeList
feature: Journeys
role: Engineer
level: Experienced
keywords: serializeList, função, expressão, jornada
exl-id: 7ead9fa1-59b3-4960-818c-fe6321422952
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 12%

---

# serializeList {#serializeList}

Converte uma determinada lista (qualquer tipo, exceto listObject) em uma cadeia de caracteres.

## Categoria

Lista

## Sintaxe da função

`serializeList(<parameters>)`

## Parâmetros

| Parâmetro | Tipo | Descrição |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly | Lista para converter em uma cadeia de caracteres. |
| separador | sequência de caracteres | Separador entre cada elemento da lista na cadeia de caracteres de saída. |
| addQuotes | booleano | Esse parâmetro indica se cada elemento na string de saída deve incluir aspas (true) ou não (false). |

## Assinatura e tipo retornado

`serializeList(<listInteger>,<string>,<boolean>)`

`serializeList(<listDecimal>,<string>,<boolean>)`

`serializeList(<listString>,<string>,<boolean>)`

`serializeList(<listBoolean>,<string>,<boolean>)`

`serializeList(<listDateTimeOnly>,<string>,<boolean>)`

`serializeList(<listDateTime>,<string>,<boolean>)`

`serializeList(<listDateOnly>,<string>,<boolean>)`

`serializeList(<listDuration>,<string>,<boolean>)`

Retorna uma string.

## Exemplo

`serializeList(["Hello","World"], " ", false)`

Retorna &quot;Olá, Mundo&quot;.

`serializeList(["Hello", "World"], ",", true)`

Retorna &quot;&quot;Olá&quot;,&quot;Mundo&quot;&quot;.
