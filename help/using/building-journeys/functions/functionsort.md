---
product: adobe campaign
title: sort
description: Saiba mais sobre a classificação de função
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 607e1424-4165-48ae-b896-cce2d18f7dcc
source-git-commit: 0facae9e7eafc9f6fcbefbdc6d5563322eaf1251
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 9%

---

# sort {#sort}

Classifica uma lista de valores ou objetos na ordem natural.

## Categoria

Lista

## Sintaxe da função

`sort(<parameters>)`

## Parâmetros

| Parâmetro | Tipo | Descrição |
|-----------|------------------|------------------|
| listToSort | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly ou listObject | Lista para classificar. Para listObject, deve ser uma referência de campo. |
| keyAttributeName | string | Esse parâmetro é somente para listObject. O nome do atributo nos objetos da lista fornecida é usado como chave para classificação. |
| sortingOrder | booleano | Crescente (true) ou decrescente (false) |

## Assinatura e tipo retornado

`sort(<listInteger>,<boolean>)`

Retorna uma lista de números inteiros.

`sort(<listDecimal>,<boolean>)`

Retorna uma lista de decimais.

`sort(<listString>,<boolean>)`

Retorna uma lista de cadeias de caracteres.

`sort(<listDateTimeOnly>,<boolean>)`

Retorna uma lista de datetimes sem considerar o fuso horário.

`sort(<listDateTime>,<boolean>)`

Retorna uma lista de datetimes.

`sort(<listDateOnly>,<boolean>)`

Retorna uma lista de datas.

`sort(<listBoolean>,<boolean>)`

Retorna uma lista de booleanos.

`sort(<listObject>,<string>,<boolean>)`

Retorna uma lista de objetos.

## Exemplo

`sort(["A", "C", "B"], true)`

Devoluções `["A","B","C"]`.

`sort([1, 3, 2], false)`

Devoluções `[3, 2, 1]`.

