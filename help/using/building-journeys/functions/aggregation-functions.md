---
product: journey optimizer
title: Funções de agregação
description: Saiba mais sobre funções de agregação
feature: Journeys
role: Developer
level: Experienced
keywords: agregação, funções, expressão, jornada, média, contagem, máx, mín, soma
version: Journey Orchestration
source-git-commit: af1babe501a5b2c6a67730396a8f5e2c5d85e60a
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 8%

---

# Funções de agregação {#aggregation-functions}

As funções de agregação são usadas para realizar cálculos em um conjunto de valores e retornar um único valor. Essas funções são particularmente úteis ao trabalhar com listas e matrizes em suas expressões de jornada.

## avg {#avg}

Retorna o valor médio entre um conjunto de expressões, fornecido como uma lista ou duas expressões. Valores nulos são ignorados.

+++Sintaxe

`avg(<parameter>)`

+++

+++Parâmetros

Tipos suportados:

* listInteger
* listDecimal
* decimal
* inteiro

+++

+++Assinaturas e tipo retornado

`avg(<listInteger>)`

`avg(<listDecimal>)`

`avg(<decimal>,<decimal>)`

`avg(<decimal>,<integer>)`

`avg(<integer>,<decimal>)`

`avg(<integer>,<integer>)`

Retorna um decimal.

+++

+++Exemplos

`avg(@event{BarBeacon.inventory},5)`

`avg([10,3,8])`

Retorna 7.0.

`avg(10.2, 3)`

Retorna 6.6.

+++

## contagem {#count}

Conta os elementos da lista sem levar em conta os valores nulos.

+++Sintaxe

`count(<listAny>)`

`count(<listObject>)`

+++

+++Parâmetros

| Parâmetro | Tipo | Descrição |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly ou listObject | Lista a processar. Para listObject, ele deve ser uma referência de campo. Um listObject não pode conter um objeto nulo. |

+++

+++Assinaturas e tipo retornado

`count(<listAny>)`

Retorna um inteiro.

+++

+++Exemplos

`count([10,2,10,null])`

Retorna 3.

`count(@event{my_event.productListItems})`

Retorna o número de objetos na matriz de objetos fornecida (tipo listObject). Observação: um listObject não pode conter objeto nulo

+++

## countOnlyNull {#countOnlyNull}

Conta o número de valores nulos na lista.

**Observação:** o parâmetro `<listObject>` não tem suporte nesta função.

+++Sintaxe

`countOnlyNull(<listAny>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

+++

+++Assinaturas e tipo retornado

`countOnlyNull(<listAny>)`

Retorna um inteiro.

+++

+++Exemplos

`countOnlyNull([10,2,10,null])`

Retorna 1.

+++

## countWithNull {#countWithNull}

Conta todos os elementos da lista, incluindo valores nulos.

**Observação:** o parâmetro `<listObject>` não tem suporte nesta função.

+++Sintaxe

`countWithNull(<listAny>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

+++

+++Assinaturas e tipo retornado

`countWithNull(<listAny>)`

Retorna um inteiro.

+++

+++Exemplos

`countWithNull([10,2,10,null])`

Retorna 4.

+++

## distinctCount {#distinctCount}

Conta o número de valores diferentes ignorando os valores nulos.

+++Sintaxe

`distinctCount(<listAny>)`

+++

+++Parâmetros

| Parâmetro | Tipo | Descrição |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly ou listObject | Lista a processar. Para listObject, ele deve ser uma referência de campo. |
| keyAttributeName | sequência de caracteres | Este parâmetro é opcional e somente para listObject. Se o parâmetro não for fornecido, um objeto será considerado duplicado se todos os atributos tiverem os mesmos valores. Caso contrário, um objeto será considerado duplicado se o atributo em questão tiver o mesmo valor. |

+++

+++Assinaturas e tipo retornado

`distinctCount(<listAny>)`

Retorna um inteiro.

`distinctCount(<listObject>)`

`distinctCount(<listObject>,<string>)`

Retorna uma lista de objetos.

+++

+++Exemplos

`distinctCount([10,2,10,null])`

Retorna 2.

`distinctCount(@event{my_event.productListItems})`

Retorna o número de objetos estritamente distintos na matriz de objetos fornecida (tipo listObject).

`distinctCount(@event{my_event.productListItems}, "SKU")`

Retorna o número de objetos que têm um valor de atributo &quot;SKU&quot; distinto {}.

+++

## distinctCountWithNull {#distinctCountWithNull}

Conta o número de valores diferentes, incluindo os valores nulos.

**Observação:** o parâmetro `<listObject>` não tem suporte nesta função.

+++Sintaxe

`distinctCountWithNull(<listAny>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

+++

+++Assinaturas e tipo retornado

`distinctCountWithNull(<listAny>)`

Retorna um inteiro.

+++

+++Exemplos

`distinctCountWithNull([10,2,10,null])`

Retorna 3.

+++

## max {#max}

Retorna o valor máximo entre um conjunto de expressões, fornecido como uma lista ou duas expressões. Valores nulos são ignorados.

+++Sintaxe

`max(<parameter>)`

+++

+++Parâmetros

* listDuration
* listInteger
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* duração
* inteiro
* decimal
* dateTime
* dateTimeOnly

+++

+++Assinaturas e tipos retornados

`max(<listDuration>)`

Retorna uma duração.

`max(<listInteger>)`

Retorna uma duração.

`max(<listDateTimeOnly>)`

Retorna uma data e hora sem considerar o fuso horário.

`max(<listDateTime>)`

Retorna um datetime.

`max(<listDateOnly>)`

Retorna uma data.

`max(<listDecimal>)`

Retorna um decimal.

`max(<decimal>,<decimal>)`

Retorna um decimal.

`max(<duration>,<duration>)`

Retorna uma duração.

`max(<dateTime>,<dateTime>)`

Retorna um datetime.

`max(<dateTimeOnly>,<dateTimeOnly>)`

Retorna uma data e hora sem considerar o fuso horário.

`max(<integer>,<integer>)`

Retorna um inteiro.

+++

+++Exemplos

`max(@event{BarBeacon.inventory},5)`

`max([10,3,8])`

Retorna 10.

`max([10,null,8])`

Retorna 10.

+++

## min {#min}

Retorna o valor mínimo entre um conjunto de expressões, fornecido como uma lista ou duas expressões. Valores nulos são ignorados.

+++Sintaxe

`min(<parameters>)`

+++

+++Parâmetros

* listDuration
* listInteger
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* duração
* inteiro
* decimal
* dateTime
* dateTimeOnly

+++

+++Assinaturas e tipos retornados

`min(<listDuration>)`

Retorna uma duração.

`min(<listInteger>)`

Retorna uma duração.

`min(<listDateTimeOnly>)`

Retorna uma data e hora sem considerar o fuso horário.

`min(<listDateTime>)`

Retorna um datetime.

`min(<listDateOnly>)`

Retorna uma data.

`min(<listDecimal>)`

Retorna um decimal.

`min(<decimal>,<decimal>)`

Retorna um decimal.

`min(<duration>,<duration>)`

Retorna uma duração.

`min(<dateTime>,<dateTime>)`

Retorna um datetime.

`min(<dateTimeOnly>,<dateTimeOnly>)`

Retorna uma data e hora sem considerar o fuso horário.

`min(<integer>,<integer>)`

Retorna um inteiro.

+++

+++Exemplos

`min(@event{BarBeacon.inventory},5)`

`min([10,3,8])`

Retorna 3.

`min([10,null,8])`

Retorna 8.

+++

## sum {#sum}

Retorna a soma dos valores de um conjunto de expressões. Valores nulos são ignorados.

+++Sintaxe

`sum(<parameters>)`

+++

+++Parâmetros

* listInteger
* listDecimal
* duração
* inteiro
* decimal

+++

+++Assinaturas e tipos retornados

`sum(<listDecimal>)`

Retorna um decimal.

`sum(<listInteger>)`

Retorna um inteiro.

`sum(<integer>,<integer>)`

Retorna um inteiro.

`sum(<decimal>,<decimal>)`

Retorna um decimal.

+++

+++Exemplos

`sum(@event{BarBeacon.inventory},5)`

`sum([10,3,8])`

Retorna 21.

`sum([10.5,null,8.1])`

Retorna 18,6.

+++
