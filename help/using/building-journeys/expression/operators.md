---
solution: Journey Optimizer
product: journey optimizer
title: Operadores
description: Saiba mais sobre operadores em expressões avançadas
feature: Journeys
role: Developer
level: Experienced
keywords: expressão, sintaxe, operadores, editor, jornada
exl-id: 706e2e02-9bd9-46e7-a73d-dda3c9ae4ba8
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/sK2GNHkkiJ4M5V99Uucc-b68iESNW7kCNBjHVNT-dMs
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1001
ht-degree: 3%

---

# Operadores {#operators}

Há dois tipos de operadores: operadores unários e operadores binários. Há operadores unários à esquerda e operadores unários à direita.

```json
// left-hand unary operators
// <operator> <operand> 
// operand is an expression
not (@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example@adobe.com")

// right-hand unary operators
// <operator> <operand> 
// operand is an expression
@event{LobbyBeacon.endUserIDs._experience.emailid.id} is not null

// binary operators
// <operand1> <operator> <operand2>
// operand is an expression
(@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example1@adobe.com") or (@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example2@adobe.com") 
```

## Observações importantes{#important-notes}

* Ao usar uma multiplicação (`*`), ambos os campos de operação devem ter o mesmo tipo, inteiro ou decimal. Exemplo:
   * o exemplo a seguir está correto: `3.0 * 4.0`
   * `3 * 4.0` levará a um erro

* Ao usar o operador `+`, a expressão precisa ser encapsulada entre parênteses. Exemplo:
   * `toDateTimeOnly(toDateTime((currentTimeInMillis()) + 1))` está correto
   * `toDateTimeOnly(toDateTime(currentTimeInMillis() + 1))` levará a um erro

## Lógico  {#logical}

### e

```json
<expression1> and <expression2>
```

&lt;expression1> e &lt;expression2> devem ser booleanos. O resultado é booleano.

Exemplo:

```json
3.14 > 2 and 3.15 < 1
```

### ou

```json
<expression1> or <expression2>
```

&lt;expression1> e &lt;expression2> devem ser booleanos. O resultado é booleano.

Exemplo:

```json
3.14 > 2 or 3.15 < 1
```

### não

```json
not <expression>
```

&lt;expression> deve ser booleano. O resultado é booleano.

Exemplo:

```json
not 3.15 < 1
```

## Comparação {#comparison}

### é nulo

```json
<expression> is null
```

O resultado é booleano.

Observe que nulo significa que a expressão não tem um valor avaliado.

Exemplo:

```json
@event{BarBeacon.location} is null
```

### não é nulo

```json
<expression> is not null
```

O resultado é booleano.

Observe que nulo significa que a expressão não tem um valor avaliado.

Exemplo:

```json
@event{BarBeacon.location} is not null
```

### tem nulo

```json
<expression> has null
```

&lt;expression> deve ser uma lista. O resultado é booleano.

Útil para identificar se uma lista contém pelo menos um valor nulo.

Exemplo:

```json
["foo", "bar", null] has null
```

Retorna verdadeiro

```json
["foo", "bar", ""] has null
```

Retorna falso porque &quot;&quot; não é considerado nulo.

### ==

```json
<expression1> == <expression2>
```

>[!NOTE]
>
>Para &lt;expression1> e &lt;expression2>, não há controle de tipo de dados.

Exemplo:

```json
3.14 == 42
```

```json
"foo" == "bar"
```

### !=

```json
<expression1> != <expression2>
```

>[!NOTE]
>
>Para &lt;expression1> e &lt;expression2>, não há controle de tipo de dados.

O resultado é booleano.

Exemplo:

```json
3.14 != 42
```

```json
"foo" != "bar"
```

### >

```json
<expression1> > <expression2>
```

Datetime pode ser comparado com Datetime.

Datetimeonly pode ser comparado com Datetimeonly.

O inteiro ou o decimal podem ser comparados com o inteiro ou o decimal.

Qualquer outra combinação é proibida.

O resultado é booleano.

Exemplo:

```json
3.14 > 42
```

### >=

```json
<expression1> >= <expression2>
```

Datetime pode ser comparado com Datetime.

Datetimeonly pode ser comparado com Datetimeonly.

O inteiro ou o decimal podem ser comparados com o inteiro ou o decimal.

Qualquer outra combinação é proibida.

O resultado é booleano.

Exemplo:

```json
42 >= 3.14
```

### &lt;

```json
<expression1> < <expression2>
```

Datetime pode ser comparado com Datetime.

Datetimeonly pode ser comparado com Datetimeonly.

O inteiro ou o decimal podem ser comparados com o inteiro ou o decimal.

Qualquer outra combinação é proibida.

O resultado é booleano.

Exemplo:

```json
42 < 3.14
```

### &lt;=

```json
<expression1> <= <expression2>
```

Datetime pode ser comparado com Datetime.

Datetimeonly pode ser comparado com Datetimeonly.

O inteiro ou o decimal podem ser comparados com o inteiro ou o decimal.

Qualquer outra combinação é proibida.

O resultado é booleano.

Exemplo:

```json
42 <= 3.14
```

## Aritmética {#arithmetic}

### +

```json
<expression1> + <expression2>
```

Ambas as expressões devem ser numéricas (números inteiros ou decimais).

O resultado também é numérico.

Exemplo:

```json
1 + 2
```

Devoluções 3

### -

```json
<expression1> - <expression2>
```

Ambas as expressões devem ser numéricas (números inteiros ou decimais).

O resultado também é numérico.

Exemplo:

```json
2 - 1 
```

Devoluções 1

### /

```json
<expression1> / <expression2>
```

Ambas as expressões devem ser numéricas (números inteiros ou decimais).

O resultado também é numérico.

&lt;expression2> não deve ser igual a 0 (retorna 0).

Exemplo:

```json
4 / 2
```

Devoluções 2

### *

```json
<expression1> * <expression2>
```

Ambas as expressões devem ser numéricas (números inteiros ou decimais).

O resultado também é numérico.

Exemplo:

```json
3 * 4
```

Retorna 12

### %

```json
<expression1> % <expression2>
```

Ambas as expressões devem ser numéricas (números inteiros ou decimais).

O resultado também é numérico.

Exemplo:

```json
3 % 2
```

Retorna 1.

## Matemática {#math}

### é numérico

```json
<expression> is numeric
```

O tipo da expressão é inteiro ou decimal.

Exemplo:

```json
@ is numeric
```

### é inteiro

```json
<expression> is integer
```

O tipo da expressão é inteiro.

Exemplo:

```json
@ is integer
```

### é decimal

```json
<expression> is decimal
```

O tipo da expressão é decimal.

Exemplo:

```json
@ is decimal
```

## String {#string}

### +

```json
<string> + <expression>
```

```json
<expression> + <string>
```

Ela concatena duas expressões.

Uma expressão deve ser uma sequência de caracteres encadeada.

Exemplo:

```json
"the current time is " + (now())
```

Retorna &quot;a hora atual é 23T09-2023:30:06.693Z&quot;

```json
(now()) + " is the current time"
```

Retorna &quot;2023-09-23T09:30:06.693Z é a hora atual&quot;

```json
"a" + "b" + "c" + 1234
```

Retorna &quot;abc1234&quot;.

## Data {#date}

### +

```json
<expression> + <duration>
```

Anexe uma duração a um dateTime, um dateTimeOnly ou uma duração.

Exemplo:

```json
(toDateTime("2023-12-03T15:15:30Z")) + (toDuration("PT15M"))  
```

Retorna um _dateTime_ 2023-12-03T15:30:30Z

```json
(toDateTimeOnly("2023-12-03T15:15:30")) + (toDuration("PT15M"))
```

Retorna um _dateTimeOnly_ 2023-12-03T15:30:30

```json
(now()) + (toDuration("PT1H"))
```

Retorna um _dateTime_ (com fuso horário UTC) uma hora depois da hora atual

```json
(toDuration("PT1H")) + (toDuration("PT1H"))
```

Retorna uma _duração_ PT2H

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** Esta página é uma referência completa de operadores disponíveis no editor de expressão avançado de Jornada, abrangendo lógica (`and`, `or`, `not`), comparação (`==`, `!=`, `>`, `>=`, `<`, `<=`, `is null`, `is not null`, `has null`), aritmética (`+`, `-`, `/`, `*`, `%`), verificação de tipo matemático (`is numeric`, `is integer`, `is decimal`), concatenação de cadeias de caracteres e operadores aritméticos de data.

**Intenções:**

* Combinar condições booleanas usando operadores lógicos `and`, `or` e `not`
* Verifique se um valor de campo ou expressão é nulo ou não usando `is null` / `is not null`
* Detectar valores nulos em uma lista usando o operador `has null`
* Comparar valores numeric, datetime e datetimeonly usando `>`, `>=`, `<`, `<=`, `==` e `!=`
* Executar aritmética em valores numéricos usando `+`, `-`, `/`, `*` e `%`
* Adicione uma duração a um valor dateTime, dateTimeOnly ou duration usando o operador `+`

**Glossário:**

* **Operador unário**: um operador aplicado a um único operando; pode ser à esquerda (por exemplo, `not`) ou à direita (por exemplo, `is null`) *(específico do produto)*
* **Operador binário**: um operador aplicado entre dois operandos (por exemplo, `and`, `==`, `+`) *(específico do produto)*
* **tem nulo**: um operador unário à direita que retorna verdadeiro se uma lista contiver pelo menos um elemento nulo *(específico do produto)*
* **é numérico / é inteiro / é decimal**: operadores de verificação de tipo que retornam um booleano com base no subtipo numérico da expressão *(específico do produto)*

**Medidas de Proteção:**

* Ao usar a multiplicação (`*`), ambos os operandos devem ser do mesmo tipo numérico (inteiro ou ambos decimais) — a mistura de tipos causa um erro
* Ao usar o operador `+` para a aritmética de data, a expressão deve ser colocada entre parênteses para evitar erros de análise
* Os operadores de comparação (`>`, `>=`, `<`, `<=`) só são válidos entre tipos compatíveis: Datetime com Datetime, DatetimeOnly com DatetimeOnly ou numeric com numeric — qualquer outra combinação é proibida
* Uma cadeia de caracteres vazia `""` não é considerada nula — `has null` retorna falso para uma lista que contém `""`
* Os operadores `==` e `!=` não executam controle de tipo de dados entre operandos

**Terminologia:**

* Nome canônico: Operadores — Acrônimo: none — variantes: operadores de expressão, operadores de jornada
* Sinônimos: `and` = &quot;AND lógico&quot;; `or` = &quot;OR lógico&quot;; `not` = &quot;NOT lógico&quot;; `%` = &quot;módulo&quot;
* Não confunda: `is null` (a expressão não tem valor avaliado) ≠ `== null` (não é uma sintaxe válida); `has null` (a lista contém nulo) ≠ `is null` (a própria expressão é nula)

**Perguntas frequentes:**

* **P: Posso multiplicar um inteiro por um decimal diretamente?** — Não; ambos os operandos de `*` devem ser do mesmo tipo. Use `3.0 * 4.0` (ambos decimais) ou `3 * 4` (ambos inteiros).
* **P: Como adiciono 15 minutos a um dateTime?** — Use `(toDateTime("...")) + (toDuration("PT15M"))`.
* **P: Qual é a diferença entre `is null` e `has null`?** — `is null` verifica se uma única expressão não tem valor avaliado; `has null` verifica se uma lista contém pelo menos um elemento nulo.
* **P: `"" has null` retorna verdadeiro?** — Não; uma cadeia de caracteres vazia não é considerada nula, portanto, o resultado é falso.
* **P: Por que o `3 * 4.0` causa um erro?** — O operador `*` requer que ambos os operandos sejam do mesmo tipo numérico; não é permitido misturar números inteiros e decimais.

+++
