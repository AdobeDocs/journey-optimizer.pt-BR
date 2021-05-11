---
title: Biblioteca de funções
description: Biblioteca de funções
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 5%

---

# Matrizes e funções de lista {#arrays}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL) oferece funções para facilitar a interação com arrays, listas e strings.

## Em

A função `in` é usada para determinar se um item é membro de uma matriz ou lista.

**Formato**

```sql
in ({VALUE},{ARRAY})
```

**Exemplo**

A consulta PQL a seguir define as pessoas com aniversários em março, junho ou setembro.

```sql
in (person.birthMonth, [3, 6, 9])
```

## Não está em

A função `notIn` é usada para determinar se um item não é membro de uma matriz ou lista.

>[!NOTE]
>
>A função `notIn` *também* garante que nenhum dos valores seja igual a nulo. Portanto, os resultados não são uma negação exata da função `in`.

**Formato**

```sql
notIn ({VALUE},{ARRAY})
```

**Exemplo**

A consulta PQL a seguir define pessoas com aniversários que não estejam em março, junho ou setembro.

```sql
notIn (person.birthMonth ,[3, 6, 9])
```

## Intersetos

A função `intersects` é usada para determinar se duas matrizes ou listas têm pelo menos um membro comum.

**Formato**

```sql
intersects({ARRAY},{ARRAY})
```

**Exemplo**

A consulta PQL a seguir define as pessoas cujas cores favoritas incluem pelo menos um vermelho, azul ou verde.

```sql
intersects(person.favoriteColors,["red", "blue", "green"])
```

## Interseção

A função `intersection` é usada para determinar os membros comuns de duas matrizes ou listas.

**Formato**

```sql
intersection({ARRAY},{ARRAY})
```

**Exemplo**

A consulta PQL a seguir define se a pessoa 1 e a pessoa 2 têm cores favoritas de vermelho, azul e verde.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```

## Subconjunto de

A função `subsetOf` é usada para determinar se uma matriz específica (matriz A) é um subconjunto de outra matriz (matriz B). Em outras palavras, todos os elementos na matriz A são elementos da matriz B.

**Formato**

```sql
subsetOf({ARRAY},{ARRAY})
```

**Exemplo**

A consulta PQL a seguir define as pessoas que visitaram todas as cidades favoritas.

```sql
subsetOf(person.favoriteCities,person.visitedCities)
```

## Superconjunto de

A função `supersetOf` é usada para determinar se uma matriz específica (matriz A) é um superconjunto de outra matriz (matriz B). Em outras palavras, essa matriz A contém todos os elementos na matriz B.

**Formato**

```sql
supersetOf({ARRAY},{ARRAY})
```

**Exemplo**

A consulta PQL a seguir define as pessoas que comeram sushi e pizza pelo menos uma vez.

```sql
supersetOf(person.eatenFoods,["sushi", "pizza"])
```

## Inclui

A função `includes` é usada para determinar se uma matriz ou lista contém um determinado item.

**Formato**

```sql
includes({ARRAY},{ITEM})
```

**Exemplo**

A consulta PQL a seguir define as pessoas cuja cor favorita inclui o vermelho.

```sql
includes(person.favoriteColors,"red")
```

## Distinct

A função `distinct` é usada para remover valores duplicados de uma matriz ou lista.

**Formato**

```sql
distinct({ARRAY})
```

**Exemplo**

A consulta PQL a seguir especifica pessoas que fizeram pedidos em mais de um armazenamento.

```sql
distinct(person.orders.storeId).count() > 1
```

## Primeiro `n` na matriz {#first-n}

A função `topN` é usada para retornar os primeiros `N` itens em uma matriz, quando classificada em ordem crescente com base na expressão numérica fornecida.

**Formato**

```sql
topN({ARRAY},{VALUE}, {AMOUNT})
```

| Argumento | Descrição |
| --------- | ----------- |
| `{ARRAY}` | A matriz ou lista que deve ser classificada. |
| `{VALUE}` | A propriedade na qual classificar a matriz ou lista. |
| `{AMOUNT}` | O número de itens a serem retornados. |

**Exemplo**

A consulta PQL a seguir retorna os cinco principais pedidos com o preço mais alto.

```sql
topN(orders,price, 5)
```

## Último `n` na matriz

A função `bottomN` é usada para retornar os últimos `N` itens em uma matriz, quando classificada em ordem crescente com base na expressão numérica fornecida.

**Formato**

```sql
bottomN({ARRAY},{VALUE}, {AMOUNT})
```

| Argumento | Descrição |
| --------- | ----------- | 
| `{ARRAY}` | A matriz ou lista que deve ser classificada. |
| `{VALUE}` | A propriedade na qual classificar a matriz ou lista. |
| `{AMOUNT}` | O número de itens a serem retornados. |

**Exemplo**

A consulta PQL a seguir retorna os cinco principais pedidos com o preço mais baixo.

```sql
bottomN(orders,price, 5)
```

## Primeiro item

A função `head` é usada para retornar o primeiro item na matriz ou lista.

**Formato**

```sql
head({ARRAY})
```

**Exemplo**

A consulta PQL a seguir retorna o primeiro dos cinco principais pedidos com o preço mais alto. Mais informações sobre a função `topN` podem ser encontradas na seção [first `n` no array](#first-n).

```sql
head(topN(orders,price, 5))
```
