---
product: adobe campaign
title: distinct
description: Saiba mais sobre a função distinta
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: f4e2dd34-b634-4a91-af53-60be155a65d0
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 18%

---

# distinct {#distinct}

Retorna os valores distintos da lista sem valores nulos.

## Categoria

Lista

## Sintaxe da função

`distinct(<parameter>)`

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

## Assinaturas e tipos retornados

`distinct(<listInteger>)`

Retorna uma lista de números inteiros.

`distinct(<listDecimal>)`

Retorna uma lista de decimais.

`distinct(<listString>)`

Retorna uma lista de cadeias de caracteres.

`distinct(<listDateTimeOnly>)`

Retorna uma lista de datetimes sem considerar o fuso horário.

`distinct(<listDateTime>)`

Retorna uma lista de datetimes.

`distinct(<listDateOnly>)`

Retorna uma lista de datas.

`distinct(<listBoolean>)`

Retorna uma lista de booleanos.

`distinct(<listDuration>)`

Retorna uma lista de durações.

## Exemplos

`distinct([10,2,10,null])`

Devoluções `[10, 2]`.
