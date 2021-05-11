---
title: Biblioteca de funções
description: Biblioteca de funções
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 9%

---

# Operadores {#operators}

![](../../assets/do-not-localize/badge.png)

## E

A função `and` é usada para criar uma conjunção lógica.

**Formato**

```sql
{QUERY} and {QUERY}
```

**Exemplo**

A consulta PQL a seguir retornará todas as pessoas com o país de origem como Canadá e o ano de nascimento de 1985.

```sql
homeAddress.countryISO = "CA" and person.birthYear = 1985
```

## Ou

A função `or` é usada para criar uma disjunção lógica.

**Formato**

```sql
{QUERY} or {QUERY}
```

**Exemplo**

A consulta PQL a seguir retornará todas as pessoas com o país de origem como Canadá ou o ano de nascimento de 1985.

```sql
homeAddress.countryISO = "CA" or person.birthYear = 1985
```

## Não

A função `not` (ou `!`) é usada para criar uma negação lógica.

**Formato**

```sql
not ({QUERY})
!({QUERY})
```

**Exemplo**

A consulta PQL a seguir retornará todas as pessoas que não têm o país de origem como o Canadá.

```sql
not (homeAddress.countryISO = "CA")
```

## Se

A função `if` é usada para resolver uma expressão dependendo de se uma condição especificada é verdadeira.

**Formato**

```sql
if ({TEST_EXPRESSION}, {TRUE_EXPRESSION}, {FALSE_EXPRESSION})
```

| Argumento | Descrição |
| --------- | ----------- |
| `{TEST_EXPRESSION}` | A expressão booleana que está sendo testada. |
| `{TRUE_EXPRESSION}` | A expressão cujo valor será usado se `{TEST_EXPRESSION}` for true. |
| `{FALSE_EXPRESSION}` | A expressão cujo valor será usado se `{TEST_EXPRESSION}` for false. |

**Exemplo**

A consulta PQL a seguir definirá o valor como `1` se o país de origem for o Canadá e `2` se o país de origem não for o Canadá.

```sql
if (homeAddress.countryISO = "CA", 1, 2)
```

## Igual a

A função `=` (igual) verifica se um valor ou expressão é igual a outro valor ou expressão.

**Formato**

```sql
{EXPRESSION} = {VALUE}
```

**Exemplo**

A consulta PQL a seguir verifica se o país do endereço residencial está no Canadá.

```sql
homeAddress.countryISO = "CA"
```

## Diferente de

A função `!=` (não igual) verifica se um valor ou expressão é **not** igual a outro valor ou expressão.

**Formato**

```sql
{EXPRESSION} != {VALUE}
```

**Exemplo**

A consulta PQL a seguir verifica se o país do endereço residencial não está no Canadá.

```sql
homeAddress.countryISO != "CA"
```

## Greater than

A função `>` (maior que) é usada para verificar se o primeiro valor é maior que o segundo valor.

**Formato**

```sql
{EXPRESSION} > {EXPRESSION} 
```

**Exemplo**

A consulta PQL a seguir define as pessoas cujos aniversários não caem em janeiro ou fevereiro.

```sql
person.birthMonth > 2
```

## Greater than or equal to

A função `>=` (maior que ou igual a) é usada para verificar se o primeiro valor é maior ou igual ao segundo valor.

**Formato**

```sql
{EXPRESSION} >= {EXPRESSION} 
```

**Exemplo**

A consulta PQL a seguir define as pessoas cujos aniversários não caem em janeiro ou fevereiro.

```sql
person.birthMonth >= 3
```

## Less than

A função de comparação `<` (menor que) é usada para verificar se o primeiro valor é menor que o segundo valor.

**Formato**

```sql
{EXPRESSION} < {EXPRESSION} 
```

**Exemplo**

A consulta PQL a seguir define as pessoas cujo aniversário é em janeiro.

```sql
person.birthMonth < 2
```

## Less than or equal to

A função de comparação `<=` (menor que ou igual a) é usada para verificar se o primeiro valor é menor que ou igual ao segundo valor.

**Formato**

```sql
{EXPRESSION} <= {EXPRESSION} 
```

**Exemplo**

A consulta PQL a seguir define as pessoas cujo aniversário é em janeiro ou fevereiro.

```sql
person.birthMonth <= 2
```

## Add

A função `+` (adição) é usada para encontrar a soma de duas expressões de argumento.

**Formato**

```sql
{NUMBER} + {NUMBER}
```

**Exemplo**

A consulta PQL a seguir soma o preço de dois produtos diferentes.

```sql
product1.price + product2.price
```

## Multiplicar

A função `*` (multiplicação) é usada para encontrar o produto de duas expressões de argumento.

**Formato**

```sql
{NUMBER} * {NUMBER}
```

**Exemplo**

A consulta PQL a seguir encontra o produto do inventário e o preço de um produto para descobrir o valor bruto do produto.

```sql
product.inventory * product.price
```

## Subtrair

A função `-` (subtração) é usada para encontrar a diferença de duas expressões de argumento.

**Formato**

```sql
{NUMBER} - {NUMBER}
```

**Exemplo**

A consulta PQL a seguir encontra a diferença de preço entre dois produtos diferentes.

```sql
product1.price - product2.price
```

## Dividir

A função `/` (divisão) é usada para encontrar o quociente de duas expressões de argumento.

**Formato**

```sql
{NUMBER} / {NUMBER}
```

**Exemplo**

A consulta PQL a seguir encontra o quociente entre o total de produtos vendidos e o total de dinheiro ganho para ver o custo médio por item.

```sql
totalProduct.price / totalProduct.sold
```

## Remanescente

A função `%` (modulo/rest) é usada para localizar o restante após dividir as duas expressões de argumento.

**Formato**

```sql
{NUMBER} % {NUMBER}
```

**Exemplo**

A consulta PQL a seguir verifica se a idade da pessoa é divisível por cinco.

```sql
person.age % 5 = 0
```
