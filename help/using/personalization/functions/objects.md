---
title: Biblioteca de funções de objetos
description: Biblioteca de funções de objetos
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 6ce70e32-aac3-4a2c-bfeb-c370521853ca
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 7%

---

# Funções do objeto {#objects}

## É nulo{#isNull}

A função `isNull` determina se uma referência de objeto não existe.

**Sintaxe**

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

**Sintaxe**

```sql
{%= isNotNull(object) %}
```

**Exemplo**

A operação a seguir verifica se o endereço residencial da pessoa existe.

```sql
{%= isNotNull(person.homeAddress) %}
```
