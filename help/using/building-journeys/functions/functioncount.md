---
product: journey optimizer
title: contagem
description: Saiba mais sobre a contagem de funções
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: count, function, expression, jornada
exl-id: 6980c1ec-3afd-4fc9-ae10-76bcf7364a04
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 10%

---

# contagem {#count}

Conta os elementos da lista sem levar em conta os valores nulos.

## Categoria

Agregação

## Sintaxe da função

`count(<listAny>)`

`count(<listObject>)`

## Parâmetros

| Parâmetro | Tipo | Descrição |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly ou listObject | Lista a processar. Para listObject, ele deve ser uma referência de campo. Um listObject não pode conter um objeto nulo. |

## Assinaturas e tipo retornado

`count(<listAny>)`

Retorna um inteiro.

## Exemplo

`count([10,2,10,null])`

Retorna 3.

`count(@event{my_event.productListItems})`

Retorna o número de objetos na matriz de objetos fornecida (tipo listObject). Observação: um listObject não pode conter objeto nulo
