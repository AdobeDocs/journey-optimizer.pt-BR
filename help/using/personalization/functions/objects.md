---
title: Biblioteca de funções de objetos
description: Biblioteca de funções de objetos
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 6ce70e32-aac3-4a2c-bfeb-c370521853ca
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 7%

---

# Funções do objeto {#objects}

## É nulo{#isNull}

O `isNull` determina se uma referência de objeto não existe.

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

O `isNotNull` determina se existe uma referência de objeto.

**Formato**

```sql
{%= isNotNull(object) %}
```

**Exemplo**

A operação a seguir verifica se o endereço residencial da pessoa existe.

```sql
{%= isNotNull(person.homeAddress) %}
```
