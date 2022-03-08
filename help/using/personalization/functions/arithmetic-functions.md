---
title: Biblioteca de funções aritméticas
description: Biblioteca de funções aritméticas
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 21ef8f50-8389-4675-a8e5-0438a3eee592
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 7%

---

# Funções aritméticas {#maths}

As funções aritméticas são usadas para executar cálculos básicos em valores.

## Add{#add}

O `+` (adição) é usada para encontrar a soma de duas expressões de argumento.

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

O `*` (multiplicação) é usada para encontrar o produto de duas expressões de argumento.

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

O `-` (subtração) é usada para encontrar a diferença de duas expressões de argumento.

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

O `/` (divisão) é usada para encontrar o quociente de duas expressões de argumento.

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

O `%` (modulo/rest) é usada para encontrar o restante após dividir as duas expressões de argumento.

**Formato**

```sql
{%= double % double %}
```

**Exemplo**

A operação a seguir verifica se a idade da pessoa é divisível por cinco.

```sql
{%= person.age % 5 = 0 %}
```
