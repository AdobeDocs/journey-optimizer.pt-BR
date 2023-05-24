---
product: journey optimizer
title: false
description: Saiba mais sobre a função em
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: em, função, expressão, jornada
exl-id: 629b7aa3-8904-453b-ba3c-c6a333b13c81
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 18%

---

# no {#in}

Verifica se o primeiro valor de argumento está na lista. A verificação é executada por meio de um valor Igual em cada argumento. Retornará true se o valor do argumento for encontrado; caso contrário, retornará false.

O tipo de `<expression>` deve corresponder aos itens da lista. Os tipos de itens da lista, como lembrete, devem corresponder um ao outro.

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

Retornar um booleano.

## Exemplo

`in(4,[4,5,3,4])`

Retorna verdadeiro.

`in(8,[4,5,3,4])`

Retorna falso.

`in(#{ExperiencePlatform.ProfileFieldGroup.profile.person.gender}, ["male"])`
