---
title: Adicionar ofertas personalizadas
description: Saiba como adicionar ofertas personalizadas às suas mensagens
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# Adicionar ofertas personalizadas {#deliver-personalized-offers}

![](assets/do-not-localize/badge.png)

## Sobre o Gerenciamento de decisões {#about-offer-decisioning}

Com [!DNL Journey Optimizer], você pode inserir em suas decisões de mensagens de email (anteriormente conhecidas como atividades de oferta) que aproveitarão o mecanismo de decisão da oferta para escolher a melhor oferta a ser entregue aos clientes.

Por exemplo, você pode adicionar uma decisão que exibirá em seu email uma oferta de desconto especial que varia de acordo com o nível de fidelidade do recipient.

Para obter mais informações sobre como criar e gerenciar ofertas, consulte [esta seção](offers/get-started/starting-offer-decisioning.md).

## Inserir uma decisão em um email {#insert-offers}

Para inserir uma decisão em uma mensagem de email, siga as etapas abaixo:

1. Crie seu email e abra o Designer de email para configurar seu conteúdo.

1. Adicione um componente de conteúdo **[!UICONTROL Offer decision]** (consulte [Usar componentes de conteúdo](content-components.md)).

   ![](assets/deliver-offer-component.png)

1. Uma guia **[!UICONTROL Offer decision]** é adicionada ao componente. Clique em **[!UICONTROL Add personalization - Offer decision]** para adicionar uma atividade de oferta.

   ![](assets/deliver-offer-tab.png)

1. Selecione a disposição correspondente às ofertas que deseja exibir.

   As disposições são contêineres usados para mostrar suas ofertas. Neste exemplo, usaremos a disposição &quot;imagem superior do email&quot;. Essa disposição foi criada na Biblioteca de ofertas para exibir ofertas do tipo imagem situadas na parte superior das mensagens.

1. Selecione a atividade de oferta a ser usada no componente de conteúdo e clique em **[!UICONTROL Add]**.

   >[!NOTE]
   >
   >Observe que somente as decisões compatíveis com a disposição selecionada são exibidas na lista. Neste exemplo, apenas uma atividade de oferta corresponde à disposição &quot;imagem superior do email&quot;.

   ![](assets/deliver-offer-placement.png)

1. A atividade de oferta agora é adicionada ao componente . Você pode visualizar as diferentes ofertas que fazem parte da decisão usando a seção **[!UICONTROL Offers]** ou as setas dos componentes de conteúdo.

   ![](assets/deliver-offer-preview.png)
