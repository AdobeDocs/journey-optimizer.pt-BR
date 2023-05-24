---
title: Biblioteca de funções aritméticas
description: Biblioteca de funções aritméticas
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 21ef8f50-8389-4675-a8e5-0438a3eee592
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 7%

---

# Funções aritméticas {#maths}

Funções aritméticas são usadas para realizar cálculos básicos em valores.

## Add{#add}

A variável `+` (adição) é usada para encontrar a soma de duas expressões de argumento.

**Sintaxe**

```sql
{%= double + double %}
```

**Exemplo**

A operação a seguir soma o preço de dois produtos diferentes.

```sql
{%= product1.price + product2.price %}
```

## Multiplicar{#multiply}

A variável `*` A função (multiplicação) é usada para encontrar o produto de duas expressões de argumento.

**Sintaxe**

```sql
{%= double * double %}
```

**Exemplo**

A operação a seguir localiza o produto do estoque e o preço de um produto para localizar o valor bruto do produto.

```sql
{%= product.inventory * product.price %}
```

## Subtrair{#substract}

A variável `-` A função (subtração) é usada para encontrar a diferença de duas expressões de argumento.

**Sintaxe**

```sql
{%= double - double %}
```

**Exemplo**

A operação a seguir encontra a diferença de preço entre dois produtos diferentes.

```sql
{%= product1.price - product2.price %}
```

## Divisão{#divide}

A variável `/` A função (divisão) é usada para encontrar o quociente de duas expressões de argumento.

**Sintaxe**

```sql
{%= double / double %}
```

**Exemplo**

A operação a seguir encontra o quociente entre o total de produtos vendidos e o dinheiro total ganho para ver o custo médio por item.

```sql
{%= totalProduct.price / totalProduct.sold %}
```

## Restante{#remainder}

A variável `%` A função (modulo/resto) é usada para encontrar o restante após dividir as duas expressões de argumento.

**Sintaxe**

```sql
{%= double % double %}
```

**Exemplo**

A operação a seguir verifica se a idade da pessoa é divisível por cinco.

```sql
{%= person.age % 5 = 0 %}
```
