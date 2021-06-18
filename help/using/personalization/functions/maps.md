---
title: Biblioteca de funções do Maps
description: Biblioteca de funções do Maps
feature: Personalização
topic: Personalização
role: Data Engineer
level: Experienced
source-git-commit: e3b7e80b72e6be71d5b38cd5507d20ad2e8ca8d4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 8%

---

# Mapear funções{#maps}

Use as funções de Mapa na personalização para facilitar a interação com mapas.

## Obtenha{#get}

A função `get` é usada para recuperar o valor de um mapa para uma determinada chave.

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

A função `keys` é usada para recuperar todas as chaves de um determinado mapa.

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

A função `values` é usada para recuperar todos os valores de um determinado mapa.

**Formato**

```sql
{%= values(map) %}
```

**Exemplo**

A operação a seguir obtém todos os valores para o mapa `identityMap`.

```sql
{%= values(identityMap) %}
```
