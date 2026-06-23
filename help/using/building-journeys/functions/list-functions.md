---
product: journey optimizer
title: Listar funções
description: Saiba mais sobre funções de lista
feature: Journeys
role: Developer
level: Experienced
keywords: lista, funções, expressão, jornada, matriz, coleção
version: Journey Orchestration
exl-id: b17245ba-4ffa-4f5b-914e-4c0972e9c7c4
TQID: https://experienceleague.adobe.com/XWWixhfBVKw-kdgO4WPWrtiIqA8sFt0ql0IVZ-2QsUI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: d00e9f03-e50b-4162-b143-0c0817c937c2
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1642
ht-degree: 6%

---

# Listar funções {#list-functions}

As funções de lista permitem manipular e trabalhar com coleções de valores nas expressões de jornada. Essas funções são essenciais para filtrar, classificar, transformar e analisar matrizes e listas nas jornadas do cliente.

Use as funções de lista quando precisar:

* Filtrar e extrair itens específicos de coleções com base em critérios ([filtro](#filter), [getListItem](#getListItem))
* Classificar e organizar elementos de lista em ordem crescente ou decrescente ([sort](#sort))
* Remova as duplicatas e obtenha valores exclusivos das listas ([distinct](#distinct), [distinctWithNull](#distinctWithNull))
* Verificar se existem valores em coleções ([em](#in))
* Limitar o número de itens retornados de uma lista ([limit](#limit))
* Obter o tamanho de uma lista ([listSize](#listSize)) ou transformar listas em diferentes formatos ([serializeList](#serializeList))
* Execute operações de definição, como localizar elementos comuns entre listas ([interseção](#intersect))

As funções de lista fornecem ferramentas poderosas para trabalhar com estruturas de dados complexas, permitindo uma manipulação de dados sofisticada e lógica condicional com base no conteúdo da coleção.

## distinct {#distinct}

Retorna os valores ou objetos distintos de uma determinada lista. Entradas nulas são ignoradas.

+++Sintaxe

`distinct(<parameters>)`

+++

+++Parâmetros

| Parâmetro | Tipo | Descrição |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly ou listObject | Lista a processar. Para listObject, ele deve ser uma referência de campo. |
| keyAttributeName | sequência de caracteres | Este parâmetro é opcional e somente para listObject. Se o parâmetro não for fornecido, um objeto será considerado duplicado se todos os atributos tiverem os mesmos valores. Caso contrário, um objeto será considerado duplicado se o atributo em questão tiver o mesmo valor. |

+++

+++Assinaturas e tipos retornados

`distinct(<listInteger>)`

Retorna uma lista de inteiros.

`distinct(<listDecimal>)`

Retorna uma lista de decimais.

`distinct(<listString>)`

Retorna uma lista de strings.

`distinct(<listDateTimeOnly>)`

Retorna uma lista de datetimes sem considerar o fuso horário.

`distinct(<listDateTime>)`

Retorna uma lista de datetimes.

`distinct(<listDateOnly>)`

Retorna uma lista de datas.

`distinct(<listBoolean>)`

Retorna uma lista de booleanos.

`distinct(<listDuration>)`

Retorna uma lista de durações.

`distinct(<listObject>)`

`distinct(<listObject>,<string>)`

Retorna uma lista de objetos.

+++

+++Exemplos

`distinct([10,2,10,null])`

Retorna `[10, 2]`.

+++

## distinctWithNull {#distinctWithNull}

Retorna os valores ou objetos distintos de uma determinada lista. Se a lista tiver pelo menos uma entrada nula, uma entrada nula estará presente na lista retornada.

+++Sintaxe

`distinctWithNull(<parameters>)`

+++

+++Parâmetros

| Parâmetro | Tipo | Descrição |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly | Lista a processar. |

+++

+++Assinaturas e tipos retornados

`distinctWithNull(<listInteger>)`

Retorna uma lista de inteiros.

`distinctWithNull(<listDecimal>)`

Retorna uma lista de decimais.

`distinctWithNull(<listString>)`

Retorna uma lista de strings.

`distinctWithNull(<listDateTimeOnly>)`

Retorna uma lista de datetimes sem considerar o fuso horário.

`distinctWithNull(<listDateTime>)`

Retorna uma lista de datetimes.

`distinctWithNull(<listDateOnly>)`

Retorna uma lista de datas.

`distinctWithNull(<listBoolean>)`

Retorna uma lista de booleanos.

`distinctWithNull(<listDuration>)`

Retorna uma lista de durações.

+++

+++Exemplos

`distinctWithNull([10,2,10,null])`

Retorna [10, 2, nulo]

+++

**Observação:** o parâmetro `<listObject>` não tem suporte nesta função.

## filtro {#filter}

Retorna um listObject com objetos que têm o atributo de chave correspondente a um dos valores de chave fornecidos.

+++Sintaxe

`filter(<parameters>)`

+++

+++Parâmetros

| Parâmetro | Tipo | Descrição |
|-----------|------------------|------------------|
| listToFilter | listObject | lista de objetos a serem filtrados. Deve ser uma referência de campo. |
| keyAttributeName | sequência de caracteres | nome do atributo nos objetos da lista fornecida, usado como chave para filtragem |
| keyValueList | list | matriz de valores principais para filtragem |

+++

+++Assinaturas e tipos retornados

`filter(listObject, string, listString)`

`filter(listObject, string, listInteger)`

`filter(listObject, string, listDecimal)`

`filter(listObject, string, listDateTime)`

`filter(listObject, string, listDateTimeOnly)`

`filter(listObject, string, listDateOnly)`

`filter(listObject, string, listDuration)`

`filter(listObject, string, listBoolean)`

Retorna um listObject.

+++

+++Exemplos

Este é um exemplo de uma carga útil transmitida em um evento de entrada &quot;myevent&quot;:

```json
"productListItems": [{
   "id": "product1",
   "name": "the product 1",
   "price": 20
},{
   "id": "product2",
   "name": "the product 2",
   "price": 30
},{
   "id": "product3",
   "name": "the product 3",
   "price": 50
}]
```

Você pode usar a seguinte expressão:

```json
filter(
 @event{myevent.productListItems},
 "id", 
 ["product2", "product3", "product4"]
)
```

Retorna um listObject contendo os dois objetos com &quot;product2&quot; e &quot;product3&quot; como id.

+++

## getListItem {#getListItem}

Retorna o item da lista no índice fornecido.

+++Sintaxe

`getListItem(<parameters>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| list | listString |
| list | listBoolean |
| list | listInteger |
| list | listDecimal |
| list | listDuration |
| list | listDateTime |
| list | listDateTimeOnly |
| list | listDateOnly |
| índice | inteiro |

+++

+++Assinaturas e tipo retornado

`getListItem(<listInteger>,<index>)`

Retorna um inteiro.

`getListItem(<listDecimal>,<index>)`

Retorna um decimal.

`getListItem(<listString>,<index>)`

Retorna uma string.

`getListItem(<listDateTimeOnly>,<index>)`

Retorna uma data e hora sem considerar o fuso horário.

`getListItem(<listDateTime>,<index>)`

Retorna um datetime.

`getListItem(<listDateOnly>,<index>)`

Retorna uma lista de datas.

`getListItem(<listBoolean>,<index>)`

Retorna um valor booleano.

`getListItem(<listDuration>,<index>)`

Retorna uma duração.

+++

+++Exemplos

`getListItem([10, 2, 3], 1)`

Retorna &quot;2&quot;

`getListItem(["A", "B", "C"], 2)`

Retorna &quot;C&quot;

Exemplos com um campo de evento &quot;event.appVersion&quot; com valor: &quot;20.45.2.3434&quot;

`split(@event{event.appVersion}, "\\.")`

Retorna `["20", "45", "2", "3434"]`

`getListItem(split(@event{event.appVersion}, "\\."), 0)`

Retorna &quot;20&quot;

+++

## no {#in}

Verifica se o primeiro valor de argumento está na lista. A verificação é executada por meio de um valor Igual em cada argumento. Retornará true se o valor do argumento for encontrado; caso contrário, retornará false.

O tipo de `<expression>` deve corresponder aos itens da lista. Os tipos de itens da lista, como lembrete, devem corresponder um ao outro.

+++Sintaxe

`in(<parameters>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| String | String |
| Booleano | Booleano |
| Número inteiro | Número inteiro |
| Decimal | Decimal |
| Duração | Duração |
| DateTime | DateTime |
| DateTimeOnly | DateTimeOnly |
| Lista | listString |
| Lista | listBoolean |
| Lista | listInteger |
| Lista | listDecimal |
| Lista | listDuration |
| Lista | listDateTime |
| Lista | listDateTimeOnly |
| Lista | listDateOnly |

+++

+++Assinatura e tipo retornado

`in(<integer>,<listInteger>)`

`in(<decimal>,<listDecimal>)`

`in(<string>,<listString>)`

`in(<boolean>,<listBoolean>)`

`in(<dateTimeOnly>,<listDateTimeOnly>)`

`in(<dateTime>,<listDateTime>)`

`in(<dateOnly>,<listDateOnly>)`

`in(<duration>,<listDuration>)`

Retornar um booleano.

+++

+++Exemplos

`in(4,[4,5,3,4])`

Retorna verdadeiro.

`in(8,[4,5,3,4])`

Retorna falso.

`in(#{ExperiencePlatform.ProfileFieldGroup.profile.person.gender}, ["male"])`

+++

## interseção {#intersect}

Retorna os valores comuns nas duas listas de entrada. Se uma das duas listas for nula, retorna uma lista vazia.

+++Sintaxe

`intersect(<parameters>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| lista 1 | list |
| lista 2 | list |

+++

+++Assinaturas e tipos retornados

`intersect(listString,listString)`: listString

`intersect(listDecimal,listDecimal)`: listDecimal

`intersect(listInteger,listInteger)`: listInteger

`intersect(listDateTime,listDateTime)`: listDateTime

`intersect(listDateTimeOnly,listDateTimeOnly)`: listDateTimeOnly

`intersect(listDateOnly,listDateOnly)`: listDateOnly

`intersect(listDuration,listDuration)`: listDuration

`intersect(listBoolean,listBoolean)`: listBoolean

Retorna uma lista.

+++

+++Exemplos

```json
intersect(
    ["sports", "news", "documentary"],
    ["sports", "movies", "documentary"]
)
```

Retorna [&quot;esportes&quot;, &quot;notícias&quot;]

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
    ["sports", "documentary"]
)
```

Retorna itens comuns entre atributos de perfil e determinada lista de categorias.

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
        @event{myEvent.sport_interests}
)
```

Retorna itens comuns entre os atributos de perfil e o campo de evento especificado.

+++

## limite {#limit}

Retorna o primeiro ou o último elemento N de uma lista.

+++Sintaxe

`limit(<parameters>)`

+++

+++Parâmetros

| Parâmetro | Tipo | Descrição |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly ou listObject | Lista a ser considerada. Para listObject, ele deve ser uma referência de campo. |
| numberOfItems | inteiro | Número de itens a serem retornados da lista fornecida. |
| firstOrLastItems | booleano | Esse parâmetro é opcional (true por padrão). true retorna os primeiros itens. false retorna os últimos itens. |

+++

+++Assinatura e tipo retornado

`limit(<listString>,<integer>)`

`limit(<listString>,<integer>,<boolean>)`

Retorna uma lista de strings.

`limit(<listInteger>,<integer>)`

`limit(<listInteger>,<integer>,<boolean>)`

Retorna uma lista de inteiros.

`limit(<listDecimal>,<integer>)`

`limit(<listDecimal>,<integer>,<boolean>)`

Retorna uma lista de decimais.

`limit(<listBoolean>,<integer>)`

`limit(<listBoolean>,<integer>,<boolean>)`

Retorna uma lista de booleanos.

`limit(<listDateOnly>,<integer>)`

`limit(<listDateOnly>,<integer>,<boolean>)`

Retorna uma lista de datas.

`limit(<listDateTimeOnly>,<integer>)`

`limit(<listDateTimeOnly>,<integer>,<boolean>)`

Retorna uma lista de datetimes sem considerar o fuso horário.

`limit(<listDateTime>,integer>)`

`limit(<listDateTime>,<integer>,<boolean>)`

Retorna uma lista de datetimes.

`limit(<listDuration>,<integer>)`

`limit(<listDuration>,<integer>,<boolean>)`

Retorna uma lista de durações.

`limit(<listObject>,<integer>)`

`limit(<listObject>,<integer>,<boolean>)`

Retorna uma lista de objetos.

+++

+++Exemplos

`limit(["A", "B", "C", "D", "E"], 3)`

Retorna `["A","B","C"]`.

`limit(["A", "B", "C", "D", "E"], 3, false)`

Retorna `["C","D","E"]`.

+++

## listSize {#listSize}

Conta o número de elementos na lista.

+++Sintaxe

`listSize(<parameters>)`

+++

+++Parâmetros

| Parâmetro | Tipo | Descrição |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly ou listObject | Lista a processar. Para listObject, ele deve ser uma referência de campo. Um listObject não pode conter um objeto nulo. |

+++

+++Assinaturas e tipo retornado

`listSize(<listInteger>)`

`listSize(<listDecimal>)`

`listSize(<listString>)`

`listSize(<listBoolean>)`

`listSize(<listDateTimeOnly>)`

`listSize(<listDateTime>)`

`listSize(<listDateOnly>)`

`listSize(<listDuration>)`

Retorna um número inteiro.

`listSize(<listObject>)`

+++

+++Exemplos

`listSize([10,2,3])`

Retorna 3.

`listSize(@event{my_event.productListItems})`

Retorna o número de objetos na matriz de objetos fornecida (tipo listObject).

+++

## serializeList {#serializeList}

Converte uma determinada lista (qualquer tipo, exceto listObject) em uma cadeia de caracteres.

+++Sintaxe

`serializeList(<parameters>)`

+++

+++Parâmetros

| Parâmetro | Tipo | Descrição |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly | Lista para converter em uma cadeia de caracteres. |
| separador | sequência de caracteres | Separador entre cada elemento da lista na cadeia de caracteres de saída. |
| addQuotes | booleano | Esse parâmetro indica se cada elemento na string de saída deve incluir aspas (true) ou não (false). |

+++

+++Assinatura e tipo retornado

`serializeList(<listInteger>,<string>,<boolean>)`

`serializeList(<listDecimal>,<string>,<boolean>)`

`serializeList(<listString>,<string>,<boolean>)`

`serializeList(<listBoolean>,<string>,<boolean>)`

`serializeList(<listDateTimeOnly>,<string>,<boolean>)`

`serializeList(<listDateTime>,<string>,<boolean>)`

`serializeList(<listDateOnly>,<string>,<boolean>)`

`serializeList(<listDuration>,<string>,<boolean>)`

Retorna uma string.

+++

+++Exemplos

`serializeList(["Hello","World"], " ", false)`

Retorna &quot;Olá, Mundo&quot;.

`serializeList(["Hello", "World"], ",", true)`

Retorna &quot;&quot;Olá&quot;,&quot;Mundo&quot;&quot;.

+++

## sort {#sort}

Classifica uma lista de valores ou objetos na ordem natural.

+++Sintaxe

`sort(<parameters>)`

+++

+++Parâmetros

| Parâmetro | Tipo | Descrição |
|-----------|------------------|------------------|
| listToSort | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly ou listObject | Lista para classificar. Para listObject, ele deve ser uma referência de campo. |
| keyAttributeName | sequência de caracteres | Este parâmetro é somente para listObject. O nome do atributo nos objetos da lista fornecida é usado como chave para classificação. |
| sortingOrder | booleano | Crescente (verdadeiro) ou decrescente (falso) |

+++

+++Assinatura e tipo retornado

`sort(<listInteger>,<boolean>)`

Retorna uma lista de inteiros.

`sort(<listDecimal>,<boolean>)`

Retorna uma lista de decimais.

`sort(<listString>,<boolean>)`

Retorna uma lista de strings.

`sort(<listDateTimeOnly>,<boolean>)`

Retorna uma lista de datetimes sem considerar o fuso horário.

`sort(<listDateTime>,<boolean>)`

Retorna uma lista de datetimes.

`sort(<listDateOnly>,<boolean>)`

Retorna uma lista de datas.

`sort(<listBoolean>,<boolean>)`

Retorna uma lista de booleanos.

`sort(<listObject>,<string>,<boolean>)`

Retorna uma lista de objetos.

+++

+++Exemplos

`sort(["A", "C", "B"], true)`

Retorna `["A","B","C"]`.

`sort([1, 3, 2], false)`

Retorna `[3, 2, 1]`.

`sort(@event{my_event.productListItems}, "SKU", true)`

Retorna o listObject ordenado pelo atributo SKU (ordem crescente)

+++

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** esta página documenta todas as funções de lista disponíveis nas expressões de jornada do AJO, abordando como filtrar, classificar, desduplicar, verificar associação, limitar, serializar e encontrar interseções de listas e matrizes.

**Intenções:**
* Remover valores duplicados de uma lista usando `distinct` (ignorando nulos) ou `distinctWithNull` (preservando nulos)
* Filtrar um listObject para retornar somente objetos correspondentes a valores de chave específicos usando `filter`
* Recuperar um elemento em um índice específico de uma lista usando `getListItem`
* Verificar se existe um valor em uma lista usando `in`
* Encontrar elementos comuns entre duas listas usando `intersect`
* Retorna o primeiro ou o último N elementos de uma lista usando `limit`
* Contar o número total de elementos em uma lista usando `listSize`
* Converter uma lista em uma cadeia de caracteres delimitada usando `serializeList`
* Classificar uma lista em ordem crescente ou decrescente usando `sort`

**Glossário:**
* **listObject**: uma lista de objetos complexos que devem ser uma referência de campo; não pode conter objetos nulos *(específico do produto)*
* **keyAttributeName**: um parâmetro de cadeia opcional usado com `distinct`, `filter` e `sort` para identificar qual atributo de objeto usar para eliminação de duplicação, filtragem ou classificação *(específico do produto)*
* **interseção**: uma operação de conjunto que retorna somente os elementos presentes em ambas as listas de entrada

**Medidas de Proteção:**
* `distinctWithNull` não dá suporte ao tipo de parâmetro `<listObject>`
* `filter` requer que o parâmetro listObject seja uma referência de campo, não um literal embutido
* `listSize` em um listObject requer que a lista seja uma referência de campo; um listObject não pode conter objetos nulos
* `serializeList` não dá suporte ao tipo `listObject`

**Terminologia:**
* Nome canônico: funções de lista — Acrônimo: none — variantes: funções de coleção, funções de matriz
* Sinônimos: &quot;listSize&quot; = &quot;count list elements&quot;; &quot;serializeList&quot; = &quot;join list to string&quot;
* Não confunda: &quot;distinct&quot; (ignora nulos) ≠ &quot;distinctWithNull&quot; (preserva nulo como um valor distinto)
* Não confunda: &quot;limit&quot; com o terceiro parâmetro `true` (retorna os primeiros N itens) ≠ &quot;limit&quot; com `false` (retorna os últimos N itens)
* Não confunda: &quot;intersect&quot; (elementos comuns entre duas listas) ≠ &quot;filter&quot; (elementos que correspondem a valores de chave específicos)

**Perguntas frequentes:**
* **P: Como faço para obter os primeiros 3 itens de uma lista?** — Use `limit(myList, 3)` ou `limit(myList, 3, true)`; o padrão é retornar os primeiros itens.
* **P: Como obter os últimos 3 itens de uma lista?** — Use `limit(myList, 3, false)`.
* **P: Qual é a diferença entre `distinct` e `distinctWithNull`?** — `distinct` ignora valores nulos e os exclui do resultado; `distinctWithNull` trata nulo como um valor distinto e inclui uma entrada nula se houver nulos.
* **P: Posso filtrar uma lista de cadeias de caracteres com `filter`?** — Não, `filter` funciona somente em `listObject`; para listas escalares, use `in` ou `distinct` para desduplicação.
* **P: Como verificar se um valor está em uma lista?** — Use `in(value, myList)`, que retornará true se o valor for encontrado na lista.
* **P: Posso classificar um listObject por um atributo específico?** — Sim, use `sort(@event{...}, "attributeName", true)` onde o segundo parâmetro é o nome do atributo e o terceiro é a direção da classificação (true = crescente).

+++
