---
product: adobe campaign
title: count
description: Saiba mais sobre a contagem de funções
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 6980c1ec-3afd-4fc9-ae10-76bcf7364a04
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 30%

---

# count {#count}

Conta os elementos da lista que não consideram os valores nulos.

## Categoria

Agregação

## Sintaxe da função

`count(<listAny>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| Lista | listString |
| Lista | listBoolean |
| Lista | listInteger |
| Lista | listDecimal |
| Lista | listDuration |
| Lista | listDateTime |
| Lista | listDateTimeOnly |
| Lista | listDateOnly |

## Assinaturas e tipo retornado

`count(<listAny>)`

Retorna um número inteiro.

## Exemplo

`count([10,2,10,null])`

Retorna 3.
