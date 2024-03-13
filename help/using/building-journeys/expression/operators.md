---
solution: Journey Optimizer
product: journey optimizer
title: Operadores
description: Saiba mais sobre operadores em expressões avançadas
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: expressão, sintaxe, operadores, editor, jornada
exl-id: 706e2e02-9bd9-46e7-a73d-dda3c9ae4ba8
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 5%

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

* Ao usar uma multiplicação (`*`), ambos os campos de operação devem ter o mesmo tipo, seja inteiro ou decimal. Exemplo:
   * o exemplo a seguir está correto: `3.0 * 4.0`
   * `3 * 4.0` resultará em um erro

## Lógico  {#logical}

### e

```json
<expression1> and <expression2>
```

Ambos &lt;expression1> e &lt;expression2> deve ser booleano. O resultado é booleano.

Exemplo:

```json
3.14 > 2 and 3.15 < 1
```

### ou

```json
<expression1> or <expression2>
```

Ambos &lt;expression1> e &lt;expression2> deve ser booleano. O resultado é booleano.

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
>Para &lt;expression1> e &lt;expression2> não há controle de tipo de dados.

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
Para &lt;expression1> e &lt;expression2> não há controle de tipo de dados.

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

Retorna &quot;a hora atual é 23/09/2023:30:06.693Z&quot;

```json
(now()) + " is the current time"
```

Retorna &quot;23/09/2009:30:06.693Z é a hora atual&quot;

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

Retorna um _duração_ PT2H
