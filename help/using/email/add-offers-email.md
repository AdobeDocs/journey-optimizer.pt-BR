---
solution: Journey Optimizer
product: journey optimizer
title: Adicionar ofertas personalizadas
description: Saiba como adicionar ofertas personalizadas às suas mensagens
feature: Email Design, Offers
topic: Content Management
role: User
level: Intermediate
keywords: ofertas, decisão, emails, personalização, decisão
exl-id: 1e648eca-b5ca-4767-b45d-c179243e347f
TQID: https://experienceleague.adobe.com/ajycOqX0Q6spKP8RgXmF-QLR95AYsCLLfIaKofpd95k
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
  - id: c41e8697-e629-4c38-96b3-564faaa17acf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: bc98cb2b61c7c5c8dac78b494fe293a4106a88c4
workflow-type: tm+mt
source-wordcount: 678
ht-degree: 1%

---

# Adicionar ofertas personalizadas {#deliver-personalized-offers}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como inserir e visualizar decisões de oferta em seus emails para que o Adobe Journey Optimizer forneça a melhor oferta personalizada para cada destinatário.

>[!ENDSHADEBOX]

Em emails do [!DNL Journey Optimizer], você pode inserir decisões que aproveitarão o mecanismo da Gestão de decisões para escolher a melhor oferta a ser entregue aos clientes.

Por exemplo, você pode adicionar uma decisão que exibirá no email uma oferta de desconto especial que varia de acordo com o nível de fidelidade do recipient.

>[!IMPORTANT]
>
>Se forem feitas alterações em uma decisão de oferta em uso na mensagem de uma jornada, será necessário desfazer a publicação da jornada e republicá-la.  Isso garantirá que as alterações sejam incorporadas à mensagem da jornada e que ela seja consistente com as atualizações mais recentes.

* Para obter mais informações sobre como criar e gerenciar ofertas, consulte [esta seção](../offers/get-started/starting-offer-decisioning.md).
* Para um **exemplo completo** mostrando como configurar ofertas, usá-las em uma decisão e aproveitar esta decisão em um email, confira [esta seção](../offers/offers-e2e.md#insert-decision-in-email).

➡️ [Saiba como adicionar ofertas como personalização neste vídeo](#video-offers)

## Inserir uma decisão em um email {#insert-offers}

>[!CAUTION]
>
>Antes de começar, você deve [definir uma decisão de oferta](../offers/offer-activities/create-offer-activities.md).

Para inserir uma decisão em uma mensagem de email, siga as etapas abaixo:

1. Crie seu email e abra o Designer de email para configurar seu conteúdo.

1. Adicione um componente de conteúdo **[!UICONTROL Offer decision]**.

   ![](assets/deliver-offer-component.png)

   Saiba como usar componentes de conteúdo em [esta seção](content-components.md).

1. A guia **[!UICONTROL Offer decision]** é exibida na paleta direita. Clique em **[!UICONTROL Selecionar decisão de oferta]**:

   1. Na janela exibida, selecione o posicionamento correspondente às ofertas que deseja exibir.

      [Posicionamentos](../offers/offer-library/creating-placements.md) são contêineres usados para exibir suas ofertas. Neste exemplo, usaremos a inserção &quot;imagem superior do email&quot;. Esse posicionamento foi criado na Biblioteca de ofertas para exibir ofertas do tipo imagem situadas na parte superior das mensagens.

   1. As decisões correspondentes à disposição selecionada são exibidas. Selecione a decisão a ser usada no componente de conteúdo e clique em **[!UICONTROL Adicionar]**.

      >[!NOTE]
      >
      >Somente as decisões compatíveis com o posicionamento selecionado são exibidas na lista. Neste exemplo, apenas uma atividade de oferta corresponde à disposição da &quot;imagem superior do email&quot;.

      ![](assets/deliver-offer-placement.png)

A decisão foi adicionada ao componente. Depois de salvar as alterações, as ofertas estarão prontas para serem exibidas nos perfis relevantes ao enviar a mensagem como parte de uma jornada.

>[!NOTE]
>
>Ao atualizar uma oferta, oferta substituta, coleção de ofertas ou decisão de oferta que é mencionada direta ou indiretamente na mensagem, as atualizações são refletidas automaticamente na mensagem correspondente.

## Visualizar ofertas em um email {#preview-offers-in-email}

Você pode visualizar as diferentes ofertas que fazem parte da decisão adicionada ao email usando a seção **[!UICONTROL Oferta]** ou as setas de componentes de conteúdo.

![](assets/deliver-offer-preview.png)

Para exibir as diferentes ofertas que fazem parte da decisão com um perfil de cliente, siga as etapas abaixo.

1. Selecione os perfis de teste que serão usados para visualizar a oferta:

   1. Clique em **[!UICONTROL Simular conteúdo]**, selecione **[!UICONTROL Simular conteúdo (perfis do AEP)]** na lista suspensa e escolha o namespace a ser usado para identificar perfis de teste do campo **[!UICONTROL Namespace de identidade]**. Para testar as variações de conteúdo com dados de entrada de exemplo ou a geração automática de IA, clique diretamente em **[!UICONTROL Simular conteúdo]**. [Saiba como simular variações de conteúdo](../test-approve/simulate-sample-input.md)

      >[!NOTE]
      >
      >Neste exemplo, usamos o namespace **Email**. Saiba mais sobre os namespaces de identidade do Adobe Experience Platform [nesta seção](../audience/get-started-identity.md).

   1. No campo **[!UICONTROL Valor de identidade]**, insira o valor para identificar o perfil de teste. Neste exemplo, insira o endereço de email de um perfil de teste.

   <!--For example enter smith@adobe.com and click the **[!UICONTROL Add profile]** button.-->

   1. Adicione outros perfis para testar diferentes variantes da mensagem, dependendo dos dados do perfil.

      ![](assets/deliver-offer-test-profiles.png)

1. Clique na guia **[!UICONTROL Visualização]** para testar sua mensagem e selecione um perfil de teste. A oferta correspondente ao perfil selecionado (uma mulher) é exibida.

   ![](assets/deliver-offer-test-profile-female-preview.png)

   É possível selecionar outros perfis de teste para visualizar o conteúdo do email para cada variante da mensagem. No conteúdo da mensagem, a oferta correspondente ao perfil de teste selecionado (agora um manual) é exibida.

Saiba mais sobre as etapas detalhadas para verificar a visualização da mensagem em [esta seção](#preview-your-messages).

## Vídeo tutorial{#video-offers}

Saiba como adicionar um componente de gestão de decisões a mensagens no [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/334088?quality=12)
