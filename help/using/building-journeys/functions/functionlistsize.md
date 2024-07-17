---
product: journey optimizer
title: listSize
description: Saiba mais sobre a função listSize
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: listSize, função, expressão, jornada
exl-id: dd378e4d-f65a-495c-ac10-b4209d6b6b88
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 11%

---

# listSize {#listSize}

Conta o número de elementos na lista.

## Categoria

Lista

## Sintaxe da função

`listSize(<parameters>)`

## Parâmetros

| Parâmetro | Tipo | Descrição |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly ou listObject | Lista a processar. Para listObject, ele deve ser uma referência de campo. Um listObject não pode conter um objeto nulo. |

## Assinaturas e tipo retornado

`listSize(<listInteger>)`

`listSize(<listDecimal>)`

`listSize(<listString>)`

`listSize(<listBoolean>)`

`listSize(<listDateTimeOnly>)`

`listSize(<listDateTime>)`

`listSize(<listDateOnly>)`

`listSize(<listDuration>)`

Retorna um número inteiro.

`listSize(<listObject>)`

## Exemplo

`listSize([10,2,3])`

Retorna 3.

`listSize(@event{my_event.productListItems})`

Retorna o número de objetos na matriz de objetos fornecida (tipo listObject).
