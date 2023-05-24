---
product: journey optimizer
title: countOnlyNull
description: Saiba mais sobre a função countOnlyNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countOnlyNull, função, expressão, jornada
exl-id: d06fc594-33dd-48ce-8c62-2f2892a867da
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 30%

---

# countOnlyNull {#countOnlyNull}

Conta o número de valores nulos na lista.

## Categoria

Agregação

## Sintaxe da função

`countOnlyNull(<listAny>)`

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

`countOnlyNull(<listAny>)`

Retorna um inteiro.

## Exemplo

`countOnlyNull([10,2,10,null])`

Retorna 1.
