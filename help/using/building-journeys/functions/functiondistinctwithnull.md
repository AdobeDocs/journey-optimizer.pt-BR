---
product: journey optimizer
title: distinctWithNull
description: Saiba mais sobre a função distinctWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctWithNull, função, expressão, jornada
exl-id: 73fa9837-d2e1-4f0a-a423-cf7728882eba
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 7%

---

# distinctWithNull {#distinctWithNull}

Retorna os valores ou objetos distintos de uma determinada lista. Se a lista tiver pelo menos uma entrada nula, uma entrada nula estará presente na lista retornada.

Observe que o parâmetro `<listObject>` não tem suporte nessa função.

## Categoria

Lista

## Sintaxe da função

`distinctWithNull(<parameters>)`

## Parâmetros

| Parâmetro | Tipo | Descrição |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly | Lista a processar. |

## Assinaturas e tipos retornados

`distinctWithNull(<listInteger>)`

Retorna uma lista de inteiros.

`distinctWithNull(<listDecimal>)`

Retorna uma lista de decimais.

`distinctWithNull(<listString>)`

Retorna uma lista de strings.

`distinctWithNull(<listDateTimeOnly>)`

Retorna uma lista de datetimes sem considerar o fuso horário.

`distinctWithNull(<listDateTime>)`

Retorna uma lista de datetimes.

`distinctWithNull(<listDateOnly>)`

Retorna uma lista de datas.

`distinctWithNull(<listBoolean>)`

Retorna uma lista de booleanos.

`distinctWithNull(<listDuration>)`

Retorna uma lista de durações.

## Exemplos

`distinctWithNull([10,2,10,null])`

Retorna [10, 2, nulo]
