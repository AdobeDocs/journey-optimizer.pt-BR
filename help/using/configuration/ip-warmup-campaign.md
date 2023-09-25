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
source-git-commit: 1ec2c406e777e08de97c3ad53cee5986afeb3c44
workflow-type: tm+mt
source-wordcount: '344'
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

Antes de criar o plano de aquecimento de IP em si [!DNL Journey Optimizer], primeiro é necessário criar uma ou mais campanhas com a opção dedicada ativada para que elas possam ser usadas em um plano de aquecimento de IP.

Para criar uma campanha de aquecimento de IP, siga as etapas abaixo.

1. Criar um [email](../email/email-settings.md) channel [superfície](channel-surfaces.md) para o domínio e os IPs identificados para o seu plano de aquecimento.

   >[!NOTE]
   >
   >Saiba como selecionar o domínio e os IPs a serem usados em uma superfície de email no [nesta seção](../email/email-settings.md#subdomains-and-ip-pools).
   >
   >Se necessário, trabalhe com seu consultor de entrega para identificar o domínio e os IPs a serem usados para seu plano de aquecimento de IP.<!--TBC-->

1. Criar um [campaign](../campaigns/create-campaign.md) e selecione o [E-mail](../email/create-email.md#create-email-journey-campaign) ação.

1. Selecione a superfície criada para aquecimento de IP.

   ![](assets/ip-warmup-campaign-surface.png)

   <!--You must use the same surface as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. Clique em **[!UICONTROL Criar]**.

1. No **[!UICONTROL Agendar]** , selecione **[!UICONTROL Ativação do plano de aquecimento de IP]**.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   A campanha [programação](../campaigns/create-campaign.md#schedule) será orientada pelo plano de aquecimento de IP ao qual será associado, o que significa que a programação não será mais definida na própria campanha.

1. Conclua as etapas para criar uma campanha de email, como definir as propriedades da campanha, [público](../audience/about-audiences.md)<!--best practices for IP warmup in terms of audience?-->, e [conteúdo](../email/get-started-email-design.md#key-steps).

   >[!NOTE]
   >
   >Para obter mais informações sobre como configurar uma campanha, consulte [esta página](../campaigns/get-started-with-campaigns.md).

1. [Ativar](../campaigns/review-activate-campaign.md) a campanha.

   >[!NOTE]
   >
   >Para uma campanha ativa com o plano de aquecimento de IP ativado, a variável **[!UICONTROL Excluir]** estará disponível até ser associado a um plano de aquecimento de IP. Depois de usada em um plano de aquecimento de IP, a campanha não pode mais ser excluída.

1. A campanha é exibida na janela **[!UICONTROL Campanhas]** lista. Para recuperar facilmente todas as campanhas de aquecimento de IP criadas na sandbox atual, você pode filtrar na opção de campanha **[!UICONTROL Aquecimento de IP]**.

   ![](assets/ip-warmup-campaign-filter.png)

Uma vez ativa, a campanha estará pronta para uso em um plano de aquecimento de IP. [Saiba mais](ip-warmup-plan.md)

<!--Any recommendations when defining an audience? i.e do you have to include all your database or a limited number or according to your Excel file?-->

