---
product: journey optimizer
title: Funções matemáticas
description: Saiba mais sobre funções matemáticas
feature: Journeys
role: Developer
level: Experienced
keywords: matemática, funções, expressão, jornada, cálculo, número
version: Journey Orchestration
exl-id: da710b22-3112-41fe-8b91-2b6563b79f27
TQID: https://experienceleague.adobe.com/POIbPCZrqtqGjHqn3ehGonxwv9KhKWlgg2igdN8Y4yw
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 156
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
