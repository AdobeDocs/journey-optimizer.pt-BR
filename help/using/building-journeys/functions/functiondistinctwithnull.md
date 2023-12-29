---
product: journey optimizer
title: distinctWithNull
description: Saiba mais sobre a função distinctWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctWithNull, função, expressão, jornada
exl-id: 73fa9837-d2e1-4f0a-a423-cf7728882eba
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 5%

---

# distinctWithNull {#distinctWithNull}

Retorna os valores ou objetos distintos de uma determinada lista. Se a lista tiver pelo menos uma entrada nula, uma entrada nula estará presente na lista retornada.

## Categoria

Lista

## Sintaxe da função

`distinctWithNull(<parameters>)`

## Parâmetros

| Parâmetro | Tipo | Descrição |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly ou listObject | Lista a processar. Para listObject, ele deve ser uma referência de campo. |
| keyAttributeName | string | Este parâmetro é opcional e somente para listObject. Se o parâmetro não for fornecido, um objeto será considerado duplicado se todos os atributos tiverem os mesmos valores. Caso contrário, um objeto será considerado duplicado se o atributo em questão tiver o mesmo valor. |

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

`distinctWithNull(<listObject>)`

`distinctWithNull(<listObject>,<string>)`

Retorna uma lista de objetos.

## Exemplos

`distinctWithNull([10,2,10,null])`

Devoluções [10, 2, nulo]
