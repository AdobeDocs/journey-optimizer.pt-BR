---
product: adobe campaign
title: notEqualIgnoreCase
description: Saiba mais sobre a função notEqualIgnoreCase
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '37'
ht-degree: 13%

---

# notEqualIgnoreCase {#notEqualIgnoreCase}

Verifique se a primeira string de argumento com a segunda string de argumento é diferente, ignorando considerações de caso.

## Categoria

String

## Sintaxe da função

`notEqualIgnoreCase(<parameters>)`

## Parâmetros

* string

## Assinatura e tipo retornado

`notEqualIgnoreCase(<string>,<string>)`

Retorna um booleano.

## Exemplo

`notEqualIgnoreCase(@{iOSPushPermissionAllowed.device.model}, "iPad")`
