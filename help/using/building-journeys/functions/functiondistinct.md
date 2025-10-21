---
product: journey optimizer
title: distinct
description: Saiba mais sobre a distinção de função
feature: Journeys
role: Developer
level: Experienced
keywords: distinct, função, expressão, jornada
exl-id: f4e2dd34-b634-4a91-af53-60be155a65d0
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 6%

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
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly ou listObject | Lista a processar. Para listObject, ele deve ser uma referência de campo. |
| keyAttributeName | sequência de caracteres | Este parâmetro é opcional e somente para listObject. Se o parâmetro não for fornecido, um objeto será considerado duplicado se todos os atributos tiverem os mesmos valores. Caso contrário, um objeto será considerado duplicado se o atributo em questão tiver o mesmo valor. |

## Assinaturas e tipos retornados

`distinct(<listInteger>)`

Retorna uma lista de inteiros.

`distinct(<listDecimal>)`

Retorna uma lista de decimais.

`distinct(<listString>)`

Retorna uma lista de strings.

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

Retorna `[10, 2]`.
