---
product: journey optimizer
title: Funções de agregação
description: Saiba mais sobre funções de agregação
feature: Journeys
role: Developer
level: Experienced
keywords: agregação, funções, expressão, jornada, média, contagem, máx, mín, soma
version: Journey Orchestration
exl-id: 871a5212-5b94-4a54-bf1d-276022be3c95
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1105
ht-degree: 5%

---

# Funções de agregação {#aggregation-functions}

As funções de agregação executam cálculos em um conjunto de valores e retornam um único resultado resumido. Essas funções permitem analisar dados nas expressões de jornada calculando médias, localizando valores mínimos e máximos, contando elementos e somando valores numéricos.

Use funções de agregação quando precisar:

* Calcular valores estatísticos a partir de listas ou matrizes ([avg](#avg), [sum](#sum), [min](#min), [max](#max))
* Contar elementos em coleções ([count](#count), [countOnlyNull](#countOnlyNull), [countWithNull](#countWithNull)), com opções para incluir ou excluir valores nulos
* Determinar valores exclusivos nos conjuntos de dados ([distinctCount](#distinctCount), [distinctCountWithNull](#distinctCountWithNull))
* Tomar decisões orientadas por dados com base em métricas calculadas

As funções de agregação tratam automaticamente valores nulos de acordo com seu comportamento específico, facilitando o trabalho com dados reais que podem conter valores ausentes ou indefinidos.


## avg {#avg}

Retorna o valor médio entre um conjunto de expressões, fornecido como uma lista ou duas expressões. Valores nulos são ignorados.

+++Sintaxe

`avg(<parameter>)`

+++

+++Parâmetros

Tipos suportados:

* listInteger
* listDecimal
* decimal
* inteiro

+++

+++Assinaturas e tipo retornado

`avg(<listInteger>)`

`avg(<listDecimal>)`

`avg(<decimal>,<decimal>)`

`avg(<decimal>,<integer>)`

`avg(<integer>,<decimal>)`

`avg(<integer>,<integer>)`

Retorna um decimal.

+++

+++Exemplos

`avg(@event{BarBeacon.inventory},5)`

`avg([10,3,8])`

Retorna 7.0.

`avg(10.2, 3)`

Retorna 6.6.

+++

## contagem {#count}

Conta os elementos da lista sem levar em conta os valores nulos.

+++Sintaxe

`count(<listAny>)`

`count(<listObject>)`

+++

+++Parâmetros

| Parâmetro | Tipo | Descrição |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly ou listObject | Lista a processar. Para listObject, ele deve ser uma referência de campo. Um listObject não pode conter um objeto nulo. |

+++

+++Assinaturas e tipo retornado

`count(<listAny>)`

Retorna um inteiro.

+++

+++Exemplos

`count([10,2,10,null])`

Retorna 3.

`count(@event{my_event.productListItems})`

Retorna o número de objetos na matriz de objetos fornecida (tipo listObject). Observação: um listObject não pode conter objeto nulo

+++

## countOnlyNull {#countOnlyNull}

Conta o número de valores nulos na lista.

+++Sintaxe

`countOnlyNull(<listAny>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

+++

+++Assinaturas e tipo retornado

`countOnlyNull(<listAny>)`

Retorna um inteiro.

+++

+++Exemplos

`countOnlyNull([10,2,10,null])`

Retorna 1.

+++

**Observação:** o parâmetro `<listObject>` não tem suporte nesta função.

## countWithNull {#countWithNull}

Conta todos os elementos da lista, incluindo valores nulos.

+++Sintaxe

`countWithNull(<listAny>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

+++

+++Assinaturas e tipo retornado

`countWithNull(<listAny>)`

Retorna um inteiro.

+++

+++Exemplos

`countWithNull([10,2,10,null])`

Retorna 4.

+++

**Observação:** o parâmetro `<listObject>` não tem suporte nesta função.

## distinctCount {#distinctCount}

Conta o número de valores diferentes ignorando os valores nulos.

+++Sintaxe

`distinctCount(<listAny>)`

+++

+++Parâmetros

| Parâmetro | Tipo | Descrição |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly ou listObject | Lista a processar. Para listObject, ele deve ser uma referência de campo. |
| keyAttributeName | sequência de caracteres | Este parâmetro é opcional e somente para listObject. Se o parâmetro não for fornecido, um objeto será considerado duplicado se todos os atributos tiverem os mesmos valores. Caso contrário, um objeto será considerado duplicado se o atributo em questão tiver o mesmo valor. |

+++

+++Assinaturas e tipo retornado

`distinctCount(<listAny>)`

Retorna um inteiro.

`distinctCount(<listObject>)`

`distinctCount(<listObject>,<string>)`

Retorna uma lista de objetos.

+++

+++Exemplos

`distinctCount([10,2,10,null])`

Retorna 2.

`distinctCount(@event{my_event.productListItems})`

Retorna o número de objetos estritamente distintos na matriz de objetos fornecida (tipo listObject).

`distinctCount(@event{my_event.productListItems}, "SKU")`

Retorna o número de objetos que têm um valor de atributo &quot;SKU&quot; distinto {}.

+++

## distinctCountWithNull {#distinctCountWithNull}

Conta o número de valores diferentes, incluindo os valores nulos.

+++Sintaxe

`distinctCountWithNull(<listAny>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

+++

+++Assinaturas e tipo retornado

`distinctCountWithNull(<listAny>)`

Retorna um inteiro.

+++

+++Exemplos

`distinctCountWithNull([10,2,10,null])`

Retorna 3.

+++

**Observação:** o parâmetro `<listObject>` não tem suporte nesta função.

## max {#max}

Retorna o valor máximo entre um conjunto de expressões, fornecido como uma lista ou duas expressões. Valores nulos são ignorados.

+++Sintaxe

`max(<parameter>)`

+++

+++Parâmetros

* listDuration
* listInteger
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* duração
* inteiro
* decimal
* dateTime
* dateTimeOnly

+++

+++Assinaturas e tipos retornados

`max(<listDuration>)`

Retorna uma duração.

`max(<listInteger>)`

Retorna uma duração.

`max(<listDateTimeOnly>)`

Retorna uma data e hora sem considerar o fuso horário.

`max(<listDateTime>)`

Retorna um datetime.

`max(<listDateOnly>)`

Retorna uma data.

`max(<listDecimal>)`

Retorna um decimal.

`max(<decimal>,<decimal>)`

Retorna um decimal.

`max(<duration>,<duration>)`

Retorna uma duração.

`max(<dateTime>,<dateTime>)`

Retorna um datetime.

`max(<dateTimeOnly>,<dateTimeOnly>)`

Retorna uma data e hora sem considerar o fuso horário.

`max(<integer>,<integer>)`

Retorna um inteiro.

+++

+++Exemplos

`max(@event{BarBeacon.inventory},5)`

`max([10,3,8])`

Retorna 10.

`max([10,null,8])`

Retorna 10.

+++

## min {#min}

Retorna o valor mínimo entre um conjunto de expressões, fornecido como uma lista ou duas expressões. Valores nulos são ignorados.

+++Sintaxe

`min(<parameters>)`

+++

+++Parâmetros

* listDuration
* listInteger
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* duração
* inteiro
* decimal
* dateTime
* dateTimeOnly

+++

+++Assinaturas e tipos retornados

`min(<listDuration>)`

Retorna uma duração.

`min(<listInteger>)`

Retorna uma duração.

`min(<listDateTimeOnly>)`

Retorna uma data e hora sem considerar o fuso horário.

`min(<listDateTime>)`

Retorna um datetime.

`min(<listDateOnly>)`

Retorna uma data.

`min(<listDecimal>)`

Retorna um decimal.

`min(<decimal>,<decimal>)`

Retorna um decimal.

`min(<duration>,<duration>)`

Retorna uma duração.

`min(<dateTime>,<dateTime>)`

Retorna um datetime.

`min(<dateTimeOnly>,<dateTimeOnly>)`

Retorna uma data e hora sem considerar o fuso horário.

`min(<integer>,<integer>)`

Retorna um inteiro.

+++

+++Exemplos

`min(@event{BarBeacon.inventory},5)`

`min([10,3,8])`

Retorna 3.

`min([10,null,8])`

Retorna 8.

+++

## sum {#sum}

Retorna a soma dos valores de um conjunto de expressões. Valores nulos são ignorados.

+++Sintaxe

`sum(<parameters>)`

+++

+++Parâmetros

* listInteger
* listDecimal
* duração
* inteiro
* decimal

+++

+++Assinaturas e tipos retornados

`sum(<listDecimal>)`

Retorna um decimal.

`sum(<listInteger>)`

Retorna um inteiro.

`sum(<integer>,<integer>)`

Retorna um inteiro.

`sum(<decimal>,<decimal>)`

Retorna um decimal.

+++

+++Exemplos

`sum(@event{BarBeacon.inventory},5)`

`sum([10,3,8])`

Retorna 21.

`sum([10.5,null,8.1])`

Retorna 18,6.

+++

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** esta página documenta todas as funções de agregação disponíveis nas expressões de jornada do AJO, abordando como calcular médias, somas, valores mín./máx., contagens e contagens distintas em listas e matrizes.

**Intenções:**
* Calcular a média de uma lista de valores numéricos usando `avg`
* Soma valores numéricos em uma lista ou de campos de evento usando `sum`
* Localizar o valor mínimo ou máximo em uma lista usando `min` ou `max`
* Contar elementos não nulos, somente nulos ou todos os elementos de uma lista usando `count`, `countOnlyNull` ou `countWithNull`
* Contar valores distintos em uma lista, com ou sem nulos, usando `distinctCount` ou `distinctCountWithNull`
* Filtrar objetos exclusivos em um listObject por um atributo de chave específico usando `distinctCount` com um parâmetro de chave

**Glossário:**
* **listObject**: uma lista de objetos complexos (referências de campo); não pode conter objetos nulos *(específico do produto)*
* **listAny**: uma lista de qualquer tipo escalar com suporte (string, booleano, inteiro, decimal, duração, dateTime, dateTimeOnly, dateOnly) *(específico do produto)*
* **Valor nulo**: um elemento ausente ou indefinido em uma lista; a maioria das funções de agregação ignora nulos, a menos que a função os manipule explicitamente (por exemplo, `countOnlyNull`, `countWithNull`, `distinctCountWithNull`)

**Medidas de Proteção:**
* `countOnlyNull`, `countWithNull` e `distinctCountWithNull` não dão suporte ao tipo de parâmetro `<listObject>`
* `distinctCount` em `listObject` requer que a lista seja uma referência de campo, não um literal embutido
* `count` em `listObject` requer que a lista seja uma referência de campo; listObject não pode conter objetos nulos

**Terminologia:**
* Nome canônico: Funções de agregação — Acrônimo: none — variantes: funções de agregação, funções de coleção
* Sinônimos: &quot;count&quot; = &quot;count elementos não nulos&quot;; &quot;countWithNull&quot; = &quot;count todos os elementos, incluindo nulos&quot;
* Não confunda: &quot;distinctCount&quot; (ignora nulos) ≠ &quot;distinctCountWithNull&quot; (inclui nulos como um valor distinto)

**Perguntas frequentes:**
* **P: `avg` inclui valores nulos em seu cálculo?** — Não, `avg` ignora valores nulos automaticamente.
* **P: Qual é a diferença entre `count` e `countWithNull`?** — `count` exclui valores nulos do total, enquanto `countWithNull` conta cada elemento, incluindo nulos.
* **P: Posso usar `countOnlyNull` em um listObject?** — Não, `<listObject>` não é suportado por `countOnlyNull`, `countWithNull` ou `distinctCountWithNull`.
* **P: Como posso contar objetos distintos em uma matriz com base em um atributo específico?** — Use `distinctCount(@event{...}, "attributeName")` fornecendo o nome do atributo de chave como o segundo parâmetro.
* **P: O que `max` retorna quando a lista contém nulos?** — `max` ignora valores nulos e retorna o máximo entre os elementos não nulos.

+++
