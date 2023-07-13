---
title: Páginas da Web de autor
description: Saiba como criar uma página da Web e editar seu conteúdo no Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: 3847ac1d-2c0a-4f80-8df9-e8e304faf261
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '1623'
ht-degree: 14%

---

# Páginas da Web de autor {#author-web}

Uma vez que [adicionou uma ação da web](create-web.md#create-web-campaign) para editar o conteúdo do site usando o web designer.

Entrada [!DNL Journey Optimizer], a criação na web é possibilitada pelo **Adobe Experience Cloud Visual Helper** extensão do navegador chrome. [Saiba mais](web-prerequisites.md#visual-authoring-prerequisites)

>[!CAUTION]
>
>Para acessar e criar páginas da Web na [!DNL Journey Optimizer] verifique se você segue os pré-requisitos listados na [nesta seção](web-prerequisites.md).

[Saiba como criar uma campanha da Web neste vídeo](#video)

## Editar conteúdo da página da Web {#edit-web-content}

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_surface"
>title="Confirmar o URL para editar"
>abstract="Confirme o URL da página da Web específica a ser usada para editar o conteúdo que será aplicado na superfície da Web definida acima. A página da Web deve ser implementada usando o SDK da Web da Adobe Experience Platform."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR" text="Saiba mais"

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_rule"
>title="Inserir o URL para editar"
>abstract="Insira o URL de uma página da Web específica a ser usada para editar o conteúdo que será aplicado a todas as páginas que correspondem à regra. A página da Web deve ser implementada usando o SDK da Web da Adobe Experience Platform."
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

1. Use:

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
>title="Adicionar componentes à página da Web"
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

Para adicionar personalização, selecione um container e selecione o ícone de personalização na barra de menu contextual exibida. Adicione as alterações usando o Editor de expressão. [Saiba mais](../personalization/personalization-build-expressions.md)

![](assets/web-designer-personalization.png)

Use o **[!UICONTROL Decisão de oferta]** componente a ser inserido [ofertas](../offers/get-started/starting-offer-decisioning.md) em suas páginas da Web. O processo é o mesmo de quando [adicionar uma oferta a um email](../email/add-offers-email.md). Ele aproveitará o Gerenciamento de decisão para escolher a melhor oferta a ser entregue aos clientes.

![](assets/web-designer-offer.png)

## Gerenciar modificações {#manage-modifications}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications"
>title="Gerenciar facilmente todas as alterações"
>abstract="Usando esse painel, você pode navegar e gerenciar todos os ajustes e estilos adicionados à sua página da Web."

É possível gerenciar facilmente todos os componentes, ajustes e estilos adicionados à página da Web.

1. Selecione o **[!UICONTROL Modificações]** ícone para exibir o painel correspondente à esquerda.

   ![](assets/web-designer-modifications-pane.png)

1. Você pode revisar cada uma das alterações feitas na página.

1. Selecione uma modificação indesejada e clique no ícone Excluir para removê-la.

   ![](assets/web-designer-modifications-delete.png)

   >[!CAUTION]
   >
   >Continue com cuidado ao excluir uma ação, pois ela pode afetar as ações subsequentes.

1. Use o **[!UICONTROL Mais ações]** na parte superior do **[!UICONTROL Modificações]** para excluir todas as modificações de uma só vez.

   ![](assets/web-designer-delete-modifications.png)

1. No **[!UICONTROL Mais ações]** você também pode excluir somente as modificações inválidas, ou seja, as alterações que foram substituídas por outras alterações. Por exemplo, se você modificar a cor de um texto e, em seguida, excluir esse texto, a modificação de cor se tornará inválida, pois o texto não existe mais.

1. Também é possível cancelar e refazer ações usando a variável **[!UICONTROL Desfazer/Refazer]** botão na parte superior direita da tela.

   ![](assets/web-designer-undo-redo.png)

   Clique e mantenha pressionado o botão para alternar entre as **[!UICONTROL Desfazer]** e **[!UICONTROL Refazer]** opções. Em seguida, clique no próprio botão para aplicar a ação desejada.

## Usar o rastreamento de cliques {#use-click-tracing}

Essa capacidade no web designer permite selecionar qualquer elemento do site e rastrear os cliques nesse elemento.

Assim que a campanha estiver ativa, você poderá verificar o número de cliques para cada elemento no relatório da Web da campanha. Essas informações podem ser úteis para melhorar a experiência dos usuários do site. Por exemplo, se a variável [relatórios da web](../reports/campaign-global-report.md#web-tab) Para mostrar que muitos usuários clicam em um elemento que não é realmente clicável, talvez você queira adicionar um link a esse elemento.

1. Selecione um elemento na página e escolha **[!UICONTROL Clicar no elemento de rastreamento]** no menu contextual.

   ![](assets/web-designer-click-track.png)

   >[!NOTE]
   >
   >Qualquer item, clicável ou não, pode ser selecionado.

1. A ação rastreada correspondente é exibida automaticamente na variável **[!UICONTROL Rastrear cliques]** à esquerda.

   ![](assets/web-designer-click-track-pane.png)

1. Adicione um rótulo significativo para gerenciar todos os elementos rastreados e encontrá-los facilmente nos relatórios. A variável **[!UICONTROL Seletor de CSS]** O campo mostra informações para localizar o elemento selecionado.

1. Repita as etapas acima para selecionar quantos outros elementos forem necessários para o rastreamento de cliques. As ações correspondentes são todas listadas no painel esquerdo.

   ![](assets/web-designer-click-tracking-actions.png)

1. Para remover o rastreamento de cliques em um elemento, selecione o ícone excluir correspondente.

Quando a campanha estiver ativa, você pode verificar o relatório da campanha **[!UICONTROL Web]** para comparar o número de impressões, a taxa de cliques e o número de cliques por elemento. [Saiba mais](../reports/campaign-global-report.md#web-tab)

## Navegar pelo web designer {#navigate-web-designer}

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
>abstract="Nesse modo, você pode navegar até a página exata da superfície selecionada que deseja personalizar."

Você pode trocar do padrão **[!UICONTROL Design]** para o modo **[!UICONTROL Procurar]** usando o botão dedicado.

![](assets/web-designer-browse-mode.png)

No **[!UICONTROL Procurar]** , você pode navegar para a página exata a partir da superfície selecionada que deseja personalizar.

É especialmente útil ao lidar com páginas que estão por trás da autenticação ou que não estão disponíveis desde o início em um determinado URL. Por exemplo, você poderá se autenticar, navegar até a página da sua conta ou até a página do carrinho e voltar para **[!UICONTROL Design]** para executar as alterações na página desejada.

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

## Testar a campanha da Web {#test-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_preview"
>title="Visualizar a experiência da Web"
>abstract="Acesse uma simulação de como sua experiência da Web será."

Para exibir uma pré-visualização de sua experiência da Web modificada, siga as etapas abaixo.

>[!CAUTION]
>
>Você deve ter perfis de teste disponíveis para simular quais ofertas serão entregues a eles. Saiba como [criar perfis de teste](../audience/creating-test-profiles.md).

1. Na tela de conteúdo de edição da campanha da Web, selecione **[!UICONTROL Simular conteúdo]**.

   <!--![](assets/web-designer-simulate.png)-->

   ![](assets/web-campaign-simulate.png)

1. Clique em **[!UICONTROL Gerenciar perfis de teste]** para selecionar um ou mais perfis de teste.
1. Uma pré-visualização da página da Web modificada é exibida.

   ![](assets/web-designer-preview.png)

1. Você também pode abri-lo no navegador padrão ou copiar o URL de teste para colá-lo em qualquer navegador. Isso permite compartilhar o link com a equipe e as partes interessadas, que poderão visualizar a nova experiência da Web em qualquer navegador antes que a campanha entre em vigor.

   >[!NOTE]
   >
   >Ao copiar o URL de teste, o conteúdo exibido é aquele personalizado para o perfil de teste usado quando a simulação de conteúdo foi gerada no [!DNL Journey Optimizer].

## Vídeo explicativo{#video}

O vídeo abaixo mostra como criar uma experiência na Web usando o designer da Web no [!DNL Journey Optimizer] campanhas.

>[!VIDEO](https://video.tv.adobe.com/v/3418803/?quality=12&learn=on)
