---
title: Biblioteca de funções de matrizes
description: Biblioteca de funções de matrizes
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: dfe611fb-9c50-473c-9eb7-b983e1e6f01e
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 6%

---

# Matrizes e funções de lista {#arrays}

Use essas funções para facilitar a interação com matrizes, listas e sequências de caracteres.

## Somente contagem nula {#count-only-null}

A variável `countOnlyNull` é usada para contar o número de valores nulos em uma lista.

**Sintaxe**

```sql
{%= countOnlyNull(array) %}
```

**Exemplo**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Retorna 3.

## Contagem com nulo {#count-with-null}

A variável `countWithNull` é usada para contar todos os elementos de uma lista, incluindo valores nulos.

**Sintaxe**

```sql
{%= countWithNull(array) %}
```

**Exemplo**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Retorna 6.

## Distinto{#distinct}

A variável `distinct` é usada para obter valores de uma matriz ou lista com valores duplicados removidos.

**Sintaxe**

```sql
{%= distinct(array) %}
```

**Exemplo**

A operação a seguir especifica as pessoas que fizeram pedidos em mais de um armazenamento.

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

## Contagem distinta com nulo {#distinct-count-with-null}

A variável `distinctCountWithNull` é usada para contar o número de valores diferentes em uma lista, incluindo os valores nulos.

**Sintaxe**

```sql
{%= distinctCountWithNull(array) %}
```

**Exemplo**

```sql
{%= distinctCountWithNull([10,2,10,null]) %}
```

Retorna 3.

## Primeiro item{#head}

A variável `head` é usada para retornar o primeiro item em uma matriz ou lista.

**Sintaxe**

```sql
{%= head(array) %}
```

**Exemplo**

A operação a seguir retorna a primeira das cinco ordens principais com o preço mais alto. Mais informações sobre o `topN` pode ser encontrada na variável [primeiro `n` na matriz](#first-n) seção.

```sql
{%= head(topN(orders,price, 5)) %}
```

## Primeiro `n` na matriz {#first-n}

A variável `topN` é usada para retornar a primeira `N` itens em uma matriz, quando classificados em ordem crescente com base na expressão numérica fornecida.

**Sintaxe**

```sql
{%= topN(array, value, amount) %}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{ARRAY}` | A matriz ou lista que deve ser classificada. |
| `{VALUE}` | A propriedade na qual classificar a matriz ou lista. |
| `{AMOUNT}` | O número de itens a serem retornados. |

**Exemplo**

A operação a seguir retorna as cinco primeiras ordens com o preço mais baixo.

```sql
{%= topN(orders,price, 5) %}
```

## Entrada{#in}

A variável `in` é usada para determinar se um item é membro de uma matriz ou lista.

**Sintaxe**

```sql
{%= in(value, array) %}
```

**Exemplo**

A operação a seguir define as pessoas com aniversários em março, junho ou setembro.

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

## Inclui{#includes}

A variável `includes` é usada para determinar se uma matriz ou lista contém um determinado item.

**Sintaxe**

```sql
{%= includes(array,item) %}
```

**Exemplo**

A operação a seguir define as pessoas cuja cor favorita inclui vermelho.

```sql
{%= includes(person.favoriteColors,"red") %}
```

## Interseta{#intersects}

A variável `intersects` é usada para determinar se duas matrizes ou listas têm pelo menos um membro comum.

**Sintaxe**

```sql
{%= intersects(array1, array2) %}
```

**Exemplo**

A operação a seguir define as pessoas cujas cores favoritas incluem pelo menos uma das cores vermelha, azul ou verde.

```sql
{%= intersects(person.favoriteColors,["red", "blue", "green"]) %}
```


<!-- ## Intersection{#intersection}

The `intersection` function is used to determine the common members of two arrays or lists.

**Syntax**

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

A variável `bottomN` é usada para retornar a última `N` itens em uma matriz, quando classificados em ordem crescente com base na expressão numérica fornecida.

**Sintaxe**

```sql
{%= bottomN(array, value, amount) %}
```

| Argumento | Descrição |
| --------- | ----------- | 
| `{ARRAY}` | A matriz ou lista que deve ser classificada. |
| `{VALUE}` | A propriedade na qual classificar a matriz ou lista. |
| `{AMOUNT}` | O número de itens a serem retornados. |

**Exemplo**

A operação a seguir retorna as cinco últimas ordens com o preço mais alto.

```sql
{%= bottomN(orders,price, 5) %}
```

## Não está em{#notin}

A variável `notIn` é usada para determinar se um item não é membro de uma matriz ou lista.

>[!NOTE]
>
>A variável `notIn` função *também* garante que nenhum dos valores seja igual a nulo. Portanto, os resultados não são uma negação exata do `in` função.

**Sintaxe**

```sql
{%= notIn(value, array) %}
```

**Exemplo**

A operação a seguir define as pessoas com aniversários que não são em março, junho ou setembro.

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```


## Subconjunto de{#subset}

A variável `subsetOf` é usada para determinar se uma matriz específica (matriz A) é um subconjunto de outra matriz (matriz B). Em outras palavras, que todos os elementos na matriz A são elementos da matriz B.

**Sintaxe**

```sql
{%= subsetOf(array1, array2) %}
```

**Exemplo**

A operação a seguir define as pessoas que visitaram todas as cidades favoritas.

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

## Superconjunto de{#superset}

A variável `supersetOf` é usada para determinar se uma matriz específica (matriz A) é um superconjunto de outra matriz (matriz B). Em outras palavras, essa matriz A contém todos os elementos na matriz B.

**Sintaxe**

```sql
{%= supersetOf(array1, array2) %}
```

**Exemplo**

A operação seguinte define as pessoas que comeram sushi e pizza pelo menos uma vez.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"] %}
```
