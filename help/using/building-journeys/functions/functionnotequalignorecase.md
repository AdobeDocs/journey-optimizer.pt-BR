---
product: journey optimizer
title: notEqualIgnoreCase
description: Saiba mais sobre a função notEqualIgnoreCase
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: notEqualIgnoreCase, função, expressão, jornada
exl-id: 74f8cae0-7d2f-4f5e-bc13-837c9bc69ad9
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '41'
ht-degree: 12%

---

# notEqualIgnoreCase {#notEqualIgnoreCase}

Verifique se a primeira string do argumento com a segunda string do argumento é diferente, ignorando as considerações sobre maiúsculas e minúsculas.

## Categoria

String

## Sintaxe da função

`notEqualIgnoreCase(<parameters>)`

## Parâmetros

* string

## Assinatura e tipo retornado

`notEqualIgnoreCase(<string>,<string>)`

Retorna um valor booleano.

## Exemplo

`notEqualIgnoreCase(@event{iOSPushPermissionAllowed.device.model}, "iPad")`
