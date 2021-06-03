---
title: Biblioteca de funções
description: Biblioteca de funções
source-git-commit: 8c58dd667ea59a17833bbe3482b1a233ac2e28fe
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 7%

---

# Mapear funções{#maps}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL) oferece funções para facilitar a interação com mapas.

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
