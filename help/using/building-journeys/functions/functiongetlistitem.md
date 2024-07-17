---
product: journey optimizer
title: getListItem
description: Saiba mais sobre a função gstListItem
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: getListItem, função, expressão, jornada
exl-id: e995f479-bbaa-45f3-9531-e05680c5a723
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 18%

---

# getListItem {#gestListItem}

Retorna o item da lista no índice fornecido.

## Categoria

Lista

## Sintaxe da função

`getListItem(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| list | listString |
| list | listBoolean |
| list | listInteger |
| list | listDecimal |
| list | listDuration |
| list | listDateTime |
| list | listDateTimeOnly |
| list | listDateOnly |
| índice | inteiro |

## Assinaturas e tipo retornado

`getListItem(<listInteger>,<index>)`

Retorna um inteiro.

`getListItem(<listDecimal>,<index>)`

Retorna um decimal.

`getListItem(<listString>,<index>)`

Retorna uma string.

`getListItem(<listDateTimeOnly>,<index>)`

Retorna uma data e hora sem considerar o fuso horário.

`getListItem(<listDateTime>,<index>)`

Retorna um datetime.

`getListItem(<listDateOnly>,<index>)`

Retorna uma lista de datas.

`getListItem(<listBoolean>,<index>)`

Retorna um valor booleano.

`getListItem(<listDuration>,<index>)`

Retorna uma duração.

## Exemplo

`getListItem([10, 2, 3], 1)`

Retorna &quot;2&quot;

`getListItem(["A", "B", "C"], 2)`
Retorna &quot;C&quot;

Exemplos com um campo de evento &quot;event.appVersion&quot; com valor: &quot;20.45.2.3434&quot;

`split(@event{event.appVersion}, "\\.")`

Retorna `["20", "45", "2", "3434"]`

`getListItem(split(@event{event.appVersion}, "\\."), 0)`

Retorna &quot;20&quot;
