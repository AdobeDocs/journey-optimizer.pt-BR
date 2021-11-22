---
title: Biblioteca de funções de arrays
description: Biblioteca de funções de arrays
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: dfe611fb-9c50-473c-9eb7-b983e1e6f01e
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 5%

---

# Matrizes e funções de lista {#arrays}

Use essas funções para facilitar a interação com arrays, listas e strings.

## Distinct{#distinct}

O `distinct` é usada para obter valores de uma matriz ou lista com valores duplicados removidos.

**Formato**

```sql
{%= distinct(array) %}
```

**Exemplo**

A operação a seguir especifica pessoas que fizeram pedidos em mais de um armazenamento.

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

## Primeiro item{#head}

O `head` é usada para retornar o primeiro item na matriz ou lista.

**Formato**

```sql
{%= head({array}) %}
```

**Exemplo**

A operação a seguir retorna o primeiro dos cinco principais pedidos com o preço mais alto. Mais informações sobre o `topN` pode ser encontrada no [first `n` em matriz](#first-n) seção.

```sql
{%= head(topN(orders,price, 5)) %}
```

## First `n` em matriz {#first-n}

O `topN` é usada para retornar a primeira `N` itens em uma matriz, quando classificados em ordem crescente com base na expressão numérica fornecida.

**Formato**

```sql
{%= topN(array, value, amount) %}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{ARRAY}` | A matriz ou lista que deve ser classificada. |
| `{VALUE}` | A propriedade na qual classificar a matriz ou lista. |
| `{AMOUNT}` | O número de itens a serem retornados. |

**Exemplo**

A operação a seguir retorna os cinco principais pedidos com o preço mais alto.

```sql
{%= topN(orders,price, 5) %}
```

## Em{#in}

O `in` é usada para determinar se um item é membro de uma matriz ou lista.

**Formato**

```sql
{%= in(value, array) %}
```

**Exemplo**

A operação a seguir define as pessoas com aniversários em março, junho ou setembro.

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

## Inclui{#includes}

O `includes` é usada para determinar se uma matriz ou lista contém um determinado item.

**Formato**

```sql
{%= includes(array,item) %}
```

**Exemplo**

A operação a seguir define as pessoas cuja cor favorita inclui o vermelho.

```sql
{%= includes(person.favoriteColors,"red") %}
```

## Intersetos{#intersects}

O `intersects` é usada para determinar se duas matrizes ou listas têm pelo menos um membro comum.

**Formato**

```sql
{%= intersects(array1, array2) %}
```

**Exemplo**

A operação a seguir define as pessoas cujas cores favoritas incluem pelo menos um vermelho, azul ou verde.

```sql
{%= intersects(person.favoriteColors,["red", "blue", "green"]) %}
```


<!-- ## Intersection{#intersection}

The `intersection` function is used to determine the common members of two arrays or lists.

**Format**

```sql
intersection({ARRAY},{ARRAY})
```

**Example**

The following operation defines if person 1 and person 2 both have favorite colors of red, blue, and green.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```
-->

## Último `n` em matriz{#last-n}

O `bottomN` é usada para retornar a última `N` itens em uma matriz, quando classificados em ordem crescente com base na expressão numérica fornecida.

**Formato**

```sql
{%= bottomN(array, value, amount) %}
```

| Argumento | Descrição |
| --------- | ----------- | 
| `{ARRAY}` | A matriz ou lista que deve ser classificada. |
| `{VALUE}` | A propriedade na qual classificar a matriz ou lista. |
| `{AMOUNT}` | O número de itens a serem retornados. |

**Exemplo**

A operação a seguir retorna os cinco principais pedidos com o preço mais baixo.

```sql
{%= bottomN(orders,price, 5) %}
```


## Não está em{#notin}

O `notIn` é usada para determinar se um item não é membro de uma matriz ou lista.

>[!NOTE]
>
>O `notIn` função *also* garante que nenhum dos valores seja igual a nulo. Portanto, os resultados não são uma negação exata do `in` .

**Formato**

```sql
{%= notIn(value, array) %}
```

**Exemplo**

A operação a seguir define pessoas com aniversários que não estão em março, junho ou setembro.

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```


## Subconjunto de{#subset}

O `subsetOf` é usada para determinar se uma matriz específica (matriz A) é um subconjunto de outra matriz (matriz B). Em outras palavras, todos os elementos na matriz A são elementos da matriz B.

**Formato**

```sql
{%= subsetOf(array1, array2) %}
```

**Exemplo**

A operação a seguir define as pessoas que visitaram todas as cidades favoritas.

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

## Superconjunto de{#superset}

O `supersetOf` é usada para determinar se uma matriz específica (matriz A) é um superconjunto de outra matriz (matriz B). Em outras palavras, essa matriz A contém todos os elementos na matriz B.

**Formato**

```sql
{%= supersetOf(array1, array2) %}
```

**Exemplo**

A operação a seguir define pessoas que comeram sushi e pizza pelo menos uma vez.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"] %}
```
