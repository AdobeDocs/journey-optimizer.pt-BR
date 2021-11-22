---
title: Biblioteca de funções dos operadores
description: Biblioteca de funções dos operadores
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 75b0b380-d9a6-418e-b9f6-e64de385ba8d
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 11%

---

# Operadores {#operators}

## Funções booleanas

As funções booleanas são usadas para executar lógica booleana em elementos diferentes.

### E{#and}

O `and` é usada para criar uma conjunção lógica.

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

O `or` é usada para criar uma disjunção lógica.

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

O `=` (igual) verifica se um valor ou expressão é igual a outro valor ou expressão.

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

O `!=` (não é igual) verifica se um valor ou expressão é **not** igual a outro valor ou expressão.

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

O `>` (greater than) é usada para verificar se o primeiro valor é maior que o segundo valor.

**Formato**

```sql
{%= expression1 > expression2 %}
```

**Exemplo**

A operação a seguir define pessoas que nasceram estritamente após 1970.

```sql
{%= profile.person.birthYear > 1970 %}
```

### Maior que ou igual a{#greaterthanorequal}

O `>=` (maior que ou igual a) é usada para verificar se o primeiro valor é maior ou igual ao segundo valor.

**Formato**

```sql
{%= expression1 >= expression2 %}
```

**Exemplo**

A operação a seguir define pessoas nascidas em ou após 1970.

```sql
{%= profile.person.birthYear >= 1970 %}
```

### Menos que{#lessthan}

O `<` (less than) é usada para verificar se o primeiro valor é menor que o segundo valor.

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

O `<=` A função de comparação (menor que ou igual a) é usada para verificar se o primeiro valor é menor que ou igual ao segundo valor.

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
