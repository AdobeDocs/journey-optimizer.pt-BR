---
title: Páginas da Web de autor
description: Saiba como criar uma página da Web e editar seu conteúdo no Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 3847ac1d-2c0a-4f80-8df9-e8e304faf261
badge: label="Beta" type="Informativo"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 6%

---

# Páginas da Web de autor {#author-web}

>[!BEGINSHADEBOX]

O que você encontrará nesta documentação:

* [Introdução ao canal Web](get-started-web.md)
* [Criação de experiências da Web](create-web.md)
* **[Páginas da Web de autor](author-web.md)**
* [Extensão Auxiliar de edição visual](visual-editing-helper.md)
* [Relatórios da Web](web-report.md)

>[!ENDSHADEBOX]

Entrada [!DNL Journey Optimizer] a criação na web é possibilitada pela extensão de navegador chrome do Adobe Experience Cloud Visual Helper. [Saiba mais](visual-editing-helper.md)

Para acessar e criar páginas da Web na [!DNL Journey Optimizer] seguir os pré-requisitos listados na [nesta seção](create-web.md#prerequesites).

## Editar conteúdo da página da Web {#edit-web-content}

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

<!--Confirm the URL to use for authoring content on the surface. Typically the Authoring URL will be the surface URL itself, but you may include extra parameters if required. The page must include the Adobe Experience Platform Web SDK.-->

Depois de criar uma ação da Web a partir da campanha, você pode editar o conteúdo usando o web designer. Para isso, siga as etapas abaixo.

>[!CAUTION]
>
>Para ser acessado em [!DNL Journey Optimizer], sua página da Web deve ser implementada usando o [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR){target="_blank"}.

1. No **[!UICONTROL Ação]** da campanha, selecione **[!UICONTROL Editar conteúdo]** para começar a criar sua campanha da web.

1. Se você criou uma regra de correspondência de páginas, deve inserir qualquer URL que corresponda a essa regra. As alterações serão aplicadas a todas as páginas que correspondam à regra.

   >[!NOTE]
   >
   >Se você inseriu um único URL como a superfície da web, o URL para personalizar já está preenchido.

   ![](assets/web-edit-enter-url.png)

1. O conteúdo da página é exibido.

   >[!CAUTION]
   >
   >A página da Web deve incluir o [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR){target="_blank"}.

1. Clique em **[!UICONTROL Abrir web designer]** para editá-lo. [Saiba mais](author-web.md)

   ![](assets/web-open-designer.png)

1. O web designer é exibido.

   ![](assets/web-designer.png)

1. Selecione qualquer elemento da tela de desenho, como imagem, botão, parágrafo, texto, contêiner, cabeçalho, link etc. e usar:

   * O menu contextual para editar conteúdo, layout, inserir links ou personalização, etc.

      ![](assets/web-designer-contextual-bar.png)

   * Os ícones na parte superior do painel direito permitem editar, duplicar, excluir ou ocultar cada elemento.

      ![](assets/web-designer-right-panel-icons.png)

   * O painel direito que muda dinamicamente de acordo com o elemento selecionado. Por exemplo, você pode editar o plano de fundo, a tipografia, a borda, o tamanho, a posição, o espaçamento, os efeitos ou os estilos embutidos de um elemento.

      ![](assets/web-designer-right-panel.png)

## Usar componentes de conteúdo {#content-components}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_components"
>title="Adicionar componentes de conteúdo à página da Web"
>abstract="Você pode adicionar vários componentes à sua página da Web e editá-los conforme necessário."

1. No **[!UICONTROL Componentes]** à esquerda, você pode adicionar os seguintes componentes à sua página da Web e editá-los conforme necessário:

   * [Divisor](../email/content-components.md#divider)
   * [HTML](../email/content-components.md#HTML)
   * [Imagem](../email/content-components.md#image)
   * Cabeçalho - O uso desse componente é semelhante ao uso do **[!UICONTROL Texto]** componente no designer de email. [Saiba mais](../email/content-components.md#text)
   * Parágrafo - O uso deste componente é semelhante ao uso da variável **[!UICONTROL Texto]** componente no designer de email. [Saiba mais](../email/content-components.md#text)
   * Link - Saiba como definir o estilo de link no [nesta seção](../email/styling-links.md)
   * [Decisão de oferta](../email/add-offers-email.md)

   ![](assets/web-designer-components.png)

1. Passe o mouse na página e clique no ícone **[!UICONTROL Inserir antes de]** ou **[!UICONTROL Inserir depois de]** botão para anexar o componente a um elemento existente na página.

   ![](assets/web-designer-insert-components.png)

1. No contêiner exibido para esse componente, edite o conteúdo do componente conforme necessário.

   ![](assets/web-designer-edit-html.png)

1. Ajustar os estilos exibidos no **[!UICONTROL Container]** painel à direita, como plano de fundo, cor do texto, borda, tamanho, posição etc. dependendo do componente selecionado.

   ![](assets/web-designer-html-style.png)

## Navegar pelo web designer

### Usar navegações estruturais

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

### Alterar tamanho do dispositivo

É possível alterar o tamanho do dispositivo para um tamanho predefinido, como **[!UICONTROL Tablet]** ou **[!UICONTROL Paisagem móvel]** ou defina um tamanho personalizado. Insira o número desejado de pixels para definir um tamanho personalizado.

Também é possível alterar o foco do zoom de 25% para 400%.

![](assets/web-designer-device.png)

## Gerenciar modificações {#manage-modifications}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications"
>title="Gerenciar facilmente todas as suas alterações"
>abstract="Com esse painel, você pode navegar por todos os ajustes e estilos adicionados à sua página da Web e gerenciá-los."

É possível gerenciar facilmente todos os componentes, ajustes e estilos adicionados à página da Web.

1. Selecione o **[!UICONTROL Modificações]** botão para exibir o painel correspondente à esquerda.

   ![](assets/web-designer-modifications-pane.png)

1. Você pode revisar cada uma das alterações feitas na página.

1. Selecione uma modificação indesejada e clique no ícone Excluir para removê-la.

   ![](assets/web-designer-modifications-delete.png)

   >[!CAUTION]
   >
   >Continue com cuidado ao excluir uma ação, pois ela pode afetar as ações subsequentes.

1. Também é possível cancelar e refazer ações usando a variável **[!UICONTROL Desfazer/Refazer]** botão na parte superior direita da tela.

   ![](assets/web-designer-undo-redo.png)

   Clique e mantenha pressionado o botão para alternar entre as **[!UICONTROL Desfazer]** e **[!UICONTROL Refazer]** opções. Em seguida, clique no próprio botão para aplicar a ação desejada.

## Adicionar personalização e ofertas

Para adicionar personalização, selecione um container e selecione o ícone de personalização na barra de menu contextual exibida. Adicione as alterações usando o Editor de expressão. [Saiba mais](../personalization/personalization-build-expressions.md)

![](assets/web-designer-personalization.png)

Use o **[!UICONTROL Decisão de oferta]** componente a ser inserido [ofertas](../offers/get-started/starting-offer-decisioning.md) em suas páginas da Web. O processo é o mesmo de quando [adicionar uma oferta a um email](../email/add-offers-email.md). Ele aproveitará o Gerenciamento de decisão para escolher a melhor oferta a ser entregue aos clientes.

![](assets/web-designer-offer.png)

## Testar a campanha da Web {#test-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_preview"
>title="Pré-visualizar sua experiência online"
>abstract="Obtenha uma simulação de como será sua experiência na Web."

Para exibir uma pré-visualização de sua experiência da Web modificada, siga as etapas abaixo.

>[!CAUTION]
>
>Você deve ter perfis de teste disponíveis para simular quais ofertas serão entregues a eles. Saiba como [criar perfis de teste](../segment/creating-test-profiles.md).

1. De qualquer uma das **[!UICONTROL Editar conteúdo]** ou o web designer, selecione **[!UICONTROL Simular conteúdo]**.

   ![](assets/web-designer-simulate.png)

1. Clique em **[!UICONTROL Gerenciar perfis de teste]** para selecionar um ou mais perfis de teste.
1. Uma pré-visualização da página da Web modificada é exibida.

   ![](assets/web-designer-preview.png)

1. Você também pode copiar o URL de teste para colá-lo em qualquer navegador ou abri-lo no navegador padrão.
