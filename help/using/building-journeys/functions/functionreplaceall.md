---
product: adobe campaign
title: replaceAll
description: Saiba mais sobre a função replaceAll
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 5543e123-a5f4-4153-8709-97eeb9be83ba
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 10%

---

# replaceAll {#replaceAll}

Substitui todas as ocorrências que correspondem à string de destino pela string de substituição na string base.

A substituição prossegue do início da string para o final, por exemplo, a substituição de &quot;aa&quot; por &quot;b&quot; na string &quot;aaa&quot; resultará em &quot;ba&quot; em vez de &quot;ab&quot;.

## Categoria

String

## Sintaxe da função

`replaceAll(<parameters>)`

## Parâmetros

| Parâmetro | Tipo |
|-----------|--------------|
| base | string |
| target | string (RegExp) |
| substituição | string |

## Assinatura e tipo retornado

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

Retorna uma string.

## Exemplo{#example}

`replaceAll("Hello World", "l", "x")`

Retorna &quot;Hexxo Worxd&quot;.

Como o parâmetro de destino é RegExp, dependendo da string que você deseja substituir, talvez seja necessário evitar alguns caracteres. Consulte o exemplo em [esta página](../functions/functionreplace.md#example_2).
