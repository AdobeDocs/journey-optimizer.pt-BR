---
title: Biblioteca de funções aritméticas
description: Biblioteca de funções aritméticas
feature: Personalização
topic: Personalização
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 7%

---

# Funções aritméticas {#maths}

![](../../assets/do-not-localize/badge.png)

As funções aritméticas são usadas para executar cálculos básicos em valores.

## Add{#add}

A função `+` (adição) é usada para encontrar a soma de duas expressões de argumento.

**Formato**

```sql
{%= double + double %}
```

**Exemplo**

A operação seguinte soma o preço de dois produtos diferentes.

```sql
{%= product1.price + product2.price %}
```

## Multiplicar{#multiply}

A função `*` (multiplicação) é usada para encontrar o produto de duas expressões de argumento.

**Formato**

```sql
{%= double * double %}
```

**Exemplo**

A operação seguinte indica o produto do inventário e o preço de um produto para determinar o valor bruto do produto.

```sql
{%= product.inventory * product.price %}
```

## Subtrair{#substract}

A função `-` (subtração) é usada para encontrar a diferença de duas expressões de argumento.

**Formato**

```sql
{%= double - double %}
```

**Exemplo**

A operação seguinte indica a diferença de preço entre dois produtos diferentes.

```sql
{%= product1.price - product2.price %}
```

## Dividir{#divide}

A função `/` (divisão) é usada para encontrar o quociente de duas expressões de argumento.

**Formato**

```sql
{%= double / double %}
```

**Exemplo**

A operação a seguir encontra o quociente entre o total de produtos vendidos e o total de dinheiro ganho para ver o custo médio por item.

```sql
{%= totalProduct.price / totalProduct.sold %}
```

## Remanescente{#remainder}

A função `%` (modulo/rest) é usada para localizar o restante após dividir as duas expressões de argumento.

**Formato**

```sql
{%= double % double %}
```

**Exemplo**

A operação a seguir verifica se a idade da pessoa é divisível por cinco.

```sql
{%= person.age % 5 = 0 %}
```
