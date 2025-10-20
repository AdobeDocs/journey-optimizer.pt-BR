---
title: Biblioteca de funções de mapas
description: Biblioteca de funções de mapas
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: de6a8da2-55cf-4105-ba93-40c556732626
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 6%

---

# Funções de Mapas{#maps}

Use as funções de Mapa na personalização para facilitar a interação com mapas.

## Obter{#get}

A função `get` é usada para recuperar o valor de um mapa para uma determinada chave.

**Sintaxe**

```sql
{%= get(map, string) %}
```

**Exemplo**

A operação a seguir obtém o valor do mapa de identidade para a chave `example@example.com`.

```sql
{%= get(identityMap,"example@example.com") %}
```

## Chaves{#keys}

A função `keys` é usada para recuperar todas as chaves de um determinado mapa.

**Sintaxe**

```sql
{%= keys(map) %}
```

**Exemplo**

A operação a seguir obtém todas as chaves do mapa `identityMap`.

```sql
{%= keys(identityMap) %}
```

## Valores{#values}

A função `values` é usada para recuperar todos os valores de um determinado mapa.

**Sintaxe**

```sql
{%= values(map) %}
```

**Exemplo**

A operação a seguir obtém todos os valores do mapa `identityMap`.

```sql
{%= values(identityMap) %}
```
