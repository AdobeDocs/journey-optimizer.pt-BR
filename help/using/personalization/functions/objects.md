---
title: Biblioteca de funções
description: Biblioteca de funções
source-git-commit: 8c58dd667ea59a17833bbe3482b1a233ac2e28fe
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 7%

---

# Funções do objeto {#objects}

![](../../assets/do-not-localize/badge.png)

## É nulo{#isNull}

A função `isNull` determina se uma referência de objeto não existe.

**Formato**

```sql
{%= isNull(object) %}
```

**Exemplo**

A operação a seguir verifica se o endereço residencial da pessoa não existe.

```sql
{%= isNull(person.homeAddress) %}
```

## Não é nulo{#isNotNull}

A função `isNotNull` determina se existe uma referência de objeto.

**Formato**

```sql
{%= isNotNull(object) %}
```

**Exemplo**

A operação a seguir verifica se o endereço residencial da pessoa existe.

```sql
{%= isNotNull(person.homeAddress) %}
```
