---
title: Criação de experiências da Web
description: Saiba como criar uma página da Web e editar seu conteúdo no Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: e28c038b-49ed-4685-bfe6-514116eb0711
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 21%

---

# Criação de experiências da Web {#create-web}

[!DNL Journey Optimizer] O permite personalizar a experiência da web fornecida aos clientes por meio de campanhas da web de entrada.

>[!CAUTION]
>
>Atualmente, no [!DNL Journey Optimizer], você só pode criar experiências da web usando **campanhas**.

[Saiba como criar uma campanha da Web neste vídeo](#video)

## Criar uma campanha da Web {#create-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_surface"
>title="Definir uma superfície da Web"
>abstract="Uma superfície da Web pode corresponder a um URL de página única ou várias páginas, permitindo que você faça modificações no conteúdo em uma ou várias páginas da Web."

>[!CONTEXTUALHELP]
>id="ajo_web_surface_rule"
>title="Criar uma regra de correspondência de páginas"
>abstract="Uma regra de correspondência de páginas permite direcionar vários URLs que correspondem à mesma regra, por exemplo, se você deseja aplicar as alterações em um banner principal no site inteiro ou adicionar uma imagem superior que é exibida em todas as páginas de produtos de um site."

Para começar a criar sua experiência da Web por meio de uma campanha, siga as etapas abaixo.

>[!NOTE]
>
>Se esta for a primeira vez que estiver criando uma experiência online, certifique-se de seguir os pré-requisitos descritos [nesta seção](web-prerequisites.md).

1. Criar uma campanha. [Saiba mais](../campaigns/create-campaign.md)

1. Selecione o **[!UICONTROL Web]** ação.

1. Definir uma superfície da Web.

   >[!NOTE]
   >
   >Uma superfície da Web é uma propriedade da Web identificada por um URL em que o conteúdo será entregue. Ele pode corresponder a um único URL de página ou a várias páginas, permitindo que você faça modificações em uma ou várias páginas da Web.

   Você pode inserir um **[!UICONTROL URL da página]** se quiser aplicar as alterações somente a uma única página.

   ![](assets/web-campaign-surface.png)

1. Ou você pode criar um **[!UICONTROL Regra de correspondência de páginas]** para direcionar vários URLs que correspondem à mesma regra, por exemplo, se você deseja aplicar as alterações em um banner principal em um site inteiro ou adicionar uma imagem superior que é exibida em todas as páginas de produto de um site.

   Para fazer isso, selecione **[!UICONTROL Regra de correspondência de páginas]** e clique em **[!UICONTROL Criar regra]**.

   ![](assets/web-campaign-matching-rule.png)

1. Defina seus critérios para o **[!UICONTROL Domínio]** e **[!UICONTROL Página]** campos.

   Por exemplo, se você quiser editar elementos exibidos em todas as páginas de produtos para mulheres do seu site Luma, selecione **[!UICONTROL Domínio]** > **[!UICONTROL Começa com]** > `luma` e **[!UICONTROL Página]** > **[!UICONTROL Contém]** > `women`.

   ![](assets/web-pages-matching-rule.png)

1. Salve as alterações. A regra é exibida na variável **[!UICONTROL Criar campanha]** tela.

   ![](assets/web-pages-matching-rule-example.png)

1. Depois de definir a superfície da Web, selecione **[!UICONTROL Criar]**.

1. Conclua as etapas para criar uma campanha da Web, como as propriedades da campanha, [público](../audience/about-audiences.md), e [programação](../campaigns/create-campaign.md#schedule).

   ![](assets/web-campaign-steps.png)

Para obter mais informações sobre como configurar uma campanha, consulte [esta página](../campaigns/get-started-with-campaigns.md).

## Ativar a campanha da Web {#activate-web-campaign}

Depois de definir o [configurações de campanha da web](#configure-web-campaign) e você editou seu conteúdo conforme desejado usando o [web designer](author-web.md), você pode revisar e ativar sua campanha da web. Siga as etapas abaixo.

>[!NOTE]
>
>Você também pode pré-visualizar o conteúdo da campanha da Web antes de ativá-lo. [Saiba mais](author-web.md#test-web-campaign)

1. Em sua campanha da Web, selecione **[!UICONTROL Revisar para ativar]**.

1. Verifique e edite, se necessário, o conteúdo, as propriedades, a superfície, o público-alvo e o agendamento.

1. Selecionar **[!UICONTROL Ativar]**.

   ![](assets/web-campaign-activate.png)

   >[!NOTE]
   >
   >Depois de clicar em **[!UICONTROL Ativar]**, pode levar até 15 minutos para que as alterações nas campanhas da Web sejam disponibilizadas ao vivo no seu site.

Sua campanha da Web usa o **[!UICONTROL Ao vivo]** e agora está visível para o público-alvo selecionado. Cada recipient da campanha pode ver as modificações adicionadas ao site usando o [!DNL Journey Optimizer] web designer.

>[!NOTE]
>
>Se você definiu uma programação para sua campanha da Web, ela tem a **[!UICONTROL Agendado]** até que a data e a hora de início sejam atingidas.
>
>Se você ativar uma campanha da Web que afeta as mesmas páginas que outra campanha que já está ativa, todas as alterações serão aplicadas às suas páginas da Web.

Saiba mais sobre como ativar campanhas no [nesta seção](../campaigns/review-activate-campaign.md).

## Parar uma campanha da Web {#stop-web-campaign}

Quando uma campanha da Web está ativa, você pode interrompê-la para impedir que seu público veja as modificações. Siga as etapas abaixo.

1. Selecione uma campanha ao vivo da lista.

1. No menu superior, selecione **[!UICONTROL Interromper campanha]**.

   ![](assets/web-campaign-stop.png)

1. As modificações adicionadas não estarão mais visíveis para o público-alvo definido.

>[!NOTE]
>
>Quando uma campanha da Web é interrompida, não é possível editá-la ou ativá-la novamente. Você só pode duplicá-la e ativar a campanha duplicada.

## Vídeo explicativo{#video}

O vídeo abaixo mostra como criar uma campanha da Web, configurar suas propriedades, revisá-la e publicá-la.

>[!VIDEO](https://video.tv.adobe.com/v/3418800/?quality=12&learn=on)