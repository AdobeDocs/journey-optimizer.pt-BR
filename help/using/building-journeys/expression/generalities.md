---
solution: Journey Optimizer
product: journey optimizer
title: Sintaxe do editor de expressão avançado
description: Saiba mais sobre a sintaxe usada no editor de expressão avançado
feature: Journeys
role: Developer
level: Experienced
keywords: sintaxe, editor, jornada
exl-id: c9434b28-2750-4a53-985e-c4a3f940472c
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/-PTYUf-njT3-LsI-A5IKEMDGOl4JecZ-ayM0rU4f2HI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 620
ht-degree: 2%

---

# Sintaxe do editor de expressão avançado {#syntax}

As noções básicas de sintaxe ao usar o [editor de expressão avançado](expressionadvanced.md) estão listadas abaixo. <!-- Samples of use of the advanced expression editor are available on [this page](advanced-editor-use-cases.md).-->

## Parênteses e prioridade da expressão {#parentheses-and-expression-priority}

É possível usar parênteses para tornar uma expressão complexa mais legível. _(&lt;expressão>)_ é o equivalente a _&lt;expressão>_. Também é possível usar parênteses para definir a ordem de avaliação e a associatividade.

As expressões serão avaliadas da esquerda para a direita. A associatividade em operadores aritméticos deve ser aplicada: multiplicações e divisões têm prioridade sobre adições e subtrações. Para impor uma ordem específica, é necessário adicionar parênteses para delimitar as operações. Por exemplo:

<!--```5 + 2 * 10 = 25, and (5 + 2) * 10 = 70```-->

| Expressão | Avaliação |
|--- |--- |
| `4 + 2 * 10` | <ul><li>&#39;*&#39; tem prioridade sobre &#39;+&#39;: 2 \* 10 é avaliado → 20</li><li>4 + 20 → 24</li></ul> |
| `(4 + 2) * 10` | <ul><li>Os parênteses alteram a prioridade: (4 + 2) é avaliado → 6</li><li> 6 * 10 → 60</li></ul> |

## Diferenciação de maiúsculas e minúsculas {#case-sensitivity}

Estas são as diferentes regras de diferenciação entre maiúsculas e minúsculas:

* Todos os operadores (and, or etc.) deve ser escrito em minúsculas. Por exemplo, _`<expression1>`e`<expression2>`_ é uma expressão válida, enquanto a expressão _`<expression1>`E`<expression2>`_ não é.
* Todos os nomes de função fazem distinção entre maiúsculas e minúsculas. Por exemplo, _inAudience()_ é válido, enquanto a função _INAUDIENCE()_ não é.
* Referências de campo e valores constantes fazem distinção entre maiúsculas e minúsculas: eles não são elementos integrados da linguagem (em vez de operadores e funções), eles são criados pelo usuário final.

## Tipo de expressão retornada {#returned-expression-type}

Dependendo do contexto de uso, o editor de expressão pode retornar valores diferentes.

| Uso do editor de expressão avançado | Tipo de expressão retornada esperado |
|--- |--- |
| Condição (condição da fonte de dados, condição de data) | booleano |
| Temporizador personalizado | dateTimeOnly |
| Mapeamento de parâmetros de ação | Qualquer |

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** Esta página aborda as principais regras de sintaxe do editor de expressão avançado do Jornada — precedência de operador com parênteses, distinção entre maiúsculas e minúsculas para operadores e funções e o tipo de retorno esperado para cada contexto de editor.

**Intenções:**

* Controlar ordem de avaliação da expressão ao quebrar subexpressões entre parênteses
* Gravar operadores (`and`, `or`, `not`) em minúsculas para evitar erros de sintaxe
* Usar nomes de função em maiúsculas corretamente (ex: `inAudience()` não `INAUDIENCE()`)
* Entenda que as condições devem retornar um valor booleano, que os timers personalizados devem retornar `dateTimeOnly` e que os mapeamentos de parâmetros de ação podem retornar qualquer tipo

**Glossário:**

* **Prioridade de expressão**: a ordem na qual os operadores são avaliados; multiplicações e divisões têm prioridade sobre adições e subtrações *(específico do produto)*
* **Diferenciação de maiúsculas e minúsculas**: no editor avançado, os operadores devem ser minúsculas, os nomes de funções diferenciam maiúsculas de minúsculas e as referências de campo diferenciam maiúsculas de minúsculas, conforme criadas pelo usuário *(específico do produto)*
* **dateTimeOnly**: o tipo de retorno necessário para expressões de timer personalizado (atividade de espera); representa um date-time sem um fuso horário *(específico do produto)*

**Medidas de Proteção:**

* Operadores (`and`, `or`, `not` etc.) deve ser escrito em minúsculas — as variantes em maiúsculas são inválidas
* Todos os nomes de funções diferenciam maiúsculas de minúsculas — `inAudience()` é válido, mas `INAUDIENCE()` não é
* A aritmética segue a precedência padrão: `*` e `/` avaliam antes de `+` e `-`; use parênteses para substituir
* As condições sempre retornam um valor booleano; os cronômetros personalizados sempre retornam `dateTimeOnly`

**Terminologia:**

* Nome canônico: Advanced Expression Editor Sintaxe — Acrônimo: none — variantes: sintaxe de expressão, sintaxe do editor
* Sinônimos: &quot;prioridade da expressão&quot; = &quot;precedência do operador&quot;; &quot;parênteses&quot; = &quot;colchetes&quot; (no contexto da expressão)
* Não confunda: o operador diferencia maiúsculas de minúsculas (os operadores devem ser minúsculas) ≠ diferencia maiúsculas de minúsculas de referência de campo (os nomes de campo são de autoria do usuário e diferenciam maiúsculas de minúsculas conforme escritos)

**Perguntas frequentes:**

* **P: `4 + 2 * 10` é avaliado como 60 ou 24?** — É avaliado como 24 porque `*` tem prioridade sobre `+`; use `(4 + 2) * 10` para obter 60.
* **P: Posso escrever `AND` em maiúsculas em uma expressão?** — Não; todos os operadores devem estar em minúsculas (`and`, `or`, `not`).
* **P: Os nomes das funções fazem distinção entre maiúsculas e minúsculas?** — Sim; `inAudience()` é válido, mas `INAUDIENCE()` não é.
* **P: Que tipo deve ser retornado por uma expressão de condição?** — Um booleano.
* **P: Que tipo de retorno é necessário para uma expressão de timer de atividade de espera personalizada?** — `dateTimeOnly`

+++
