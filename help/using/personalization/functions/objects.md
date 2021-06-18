---
title: Biblioteca de funções de objetos
description: Biblioteca de funções de objetos
feature: Personalização
topic: Personalização
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 10%

---

# Funções do objeto {#objects}

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
