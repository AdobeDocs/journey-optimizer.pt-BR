---
product: journey optimizer
title: distinctCount
description: Saiba mais sobre a função distinctCount
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctCount, função, expressão, jornada
exl-id: 8796ba91-5c64-43c2-a444-27ac8b719c86
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 29%

---

# distinctCount{#distinctCount}

Conta o número de valores diferentes ignorando os valores nulos.

## Categoria

Agregação

## Sintaxe da função

`distinctCount(<listAny>)`

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

## Assinatura e tipo retornado

`distinctCount(<listAny>)`

Retorna um inteiro.

## Exemplo

`distinctCount([10,2,10,null])`

Retorna 2.
