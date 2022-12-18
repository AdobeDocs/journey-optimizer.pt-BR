---
solution: Journey Optimizer
product: journey optimizer
title: Ações do Adobe Campaign v7/v8
description: Saiba mais sobre as ações do Adobe Campaign v7/v8
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 3da712e7-0e08-4585-8ca4-b6ff79df0b68
source-git-commit: f6db4f7cbb1951c009fa7915f340da96eea74120
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 18%

---

# Ações do Adobe Campaign v7/v8 {#using_campaign_classic}

Uma integração está disponível se você utilizar o Adobe Campaign v7 ou v8. Ele permitirá enviar emails, notificações por push e SMS usando os recursos de Mensagens transacionais do Adobe Campaign.

A conexão entre as instâncias do Journey Optimizer e do Campaign é configurada pelo Adobe no momento do provisionamento. Entre em contato com o Adobe.

Para que isso funcione, é necessário configurar uma ação dedicada. Consulte esta [seção](../action/acc-action.md).

Um caso de uso completo é apresentado nesta [seção](../building-journeys/ajo-ac.md).

1. Projete a jornada, começando por um evento. Veja isso [seção](../building-journeys/journey.md).
1. No **Ação** da paleta, selecione uma ação Campanha e adicione-a à jornada.
1. No **Parâmetros de ação**, todos os campos esperados no payload da mensagem são exibidos. Você precisa mapear cada um desses campos com o campo que deseja usar, do evento ou da fonte de dados. Isso é semelhante às ações personalizadas. Consulte esta [seção](../building-journeys/using-custom-actions.md).

![](assets/accintegration2.png)
