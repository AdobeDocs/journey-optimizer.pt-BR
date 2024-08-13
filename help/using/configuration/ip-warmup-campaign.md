---
solution: Journey Optimizer
product: journey optimizer
title: Criar campanhas de aquecimento de IP
description: Saiba como criar uma campanha de aquecimento de IP
feature: Campaigns, IP Warmup Plans
topic: Administration
role: Admin
level: Intermediate
keywords: IP, pools, capacidade de entrega
exl-id: a9995ca1-d7eb-4f8d-a9d9-fe56198ac325
source-git-commit: bdd3b951e44adaf3ff362b8af69f5ab74d13f484
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 12%

---

# Criar campanhas de aquecimento de IP {#create-ip-warmup-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_ip_warmup"
>title="Opção Ativar o plano de aquecimento de IP"
>abstract="Ao selecionar essa opção, a campanha pode ser usada em um plano de aquecimento de IP. A programação da campanha será determinada pelo plano de aquecimento de IP ao qual está associada."

Antes de criar o plano de aquecimento de IP em si no [!DNL Journey Optimizer], primeiro é necessário criar uma ou mais campanhas especificamente projetadas para uso em um plano de aquecimento de IP<!--through a dedicated option-->.

Para criar uma campanha de aquecimento de IP, siga as etapas abaixo.

1. Crie um [email](../email/email-settings.md) canal [superfície](channel-surfaces.md) para o domínio e os IPs identificados para o seu plano de aquecimento.

   >[!NOTE]
   >
   >* Saiba como selecionar o domínio e os IPs a serem usados em uma superfície de email no [nesta seção](../email/email-settings.md#subdomains-and-ip-pools).
   >
   >* Trabalhe com seu consultor de entrega para identificar o domínio e os IPs a serem usados para seu plano de aquecimento de IP.<!--TBC-->

1. Crie uma [campanha](../campaigns/create-campaign.md) de marketing agendado e selecione a ação [Email](../email/create-email.md#create-email-journey-campaign).

   <!--Select the Marketing category. The IP warmup plan activation option is only available for  marketing-type campaigns.-->

1. Selecione a superfície criada para aquecimento de IP.

   ![](assets/ip-warmup-campaign-surface.png)

   <!--You must use the same surface as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. Clique em **[!UICONTROL Criar]**.

1. Na seção **[!UICONTROL Agendar]**, selecione **[!UICONTROL Ativação do plano de aquecimento de IP]**.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   A campanha [agenda](../campaigns/create-campaign.md#schedule) será orientada pelo plano de aquecimento de IP ao qual será associada, o que significa que a agenda não está mais definida na própria campanha.

1. Conclua as etapas para criar uma campanha de email, como definir as propriedades da campanha, [público](../audience/about-audiences.md)<!--best practices for IP warmup in terms of audience?--> e [conteúdo](../email/get-started-email-design.md#key-steps).

   Observe que é necessário selecionar um público-alvo com base em regras para sua campanha de aquecimento de IP. [Saiba mais](../audience/creating-a-segment-definition.md)

   Para obter mais informações sobre como configurar uma campanha, consulte [esta página](../campaigns/get-started-with-campaigns.md).

1. [Ativar](../campaigns/review-activate-campaign.md) a campanha. Seu status muda para **[!UICONTROL Live]**.

   Observe que as regras de negócios não devem ser usadas no plano de aquecimento de IP. A aplicação dessas regras pode impedir que se atinja o número desejado de perfis direcionados para campanhas.

   Para uma campanha ativa com o plano de aquecimento de IP ativado, o botão **[!UICONTROL Excluir]** estará disponível até ser associado a um plano de aquecimento de IP. Depois de usada em um plano, a campanha não pode mais ser excluída.

1. A campanha é exibida na lista **[!UICONTROL Campanhas]**. Para recuperar facilmente todas as campanhas de aquecimento de IP criadas na sandbox atual, você pode filtrar na opção de campanha **[!UICONTROL Warmup de IP]**.

   ![](assets/ip-warmup-campaign-filter.png)

Uma vez ativa, a campanha estará pronta para uso em um plano de aquecimento de IP. [Saiba mais](ip-warmup-plan.md)

Uma campanha de aquecimento de IP só pode ser usada em um plano de aquecimento de IP. No entanto, a mesma campanha pode ser usada em uma ou mais fases do mesmo plano de aquecimento de IP. [Saiba mais](ip-warmup-plan.md#define-phases)

>[!NOTE]
>
>Quando uma campanha em tempo real é usada em um plano de aquecimento de IP, depois que o plano é [marcado como concluído](ip-warmup-execution.md#mark-as-completed), o status dessa campanha muda para **[!UICONTROL Parado]**.

