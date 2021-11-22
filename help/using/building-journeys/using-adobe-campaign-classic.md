---
title: Ações do Adobe Campaign v7/v8
description: Saiba mais sobre as ações do Adobe Campaign v7/v8
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 3da712e7-0e08-4585-8ca4-b6ff79df0b68
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 11%

---

# Ações do Adobe Campaign v7/v8 {#using_campaign_classic}

Uma integração está disponível se você tiver o Adobe Campaign v7 ou v8. Ele permitirá enviar emails, notificações por push e SMS usando os recursos de Mensagens transacionais do Adobe Campaign.

A conexão entre as instâncias do Journey Optimizer e do Campaign é configurada pelo Adobe no momento do provisionamento. Entre em contato com o Adobe.

Para que isso funcione, é necessário configurar uma ação dedicada. Consulte esta [seção](../action/acc-action.md).

Um caso de uso completo é apresentado nesta [seção](../building-journeys/campaign-classic-use-case.md).

1. Projete a jornada, começando por um evento. Veja isso [seção](../building-journeys/journey.md).
1. No **Ação** da paleta, selecione uma ação Campanha e adicione-a à jornada.
1. No **Parâmetros de ação**, todos os campos esperados no payload da mensagem são exibidos. Você precisa mapear cada um desses campos com o campo que deseja usar, do evento ou da fonte de dados. Isso é semelhante às ações personalizadas. Consulte esta [seção](../building-journeys/using-custom-actions.md).

![](../assets/accintegration2.png)
