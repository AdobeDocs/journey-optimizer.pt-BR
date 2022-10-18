---
product: journey optimizer
title: toString
description: Saiba mais sobre a função toString
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 06727146-2a44-4b74-aac4-be60e9e0e37c
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '116'
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
| dateTime | converte a data em formato de data UTC |
| dateTimeOnly | converte a data em formato de data UTC |
| duration | converter no número correspondente de milissegundos como uma string |
| integer | converte em representação de string do valor (1 se torna &quot;1&quot;) |
| decimal | converte em representação de string do valor (1,5 se torna &quot;1,5&quot;) |
| booleano | converter o valor booleano como &#39;true&#39; se for verdadeiro, &#39;false&#39; se for falso |

## Assinaturas e tipo retornado

`toString(<dateTimeOnly>)`

`toString(<dateTime>)`

`toString(<duration>)`

`toString(<boolean>)`

`toString(<integer>)`

`toString(<decimal>)`

Retorne uma string.

## Exemplo

`toString(4)`

Retorna &quot;4&quot;.

`toString(#{ExperiencePlatform.test_date.person.birthDate}))`

Retorna a representação da string do campo dateOnly especificado (campo Data XDM), por exemplo &quot;2016-08-18&quot;.
