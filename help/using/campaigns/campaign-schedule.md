---
solution: Journey Optimizer
product: journey optimizer
title: Agendar a campanha de ação
description: Saiba como agendar a campanha de ação.
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: criar, otimizador, campanha, superfície, mensagens
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 1%

---


# Agendar a campanha de ação {#action-campaign-schedule}

Use a guia **[!UICONTROL Agendamento]** para definir o agendamento da campanha.

Por padrão, as campanhas de ação começam assim que são ativadas manualmente e terminam assim que a mensagem é enviada uma vez. Se você não quiser executar sua campanha logo após a ativação, poderá especificar uma data e hora em que a mensagem deverá ser enviada usando a opção **[!UICONTROL Início da campanha]**.

A opção **[!UICONTROL Campaign end]** permite especificar quando uma campanha deve parar de ser executada. Fora das datas especificadas, a campanha não será executada.

![](assets/create-campaign-schedule.png)

>[!NOTE]
>
>Ao agendar campanhas em [!DNL Adobe Journey Optimizer], verifique se a data/hora de início está alinhada com a primeira entrega desejada. Para campanhas recorrentes, se o horário agendado inicial já tiver passado, as campanhas serão transferidas para o próximo período disponível, de acordo com suas regras de recorrência.

Outras opções de agendamento estão disponíveis com base no canal de campanha:

* **Frequência** (email, SMS, ação por push)

  Você pode definir uma frequência na qual a mensagem da campanha deve ser enviada. Para fazer isso, use as opções **[!UICONTROL Action triggers]** na tela de criação da campanha para especificar se a campanha deve ser executada diariamente, semanalmente ou mensalmente.

* **Ativação do plano de aquecimento de IP** (Email)

  Para campanhas de Email, você pode criar campanhas específicas de ativação do plano de aquecimento de IP. O agendamento da campanha será orientado pelo plano de aquecimento de IP ao qual será associado, o que significa que o agendamento não será mais definido na própria campanha. [Saiba como criar campanhas de aquecimento de IP](../configuration/ip-warmup-campaign.md).

## Próximas etapas {#next}

Quando a programação da campanha estiver pronta, você poderá revisar e ativar a campanha. [Saiba mais](review-activate-campaign.md)
