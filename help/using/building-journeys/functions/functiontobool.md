---
product: journey optimizer
title: toBool
description: Saiba mais sobre a função toBool
feature: Journeys
role: Engineer
level: Experienced
keywords: tobool, função, expressão, jornada
exl-id: 0bb68d05-bb90-48b7-aff3-82ab15d55ebe
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 11%

---

# toBool {#toBool}

Converte um valor de argumento em um valor booleano, dependendo de seu tipo.

* Da string: tente converter o valor da string como booleano, de &quot;true&quot; se o valor da string for &quot;true&quot;, caso contrário, false
* Do numérico: verdadeiro se o valor numérico não for igual a 0, caso contrário, falso

## Categoria

Conversão

## Sintaxe da função

`toBool(<parameter>)`

## Parâmetros

* decimal
* booleano
* sequência de caracteres
* inteiro

## Assinaturas e tipos retornados

`toBool(<decimal>)`

`toBool(<boolean>)`

`toBool(<string>)`

`toBool(<integer>)`

Retornar um booleano.

## Exemplos

`toBool("true")`

`toBool(1)`

Retorna verdadeiro.

`toBool("this is not a boolean")`

Retorna falso.
