---
title: Biblioteca de funções do Maps
description: Biblioteca de funções do Maps
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: de6a8da2-55cf-4105-ba93-40c556732626
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 6%

---

# Mapear funções{#maps}

Use as funções de Mapa na personalização para facilitar a interação com mapas.

## Obtenha{#get}

O `get` é usada para recuperar o valor de um mapa para uma determinada chave.

**Formato**

```sql
{%= get(map, string) %}
```

**Exemplo**

A operação a seguir obtém o valor do mapa de identidade da chave `example@example.com`.

```sql
{%= get(identityMap,"example@example.com") %}
```

## Teclas{#keys}

O `keys` é usada para recuperar todas as chaves de um determinado mapa.

**Formato**

```sql
{%= keys(map) %}
```

**Exemplo**

A operação a seguir obtém todas as chaves do mapa `identityMap`.

```sql
{%= keys(identityMap) %}
```

## Valores{#values}

O `values` é usada para recuperar todos os valores de um determinado mapa.

**Formato**

```sql
{%= values(map) %}
```

**Exemplo**

A operação a seguir obtém todos os valores do mapa `identityMap`.

```sql
{%= values(identityMap) %}
```
