---
title: Biblioteca de funções
description: Biblioteca de funções
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 6%

---

# Mapeia funções {#maps}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL) oferece funções para facilitar a interação com mapas.

## Obtenha

A função `get` é usada para recuperar o valor de um mapa para uma determinada chave.

**Formato**

```sql
get({MAP},{STRING})
```

**Exemplo**

A consulta PQL a seguir obtém o valor do mapa de identidade da chave `example@example.com`.

```sql
get(identityMap,"example@example.com")
```

## Teclas

A função `keys` é usada para recuperar todas as chaves de um determinado mapa.

**Formato**

```sql
keys({MAP})
```

**Exemplo**

A consulta PQL a seguir obtém todas as chaves do mapa `identityMap`.

```sql
keys(identityMap)
```

## Valores

A função `values` é usada para recuperar todos os valores de um determinado mapa.

**Formato**

```sql
values({MAP})
```

**Exemplo**

A consulta PQL a seguir obtém todos os valores para o mapa `identityMap`.

```sql
values(identityMap)
```
