---
title: Criação de experiências da Web
description: Saiba como criar uma página da Web e editar seu conteúdo no Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: e28c038b-49ed-4685-bfe6-514116eb0711
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 8%

---

# Criação de experiências da Web {#create-web}

[!DNL Journey Optimizer] O permite personalizar a experiência da Web que você oferece para seus clientes por meio de campanhas da Web de entrada.

>[!CAUTION]
>
>Atualmente em [!DNL Journey Optimizer] você só pode criar experiências da web usando **campanhas**.

[Saiba como criar uma campanha da Web neste vídeo](#video)

## Criar uma campanha da Web {#create-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_surface"
>title="Definir uma superfície da Web"
>abstract="Uma superfície da Web pode corresponder a um URL de página única ou várias páginas, permitindo que você faça modificações no conteúdo em uma ou várias páginas da Web."

>[!CONTEXTUALHELP]
>id="ajo_web_surface_rule"
>title="Criar uma regra de correspondência de páginas"
>abstract="Uma regra de correspondência de páginas permite direcionar vários URLs que correspondem à mesma regra - por exemplo, se você deseja aplicar as alterações a um banner principal em um site inteiro ou adicionar uma imagem principal que é exibida em todas as páginas de produto de um site."

Para começar a criar sua experiência da Web por meio de uma campanha, siga as etapas abaixo.

>[!NOTE]
>
>Se esta for a primeira vez que você cria uma experiência da Web, siga os pré-requisitos descritos em [esta seção](web-prerequisites.md).

1. Criar uma campanha. [Saiba mais](../campaigns/create-campaign.md)

1. Selecione o **[!UICONTROL Web]** ação.

1. Definir uma superfície da Web.

   >[!NOTE]
   >
   >Uma superfície da Web é uma propriedade da Web identificada por um URL onde o conteúdo será entregue. Ele pode corresponder a um URL de página única ou várias páginas, permitindo que você entregue modificações em uma ou várias páginas da Web.

   Você pode inserir um **[!UICONTROL URL da página]** se desejar aplicar as alterações somente a uma única página.

   ![](assets/web-campaign-surface.png)

1. Ou você pode criar uma **[!UICONTROL Regras de correspondência de páginas]** para direcionar vários URLs que correspondem à mesma regra - por exemplo, se você deseja aplicar as alterações a um banner principal em um site inteiro ou adicionar uma imagem principal que é exibida em todas as páginas de produto de um site.

   Para fazer isso, selecione **[!UICONTROL Regras de correspondência de páginas]** e clique em **[!UICONTROL Criar regra]**.

   ![](assets/web-campaign-matching-rule.png)

1. Defina seus critérios para a **[!UICONTROL Domínio]** e **[!UICONTROL Página]** campos.

   Por exemplo, se você deseja editar elementos que são exibidos em todas as páginas de produtos para mulheres do seu site Luma, selecione **[!UICONTROL Domínio]** > **[!UICONTROL Começa com]** > `luma` e **[!UICONTROL Página]** > **[!UICONTROL Contém]** > `women`.

   ![](assets/web-pages-matching-rule.png)

1. Salve as alterações. A regra é exibida no **[!UICONTROL Criar campanha]** tela.

   ![](assets/web-pages-matching-rule-example.png)

1. Depois de definir a superfície da Web, selecione **[!UICONTROL Criar]**.

1. Complete as etapas para criar uma campanha da Web, como as propriedades da campanha, [público](../segment/about-segments.md)e [programação](../campaigns/create-campaign.md#schedule).

   ![](assets/web-campaign-steps.png)

Para obter mais informações sobre como configurar uma campanha, consulte [esta página](../campaigns/get-started-with-campaigns.md).

## Ativar a campanha da Web {#activate-web-campaign}

Depois de definir o [configurações da campanha da Web](#configure-web-campaign) e você editou seu conteúdo conforme desejado usando o [web designer](author-web.md), você pode revisar e ativar sua campanha da Web. Siga as etapas abaixo.

>[!NOTE]
>
>Você também pode visualizar o conteúdo da campanha da Web antes de ativá-lo. [Saiba mais](author-web.md#test-web-campaign)

1. Em sua campanha da Web, selecione **[!UICONTROL Revisar para ativar]**.

1. Verifique e edite, se necessário, o conteúdo, as propriedades, a superfície, o público-alvo e o agendamento.

1. Selecionar **[!UICONTROL Ativar]**.

   ![](assets/web-campaign-activate.png)

   >[!NOTE]
   >
   >Depois de clicar em **[!UICONTROL Ativar]**, pode levar até 15 minutos para que as alterações nas campanhas da Web estejam disponíveis no site.

Sua campanha da Web utiliza o **[!UICONTROL Ao vivo]** e agora está visível para o público selecionado. Cada recipient da campanha pode ver as modificações adicionadas ao site usando o [!DNL Journey Optimizer] web designer.

>[!NOTE]
>
>Se você definiu um agendamento para sua campanha da Web, ele tem a variável **[!UICONTROL Programado]** status até que a data e a hora de início sejam atingidas.
>
>Se você ativar uma campanha da Web que afete as mesmas páginas de outra campanha que já esteja ativa, todas as alterações serão aplicadas às suas páginas da Web.

Saiba mais sobre como ativar campanhas em [esta seção](../campaigns/review-activate-campaign.md).

## Parar uma campanha da Web {#stop-web-campaign}

Quando uma campanha da Web está ativa, você pode interrompê-la para impedir que seu público-alvo veja as modificações. Siga as etapas abaixo.

1. Selecione uma campanha ao vivo na lista.

1. No menu superior, selecione **[!UICONTROL Parar campanha]**.

   ![](assets/web-campaign-stop.png)

1. As modificações adicionadas não estarão mais visíveis para o público-alvo definido.

>[!NOTE]
>
>Quando uma campanha da Web é interrompida, não é possível editá-la ou ativá-la novamente. Você só pode duplicá-la e ativar a campanha duplicada.

## Vídeo tutorial{#video}

O vídeo abaixo mostra como criar uma campanha da Web, configurar suas propriedades, revisar e publicá-la.

>[!VIDEO](https://video.tv.adobe.com/v/3418800/?quality=12&learn=on)