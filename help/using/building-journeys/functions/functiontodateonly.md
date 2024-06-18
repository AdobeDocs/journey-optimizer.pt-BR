---
product: journey optimizer
title: toDateOnly
description: Saiba mais sobre a função toDateOnly
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toDateOnly, função, expressão, jornada
exl-id: 1929644f-8b51-4f95-aea5-627fc1dd115d
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 9%

---

# toDateOnly{#toDateOnly}

Converte um argumento em um valor de tipo dateOnly. Para saber mais sobre tipos de dados, consulte esta [seção](../expression/data-types.md).

## Categoria

Conversão

## Sintaxe da função

`toDateOnly(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| Representação em sequência de caracteres de uma data como &quot;AAAA-MM-DD&quot; (formato XDM). Também é compatível com o formato ISO-8601: somente **data completa** é considerada (consulte [RFC 3339, seção 5.6](https://www.rfc-editor.org/rfc/rfc3339#section-5.6) | sequência de caracteres |
| data e hora | dateTime |
| data hora sem fuso horário | dateTimeOnly |
| valor inteiro de uma época em milissegundos | inteiro |

## Assinaturas e tipos retornados

`toDateOnly(<dateTime>)`

`toDateOnly(<dateTimeOnly>)`

`toDateOnly(<string>)`

`toDateOnly(<integer>, <integer>, <integer>)`

Retorna um valor de tipo dateOnly.

## Exemplos

`toDateOnly("2023-08-18")`

`toDateOnly("2023-08-18T00:00:00.000Z")`

`toDateOnly("2023-08-18T00:00:00")`

todos retornam um objeto dateOnly representando 2023-08-18.

`toDateOnly(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate})`

Retorna um dateOnly.
