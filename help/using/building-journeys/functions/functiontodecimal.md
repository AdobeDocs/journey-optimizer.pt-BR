---
product: adobe campaign
title: toDecimal
description: Saiba mais sobre a função para Decimal
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 14%

---

# toDecimal {#toDecimal}

Converte um valor de argumento em um valor decimal, dependendo de seu tipo.

## Categoria

Conversão

## Sintaxe da função

`toDecimal(<parameter>)`

## Parâmetros

| Parâmetro | Descrição |
|--- |--- |
| string | converte o valor da string como decimal |
| dateTime | converte a data como o número de milissegundos (milissegundos de época) |
| booleano | converte o valor booleano como 1 se verdadeiro, 0 se falso |
| integer | converte para um decimal (por exemplo).: 1 torna-se 1,0) |

## Assinaturas e tipos retornados

`toDecimal(<integer>)`

`toDecimal(<decimal>)`

`toDecimal(<string>)`

`toDecimal(<boolean>)`

Retorna um decimal.

## Exemplos

`toDecimal("4.0")`

Retorna 4.0.
