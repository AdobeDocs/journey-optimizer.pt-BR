---
product: journey optimizer
title: getListItem
description: Saiba mais sobre a função gstListItem
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: e995f479-bbaa-45f3-9531-e05680c5a723
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 20%

---

# getListItem {#gestListItem}

Retorna o item da lista no índice especificado.

## Categoria

Lista

## Sintaxe da função

`getListItem(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| listar | listString |
| listar | listBoolean |
| listar | listInteger |
| listar | listDecimal |
| listar | listDuration |
| listar | listDateTime |
| listar | listDateTimeOnly |
| listar | listDateOnly |
| índice | integer |

## Assinaturas e tipo retornado

`getListItem(<listInteger>,<index>)`

Retorna um número inteiro.

`getListItem(<listDecimal>,<index>)`

Retorna um decimal.

`getListItem(<listString>,<index>)`

Retorna uma string.

`getListItem(<listDateTimeOnly>,<index>)`

Retorna um datetime sem considerar o fuso horário.

`getListItem(<listDateTime>,<index>)`

Retorna um datetime.

`getListItem(<listDateOnly>,<index>)`

Retorna uma lista de datas.

`getListItem(<listBoolean>,<index>)`

Retorna um booleano.

`getListItem(<listDuration>,<index>)`

Retorna uma duração.

## Exemplo

`getListItem([10, 2, 3], 1)`

Retorna &quot;2&quot;

`getListItem(["A", "B", "C"], 2)`
Retorna &quot;C&quot;

Exemplos com um campo de evento &#39;event.appVersion&#39; com o valor: &quot;20.45.2.3434&quot;

`split(@{event.appVersion}, "\\.")`

Devoluções `["20", "45", "2", "3434"]`

`getListItem(split(@{event.appVersion}, "\\."), 0)`

Retorna &quot;20&quot;
