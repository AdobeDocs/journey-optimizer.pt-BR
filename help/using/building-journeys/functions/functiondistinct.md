---
product: journey optimizer
title: distinct
description: Saiba mais sobre a função distinta
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: f4e2dd34-b634-4a91-af53-60be155a65d0
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 7%

---

# distinct {#distinct}

Retorna os valores ou objetos distintos de uma determinada lista. Entradas nulas são ignoradas.

## Categoria

Lista

## Sintaxe da função

`distinct(<parameters>)`

## Parâmetros

| Parâmetro | Tipo | Descrição |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly ou listObject | Lista para processar. Para listObject, deve ser uma referência de campo. |
| keyAttributeName | string | Esse parâmetro é opcional e somente para listObject. Se o parâmetro não for fornecido, um objeto será considerado duplicado se todos os atributos tiverem os mesmos valores. Caso contrário, um objeto será considerado duplicado se o atributo em questão tiver o mesmo valor. |

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

`distinct(<listObject>)`

`distinct(<listObject>,<string>)`

Retorna uma lista de objetos.


## Exemplos

`distinct([10,2,10,null])`

Devoluções `[10, 2]`.
