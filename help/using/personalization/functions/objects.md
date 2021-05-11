---
title: Biblioteca de funções
description: Biblioteca de funções
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 7%

---

# Funções de objeto {#objects}

![](../../assets/do-not-localize/badge.png)

## É nulo

A função `isNull` determina se uma referência de objeto não existe.

**Formato**

```sql
isNull({OBJECT})
```

**Exemplo**

A consulta PQL a seguir verifica se o endereço residencial da pessoa não existe.

```sql
isNull(person.homeAddress)
```

## Não é nulo

A função `isNotNull` determina se existe uma referência de objeto.

**Formato**

```sql
isNotNull({OBJECT})
```

**Exemplo**

A consulta PQL a seguir verifica se o endereço residencial da pessoa existe.

```sql
isNotNull(person.homeAddress)
```
