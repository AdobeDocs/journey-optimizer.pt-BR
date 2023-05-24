---
product: journey optimizer
title: toString
description: Saiba mais sobre a função toString
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toString, função, expressão, jornada
exl-id: 06727146-2a44-4b74-aac4-be60e9e0e37c
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 8%

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

Retorna a representação da string do campo dateOnly fornecido (campo XDM Date), por exemplo &quot;2016-08-18&quot;.
