---
solution: Journey Optimizer
product: journey optimizer
title: Adicionar ofertas personalizadas
description: Saiba como adicionar ofertas personalizadas às suas mensagens
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 1e648eca-b5ca-4767-b45d-c179243e347f
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 1%

---

# Adicionar ofertas personalizadas {#deliver-personalized-offers}

Em [!DNL Journey Optimizer] e-mails, você pode inserir decisões que aproveitarão o Offer Decision Engine para escolher a melhor oferta para entregar aos seus clientes.

Por exemplo, você pode adicionar uma decisão que exibirá em seu email uma oferta de desconto especial que varia de acordo com o nível de fidelidade do recipient.

Para obter mais informações sobre como criar e gerenciar ofertas, consulte [esta seção](../offers/get-started/starting-offer-decisioning.md).

Para um **exemplo completo** mostrando como configurar ofertas, usá-las em uma decisão e aproveitar essa decisão em um email, confira [esta seção](../offers/offers-e2e.md#insert-decision-in-email).

➡️ [Saiba como adicionar ofertas como personalização neste vídeo](#video-offers)

## Inserir uma decisão em um email {#insert-offers}

>[!CAUTION]
>
>Antes de começar, você deve [definir uma decisão de oferta](../offers/offer-activities/create-offer-activities.md).

Para inserir uma decisão em uma mensagem de email, siga as etapas abaixo:

1. Crie seu email e abra o Designer de email para configurar seu conteúdo.

1. Adicione um **[!UICONTROL Decisão da oferta]** componente de conteúdo.

   ![](assets/deliver-offer-component.png)

   Saiba como usar componentes de conteúdo no [esta seção](content-components.md).

1. O **[!UICONTROL Decisão da oferta]** é exibida na paleta direita. Clique em **[!UICONTROL Selecionar decisão da oferta]**.

   ![](assets/deliver-offer-tab.png)

1. Na janela exibida, selecione a disposição correspondente às ofertas que deseja exibir.

   [Posicionamentos](../offers/offer-library/creating-placements.md) são contêineres usados para mostrar suas ofertas. Neste exemplo, usaremos a disposição &quot;imagem superior do email&quot;. Essa disposição foi criada na Biblioteca de ofertas para exibir ofertas do tipo imagem situadas na parte superior das mensagens.

1. As decisões que correspondem à exibição de disposição selecionada. Selecione a decisão a ser usada no componente de conteúdo e clique em **[!UICONTROL Adicionar]**.

   >[!NOTE]
   >
   >Somente as decisões compatíveis com a disposição selecionada são exibidas na lista. Neste exemplo, apenas uma atividade de oferta corresponde à disposição &quot;imagem superior do email&quot;.

   ![](assets/deliver-offer-placement.png)

A atividade de oferta agora é adicionada ao componente .

Depois de salvar as alterações, as ofertas estão prontas para serem exibidas aos perfis relevantes ao enviar a mensagem como parte de uma jornada.

>[!NOTE]
>
>Ao atualizar uma oferta, oferta de fallback, coleção de ofertas ou decisão de oferta que é mencionada direta ou indiretamente na mensagem, as atualizações são refletidas automaticamente na mensagem correspondente.

## Visualizar ofertas em um email {#preview-offers-in-email}

É possível visualizar as diferentes ofertas que fazem parte da decisão adicionada ao email usando a **[!UICONTROL Ofertas]** ou as setas dos componentes de conteúdo.

![](assets/deliver-offer-preview.png)

Para exibir as diferentes ofertas que fazem parte da decisão com um perfil de cliente, siga as etapas abaixo.

1. Clique em **[!UICONTROL Visualizar]**.

   ![](assets/deliver-offer-preview-button.png)

   >[!NOTE]
   >
   >Você precisa ter perfis de teste disponíveis para poder visualizar suas mensagens. Saiba como [criar perfis de teste](../segment/creating-test-profiles.md).

1. Para escolher o namespace a ser usado para identificar perfis de teste, selecione **[!UICONTROL Email]** do **[!UICONTROL Namespace de identidade]** campo.

   >[!NOTE]
   >
   >Neste exemplo, usaremos a variável **Email** namespace. Saiba mais sobre os namespaces de identidade da Adobe Experience Platform [nesta seção](../segment/get-started-identity.md).

1. Na lista de namespaces de identidade, selecione **[!UICONTROL Email]** e clique em **[!UICONTROL Selecionar]**.

1. No **[!UICONTROL Valor de identidade]** , insira o valor para identificar o perfil de teste. Neste exemplo, insira o endereço de email de um perfil de teste.

   <!--For example enter smith@adobe.com and click the **[!UICONTROL Add profile]** button.-->

1. Adicione outros perfis para testar diferentes variantes da mensagem, dependendo dos dados do perfil.

   ![](assets/deliver-offer-test-profiles.png)

1. Clique no botão **[!UICONTROL Visualizar]** para testar sua mensagem.

1. Selecione um perfil de teste. A oferta correspondente ao perfil selecionado (uma mulher) é exibida.

   ![](assets/deliver-offer-test-profile-female-preview.png)

1. Selecione outros perfis de teste para visualizar o conteúdo de email de cada variante de sua mensagem. No conteúdo da mensagem, a oferta correspondente ao perfil de teste selecionado (agora um homem) agora é exibida.

   ![](assets/deliver-offer-test-profile-male-preview.png)

Saiba mais sobre as etapas detalhadas para verificar a pré-visualização da mensagem em [esta seção](#preview-your-messages).

## Vídeo tutorial{#video-offers}

Saiba como adicionar um componente de gerenciamento de decisões a mensagens no [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/334088?quality=12)

