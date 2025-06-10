---
product: journey optimizer
title: interseção
description: Saiba mais sobre a interseção de funções
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: interseção, função, expressão, jornada
exl-id: e236efa9-91a8-4f08-94c6-45f1e060bb2f
source-git-commit: 49c3fd09d23e6394b6eff8ba4da71ed7bab8c82c
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 11%

---

# interseção{#intersect}

Retorna os valores comuns nas duas listas de entrada. Se uma das duas listas for nula, retorna uma lista vazia.

## Categoria

Lista

## Sintaxe da função

`intersect(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| lista 1 | list |
| lista 2 | list |

## Assinaturas e tipos retornados

`intersect(listString,listString)`: listString
`intersect(listDecimal,listDecimal)`: listDecimal
`intersect(listInteger,listInteger)`: listInteger
`intersect(listDateTime,listDateTime)`: listDateTime
`intersect(listDateTimeOnly,listDateTimeOnly)`: listDateTimeOnly
`intersect(listDateOnly,listDateOnly)`: listDateOnly
`intersect(listDuration,listDuration)`: listDuration
`intersect(listBoolean,listBoolean)`: listBoolean

Retorna uma lista.

## Exemplos

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
