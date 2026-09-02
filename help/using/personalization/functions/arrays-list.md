---
title: Biblioteca de funções de matrizes
description: Biblioteca de funções de matrizes
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: dfe611fb-9c50-473c-9eb7-b983e1e6f01e
TQID: https://experienceleague.adobe.com/CUiT5GFH9o4q-oOSWuKC8ZyLbRbH9lj88M92LhMIX9E
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: []
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 742
ht-degree: 4%

---

# Matrizes e funções de lista {#arrays}

Use essas funções para facilitar a interação com matrizes, listas e sequências de caracteres.

## Somente contagem nula {#count-only-null}

A função `countOnlyNull` é usada para contar o número de valores nulos em uma lista.

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

A função `countWithNull` é usada para contar todos os elementos de uma lista, incluindo valores nulos.

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

A função `distinct` é usada para obter valores de uma matriz ou lista com valores duplicados removidos.

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

A função `distinctCountWithNull` é usada para contar o número de valores diferentes em uma lista, incluindo os valores nulos.

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

A função `head` é usada para retornar o primeiro item em uma matriz ou lista.

**Sintaxe**

```sql
{%= head(array) %}
```

**Exemplo**

A operação a seguir retorna a primeira das cinco ordens principais com o preço mais alto. Mais informações sobre a função `topN` podem ser encontradas na [primeira `n` da seção de matriz](#first-n).

```sql
{%= head(topN(orders,price, 5)) %}
```

## Classificar e obter o primeiro N na matriz {#first-n}

A função `topN` classifica uma matriz em ordem decrescente com base na expressão numérica fornecida e retorna os primeiros `N` itens. Se o tamanho da matriz for menor que `N`, ela retornará toda a matriz classificada.

Esta função
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

A função `in` é usada para determinar se um item é membro de uma matriz ou lista.

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

A função `includes` é usada para determinar se uma matriz ou lista contém um determinado item.

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

A função `intersects` é usada para determinar se duas matrizes ou listas têm pelo menos um membro comum.

**Sintaxe**

```sql
{%= intersects(array1, array2) %}
```

**Exemplo**

A operação a seguir define as pessoas cujas cores favoritas incluem pelo menos uma das cores vermelha, azul ou verde.

```sql
{%= intersects(person.favoriteColors,["red", "blue", "green"]) %}
```


<!--
## Intersection{#intersection}

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

## Classificar e obter o último N na matriz {#last-n}

A função `bottomN` classifica uma matriz em ordem crescente com base na expressão numérica fornecida e retorna os primeiros `N` itens. Se o tamanho da matriz for menor que `N`, ela retornará toda a matriz classificada.

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

A função `notIn` é usada para determinar se um item não é membro de uma matriz ou lista.

>[!NOTE]
>
>A função `notIn` *também* garante que nenhum dos valores seja igual a nulo. Portanto, os resultados não são uma negação exata da função `in`.

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

A função `subsetOf` é usada para determinar se uma matriz específica (matriz A) é um subconjunto de outra matriz (matriz B). Em outras palavras, que todos os elementos na matriz A são elementos da matriz B.

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

A função `supersetOf` é usada para determinar se uma matriz específica (matriz A) é um superconjunto de outra matriz (matriz B). Em outras palavras, essa matriz A contém todos os elementos na matriz B.

**Sintaxe**

```sql
{%= supersetOf(array1, array2) %}
```

**Exemplo**

A operação seguinte define as pessoas que comeram sushi e pizza pelo menos uma vez.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"]) %}
```

## Iterar em uma matriz {#each-loop}

Use o auxiliar de bloco `{{#each}}` do Handlebars para executar um loop sobre uma matriz e renderizar o conteúdo para cada item em **conteúdo personalizado** (email, SMS, push).

>[!NOTE]
>
>`{{#each}}` está disponível somente no **editor de personalização** (corpo do email, SMS, conteúdo de push). **Não** é suportado na atividade de condição de jornada. Para filtrar ou corresponder itens de uma matriz dentro de uma condição de jornada, use [funções de gerenciamento de coleções](../../building-journeys/expression/collection-management-functions.md).

**Sintaxe**

```handlebars
{{#each arrayAttribute}}
  {{this}}
{{/each}}
```

+++Exemplo — Listar todos os itens em uma matriz

```handlebars
{{#each profile.purchases.items}}
  - {{this.name}}: {{this.price}}€
{{/each}}
```

Saída (exemplo):

```
- Running shoes: 89€
- Water bottle: 15€
- Gym bag: 45€
```

+++

+++Exemplo — Acessar o índice de loop

Usar `@index` para acessar a posição de loop atual (com base em 0):

```handlebars
{{#each profile.preferences.languages}}
  {{@index}}: {{this}}
{{/each}}
```

Saída (exemplo):

```
0: English
1: French
2: Spanish
```

+++

+++Exemplo — Renderização condicional dentro de um loop

Use o bloco `{%#if%}` dentro de `{{#each}}` para renderizar o conteúdo somente quando uma condição for atendida:

>[!NOTE]
>
>Não há suporte para `{% if %}` / `{% endif %}`. Em vez disso, use `{%#if%}` / `{%/if%}`. Além disso, `this.<field>` não funciona dentro de expressões de condição do PQL — faça referência ao campo diretamente usando o nome do atributo (por exemplo, `order.status`).

```handlebars
{{#each profile.orders as |order|}}
  {%#if order.status = "pending"%}
  Your order {{order.id}} is still pending.
  {%/if%}
{{/each}}
```

Esse é o padrão recomendado para simular uma &quot;quebra na condição&quot; — somente os itens correspondentes à condição produzem saída.

+++
