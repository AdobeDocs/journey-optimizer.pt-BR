---
product: adobe campaign
title: replaceAll
description: Saiba mais sobre a função replaceAll
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 16%

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
| target | string |
| substituição | string |

## Assinatura e tipo retornado

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

Retorna uma string.

## Exemplo

`replaceAll("Hello World", "l", "x")`

Retorna &quot;Hexxo Worxd&quot;.
