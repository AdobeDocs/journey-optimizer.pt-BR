---
product: journey optimizer
title: notEqualIgnoreCase
description: Saiba mais sobre a função notEqualIgnoreCase
feature: Journeys
role: Engineer
level: Experienced
keywords: notEqualIgnoreCase, função, expressão, jornada
exl-id: 74f8cae0-7d2f-4f5e-bc13-837c9bc69ad9
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
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

* sequência de caracteres

## Assinatura e tipo retornado

`notEqualIgnoreCase(<string>,<string>)`

Retorna um valor booleano.

## Exemplo

`notEqualIgnoreCase(@event{iOSPushPermissionAllowed.device.model}, "iPad")`
