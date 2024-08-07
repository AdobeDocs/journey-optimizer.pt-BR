---
title: Criação de experiências da web
description: Saiba como criar uma página da Web e editar seu conteúdo no Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: e28c038b-49ed-4685-bfe6-514116eb0711
source-git-commit: 27447578dad6bd2612989d79cd0dc8ddbe78d629
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 17%

---

# Criação de experiências da web {#create-web}

O [!DNL Journey Optimizer] permite personalizar a experiência da Web fornecida aos clientes por meio de campanhas da Web de entrada.

>[!CAUTION]
>
>Atualmente, no [!DNL Journey Optimizer], você só pode criar experiências da web usando **campanhas**.

[Saiba como criar uma campanha da Web neste vídeo](#video)

## Criar uma campanha da web {#create-web-campaign}

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

1. Crie uma campanha. [Saiba mais](../campaigns/create-campaign.md)

1. Selecione a ação **[!UICONTROL Web]**.

1. Defina uma superfície da web.

   >[!NOTE]
   >
   >Uma superfície da Web é uma propriedade da Web identificada por um URL em que o conteúdo será entregue. Ele pode corresponder a um único URL de página ou a várias páginas, permitindo que você faça modificações em uma ou várias páginas da Web.

   Você pode digitar uma **[!UICONTROL URL da página]** se quiser aplicar as alterações a uma única página.

   ![](assets/web-campaign-surface.png)

1. Ou você pode criar uma **[!UICONTROL regra de correspondência de páginas]** para direcionar várias URLs que correspondam à mesma regra; por exemplo, se você deseja aplicar as alterações a um banner principal em todo o site ou adicionar uma imagem superior que seja exibida em todas as páginas de produto de um site.

   Para fazer isso, selecione **[!UICONTROL Regra de correspondência de páginas]** e clique em **[!UICONTROL Criar regra]**.

   ![](assets/web-campaign-matching-rule.png)

1. Defina seus critérios para os campos **[!UICONTROL Domínio]** e **[!UICONTROL Página]**.

   Por exemplo, se você deseja editar elementos que são exibidos em todas as páginas de produtos femininas do seu site Luma, selecione **[!UICONTROL Domínio]** > **[!UICONTROL Começa com]** > `luma` e **[!UICONTROL Página]** > **[!UICONTROL Contém]** > `women`.

   ![](assets/web-pages-matching-rule.png)

1. Salve as alterações. A regra é exibida na tela **[!UICONTROL Criar campanha]**.

   ![](assets/web-pages-matching-rule-example.png)

1. Depois de definir a superfície da web, selecione **[!UICONTROL Criar]**.

1. Conclua as etapas para criar uma campanha da Web, como as propriedades da campanha, [público](../audience/about-audiences.md) e [agendamento](../campaigns/create-campaign.md#schedule).

   ![](assets/web-campaign-steps.png)

Para obter mais informações sobre como configurar uma campanha, consulte [esta página](../campaigns/get-started-with-campaigns.md).

## Testar a campanha da Web {#test-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_preview"
>title="Visualizar a experiência da Web"
>abstract="Acesse uma simulação de como sua experiência da Web será."

Depois de [criar sua experiência da Web](edit-web-content.md) usando o designer da Web, você poderá usar perfis de teste para visualizar suas páginas da Web modificadas. Se você inseriu conteúdo personalizado, é possível verificar como esse conteúdo é exibido, usando os dados do perfil de teste.

Para fazer isso, clique em **[!UICONTROL Simular conteúdo]** da tela de edição de conteúdo da campanha da Web ou do designer da Web e, em seguida, adicione um perfil de teste para verificar sua página da Web usando os dados do perfil de teste.

![](assets/web-designer-preview.png)

Você também pode abri-lo no navegador padrão ou copiar o URL de teste para colá-lo em qualquer navegador. Isso permite compartilhar o link com a equipe e as partes interessadas, que poderão visualizar a nova experiência da Web em qualquer navegador antes que a campanha entre em vigor.

>[!NOTE]
>
>Ao copiar a URL de teste, o conteúdo exibido é aquele personalizado para o perfil de teste usado quando a simulação de conteúdo foi gerada em [!DNL Journey Optimizer].

Informações detalhadas sobre como selecionar perfis de teste e pré-visualizar seu conteúdo estão disponíveis na seção [Gerenciamento de conteúdo](../content-management/preview-test.md).

## Ativar a campanha da Web {#activate-web-campaign}

Depois de definir suas [configurações da campanha da Web](#configure-web-campaign) e editar seu conteúdo conforme desejado usando o [web designer](edit-web-content.md#work-with-web-designer), você poderá revisar e ativar sua campanha da Web. Siga as etapas abaixo.

<!--
>[!NOTE]
>
>You can also preview your web campaign content before activating it. [Learn more](#test-web-campaign)-->

1. Em sua campanha da Web, selecione **[!UICONTROL Revisar para ativar]**.

1. Verifique e edite, se necessário, o conteúdo, as propriedades, a superfície, o público-alvo e o agendamento.

1. Selecione **[!UICONTROL Ativar]**.

   ![](assets/web-campaign-activate.png)

   >[!NOTE]
   >
   >Depois de clicar em **[!UICONTROL Ativar]**, pode levar até 15 minutos para que as alterações nas campanhas da Web fiquem disponíveis ao vivo no site.

Sua campanha da Web recebe o status de **[!UICONTROL Ativo]** e agora está visível para o público selecionado. Cada destinatário da campanha pode ver as modificações adicionadas ao site usando o web designer [!DNL Journey Optimizer].

>[!NOTE]
>
>Se você definiu um agendamento para sua campanha da Web, ele tem o status **[!UICONTROL Agendado]** até que a data e a hora de início sejam atingidas.
>
>Se você ativar uma campanha da Web que afeta as mesmas páginas que outra campanha que já está ativa, todas as alterações serão aplicadas às suas páginas da Web.

Saiba mais sobre como ativar campanhas em [esta seção](../campaigns/review-activate-campaign.md).

## Parar uma campanha da Web {#stop-web-campaign}

Quando uma campanha da Web está ativa, você pode interrompê-la para impedir que seu público veja as modificações. Siga as etapas abaixo.

1. Selecione uma campanha ao vivo da lista.

1. No menu superior, selecione **[!UICONTROL Parar campanha]**.

   ![](assets/web-campaign-stop.png)

1. As modificações adicionadas não estarão mais visíveis para o público-alvo definido.

>[!NOTE]
>
>Quando uma campanha da Web é interrompida, não é possível editá-la ou ativá-la novamente. Você só pode duplicá-la e ativar a campanha duplicada.

## Vídeo tutorial{#video}

O vídeo abaixo mostra como criar uma campanha da Web, configurar suas propriedades, revisá-la e publicá-la.

>[!VIDEO](https://video.tv.adobe.com/v/3418800/?quality=12&learn=on)