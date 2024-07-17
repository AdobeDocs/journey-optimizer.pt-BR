---
product: journey optimizer
title: replace
description: Saiba mais sobre a substituição de função
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: replace, function, expression, jornada
exl-id: 3eb35fd6-2d11-4f24-b0d9-5334e7ed7872
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 11%

---

# replace {#replace}

Substitui a primeira ocorrência correspondente à string de destino pela string de substituição na string de base.

A substituição continua do início da string até o fim. Por exemplo, substituir &quot;aa&quot; por &quot;b&quot; na string &quot;aaa&quot; resultará em &quot;ba&quot; em vez de &quot;ab&quot;.

## Categoria

String

## Sintaxe da função

`replace(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|--------------|
| base | sequência de caracteres |
| público-alvo | string (RegExp) |
| substituição | sequência de caracteres |

## Assinatura e tipo retornado

`replace(<base>,<target>,<replacement>)`

Retorna uma string.

## Exemplo 1

`replace("Hello World", "l", "x")`

Retorna &quot;Hexlo World&quot;.

## Exemplo 2 {#example_2}

Como o parâmetro de destino é um RegExp, dependendo da cadeia de caracteres que você deseja substituir, talvez seja necessário usar escape em alguns caracteres. Exemplo:

* cadeia de caracteres a ser avaliada: `|OFFER_A|OFFER_B`
* fornecido por um atributo de perfil `#{ExperiencePlatform.myFieldGroup.profile.myOffers}`
* Cadeia de caracteres a ser substituída: `|OFFER_A`
* Cadeia de caracteres substituída por: `''`
* É necessário adicionar `\\` antes do caractere `|`.

A expressão é:

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|OFFER_A', '')`

A cadeia de caracteres retornada é: `|OFFER_B`

Também é possível criar a cadeia de caracteres a ser substituída a partir de um determinado atributo:

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|' + #{ExperiencePlatform.myFieldGroup.profile.myOfferCode}, '')`
