---
product: adobe campaign
title: toDateOnly
description: Saiba mais sobre a função toDateOnly
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 1929644f-8b51-4f95-aea5-627fc1dd115d
source-git-commit: cca94d15da5473aa9890c67af7971f2e745d261e
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 9%

---

# toDateOnly{#toDateOnly}

Converte um argumento em um valor de tipo dateOnly. Para saber mais sobre tipos de dados, consulte esta seção [seção](../expression/data-types.md).

## Categoria

Conversão

## Sintaxe da função

`toDateOnly(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| Representação de string de uma data como &quot;AAAA-MM-DD&quot; (formato XDM). Também suporta o formato ISO-8601: only **data completa** parte é considerada (consulte [RFC 3339, seção 5.6](https://www.rfc-editor.org/rfc/rfc3339#section-5.6) | string |
| data e hora | dateTime |
| data e hora sem fuso horário | dateTimeOnly |
| valor inteiro de uma época em milissegundos | integer |

## Assinaturas e tipos retornados

`toDateOnly(<dateTime>)`

`toDateOnly(<dateTimeOnly>)`

`toDateOnly(<string>)`

`toDateOnly(<integer>, <integer>, <integer>)`

Retorna um valor do tipo dateOnly .

## Exemplos

`toDateOnly("2016-08-18")`

`toDateOnly("2016-08-18T00:00:00.000Z")`

`toDateOnly("2016-08-18T00:00:00")`

todos retornam um objeto dateOnly representando 2016-08-18.

`toDateOnly(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate})`

Retorna dateOnly.
