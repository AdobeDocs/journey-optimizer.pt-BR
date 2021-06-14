---
title: Biblioteca de funções de objetos
description: Biblioteca de funções de objetos
feature: Personalização
topic: Personalização
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 10%

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
