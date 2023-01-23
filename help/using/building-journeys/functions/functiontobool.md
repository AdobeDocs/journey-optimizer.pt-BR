---
product: journey optimizer
title: toBool
description: Saiba mais sobre a função para Bool
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: Ferramenta, função, expressão, jornada
exl-id: 0bb68d05-bb90-48b7-aff3-82ab15d55ebe
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '78'
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
