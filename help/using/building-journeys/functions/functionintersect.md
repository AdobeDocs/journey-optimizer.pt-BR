---
product: journey optimizer
title: interseção
description: Saiba mais sobre a interseção de funções
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: interseção, função, expressão, jornada
exl-id: e236efa9-91a8-4f08-94c6-45f1e060bb2f
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 12%

---

# interseção{#intersect}

Retorna os valores comuns nas duas listas de entrada. Se uma das duas listas for nula, retornará uma lista vazia.

## Categoria

Lista

## Sintaxe da função

`intersect(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| lista 1 | listar |
| lista 2 | listar |

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

Devoluções [&quot;esportes&quot;, &quot;notícias&quot;]

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
    ["sports", "news", "documentary"]
)
```

Retorna itens comuns entre atributos de perfil e uma determinada lista de categorias.

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
        @{myEvent.sport_interests}
)
```

Retorna itens comuns entre atributos de perfil e determinado campo de evento.
