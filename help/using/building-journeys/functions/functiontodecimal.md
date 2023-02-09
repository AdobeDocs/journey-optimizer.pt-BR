---
product: journey optimizer
title: toDecimal
description: Saiba mais sobre a função para Decimal
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: decimal, função, expressão, jornada
exl-id: d761fa4d-5f99-4dee-b747-3eab464c4071
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '75'
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
| inteiro | converte para um decimal (por exemplo).: 1 torna-se 1,0) |

## Assinaturas e tipos retornados

`toDecimal(<integer>)`

`toDecimal(<decimal>)`

`toDecimal(<string>)`

`toDecimal(<boolean>)`

Retorna um decimal.

## Exemplos

`toDecimal("4.0")`

Retorna 4.0.
