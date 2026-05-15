---
title: Biblioteca de funções de mapas
description: Biblioteca de funções de mapas
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: de6a8da2-55cf-4105-ba93-40c556732626
TQID: https://experienceleague.adobe.com/KeitEe0NQxxc-snCyWSGlov-OyUgiva6ddzrCTxEKSs
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 102
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
