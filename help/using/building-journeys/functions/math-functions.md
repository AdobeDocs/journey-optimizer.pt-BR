---
product: journey optimizer
title: Funções matemáticas
description: Saiba mais sobre funções matemáticas
feature: Journeys
role: Developer
level: Experienced
keywords: matemática, funções, expressão, jornada, cálculo, número
version: Journey Orchestration
source-git-commit: bb47ca4957129a4d05aa3d7286409eef0cb62143
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 7%

---

# Funções matemáticas {#math-functions}

As funções matemáticas fornecem operações matemáticas essenciais para cálculos numéricos nas expressões da jornada. Essas funções permitem executar cálculos numéricos precisos e transformações nos dados.

Use funções matemáticas quando precisar:

* Gerar valores aleatórios para teste, amostragem ou aleatoriedade ([random](#random))
* Arredondar números decimais para o número inteiro mais próximo para uma apresentação de dados mais limpa ([round](#round))
* Realizar cálculos matemáticos em campos numéricos
* Transforme valores numéricos para a lógica de negócios e a tomada de decisões

As funções matemáticas lidam com tipos decimais e inteiros, gerenciando automaticamente conversões de tipo para garantir resultados precisos em suas expressões de jornada.

## random {#random}

Gera um número aleatório entre 0 e 1.

+++Sintaxe

`random()`

+++

+++Assinatura e tipo retornado

`random()`

Retorna um decimal.

+++

## round {#round}

Retorna o valor inteiro mais próximo do argumento com vínculos arredondados para o infinito positivo.

+++Sintaxe

`round(<parameters>)`

+++

+++Parâmetros

* decimal
* inteiro

+++

+++Assinaturas e tipo retornado

`round(<decimal>)`

`round(<integer>)`

Retorna um número inteiro.

+++

+++Exemplos

`round(3.14)`

Retorna 3.

`round(3.54)`

Retorna 4.

`round(-3.14)`

Retorna -3.

`round(3)`

Retorna 3.

+++

