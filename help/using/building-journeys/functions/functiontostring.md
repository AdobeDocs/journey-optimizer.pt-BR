---
product: journey optimizer
title: toString
description: Saiba mais sobre a função toString
feature: Journeys
role: Developer
level: Experienced
keywords: toString, função, expressão, jornada
exl-id: 06727146-2a44-4b74-aac4-be60e9e0e37c
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 7%

---

# toString {#toString}

Converte um valor de argumento em um valor de string, dependendo de seu tipo. Para obter mais informações sobre tipos de dados, consulte [esta página](../expression/data-types.md).

## Categoria

Conversão

## Sintaxe da função

`toString(<parameter>)`

## Parâmetros

| Parâmetro | Descrição |
|--- |--- |
| dateTime | converte a data no formato de data UTC |
| dateTimeOnly | converte a data no formato de data UTC |
| duração | converta para o número correspondente de milissegundos como uma string |
| inteiro | converte para representação em string do valor (1 torna-se &quot;1&quot;) |
| decimal | converte para representação em string do valor (1,5 torna-se &quot;1,5&quot;) |
| booleano | converta o valor booleano como &#39;true&#39; se verdadeiro, &#39;false&#39; se falso |

## Assinaturas e tipo retornado

`toString(<dateTimeOnly>)`

`toString(<dateTime>)`

`toString(<duration>)`

`toString(<boolean>)`

`toString(<integer>)`

`toString(<decimal>)`

Retorna uma string.

## Exemplo

`toString(4)`

Retorna &quot;4&quot;.

`toString(#{ExperiencePlatform.test_date.person.birthDate}))`

Retorna a representação da string do campo dateOnly fornecido (campo XDM Date), por exemplo &quot;2023-08-18&quot;.

`toString(toDuration(1520))`

Retorna &quot;PT1.52S&quot;.
