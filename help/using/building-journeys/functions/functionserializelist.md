---
product: journey optimizer
title: serializeList
description: Saiba mais sobre a função serializeList
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: serializeList, função, expressão, jornada
exl-id: 7ead9fa1-59b3-4960-818c-fe6321422952
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
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
| separador | string | Separador entre cada elemento da lista na cadeia de caracteres de saída. |
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
