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
source-git-commit: dc1eeb3c199e7db2fc152b682404a547e2ae56c7
workflow-type: tm+mt
source-wordcount: '233'
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

1. Criar um [superfície](channel-surfaces.md) para o domínio e os IPs identificados para o seu plano de aquecimento.<!--how do you identify these or who does it at the customer level?-->

1. Criar um [campaign](../campaigns/create-campaign.md) e selecione o [E-mail](../email/create-email.md#create-email-journey-campaign) ação.

1. Selecione a superfície criada para aquecimento de IP.

   <!--You must use the same surface as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. Clique em **[!UICONTROL Criar]**.

1. No **[!UICONTROL Agendar]** , selecione **[!UICONTROL Ativação do plano de aquecimento de IP]**.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   A campanha [programação](../campaigns/create-campaign.md#schedule) será orientada pelo plano de aquecimento de IP ao qual será associado, o que significa que a programação não será mais definida na própria campanha.

1. [Ativar](../campaigns/review-activate-campaign.md) a campanha. Uma vez em funcionamento, ele estará pronto para uso em um plano de aquecimento de IP.

>[!NOTE]
>
>Para uma campanha ativa com o plano de aquecimento de IP ativado, a variável **[!UICONTROL Excluir]** estará disponível até ser associado a um plano de aquecimento de IP.

Para obter mais informações sobre como configurar uma campanha, consulte [esta página](../campaigns/get-started-with-campaigns.md).

