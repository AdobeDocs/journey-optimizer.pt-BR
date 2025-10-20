---
product: journey optimizer
title: filtro
description: Saiba mais sobre o filtro de função
feature: Journeys
role: Engineer
level: Experienced
keywords: filtro, função, expressão, jornada
exl-id: 05e3d2ba-1a27-4f27-88cc-3d83eb3b14af
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 9%

---

# filtro{#filter}

Retorna um listObject com objetos que têm o atributo de chave correspondente a um dos valores de chave fornecidos.

## Categoria

Lista

## Sintaxe da função

`filter(<parameters>)`

## Parâmetros

| Parâmetro | Tipo | Descrição |
|-----------|------------------|------------------|
| listToFilter | listObject | lista de objetos a serem filtrados. Deve ser uma referência de campo. |
| keyAttributeName | sequência de caracteres | nome do atributo nos objetos da lista fornecida, usado como chave para filtragem |
| keyValueList | list | matriz de valores principais para filtragem |

## Assinaturas e tipos retornados

`filter(listObject, string, listString)`

`filter(listObject, string, listInteger)`

`filter(listObject, string, listDecimal)`

`filter(listObject, string, listDateTime)`

`filter(listObject, string, listDateTimeOnly)`

`filter(listObject, string, listDateOnly)`

`filter(listObject, string, listDuration)`

`filter(listObject, string, listBoolean)`

Retorna um listObject.

## Exemplos

Este é um exemplo de uma carga útil transmitida em um evento de entrada &quot;myevent&quot;:

```json
"productListItems": [{
   "id": "product1",
   "name": "the product 1",
   "price": 20
},{
   "id": "product2",
   "name": "the product 2",
   "price": 30
},{
   "id": "product3",
   "name": "the product 3",
   "price": 50
}]
```

Você pode usar a seguinte expressão:

```json
filter(
 @event{myevent.productListItems},
 "id", 
 ["product2", "product3", "product4"]
)
```

Retorna um listObject contendo os dois objetos com &quot;product2&quot; e &quot;product3&quot; como id.
