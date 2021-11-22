---
title: Biblioteca de funções de agregação
description: Biblioteca de funções de agregação
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: a029f716-ea1e-4d79-82b7-59770f05161b
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 9%

---

# Funções de Agregação {#aggregation}

As funções de agregação são usadas para agrupar vários valores para formar um único valor de resumo.

## Contagem{#count}

O `count` retorna o número de elementos dentro de uma matriz específica.

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

O `sum` retorna a soma de todos os valores selecionados na matriz.

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

O `average` retorna a média aritmética de todos os valores selecionados na matriz.

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

O `min` retorna o menor de todos os valores selecionados na matriz.

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

O `max` retorna o maior de todos os valores selecionados na matriz.

**Formato**

```sql
{%= max(array) %}
```

**Exemplo**

A operação a seguir retorna o preço mais alto de todas as ordens.

```sql
{%=max(orders.order.price)%}
```
