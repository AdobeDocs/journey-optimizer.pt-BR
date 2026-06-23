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
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 475
ht-degree: 2%

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

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** Esta página documenta as duas funções matemáticas disponíveis nas expressões de jornada do AJO — `random` para gerar um decimal aleatório entre 0 e 1 e `round` para arredondar um decimal ou inteiro para o inteiro mais próximo.

**Intenções:**
* Gerar um valor decimal aleatório entre 0 e 1 para amostragem ou lógica de aleatoriedade usando `random`
* Arredondar um número decimal para o inteiro mais próximo usando `round`
* Aplicar arredondamento na lógica de negócios onde números inteiros são necessários de cálculos decimais

**Glossário:**
* **random**: uma função que retorna um valor decimal pseudo-aleatório de 0 (inclusivo) a 1 (exclusivo) *(específico do produto)*
* **round**: uma função que retorna o número inteiro mais próximo da entrada, com meio-valores arredondados em direção ao infinito positivo

**Medidas de Proteção:**
* `random()` não aceita parâmetros
* `round` aceita entrada de decimal ou inteiro e sempre retorna um inteiro
* Os vínculos em `round` são resolvidos por arredondamento em direção ao infinito positivo (por exemplo, 3,5 arredondamentos para 4, -3,5 arredondamentos para -3)

**Terminologia:**
* Nome canônico: Funções matemáticas — Acrônimo: none — variantes: funções matemáticas, funções numéricas
* Sinônimos: &quot;round&quot; = &quot;arredondar para o número inteiro mais próximo&quot;
* Não confundir: &quot;round&quot; (arredonda para o número inteiro mais próximo) ≠ funções de conversão como `toInteger` (trunca a parte decimal sem arredondar)

**Perguntas frequentes:**
* **P: O que `random()` retorna?** — Retorna um número decimal aleatório entre 0 e 1.
* **P: Como `round` lida com números negativos?** — Ele arredonda em direção ao infinito positivo, portanto `round(-3.14)` retorna -3 e `round(-3.54)` retorna -3 também (número inteiro mais próximo em direção ao infinito positivo).
* **P: Qual é a diferença entre `round` e `toInteger`?** — `round` arredonda para o inteiro mais próximo (3,7 torna-se 4), enquanto `toInteger` trunca a parte decimal sem arredondamento (3,7 torna-se 3).
* **P: `random` usa algum parâmetro?** — Não, `random()` não requer parâmetros e sempre retorna um valor decimal entre 0 e 1.

+++
