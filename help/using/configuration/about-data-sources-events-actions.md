---
title: Administração e configurações
description: Saiba mais sobre administração e diretrizes de configurações
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Configurações do aplicativo
topic: Administração
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 19%

---

# Configurar jornadas

Para enviar mensagens com o jornada, você precisa configurar **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** e **[!UICONTROL Actions]**.

![](../assets/admin-menu.png)

## Fontes de dados

A configuração da Fonte de Dados permite definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas. [Saiba mais](../../using/datasource/about-data-sources.md)

## Eventos

Os eventos permitem acionar as jornadas de forma unitária para enviar mensagens, em tempo real, ao indivíduo que flui para a jornada.

Na configuração do evento, configure os eventos esperados nas jornadas. Os dados de entrada dos eventos são normalizados de acordo com o Adobe Experience Data Model (XDM). Os eventos vêm das APIs de assimilação de streaming para eventos autenticados e não autenticados (como eventos do Adobe Mobile SDK). [Saiba mais](../../using/event/about-events.md)

## Ações

Os recursos de mensagem do Journey Optimizer são incorporados: você só precisa criar o conteúdo e publicar a mensagem. Se você estiver usando um sistema de terceiros para enviar mensagens, é possível criar uma ação personalizada. [Saiba mais](../../using/action/action.md)
