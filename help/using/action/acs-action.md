---
solution: Journey Optimizer
product: journey optimizer
title: Integrar ao Adobe Campaign Standard
description: Saiba como integrar o Journey Optimizer ao Adobe Campaign Standard
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate
keywords: campaign, standard, integration, capping, action
exl-id: 2f0218c9-e1b1-44ba-be51-15824b9fc6d2
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 3%

---

# Integrar ao Adobe Campaign Standard {#using_adobe_campaign_standard}

Você pode enviar emails, notificações por push e SMS usando os recursos de Mensagens transacionais do Adobe Campaign Standard.

Se você tiver o Adobe Campaign Standard, uma ação integrada estará disponível para permitir a conexão com o Adobe Campaign Standard.

A mensagem transacional Campaign Standard e o evento associado devem ser publicados para serem usados no Journey Optimizer. Se o evento for publicado, mas a mensagem não for, ele não estará visível na interface do Journey Optimizer. Se a mensagem for publicada, mas o evento associado não, ela ficará visível na interface do Journey Optimizer, mas não poderá ser usada.

## Observações importantes {#important-notes}

* Uma regra de limitação de 4.000 chamadas a cada 5 minutos é definida automaticamente para ações do Adobe Campaign Standard. Isso corresponde à escala oficial das Mensagens transacionais do Adobe Campaign Standard. Leia mais sobre os SLAs de mensagens transacionais em [Descrição do produto Adobe Campaign Standard](https://helpx.adobe.com/br/legal/product-descriptions/campaign-standard.html).

* A integração do Adobe Campaign Standard é configurada por meio de uma ação incorporada dedicada na lista de ações. Isso precisa ser configurado para cada sandbox.

* Não é possível usar uma ação Campaign Standard com uma atividade de qualificação de Público-alvo ou Ler público.

* Uma jornada não pode usar mensagens e ações Campaign Standard.

## Configuração da ação {#configure-action}

Estas são as etapas para configurá-la:

1. Selecione **[!UICONTROL Configurações]** na seção de menu ADMINISTRAÇÃO. Na seção **[!UICONTROL Ações]**, clique em **[!UICONTROL Gerenciar]**. A lista de ações é exibida.

1. Selecione a ação **[!UICONTROL AdobeCampaignStandard]** interna. O painel de configuração de ação é aberto no lado direito da tela.

   ![](assets/actioncampaign.png)

1. Copie a URL da instância do Adobe Campaign Standard e cole no campo **[!UICONTROL URL]**.

1. Clique em **[!UICONTROL Testar o URL da instância]** para testar a validade da instância.

   >[!NOTE]
   >
   >Este teste verifica se:
   >
   >O host é &quot;.campaign.adobe.com&quot;, &quot;.campaign-sandbox.adobe.com&quot;, &quot;.campaign-demo.adobe.com&quot;, &quot;.ats.adobe.com&quot; ou &quot;.adls.adobe.com&quot;.
   >
   >O URL começa com https,
   >
   >A ORG associada a essa instância do Adobe Campaign Standard é a mesma ORG do Journey Optimizer.

Ao criar sua jornada, três ações estarão disponíveis na categoria **[!UICONTROL Ação]**: **[!UICONTROL Email]**, **[!UICONTROL Push]**, **[!UICONTROL SMS]** (consulte [Usar ações do Adobe Campaign](../building-journeys/using-adobe-campaign-standard.md)).

![](assets/journey58.png)

Você pode usar um evento **Reações** para reagir a dados de rastreamento relacionados a uma mensagem de Campaign Standard enviada na mesma jornada. Para notificações por push, você pode reagir a mensagens clicadas, enviadas ou com falha. Para mensagens SMS, você pode reagir a mensagens enviadas ou com falha. Para emails, você pode reagir a mensagens clicadas, enviadas, abertas ou com falha. Consulte [Reações e eventos](../building-journeys/reaction-events.md).

Se você estiver usando um sistema de terceiros para enviar mensagens, será necessário adicionar e configurar uma ação personalizada. Consulte [Sobre a configuração de ação personalizada](../action/about-custom-action-configuration.md).