---
title: Biblioteca de funções de agregação
description: Biblioteca de funções de agregação
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: a029f716-ea1e-4d79-82b7-59770f05161b
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 9%

---

# Funções de Agregação {#aggregation}

As funções de agregação são usadas para agrupar vários valores para formar um único valor de resumo.

## Média{#average}

A função `average` retorna a média aritmética de todos os valores selecionados na matriz.

**Sintaxe**

```sql
{%= average(array) %}
```

**Exemplo**

A operação a seguir retorna o preço médio de todas as ordens.

```sql
{%=average(orders.order.price)%}
```

## Contagem{#count}

A função `count` retorna o número de elementos dentro da matriz especificada.

**Sintaxe**

```sql
{%= count(array) %}
```

**Exemplo**

A operação a seguir retorna o número de ordens na matriz.

```sql
{%= count(orders) %}
```

## Máximo{#max}

A função `max` retorna o maior valor dentro da matriz.

**Sintaxe**

```sql
{%= max(array) %}
```

**Exemplo**

A operação a seguir retorna o preço mais alto de todas as ordens.

```sql
{%=max(orders.order.price)%}
```

## Mínimo{#min}

A função `min` retorna o menor valor dentro da matriz.

**Sintaxe**

```sql
{%= min(array) %}
```

**Exemplo**

A operação a seguir retorna o preço mais baixo de todas as ordens.

```sql
{%=min(orders.order.price) %}
```

## Somar{#sum}

A função `sum` retorna a soma de todos os valores selecionados na matriz.

**Sintaxe**

```sql
{%= sum(array) %}
```

**Exemplo**

A operação a seguir retorna a soma de todos os preços das ordens.

```sql
{%=sum(orders.order.price)%}
```
