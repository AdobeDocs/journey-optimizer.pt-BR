---
title: Biblioteca de funções de agregação
description: Biblioteca de funções de agregação
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: a029f716-ea1e-4d79-82b7-59770f05161b
source-git-commit: 284d95976ab1b58aaea2a4c41db20a3ea5a9b761
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 9%

---

# Funções de Agregação {#aggregation}

As funções de agregação são usadas para agrupar vários valores para formar um único valor de resumo.

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

## Mínimo{#min}

O `min` retorna o menor de todos os valores selecionados na matriz.

**Formato**

```sql
{%= min(array) %}
```

**Exemplo**

A operação a seguir retorna o preço mais baixo de todas as ordens.

```sql
{%=min(orders.order.price) %}
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
