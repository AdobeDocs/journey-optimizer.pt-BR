---
solution: Journey Optimizer
product: journey optimizer
title: Integrar ao Adobe Campaign Standard
description: Saiba como fazer a integração com o Adobe Campaign Standard
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 2f0218c9-e1b1-44ba-be51-15824b9fc6d2
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 5%

---

# Integrar ao Adobe Campaign Standard {#using_adobe_campaign_standard}

Você pode enviar emails, notificações por push e SMS usando os recursos de Mensagens transacionais da Adobe Campaign Standard.

Se você tiver o Adobe Campaign Standard, uma ação incorporada estará disponível para permitir a conexão com o Adobe Campaign Standard.

A mensagem transacional do Campaign Standard e seu evento associado devem ser publicados para serem usados no Journey Optimizer. Se o evento for publicado, mas a mensagem não for , ele não estará visível na interface do Journey Optimizer. Se a mensagem for publicada, mas o evento associado não for , ela estará visível na interface do Journey Optimizer, mas não poderá ser usada.

## Observações importantes {#important-notes}

* Uma regra de limitação de 4000 chamadas por 5 minutos é automaticamente definida para ações do Adobe Campaign Standard. Isso corresponde à escala oficial do Adobe Campaign Standard Transactional Messaging. Leia mais sobre SLAs de mensagens transacionais em [Descrição do produto Adobe Campaign Standard](https://helpx.adobe.com/legal/product-descriptions/campaign-standard.html).

* A integração do Adobe Campaign Standard é configurada por meio de uma ação incorporada dedicada na lista de ações. Isso precisa ser configurado para cada sandbox.

* Não é possível usar uma Campaign Standard action com uma qualificação de segmento ou atividade de segmento de Leitura.

* Uma jornada não pode usar as ações Mensagens e Campaign Standard.

## Configurar a ação {#configure-action}

Estas são as etapas para configurá-lo:

1. Selecionar **[!UICONTROL Configurações]** na seção do menu ADMINISTRATION. No  **[!UICONTROL Ações]** seção , clique em **[!UICONTROL Gerenciar]**. A lista de ações é exibida.

1. Selecione o **[!UICONTROL AdobeCampaignStandard]** ação. O painel de configuração de ação é aberto no lado direito da tela.

   ![](assets/actioncampaign.png)

1. Copie o URL da instância do Adobe Campaign Standard e cole-o no **[!UICONTROL URL]** campo.

1. Clique no botão **[!UICONTROL Teste o URL da instância]** para testar a validade da instância.

   >[!NOTE]
   >
   >Este teste verifica se:
   >
   >O host é &quot;.campaign.adobe.com&quot;, &quot;.campaign-sandbox.adobe.com&quot;, &quot;.campaign-demo.adobe.com&quot;, &quot;.ats.adobe.com&quot; ou &quot;.adls.adobe.com&quot;.
   >
   >O URL começa com https,
   >
   >A ORG associada a essa instância do Adobe Campaign Standard é a mesma que a ORG do Journey Optimizer.

Ao projetar sua jornada, três ações estarão disponíveis no **[!UICONTROL Ação]** categoria: **[!UICONTROL Email]**, **[!UICONTROL Empurrar]**, **[!UICONTROL SMS]** (consulte [Usar ações do Adobe Campaign](../building-journeys/using-adobe-campaign-standard.md)).

![](assets/journey58.png)

Você pode usar um **Reações** para reagir a dados de rastreamento relacionados a uma mensagem de Campaign Standard enviada na mesma jornada. Para notificações por push, você pode reagir a mensagens clicadas, enviadas ou com falha. Para mensagens SMS, você pode reagir a mensagens enviadas ou com falha. Para emails, você pode reagir a mensagens clicadas, enviadas, abertas ou com falha. Consulte [Eventos de reações](../building-journeys/reaction-events.md).

Se estiver usando um sistema de terceiros para enviar mensagens, será necessário adicionar e configurar uma ação personalizada. Consulte [Sobre a configuração de ação personalizada](../action/about-custom-action-configuration.md).
