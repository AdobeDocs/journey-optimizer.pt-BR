---
title: Biblioteca de funções de operadores
description: Biblioteca de funções de operadores
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 75b0b380-d9a6-418e-b9f6-e64de385ba8d
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 11%

---

# Operadores {#operators}

## Funções booleanas {#boolean-functions}

Funções booleanas são usadas para executar lógica booleana em elementos diferentes.

### E{#and}

A função `and` é usada para criar uma conjunção lógica.

**Sintaxe**

```sql
{%= query1 and query2 %}
```

**Exemplo**

A operação a seguir retornará todas as pessoas com país de origem como França e ano de nascimento de 1985.

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

### Ou{#or}

A função `or` é usada para criar uma disjunção lógica.

**Sintaxe**

```sql
{%= query1 or query2 %}
```

**Exemplo**

A operação a seguir retornará todas as pessoas com o país de origem como França ou ano de nascimento de 1985.

```sql
{%= profile.homeAddress.country = "France" or profile.person.birthYear = 1985 %}
```

<!--
## Not{#not}

The `not` (or `!`) function is used to create a logical negation.

**Syntax**

```sql
not ({QUERY})
!({QUERY})
```

**Example**

The following operation will return all people who do not have their home country as Canada.

```sql
not (homeAddress.countryISO = "CA")
```
-->

## Funções de comparação {#comparison-functions}

As funções de comparação são usadas para comparar entre diferentes expressões e valores, retornando verdadeiro ou falso de acordo.

### Igual a{#equals}

A função `=` (igual a) verifica se um valor ou expressão é igual a outro valor ou expressão.

**Sintaxe**

```sql
{%= expression = value %}
```

**Exemplo**

A operação a seguir verifica se o país do endereço residencial é a França.

```sql
{%= profile.homeAddress.country = "France" %}
```

### Diferente de{#notequal}

A função `!=` (diferente de) verifica se um valor ou expressão é **não** igual a outro valor ou expressão.

**Sintaxe**

```sql
{%= expression != value %}
```

**Exemplo**

A operação a seguir verifica se o país do endereço residencial não é a França.

```sql
{%= profile.homeAddress.country != "France" %}
```

### Maior que{#greaterthan}

A função `>` (maior que) é usada para verificar se o primeiro valor é maior que o segundo valor.

**Sintaxe**

```sql
{%= expression1 > expression2 %}
```

**Exemplo**

A operação a seguir define pessoas nascidas estritamente após 1970.

```sql
{%= profile.person.birthYear > 1970 %}
```

### Maior que ou igual a{#greaterthanorequal}

A função `>=` (maior que ou igual a) é usada para verificar se o primeiro valor é maior que ou igual ao segundo valor.

**Sintaxe**

```sql
{%= expression1 >= expression2 %}
```

**Exemplo**

A operação a seguir define pessoas nascidas em ou após 1970.

```sql
{%= profile.person.birthYear >= 1970 %}
```

### Menor que{#lessthan}

A função de comparação `<` (menor que) é usada para verificar se o primeiro valor é menor que o segundo valor.

**Sintaxe**

```sql
{%= expression1 < expression2 %}
```

**Exemplo**

A operação a seguir define pessoas nascidas antes de 2000.

```sql
{%= profile.person.birthYear < 2000 %}
```

### Menor que ou igual a{#lessthanorequal}

A função de comparação `<=` (menor que ou igual a) é usada para verificar se o primeiro valor é menor que ou igual ao segundo valor.

**Sintaxe**

```sql
{%= expression1 <= expression2 %}
```

**Exemplo**

A operação a seguir define pessoas nascidas em 2000 ou antes.

```sql
{%= profile.person.birthYear <= 2000 %}
```

**Operações com números**
