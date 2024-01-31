---
product: journey optimizer
title: distinctCount
description: Saiba mais sobre a função distinctCount
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctCount, função, expressão, jornada
exl-id: 8796ba91-5c64-43c2-a444-27ac8b719c86
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 7%

---

# distinctCount{#distinctCount}

Conta o número de valores diferentes ignorando os valores nulos.

## Categoria

Agregação

## Sintaxe da função

`distinctCount(<listAny>)`

## Parâmetros

| Parâmetro | Tipo | Descrição |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly ou listObject | Lista a processar. Para listObject, ele deve ser uma referência de campo. |
| keyAttributeName | string | Este parâmetro é opcional e somente para listObject. Se o parâmetro não for fornecido, um objeto será considerado duplicado se todos os atributos tiverem os mesmos valores. Caso contrário, um objeto será considerado duplicado se o atributo em questão tiver o mesmo valor. |

## Assinatura e tipo retornado

`distinctCount(<listAny>)`

Retorna um inteiro.

`distinctCount(<listObject>)`

`distinctCount(<listObject>,<string>)`

Retorna uma lista de objetos.


## Exemplo

`distinctCount([10,2,10,null])`

Retorna 2.

`distinctCount(@event{my_event.productListItems})`

Retorna o número de objetos estritamente distintos na matriz de objetos fornecida (tipo listObject).

`distinctCount(@event{my_event.productListItems}, "SKU")`

Retorna o número de objetos que têm um valor de atributo &quot;SKU&quot; distinto{}.
