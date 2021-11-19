---
product: adobe campaign
title: 'no'
description: Saiba mais sobre a função em
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: d786f3d42515d65a6574f51b6cff4b85063a0126
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 19%

---

# no {#in}

Verifica se o primeiro valor do argumento está na lista. A verificação é executada por meio de um Igual em cada valor de argumento. Retorna true se o valor do argumento for encontrado, caso contrário, retornará false.

O tipo de `<expression>` deve corresponder aos itens da lista. Os tipos de itens da lista, como lembrete, devem corresponder entre si.

## Categoria

Lista

## Sintaxe da função

`in(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| String | String |
| Booleano | Booleano |
| Número inteiro | Número inteiro |
| Decimal | Decimal |
| Duração | Duração |
| DateTime | DateTime |
| DateTimeOnly | DateTimeOnly |
| Lista | listString |
| Lista | listBoolean |
| Lista | listInteger |
| Lista | listDecimal |
| Lista | listDuration |
| Lista | listDateTime |
| Lista | listDateTimeOnly |
| Lista | listDateOnly |

## Assinatura e tipo retornado

`in(<integer>,<listInteger>)`

`in(<decimal>,<listDecimal>)`

`in(<string>,<listString>)`

`in(<boolean>,<listBoolean>)`

`in(<dateTimeOnly>,<listDateTimeOnly>)`

`in(<dateTime>,<listDateTime>)`

`in(<dateOnly>,<listDateOnly>)`

`in(<duration>,<listDuration>)`

Retorne um booleano.

## Exemplo

`in(4,[4,5,3,4])`

Retorna true.

`in(8,[4,5,3,4])`

Retorna false.

`in(#{ExperiencePlatform.ProfileFieldGroup.profile.person.gender}, ["male"])`
