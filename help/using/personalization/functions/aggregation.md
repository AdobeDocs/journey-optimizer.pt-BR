---
title: Biblioteca de funções de agregação
description: Biblioteca de funções de agregação
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: a029f716-ea1e-4d79-82b7-59770f05161b
TQID: https://experienceleague.adobe.com/y1ivXVJe-Y5aIkMu--Tz22U0j-cuGcTUYrdkCkl1xyE
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: []
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 157
ht-degree: 9%

---

# Funções de agregação {#aggregation}

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

## Count{#count}

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

## Sum{#sum}

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
