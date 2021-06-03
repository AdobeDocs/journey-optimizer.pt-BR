---
title: Biblioteca de funções
description: Biblioteca de funções
source-git-commit: 8c58dd667ea59a17833bbe3482b1a233ac2e28fe
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 9%

---

# Funções de Agregação {#aggregation}

![](../../assets/do-not-localize/badge.png)

As funções de agregação são usadas para agrupar vários valores para formar um único valor de resumo.

## Contagem{#count}

A função `count` retorna o número de elementos dentro da matriz fornecida.

**Formato**

```sql
{%= count(array) %}
```

**Exemplo**

A operação a seguir retorna o número de pedidos na matriz.

```sql
{%= count(orders) %}
```

## Sum{#sum}

A função `sum` retorna a soma de todos os valores selecionados dentro da matriz.

**Formato**

```sql
{%= sum(array) %}
```

**Exemplo**

A operação a seguir retorna a soma de todos os preços das ordens.

```sql
{%=sum(orders.order.price)%}
```

## Média{#average}

A função `average` retorna a média aritmética de todos os valores selecionados dentro da matriz.

**Formato**

```sql
{%= average(array) %}
```

**Exemplo**

A operação a seguir retorna o preço médio de todas as ordens.

```sql
{%=average(orders.order.price)%}
```

## Mínimo{#min}

A função `min` retorna o menor de todos os valores selecionados na matriz.

**Formato**

```sql
{%= min(array) %}
```

**Exemplo**

A operação a seguir retorna o preço mais baixo de todas as ordens.

```sql
{%=min(orders.order.price)%}
```

## Máximo{#max}

A função `max` retorna o maior de todos os valores selecionados dentro da matriz.

**Formato**

```sql
{%= max(array) %}
```

**Exemplo**

A operação a seguir retorna o preço mais alto de todas as ordens.

```sql
{%=max(orders.order.price)%}
```
