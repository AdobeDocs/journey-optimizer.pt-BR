---
product: journey optimizer
title: toInteger
description: Saiba mais sobre a função toInteger
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toInteger, função, expressão, jornada
exl-id: 901a91d1-13dd-4283-b87f-223196eb072f
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 11%

---

# toInteger {#toInteger}

Converte um valor de argumento em um inteiro.

## Categoria

Conversão

## Sintaxe da função

`toInteger(<parameter>)`

## Parâmetros

| Parâmetro | Descrição |
|--- |--- |
| sequência de caracteres | converte o valor da string em um inteiro |
| dateTime | converte a data no número de milissegundos (milissegundos da época) |
| decimal | converte em um inteiro removendo a parte decimal (exemplo: 1,5 torna-se 1) |
| booleano | converte o valor booleano como 1 se verdadeiro, 0 se falso |

## Assinaturas e tipo retornado

`toInteger(<dateTime>)`

`toInteger(<decimal>)`

`toInteger(<integer>)`

`toInteger(<string>)`

`toInteger(<boolean>)`

Retorna um número inteiro.

## Exemplos

`toInteger("4")`

Retorna 4.
