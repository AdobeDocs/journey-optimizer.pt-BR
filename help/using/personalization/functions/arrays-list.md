---
title: Biblioteca de funções de arrays
description: Biblioteca de funções de arrays
feature: Personalização
topic: Personalização
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 5%

---

# Matrizes e funções de lista {#arrays}

Use essas funções para facilitar a interação com arrays, listas e strings.

## Distinct{#distinct}

A função `distinct` é usada para obter valores de uma matriz ou lista com valores duplicados removidos.

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

A função `head` é usada para retornar o primeiro item na matriz ou lista.

**Formato**

```sql
{%= head({array}) %}
```

**Exemplo**

A operação a seguir retorna o primeiro dos cinco principais pedidos com o preço mais alto. Mais informações sobre a função `topN` podem ser encontradas na seção [first `n` no array](#first-n).

```sql
{%= head(topN(orders,price, 5)) %}
```

## Primeiro `n` na matriz {#first-n}

A função `topN` é usada para retornar os primeiros `N` itens em uma matriz, quando classificada em ordem crescente com base na expressão numérica fornecida.

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

A função `in` é usada para determinar se um item é membro de uma matriz ou lista.

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

A função `includes` é usada para determinar se uma matriz ou lista contém um determinado item.

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

A função `intersects` é usada para determinar se duas matrizes ou listas têm pelo menos um membro comum.

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

## Último `n` na matriz{#last-n}

A função `bottomN` é usada para retornar os últimos `N` itens em uma matriz, quando classificada em ordem crescente com base na expressão numérica fornecida.

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

A função `notIn` é usada para determinar se um item não é membro de uma matriz ou lista.

>[!NOTE]
>
>A função `notIn` *também* garante que nenhum dos valores seja igual a nulo. Portanto, os resultados não são uma negação exata da função `in`.

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

A função `subsetOf` é usada para determinar se uma matriz específica (matriz A) é um subconjunto de outra matriz (matriz B). Em outras palavras, todos os elementos na matriz A são elementos da matriz B.

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

A função `supersetOf` é usada para determinar se uma matriz específica (matriz A) é um superconjunto de outra matriz (matriz B). Em outras palavras, essa matriz A contém todos os elementos na matriz B.

**Formato**

```sql
{%= supersetOf(array1, array2) %}
```

**Exemplo**

A operação a seguir define pessoas que comeram sushi e pizza pelo menos uma vez.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"] %}
```







