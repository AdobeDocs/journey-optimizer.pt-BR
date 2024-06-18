---
solution: Journey Optimizer
product: journey optimizer
title: Sintaxe
description: Saiba mais sobre o editor de expressão avançado
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: sintaxe, editor, jornada
exl-id: c9434b28-2750-4a53-985e-c4a3f940472c
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 3%

---

# Sintaxe do editor de expressão avançado {#syntax}

## Parênteses e prioridade da expressão{#parentheses-and-expression-priority}

É possível usar parênteses para tornar uma expressão complexa mais legível. _(&lt;expression>)_ equivale a _&lt;expression>_. Também é possível usar parênteses para definir a ordem de avaliação e a associatividade.

As expressões serão avaliadas da esquerda para a direita. A associatividade em operadores aritméticos deve ser aplicada: multiplicações e divisões têm prioridade sobre adições e subtrações. Para impor uma ordem específica, é necessário adicionar parênteses para delimitar as operações. Por exemplo:

<!--```5 + 2 * 10 = 25, and (5 + 2) * 10 = 70```-->

| Expressão | Avaliação |
|--- |--- |
| `4 + 2 * 10` | <ul><li>&#39;*&#39; tem prioridade sobre &#39;+&#39;: 2 * 10 é avaliado → 20</li><li>4 + 20 → 24</li></ul> |
| `(4 + 2) * 10` | <ul><li>Os parênteses alteram a prioridade: (4 + 2) é avaliado → 6</li><li> 6 * 10 → 60</li></ul> |

## Diferenciação de maiúsculas e minúsculas{#case-sensitivity}

Estas são as diferentes regras de diferenciação entre maiúsculas e minúsculas:

* Todos os operadores (and, or etc.) deve ser escrito em minúsculas. Por exemplo, _`<expression1>`e`<expression2>`_ é uma expressão válida, enquanto a expressão _`<expression1>`E`<expression2>`_ não é.
* Todos os nomes de função fazem distinção entre maiúsculas e minúsculas. Por exemplo, _inAudience()_ é válido, enquanto a função _INAUDIENCE()_ não é.
* Referências de campo e valores constantes fazem distinção entre maiúsculas e minúsculas: eles não são elementos integrados da linguagem (em vez de operadores e funções), eles são criados pelo usuário final.

## Tipo de expressão retornada{#returned-expression-type}

Dependendo do contexto de uso, o editor de expressão pode retornar valores diferentes.

| Uso do editor de expressão avançado | Tipo de expressão retornada esperado |
|--- |--- |
| Condição (condição da fonte de dados, condição de data) | booleano |
| Temporizador personalizado | dateTimeOnly |
| Mapeamento de parâmetros de ação | Qualquer uma |
