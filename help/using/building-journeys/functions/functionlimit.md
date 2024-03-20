---
product: journey optimizer
title: limite
description: Saiba mais sobre o limite de funções
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: limite, função, expressão, jornada
exl-id: 7fa1e393-2912-4392-b759-e54d08d5635a
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 7%

---

# limite {#limit}

Retorna o primeiro ou o último elemento N de uma lista.

## Categoria

Lista

## Sintaxe da função

`limit(<parameters>)`

## Parâmetros

| Parâmetro | Tipo | Descrição |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly ou listObject | Lista a ser considerada. Para listObject, ele deve ser uma referência de campo. |
| numberOfItems | inteiro | Número de itens a serem retornados da lista fornecida. |
| firstOrLastItems | booleano | Esse parâmetro é opcional (true por padrão). true retorna os primeiros itens. false retorna os últimos itens. |

## Assinatura e tipo retornado

`limit(<listString>,<integer>)`
`limit(<listString>,<integer>,<boolean>)`

Retorna uma lista de strings.

`limit(<listInteger>,<integer>)`
`limit(<listInteger>,<integer>,<boolean>)`

Retorna uma lista de inteiros.

`limit(<listDecimal>,<integer>)`
`limit(<listDecimal>,<integer>,<boolean>)`

Retorna uma lista de decimais.

`limit(<listBoolean>,<integer>)`
`limit(<listBoolean>,<integer>,<boolean>)`

Retorna uma lista de booleanos.

`limit(<listDateOnly>,<integer>)`
`limit(<listDateOnly>,<integer>,<boolean>)`

Retorna uma lista de datas.

`limit(<listDateTimeOnly>,<integer>)`
`limit(<listDateTimeOnly>,<integer>,<boolean>)`

Retorna uma lista de datetimes sem considerar o fuso horário.

`limit(<listDateTime>,integer>)`
`limit(<listDateTime>,<integer>,<boolean>)`

Retorna uma lista de datetimes.

`limit(<listDuration>,<integer>)`
`limit(<listDuration>,<integer>,<boolean>)`

Retorna uma lista de durações.

`limit(<listObject>,<integer>)`
`limit(<listObject>,<integer>,<boolean>)`

Retorna uma lista de objetos.

## Exemplo

`limit(["A", "B", "C", "D", "E"], 3)`

Devoluções `["A","B","C"]`.

`limit(["A", "B", "C", "D", "E"], 3, false)`

Devoluções `["C","D","E"]`.
