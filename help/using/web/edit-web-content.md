---
title: Editar conteúdo da Web
description: Saiba como criar uma página da Web e editar seu conteúdo no Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: 3847ac1d-2c0a-4f80-8df9-e8e304faf261
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '1101'
ht-degree: 2%

---

# Editar conteúdo da Web {#edit-web-content}

Uma vez que [adicionou uma ação da web](create-web.md#create-web-campaign) para editar o conteúdo do site usando o web designer.

[Saiba como criar uma campanha da Web neste vídeo](#video)

Entrada [!DNL Journey Optimizer], a criação na web é possibilitada pelo **Adobe Experience Cloud Visual Helper** extensão do navegador chrome. [Saiba mais](web-prerequisites.md#visual-authoring-prerequisites)

>[!CAUTION]
>
>Para acessar e criar páginas da Web na [!DNL Journey Optimizer] verifique se você segue os pré-requisitos listados na [nesta seção](web-prerequisites.md).

Acesse as seguintes seções para saber mais sobre cada tópico:

* [Gerenciar modificações](manage-web-modifications.md)

* [Monitorar suas campanhas da Web](monitor-web-campaigns.md)

## Trabalhar com o web designer {#work-with-web-designer}

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_surface"
>title="Confirmar o URL a ser editado"
>abstract="Confirme o URL da página da Web específica a ser usada para editar o conteúdo que será aplicado na superfície da Web definida acima. A página da Web deve ser implementada usando o Adobe Experience Platform Web SDK."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR" text="Saiba mais"

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_rule"
>title="Insira o URL para editar"
>abstract="Insira o URL de uma página da Web específica a ser usada para editar o conteúdo que será aplicado a todas as páginas que correspondem à regra. A página da Web deve ser implementada usando o Adobe Experience Platform Web SDK."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR" text="Saiba mais"

Para começar a criar sua campanha da Web, siga as etapas abaixo.

1. No **[!UICONTROL Ação]** guia do [campaign](create-web.md#create-web-campaign), selecione **[!UICONTROL Editar conteúdo]**.<!--change screen with rule-->

   ![](assets/web-campaign-edit-content.png)

1. Se você criou uma regra de correspondência de páginas, deve inserir qualquer URL correspondente a essa regra: as alterações serão aplicadas a todas as páginas que correspondam à regra. O conteúdo da página é exibido.

   >[!NOTE]
   >
   >Se você inseriu um único URL como a superfície da web, o URL para personalizar já está preenchido.

   ![](assets/web-edit-enter-url.png)

   >[!CAUTION]
   >
   >A página da Web deve incluir o [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR){target="_blank"}. [Saiba mais](web-prerequisites.md#implementation-prerequisites)

1. Clique em **[!UICONTROL Editar página da Web]** para começar a criá-lo. O web designer é exibido.

   ![](assets/web-designer.png)

   >[!NOTE]
   >
   >Se você tentar carregar um site que não foi carregado, uma mensagem será exibida sugerindo que você instale o [Extensão de navegador Auxiliar de edição visual](#install-visual-editing-helper). Veja algumas dicas para solução de problemas no [nesta seção](web-prerequisites.md#troubleshooting).

1. Selecione qualquer elemento da tela de desenho, como imagem, botão, parágrafo, texto, contêiner, cabeçalho, link etc. [Saiba mais](#content-components)

1. Uso:

   * O menu contextual para editar conteúdo, layout, inserir links ou personalização, etc.

     ![](assets/web-designer-contextual-bar.png)

   * Os ícones na parte superior do painel direito permitem editar, duplicar, excluir ou ocultar cada elemento.

     ![](assets/web-designer-right-panel-icons.png)

   * O painel direito que muda dinamicamente de acordo com o elemento selecionado. Por exemplo, você pode editar o plano de fundo, a tipografia, a borda, o tamanho, a posição, o espaçamento, os efeitos ou os estilos embutidos de um elemento.

     ![](assets/web-designer-right-panel.png)

>[!NOTE]
>
>O designer de conteúdo da Web é, em sua maioria, semelhante ao designer de email. Saiba mais sobre [criação de conteúdo com [!DNL Journey Optimizer]](../email/get-started-email-design.md).

## Usar componentes {#content-components}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_components"
>title="Adicionar componentes à sua página da Web"
>abstract="Você pode adicionar vários componentes à sua página da Web e editá-los conforme necessário."

1. No **[!UICONTROL Componentes]** selecione um item. Você pode adicionar os seguintes componentes à sua página da Web e editá-los conforme necessário:

   * [Divisor](../email/content-components.md#divider)
   * [HTML](../email/content-components.md#HTML)
   * [Imagem](../email/content-components.md#image)
   * Cabeçalho - O uso desse componente é semelhante ao uso do **[!UICONTROL Texto]** componente no designer de email. [Saiba mais](../email/content-components.md#text)
   * Parágrafo - O uso deste componente é semelhante ao uso da variável **[!UICONTROL Texto]** componente no designer de email. [Saiba mais](../email/content-components.md#text)
   * Link
   * [Decisão de oferta](../email/add-offers-email.md)

   ![](assets/web-designer-components.png)

1. Passe o mouse na página e clique no ícone **[!UICONTROL Inserir antes de]** ou **[!UICONTROL Inserir depois de]** botão para anexar o componente a um elemento existente na página.

   ![](assets/web-designer-insert-components.png)

   >[!NOTE]
   >
   >Para desmarcar um componente, clique no **[!UICONTROL ESC]** no banner azul contextual exibido na parte superior da tela.

1. Edite o componente conforme necessário diretamente no conteúdo da página.

   ![](assets/web-designer-edit-header.png)

1. Ajuste os estilos exibidos no painel contextual à direita, como plano de fundo, cor do texto, borda, tamanho, posição etc. - dependendo do componente selecionado.

   ![](assets/web-designer-header-style.png)

## Adicionar personalização e ofertas

Para adicionar personalização, selecione um container e selecione o ícone de personalização na barra de menu contextual exibida. Adicione as alterações usando o editor de personalização. [Saiba mais](../personalization/personalization-build-expressions.md)

![](assets/web-designer-personalization.png)

Use o **[!UICONTROL Decisão de oferta]** componente a ser inserido [ofertas](../offers/get-started/starting-offer-decisioning.md) em suas páginas da Web. O processo é o mesmo de quando [adicionar uma oferta a um email](../email/add-offers-email.md). Ele aproveitará o Gerenciamento de decisão para escolher a melhor oferta a ser entregue aos clientes.

![](assets/web-designer-offer.png)

## Navegar pelo web designer {#navigate-web-designer}

Esta seção detalha as diferentes maneiras de navegar pelo web designer. Para exibir e gerenciar as modificações adicionadas à sua experiência online, consulte [nesta seção](manage-web-modifications.md).

### Usar navegações estruturais {#breadcrumbs}

1. Selecione qualquer elemento da tela.

1. Clique em **[!UICONTROL Expandir/recolher navegações estruturais]** no lado inferior esquerdo da tela para exibir rapidamente informações sobre o elemento selecionado.

   ![](assets/web-designer-breadcrumbs.png)

1. Quando você passa o mouse sobre a navegação estrutural, o elemento correspondente é realçado no editor.

1. Ao usá-lo, você pode navegar facilmente para qualquer elemento pai, irmão ou filho no editor visual.

### Alternar para o modo de navegação {#browse-mode}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_browse"
>title="Usar o modo de navegação"
>abstract="Nesse modo, você pode navegar para a página exata da superfície selecionada que deseja personalizar."

Você pode trocar do padrão **[!UICONTROL Design]** para o modo **[!UICONTROL Procurar]** usando o botão dedicado.

![](assets/web-designer-browse-mode.png)

No **[!UICONTROL Procurar]** , você pode navegar para a página exata a partir da superfície selecionada que deseja personalizar.

É especialmente útil ao lidar com páginas que estão por trás da autenticação ou que não estão disponíveis desde o início em um determinado URL. Por exemplo, você poderá se autenticar, navegar até a página da sua conta ou até a página do carrinho e voltar para **[!UICONTROL Design]** para executar as alterações na página desejada.

Usar **[!UICONTROL Procurar]** O modo de também permite navegar por todas as exibições do site ao criar aplicativos de página única. [Saiba mais](web-spa.md)

### Alterar tamanho do dispositivo {#change-device-size}

É possível alterar o tamanho do dispositivo da exibição do web designer para um tamanho predefinido, como **[!UICONTROL Tablet]** ou **[!UICONTROL Paisagem móvel]** ou defina um tamanho personalizado inserindo o número desejado de pixels.

Também é possível alterar o foco do zoom de 25% para 400%.

![](assets/web-designer-device.png)

A capacidade de alterar o tamanho do dispositivo foi projetada para sites responsivos que são renderizados em vários dispositivos, janelas e tamanhos de tela. Sites responsivos ajustam-se e se adaptam automaticamente a qualquer tamanho de tela, incluindo desktops, laptops, tablets ou telefones celulares.

>[!CAUTION]
>
>É possível editar uma experiência da Web com um tamanho de dispositivo específico. No entanto, desde que os seletores sejam os mesmos, essas alterações se aplicam a todos os tamanhos e dispositivos, não apenas ao tamanho do dispositivo em que você está trabalhando. Da mesma forma, editar uma experiência na exibição de desktop normal aplica as alterações a todos os tamanhos de tela, não apenas à exibição de desktop.
>
>Atualmente, [!DNL Journey Optimizer] não aceita alterações de página específicas ao tamanho do dispositivo. Isso significa que, por exemplo, se você tiver um site móvel separado com uma estrutura de site separada, deverá fazer as alterações específicas no site móvel em uma campanha diferente.

## Vídeo tutorial{#video}

O vídeo abaixo mostra como criar uma experiência na Web usando o designer da Web no [!DNL Journey Optimizer] campanhas.

>[!VIDEO](https://video.tv.adobe.com/v/3418803/?quality=12&learn=on)