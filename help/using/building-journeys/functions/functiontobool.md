---
product: adobe campaign
title: toBool
description: Saiba mais sobre a função para Bool
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 10%

---

# toBool {#toBool}

Converte um valor de argumento em um valor booleano, dependendo de seu tipo.

* Da string: tente converter o valor da string como um booleano, de &quot;true&quot; se o valor da string for &quot;true&quot;, caso contrário, false
* De numérico: true se o valor numérico não for igual a 0, false caso contrário

## Categoria

Conversão

## Sintaxe da função

`toBool(<parameter>)`

## Parâmetros

* decimal
* booleano
* string
* integer

## Assinaturas e tipos retornados

`toBool(<decimal>)`

`toBool(<boolean>)`

`toBool(<string>)`

`toBool(<integer>)`

Retorne um booleano.

## Exemplos

`toBool("true")`

`toBool(1)`

Retorna true.

`toBool("this is not a boolean")`

Retorna false.
