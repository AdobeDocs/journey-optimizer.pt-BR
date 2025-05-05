---
title: Editar conteúdo usando o web designer
description: Saiba como criar uma página da Web e editar seu conteúdo usando o editor da Web do Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: 98e99978-8538-40b4-92ac-7184864017eb
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 8%

---

# Trabalhar com o web designer {#work-with-web-designer}

<!--
>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_surface"
>title="Confirm the URL to edit"
>abstract="Confirm the URL of the specific web page to use for editing the content that will be applied on the web configuration defined above. The web page must be implemented using the Adobe Experience Platform Web SDK."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR" text="Learn more"

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_rule"
>title="Enter the URL to edit"
>abstract="Enter the URL of a specific web page to use for editing the content that will be applied to all pages matching the rule. The web page must be implemented using Adobe Experience Platform Web SDK."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR" text="Learn more"
-->

No [!DNL Journey Optimizer], a criação no visual web é fornecida pela extensão de navegador do Chrome **Adobe Experience Cloud Visual Helper**. [Saiba mais](web-prerequisites.md#visual-authoring-prerequisites)

>[!CAUTION]
>
>Para acessar e criar páginas da Web na interface do usuário do [!DNL Journey Optimizer], siga os pré-requisitos listados em [esta seção](web-prerequisites.md).

## Comece a criar sua experiência na Web

Para começar a criar sua experiência online usando o visual web designer, siga as etapas abaixo.

>[!CAUTION]
>
>O [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR){target="_blank"} deve ser incluído na sua página da Web. [Saiba mais](web-prerequisites.md#implementation-prerequisites)

1. Na tela **[!UICONTROL Editar conteúdo]**, clique em **[!UICONTROL Editar página da Web]** para abrir o designer da Web.

   ![](assets/web-campaign-edit-web-page.png)

   <!--![](assets/web-designer.png)-->

   >[!NOTE]
   >
   >Se você tentar carregar um site que não é carregado, uma mensagem será exibida sugerindo que você instale a [extensão de navegador Auxiliar de edição visual](#install-visual-editing-helper). Veja algumas dicas para solução de problemas em [esta seção](web-prerequisites.md#troubleshooting).
   >
   >Você também pode editar o conteúdo da Web sem carregar o editor visual. Para fazer isso, desmarque a opção **[!UICONTROL Editor visual]** para usar o modo de edição não visual. [Saiba mais](web-non-visual-editor.md)

1. Uma vez no web designer, selecione qualquer elemento da tela, como imagem, botão, parágrafo, texto, contêiner, cabeçalho, link etc. [Saiba mais](#content-components)

1. Para editar um elemento, é possível usar:

   * O menu contextual para editar conteúdo, layout, inserir links ou personalização, etc.

     ![](assets/web-designer-contextual-bar.png)

   * Os ícones na parte superior do painel direito permitem editar, duplicar, excluir ou ocultar cada elemento.

     ![](assets/web-designer-right-panel-icons.png)

   * O painel direito que muda dinamicamente de acordo com o elemento selecionado. Por exemplo, você pode editar o plano de fundo, a tipografia, a borda, o tamanho, a posição, o espaçamento, os efeitos ou os estilos embutidos de um elemento.

     ![](assets/web-designer-right-panel.png)

>[!NOTE]
>
>O designer de conteúdo da Web é, em sua maioria, semelhante ao designer de email. Saiba mais sobre [como criar conteúdo com [!DNL Journey Optimizer]](../email/get-started-email-design.md).

Após editar o conteúdo da Web, você pode gerenciar as modificações. [Saiba mais](manage-web-modifications.md)

## Usar componentes {#content-components}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_components"
>title="Adicionar componentes à página da Web"
>abstract="Você pode adicionar vários componentes à sua página da Web e editá-los conforme necessário."

1. No painel **[!UICONTROL Componentes]** à esquerda, selecione um item. Você pode adicionar os seguintes componentes à sua página da Web e editá-los conforme necessário:

   * [Divisor](../email/content-components.md#divider)
   * [HTML](../email/content-components.md#HTML)
   * [Imagem](../email/content-components.md#image)
   * Cabeçalho - O uso deste componente é semelhante ao uso do componente **[!UICONTROL Texto]** no designer de email. [Saiba mais](../email/content-components.md#text)
   * Parágrafo - O uso deste componente é semelhante ao uso do componente **[!UICONTROL Texto]** no designer de email. [Saiba mais](../email/content-components.md#text)
   * Link

   ![](assets/web-designer-components.png)

1. Passe o mouse na página e clique no botão **[!UICONTROL Inserir antes de]** ou **[!UICONTROL Inserir depois de]** para anexar o componente a um elemento existente na página.

   ![](assets/web-designer-insert-components.png)

   >[!NOTE]
   >
   >Para desmarcar um componente, clique no botão **[!UICONTROL ESC]** no banner azul contextual exibido na parte superior da tela.

1. Edite o componente conforme necessário diretamente no conteúdo da página.

   ![](assets/web-designer-edit-header.png)

1. Ajuste os estilos exibidos no painel contextual à direita, como plano de fundo, cor do texto, borda, tamanho, posição etc. - dependendo do componente selecionado.

   ![](assets/web-designer-header-style.png)

## Adicionar personalização

Para adicionar personalização, selecione um container e selecione o ícone de personalização na barra de menu contextual exibida. Adicione as alterações usando o editor de personalização. [Saiba mais](../personalization/personalization-build-expressions.md)

![](assets/web-designer-personalization.png)

## Navegar pelo web designer {#navigate-web-designer}

Esta seção detalha as diferentes maneiras de navegar pelo web designer. Para exibir e gerenciar as modificações adicionadas à sua experiência online, consulte [esta seção](manage-web-modifications.md).

### Usar navegações estruturais {#breadcrumbs}

1. Selecione qualquer elemento da tela.

1. Clique no botão **[!UICONTROL Expandir/Recolher navegações estruturais]** no lado inferior esquerdo da tela para exibir rapidamente as informações sobre o elemento selecionado.

   ![](assets/web-designer-breadcrumbs.png)

1. Quando você passa o mouse sobre a navegação estrutural, o elemento correspondente é realçado no editor.

1. Ao usá-lo, você pode navegar facilmente para qualquer elemento pai, irmão ou filho no editor visual.

### Alternar para o modo de navegação {#browse-mode}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_browse"
>title="Usar o modo de navegação"
>abstract="Nesse modo, é possível navegar até a página exata da configuração selecionada que deseja personalizar."

Você pode alternar do modo padrão **[!UICONTROL Design]** para o modo **[!UICONTROL Procurar]** usando o botão dedicado.

![](assets/web-designer-browse-mode.png)

No modo **[!UICONTROL Procurar]**, você pode navegar para a página exata a partir da configuração selecionada que deseja personalizar.

É especialmente útil ao lidar com páginas que estão por trás da autenticação ou que não estão disponíveis desde o início em um determinado URL. Por exemplo, você poderá autenticar, navegar até a página da sua conta ou até a página do carrinho e voltar para o modo **[!UICONTROL Design]** para executar as alterações na página desejada.

Usar o modo de **[!UICONTROL Navegação]** também permite que você navegue por todas as exibições do seu site ao criar aplicativos de página única. [Saiba mais](web-spa.md)

### Alterar tamanho do dispositivo {#change-device-size}

Você pode alterar o tamanho do dispositivo da exibição do web designer para um tamanho predefinido, como **[!UICONTROL Tablet]** ou **[!UICONTROL Paisagem móvel]**, ou definir um tamanho personalizado inserindo o número desejado de pixels.

Também é possível alterar o foco do zoom de 25% para 400%.

![](assets/web-designer-device.png)

A capacidade de alterar o tamanho do dispositivo foi projetada para sites responsivos que são renderizados em vários dispositivos, janelas e tamanhos de tela. Sites responsivos ajustam-se e se adaptam automaticamente a qualquer tamanho de tela, incluindo desktops, laptops, tablets ou telefones celulares.

>[!CAUTION]
>
>É possível editar uma experiência da Web com um tamanho de dispositivo específico. No entanto, desde que os seletores sejam os mesmos, essas alterações se aplicam a todos os tamanhos e dispositivos, não apenas ao tamanho do dispositivo em que você está trabalhando. Da mesma forma, editar uma experiência na exibição de desktop normal aplica as alterações a todos os tamanhos de tela, não apenas à exibição de desktop.
>
>Atualmente, o [!DNL Journey Optimizer] não oferece suporte a alterações de página específicas de tamanho de dispositivo. Isso significa que, por exemplo, se você tiver um site móvel separado com uma estrutura de site separada, deverá fazer as alterações específicas no site móvel em uma campanha diferente.

## Vídeo tutorial{#video}

O vídeo abaixo mostra como criar uma experiência na Web usando o web designer em campanhas do [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3452640/?quality=12&learn=on&captions=por_br)
