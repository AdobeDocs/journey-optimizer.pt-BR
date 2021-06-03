---
title: Biblioteca de funções
description: Biblioteca de funções
source-git-commit: ca739254e8b113d6f511573c0aa427427b263b3b
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 11%

---

# Operadores {#operators}

![](../../assets/do-not-localize/badge.png)

## Funções booleanas

As funções booleanas são usadas para executar lógica booleana em elementos diferentes.

### E{#and}

A função `and` é usada para criar uma conjunção lógica.

**Formato**

```sql
{%= query1 and query2 %}
```

**Exemplo**

A operação seguinte irá devolver todas as pessoas com o país de origem como França e ano de nascimento de 1985.

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

### Ou{#or}

A função `or` é usada para criar uma disjunção lógica.

**Formato**

```sql
{%= query1 or query2 %}
```

**Exemplo**

A operação seguinte irá devolver todas as pessoas com o país de origem como França ou ano de nascimento de 1985.

```sql
{%= profile.homeAddress.country = "France" or profile.person.birthYear = 1985 %}
```

<!--
## Not{#not}

The `not` (or `!`) function is used to create a logical negation.

**Format**

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





## Funções de comparação

As funções de comparação são usadas para comparar diferentes expressões e valores, retornando verdadeiro ou falso de acordo.

### Igual a{#equals}

A função `=` (igual) verifica se um valor ou expressão é igual a outro valor ou expressão.

**Formato**

```sql
{%= expression = value %}
```

**Exemplo**

A operação a seguir referida verifica se o país de endereço de origem é a França.

```sql
{%= profile.homeAddress.country = "France" %}
```

### Diferente de{#notequal}

A função `!=` (não igual) verifica se um valor ou expressão é **not** igual a outro valor ou expressão.

**Formato**

```sql
{%= expression != value %}
```

**Exemplo**

A operação seguinte verifica se o país de endereço de origem não é a França.

```sql
{%= profile.homeAddress.country != "France" %}
```

### Greater than{#greaterthan}

A função `>` (maior que) é usada para verificar se o primeiro valor é maior que o segundo valor.

**Formato**

```sql
{%= expression1 > expression2 %}
```

**Exemplo**

A operação a seguir define pessoas que nasceram estritamente após 1970.

```sql
{%= profile.person.birthYear > 1970 %}
```

### Greater than or equal to{#greaterthanorequal}

A função `>=` (maior que ou igual a) é usada para verificar se o primeiro valor é maior ou igual ao segundo valor.

**Formato**

```sql
{%= expression1 >= expression2 %}
```

**Exemplo**

A operação a seguir define pessoas nascidas em ou após 1970.

```sql
{%= profile.person.birthYear >= 1970 %}
```

### Less than{#lessthan}

A função de comparação `<` (menor que) é usada para verificar se o primeiro valor é menor que o segundo valor.

**Formato**

```sql
{%= expression1 < expression2 %}
```

**Exemplo**

A operação a seguir define pessoas nascidas antes de 2000.

```sql
{%= profile.person.birthYear < 2000 %}
```

### Less than or equal to{#lessthanorequal}

A função de comparação `<=` (menor que ou igual a) é usada para verificar se o primeiro valor é menor que ou igual ao segundo valor.

**Formato**

```sql
{%= expression1 <= expression2 %}
```

**Exemplo**

A operação a seguir define pessoas nascidas em 2000 ou antes.

```sql
{%= profile.person.birthYear <= 2000 %}
```

**Operações com números**

