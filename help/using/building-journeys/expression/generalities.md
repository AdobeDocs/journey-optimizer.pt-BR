---
solution: Journey Optimizer
product: journey optimizer
title: Sintaxe
description: Saiba mais sobre o editor de expressão avançado
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: c9434b28-2750-4a53-985e-c4a3f940472c
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 0%

---

# Sintaxe do editor de expressão avançado {#syntax}

## Parênteses e prioridade da expressão{#parentheses-and-expression-priority}

Os parênteses podem ser usados para tornar uma expressão complexa mais legível. _(&lt;expression>)_ é equivalente a _&lt;expression>_. Os parênteses também podem ser usados para definir a ordem de avaliação e a associatividade.

As expressões serão avaliadas da esquerda para a direita. A associação em operadores aritméticos deve ser aplicada: multiplicações e divisões têm prioridade sobre adições e subtrações. Para impor uma ordem específica, os parênteses devem ser adicionados para delimitar as operações. Por exemplo:

<!--```5 + 2 * 10 = 25, and (5 + 2) * 10 = 70```-->

| Expressão | Avaliação |
|--- |--- |
| `4 + 2 * 10` | <ul><li>&#39;*&#39; tem prioridade sobre &#39;+&#39;: 2 * 10 é avaliado → 20</li><li>4 + 20 → 24</li></ul> |
| `(4 + 2) * 10` | <ul><li>Os parênteses alteram a prioridade: (4 + 2) é avaliado → 6</li><li> 6 * 10 → 60</li></ul> |

## Diferenciação de maiúsculas e minúsculas{#case-sensitivity}

Estas são as diferentes regras de diferenciação entre maiúsculas e minúsculas:

* Todos os operadores (e, ou etc.) deve ser escrito em minúsculas. Por exemplo, _`<expression1>`e`<expression2>`_ é uma expressão válida, enquanto a expressão _`<expression1>`E`<expression2>`_ não é.
* Todos os nomes de função fazem distinção entre maiúsculas e minúsculas. Por exemplo, _inSegment()_ é válida, enquanto a função _INSEGMENT()_ não é.
* As referências de campo e os valores constantes distinguem maiúsculas de minúsculas: eles não são elementos integrados do idioma (em vez de operadores e funções), eles são criados pelo usuário final.

## Tipo de expressão retornada{#returned-expression-type}

Dependendo do contexto de uso, o editor de expressão pode retornar valores diferentes.

| Uso do editor de expressão avançado | Tipo de expressão retornada esperado |
|--- |--- |
| Condição (condição da fonte de dados, condição de data) | booleano |
| Temporizador personalizado | dateTimeOnly |
| Mapeamento de parâmetros de ação | Qualquer |
