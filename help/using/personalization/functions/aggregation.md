---
title: Biblioteca de funções
description: Biblioteca de funções
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 9%

---

# Funções de agregação {#aggregation}

![](../../assets/do-not-localize/badge.png)

As funções de agregação são usadas para agrupar vários valores em matrizes [!DNL Profile Query Language] (PQL) para formar um único valor de resumo.

## Contagem

A função `count` retorna o número de elementos dentro da matriz fornecida.

**Formato**

```sql
count({ARRAY})
```

**Exemplo**

A consulta PQL a seguir retorna o número de pedidos na matriz.

```sql
count(orders)
```

## Sum

A função `sum` retorna a soma de todos os valores selecionados dentro da matriz.

**Formato**

```sql
sum({ARRAY})
```

**Exemplo**

A consulta PQL a seguir retorna a soma de todos os preços dos pedidos.

```sql
sum(orders.order.price)
```

## Média

A função `average` retorna a média aritmética de todos os valores selecionados dentro da matriz.

**Formato**

```sql
average({ARRAY})
```

**Exemplo**

A consulta PQL a seguir retorna o preço médio de todos os pedidos.

```sql
average(orders.order.price)
```

## Mínimo

A função `min` retorna o menor de todos os valores selecionados na matriz.

**Formato**

```sql
min({ARRAY})
```

**Exemplo**

A consulta PQL a seguir retorna o preço mais baixo de todos os pedidos.

```sql
min(orders.order.price)
```

## Máximo

A função `max` retorna o maior de todos os valores selecionados dentro da matriz.

**Formato**

```sql
max({ARRAY})
```

**Exemplo**

A consulta PQL a seguir retorna o preço mais alto de todos os pedidos.

```sql
max(orders.order.price)
```
