---
solution: Journey Optimizer
product: journey optimizer
title: Ações do Adobe Campaign v7/v8
description: Saiba mais sobre as ações do Adobe Campaign v7/v8
feature: Actions
topic: Administration
role: Admin
level: Intermediate
keywords: jornada, integração, campaign, v7, v8, classic
exl-id: 3da712e7-0e08-4585-8ca4-b6ff79df0b68
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 28%

---

# Ações do Adobe Campaign v7/v8 {#using_campaign_classic}

Uma integração está disponível se você utilizar o Adobe Campaign v7 ou v8. Ele permitirá enviar emails, notificações por push e SMS usando recursos de mensagens transacionais do Adobe Campaign.

A conexão entre as instâncias do Journey Optimizer e do Campaign é configurada pela Adobe no momento do provisionamento. Adobe de contato.

Para que isso funcione, é necessário configurar uma ação dedicada. Consulte esta [seção](../action/acc-action.md).

Um caso de uso completo é apresentado neste [seção](../building-journeys/ajo-ac.md).

1. Projete sua jornada, começando com um evento. Consulte esta [seção](../building-journeys/journey.md).
1. No **Ação** da paleta, selecione uma ação de Campanha e adicione-a à jornada.
1. No **Parâmetros de ação**, todos os campos esperados na carga da mensagem são exibidos. Você precisa mapear cada um desses campos com o campo que deseja usar, seja do evento ou da fonte de dados. Isso é semelhante às ações personalizadas. Consulte esta [seção](../building-journeys/using-custom-actions.md).

![](assets/accintegration2.png)
