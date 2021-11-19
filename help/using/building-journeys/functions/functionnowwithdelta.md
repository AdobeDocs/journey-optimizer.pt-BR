---
product: adobe campaign
title: nowWithDelta
description: Saiba mais sobre a função nowWithDelta
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 7%

---

# nowWithDelta {#nowWithDelta}

Retorna a data e hora atual, incluindo um deslocamento. Se um ID de fuso horário for especificado, o deslocamento de fuso horário será aplicado. Para obter mais informações sobre tipos de dados, consulte [esta página](../expression/data-types.md).

## Categoria

Data 

## Sintaxe da função

`nowWithDelta(<parameters>)`

## Parâmetros

| Parâmetro | Descrição |
|--- |--- |
| delta | valor inteiro positivo ou negativo |
| parte da data | anos, meses, dias, horas, minutos ou segundos como uma string |
| id de fuso horário | representação de string do valor de fuso horário. Para obter mais informações, consulte [Tipos de dados](../expression/data-types.md). A ID de fuso horário deve ser uma constante de string. Não pode ser uma referência de campo nem uma expressão. |

## Assinaturas e tipo retornado

`nowWithDelta(<delta>,<date part>`

`nowWithDelta(<delta>,<date part>,"<timeZone id>")`

Retorna dateTime.

## Exemplos

`nowWithDelta(-2, "hours")`

`nowWithDelta(-2, "hours", "Europe/Paris")`

Retorna dateTime exatamente 2 horas atrás.
