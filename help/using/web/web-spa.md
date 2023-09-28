---
title: Criar aplicativos de página única
description: Saiba como criar SPA e aplicar modificações a diferentes visualizações no Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
source-git-commit: 59412ecbb8df74c7185b67593131c610d6da4148
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 6%

---

# Criar aplicativos de página única {#web-author-spas}

## Sobre visualizações {#about-views}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications_views"
>title="Aplicar alterações às exibições selecionadas"
>abstract="As alterações serão aplicadas somente às exibições selecionadas. As exibições podem ser descobertas usando o **Procurar** e navegue até eles. Não consegue localizar a exibição que você está procurando?"
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR" text="Saiba mais"

**Aplicativos de página única** (SPA) agora pode ser criado no editor visual do web designer. Isso permite selecionar em quais exibições específicas você deseja aplicar as modificações da página da Web.

Uma exibição pode ser definida como um site inteiro ou um grupo de elementos visuais em um site, como a página inicial, o site de produtos inteiro ou o quadro de preferências de entrega em todas as páginas de check-out.

É necessária uma configuração de desenvolvedor única para definir as exibições na implementação do SDK da Web da Adobe Experience Platform. Isso permite criar e executar campanhas da Web do Adobe Journey Optimizer no SPA.

## Definir exibições na implementação do SDK da Web {#define-views}

As visualizações XDM podem ser aproveitadas no Adobe [!DNL Journey Optimizer] para capacitar profissionais de marketing a executar campanhas de personalização e experimentação na web sobre SPA por meio do editor visual da web. [Saiba mais](web-spa-implementation.md)

Para acessar e criar exibições na variável [!DNL Journey Optimizer] de usuário, siga as etapas listadas em [nesta seção](web-spa-implementation.md#implement-xdm-views).

## Descobrir exibições no web designer {#discover-views}

Depois que a configuração do SPA for concluída na implementação do SDK da Web da Adobe Experience Platform, será necessário navegar por todas as exibições do site às quais deseja aplicar modificações. Siga as etapas abaixo.

1. [Criar uma campanha da Web](create-web.md) e acesse o [web designer](edit-web-content.md).

   A visualização em que você está no momento é exibida no canto superior esquerdo.

   ![](assets/web-designer-view-home.png)

1. Trocar para **[!UICONTROL Procurar]** modo. [Saiba mais](../web/edit-web-content.md#browse-mode)

   ![](assets/web-designer-view-browse.png)

1. Navegue entre as diferentes páginas do site para descobrir todas elas. O nome da exibição exibido na parte superior muda quando você passa por outra página.

   ![](assets/web-designer-other-view.png)

## Aplicar modificações a outras exibições {#apply-modifications-views}

Depois de ter modificado enquanto estava em uma exibição específica, você pode aplicá-la a outras exibições selecionadas. Siga as etapas abaixo.

>[!CAUTION]
>
>Se você não tiver descoberto as exibições usando o **[!UICONTROL Procurar]** você não poderá selecioná-las para aplicar suas modificações. [Saiba mais](#discover-views)

1. Selecione o **[!UICONTROL Modificações]** ícone para exibir o painel correspondente à esquerda.

   ![](assets/web-designer-view-modifications-pane.png)

1. Selecione qualquer modificação e clique no botão **[!UICONTROL Mais ações]** botão ao lado dele. Selecionar **[!UICONTROL Aplicar a mais visualizações]**.

   ![](assets/web-designer-modifications-more-actions.png)

1. Selecione as exibições às quais deseja aplicar as alterações.

   ![](assets/web-designer-modifications-apply-to.png)

1. Clique em **[!UICONTROL Aplicar]**.

1. Trocar para **[!UICONTROL Procurar]** para verificar se as modificações são aplicadas nas páginas desejadas.

   ![](assets/web-designer-modifications-applied-view.png)