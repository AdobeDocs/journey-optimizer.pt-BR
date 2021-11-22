---
product: adobe campaign
title: toDateOnly
description: Saiba mais sobre a função toDateOnly
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 1929644f-8b51-4f95-aea5-627fc1dd115d
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 21%

---

# toDateOnly{#toDateOnly}

Converte um valor de argumento em um valor somente de data.

## Categoria

Conversão

## Sintaxe da função

`toDateOnly(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| data no formato ISO-8601 ou &quot;AAAA-MM-DD&quot; (formato Data XDM) | string |
| data | data |

## Assinaturas e tipos retornados

`toDateOnly(<date>)`

`toDateOnly(<string>)`

Retorna um datetime sem considerar o fuso horário.

## Exemplos

`toDateOnly("2016-08-18")`

retorna um objeto dateOnly representando 2016-08-18.
