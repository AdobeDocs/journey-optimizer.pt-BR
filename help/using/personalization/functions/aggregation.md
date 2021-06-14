---
title: Biblioteca de funções de agregação
description: Biblioteca de funções de agregação
feature: Personalização
topic: Personalização
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 10%

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
