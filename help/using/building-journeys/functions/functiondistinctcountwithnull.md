---
product: journey optimizer
title: distinctCountWithNull
description: Saiba mais sobre a função distinctCountWithNull
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 2c3f629f-2220-44a4-9b0c-8aa602301098
source-git-commit: 0b19af568b33d29f4b35deeab6def17919cfe824
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 0%

---

# distinctCountWithNull {#distinctCountWithNull}

Conta o número de valores diferentes, incluindo os valores nulos.

>[!NOTE]
>
>Se a lista de destino for um listObject, essa função só poderá ser usada em expressões de ação personalizada.

## Categoria

Agregação

## Sintaxe da função

`distinctCountWithNull(<listAny>)`

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

`distinctCountWithNull(<listAny>)`

Retorna um número inteiro.

## Exemplo

`distinctCountWithNull([10,2,10,null])`

Retorna 3.
