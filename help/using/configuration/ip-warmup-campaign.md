---
solution: Journey Optimizer
product: journey optimizer
title: Criar campanhas de aquecimento de IP
description: Saiba como criar uma campanha de aquecimento de IP
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, pools, grupo, subdomínios, capacidade de entrega
hide: true
hidefromtoc: true
source-git-commit: ea86d44f7c9309ff69877e01cea6a13e7907a039
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 3%

---

# Criar campanhas de aquecimento de IP {#create-ip-warmup-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_ip_warmup"
>title="Ativar a opção de plano de aquecimento de IP"
>abstract="Selecione a opção de ativação do plano de aquecimento de IP. Quando a campanha estiver ativa, ela poderá ser associada a um plano de aquecimento de IP."

>[!BEGINSHADEBOX]

O que há neste guia de documentação:

* [Introdução ao aquecimento de IP](ip-warmup-gs.md)
* **[Criar campanhas de aquecimento de IP](ip-warmup-campaign.md)**
* [Criar um plano de aquecimento de IP](ip-warmup-plan.md)
* [Executar o plano de aquecimento de IP](ip-warmup-running.md)

>[!ENDSHADEBOX]

É necessário criar uma ou mais campanhas com uma opção específica ativada para que elas possam ser usadas em um plano de aquecimento de IP.

Para criar uma campanha de aquecimento de IP, siga as etapas abaixo.

1. Criar um email [superfície](channel-surfaces.md) para o domínio e os IPs identificados para o seu plano de aquecimento.<!--how do you identify these or who does it at the customer level?-->

   >[!NOTE]
   >
   >Saiba como selecionar o domínio e os IPs a serem usados em uma superfície de email no [nesta seção](../email/email-settings.md#subdomains-and-ip-pools).

1. Criar um [campaign](../campaigns/create-campaign.md) e selecione o [E-mail](../email/create-email.md#create-email-journey-campaign) ação.

1. Selecione a superfície criada para aquecimento de IP.

   ![](assets/ip-warmup-campaign-surface.png)

   <!--You must use the same surface as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. Clique em **[!UICONTROL Criar]**.

1. No **[!UICONTROL Agendar]** , selecione **[!UICONTROL Ativação do plano de aquecimento de IP]**.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   A campanha [programação](../campaigns/create-campaign.md#schedule) será impulsionado pela [Plano de aquecimento de IP](ip-warmup-plan.md) ele será associado a, o que significa que o agendamento não será mais definido na própria campanha.

1. [Ativar](../campaigns/review-activate-campaign.md) a campanha. Uma vez em funcionamento, ele estará pronto para uso em um plano de aquecimento de IP.

>[!NOTE]
>
>Para uma campanha ativa com o plano de aquecimento de IP ativado, a variável **[!UICONTROL Excluir]** estará disponível até ser associado a um plano de aquecimento de IP.

Para obter mais informações sobre como configurar uma campanha, consulte [esta página](../campaigns/get-started-with-campaigns.md).

<!--Any recommendations when defining an audience? i.e do you have to include all your database or a limited number or according to your Excel file?-->

