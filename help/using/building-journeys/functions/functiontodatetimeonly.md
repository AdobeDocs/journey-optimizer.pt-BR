---
product: journey optimizer
title: toDateTimeOnly
description: Saiba mais sobre a função toDateTime
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toDateTimeOnly, função, expressão, jornada
exl-id: db54c119-5080-403a-b254-43645be6b4a8
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 15%

---

# toDateTimeOnly{#toDateTimeOnly}

Converte um valor de argumento em um valor somente de data e hora.

## Categoria

Conversão

## Sintaxe da função

`toDateTimeOnly(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| data e hora no formato ISO-8601 ou &quot;AAAA-MM-DD&quot; (formato de data XDM) | string |
| data e hora | dateTime |

## Assinaturas e tipos retornados

`toDateTimeOnly(<dateTime>)`

`toDateTimeOnly(<string>)`
<!--`toDateTimeOnly(<integer>,<integer>,<integer>)`
`toDateTimeOnly(<integer>,<integer>,<integer>,<integer>,<integer>,<integer>)`-->

Retorna um datetime sem considerar o fuso horário.

## Exemplos

`toDateTimeOnly ("2016-08-18")`

retorna um dateTime representando 2016-08-18T00:00:00.000

`toDateTimeOnly(now())`

<!--`toDateTimeOnly(2016,8,18,23,17,59)`

Returns 2016-08-18T23:17:59.000.

`toDateTimeOnly(2016,8,18)`

Returns 2016-08-18T00:00:00.000.-->
