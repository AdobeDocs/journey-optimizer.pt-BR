---
product: journey optimizer
title: sort
description: Saiba mais sobre a classificação de função
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: sort, function, expression, jornada
exl-id: 607e1424-4165-48ae-b896-cce2d18f7dcc
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 7%

---

# sort {#sort}

Classifica uma lista de valores ou objetos na ordem natural.

>[!NOTE]
>
>Se a lista de destino for um listObject, essa função só poderá ser usada em expressões de ação personalizadas.

## Categoria

Lista

## Sintaxe da função

`sort(<parameters>)`

## Parâmetros

| Parâmetro | Tipo | Descrição |
|-----------|------------------|------------------|
| listToSort | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly ou listObject | Lista para classificar. Para listObject, ele deve ser uma referência de campo. |
| keyAttributeName | string | Este parâmetro é somente para listObject. O nome do atributo nos objetos da lista fornecida é usado como chave para classificação. |
| sortingOrder | booleano | Crescente (verdadeiro) ou decrescente (falso) |

## Assinatura e tipo retornado

`sort(<listInteger>,<boolean>)`

Retorna uma lista de inteiros.

`sort(<listDecimal>,<boolean>)`

Retorna uma lista de decimais.

`sort(<listString>,<boolean>)`

Retorna uma lista de strings.

`sort(<listDateTimeOnly>,<boolean>)`

Retorna uma lista de datetimes sem considerar o fuso horário.

`sort(<listDateTime>,<boolean>)`

Retorna uma lista de datetimes.

`sort(<listDateOnly>,<boolean>)`

Retorna uma lista de datas.

`sort(<listBoolean>,<boolean>)`

Retorna uma lista de booleanos.

`sort(<listObject>,<string>,<boolean>)`

Retorna uma lista de objetos.

## Exemplo

`sort(["A", "C", "B"], true)`

Devoluções `["A","B","C"]`.

`sort([1, 3, 2], false)`

Devoluções `[3, 2, 1]`.

