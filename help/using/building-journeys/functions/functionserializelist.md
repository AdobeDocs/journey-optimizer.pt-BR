---
product: journey optimizer
title: serializeList
description: Saiba mais sobre a função serializeList
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: serializeList, função, expressão, jornada
exl-id: 7ead9fa1-59b3-4960-818c-fe6321422952
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 21%

---

# serializeList {#serializeList}

Converte a lista (qualquer tipo) fornecida no primeiro parâmetro em uma string. O segundo parâmetro representa o separador a ser usado. O terceiro parâmetro é um valor booleano que indica se cada elemento da expressão deve incluir aspas.

## Categoria

Lista

## Sintaxe da função

`serializeList(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| String | String |
| Booleano | Booleano |
| DateTimeOnly | DateTimeOnly |
| Lista | listString |
| Lista | listBoolean |
| Lista | listPoint |
| Lista | listDecimal |
| Lista | listDuration |
| Lista | listDateTime |
| Lista | listDateTimeOnly |
| Lista | listDateOnly |

## Assinatura e tipo retornado

`serializeList(<listInteger>,<string>,<boolean>)`

`serializeList(<listDecimal>,<string>,<boolean>)`

`serializeList(<listString>,<string>,<boolean>)`

`serializeList(<listBoolean>,<string>,<boolean>)`

`serializeList(<listDateTimeOnly>,<string>,<boolean>)`

`serializeList(<listDateTime>,<string>,<boolean>)`

`serializeList(<listDateOnly>,<string>,<boolean>)`

`serializeList(<listDuration>,<string>,<boolean>)`

`serializeList(<listPoint>,<string>,<boolean>)`

Retorna uma string.

## Exemplo

`serializeList(["Hello","World"], " ", false)`

Retorna &quot;Olá, Mundo&quot;.

`serializeList(["Hello", "World"], ",", true)`

Retorna &quot;&quot;Olá&quot;,&quot;Mundo&quot;&quot;.
