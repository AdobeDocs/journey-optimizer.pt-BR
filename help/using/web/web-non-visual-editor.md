---
title: Editar conteúdo usando o editor não visual
description: Saiba como criar uma página da Web e editar seu conteúdo usando o editor não visual do Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Experienced
source-git-commit: 59fae238326186092a29d4a451655efabaabb4b2
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# Usar o editor não visual da Web {#web-non-visual-editor}

Além do [!DNL Journey Optimizer] visual [web designer](web-visual-editor.md), você também pode adicionar modificações às suas páginas da Web usando um **editor não visual**.

Isso pode ser útil se você não puder, ou não tiver permissão, instalar extensões de navegador, como o [Adobe Experience Cloud Visual Helper](web-prerequisites.md#visual-authoring-prerequisites), que é necessário para carregar suas páginas no web designer.

Em certos casos, também é possível usar um editor não visual para aplicar modificações em um seletor de CSS específico, sem o risco de modificar outros elementos em uma página da Web ou alterar a estrutura da página.

Para criar suas experiências da Web com o editor não visual, siga as etapas abaixo.

1. Na tela **[!UICONTROL Editar conteúdo]** da jornada ou campanha, desmarque a opção **[!UICONTROL Editor visual]**.

1. Clique em **[!UICONTROL Adicionar uma modificação]** para começar a editar o conteúdo da Web.

   ![](assets/web-campaign-add-modification-button.png)

1. O editor não visual é exibido. É possível adicionar a primeira modificação usando o painel esquerdo.

   ![](assets/web-non-visual-editor.png)

1. Selecione o tipo de modificação:

   * **[!UICONTROL Seletor de CSS]** - [Saiba mais](manage-web-modifications.md#css-selector)
   * **[!UICONTROL Página`<Head>`]** - [Saiba mais](manage-web-modifications.md#page-head)

1. Clique no botão **[!UICONTROL Opções de edição avançadas]**. O editor de personalização é aberto.

   Você pode aproveitar o editor de personalização do [!DNL Journey Optimizer] com todos os seus recursos de personalização e criação. [Saiba mais](../personalization/personalization-build-expressions.md)

1. Insira seu conteúdo e **[!UICONTROL Salve]** suas alterações.

   ![](assets/web-non-visual-editor-ex-save.png)

1. Sua primeira modificação é exibida na parte superior do painel **[!UICONTROL Modificações]**.

   Clique no botão **[!UICONTROL Mais ações]** ao lado da sua modificação e selecione **[!UICONTROL Informações]** para exibir seus detalhes. Você também pode **[!UICONTROL Editar]** ou **[!UICONTROL Excluir]** a modificação.

   ![](assets/web-non-visual-editor-ex-more.png)

   >[!NOTE]
   >
   >O painel **[!UICONTROL Modificações]** é igual ao usado com o [web designer](web-visual-editor.md). Todas as ações que você pode executar com ele estão detalhadas em [esta seção](manage-web-modifications.md#use-modifications-pane).

1. Clique no botão **[!UICONTROL Mais ações]** na parte superior do painel **[!UICONTROL Modificações]** para **[!UICONTROL Adicionar uma modificação]** e repita as etapas acima. [Saiba mais](manage-web-modifications.md#add-modifications)

   ![](assets/web-non-visual-editor-more.png)

1. Selecione a seta na parte superior esquerda da tela para voltar à tela de edição de jornada ou campanha. Você pode ver o número atual de alterações e adicionar mais modificações.

   ![](assets/web-campaign-modifications.png)

   Você também pode alternar para o web designer, se desejar. Todas as modificações serão preservadas.


1. Você pode selecionar qualquer elemento do site e rastrear os cliques nesse elemento. Para ativar o rastreamento de cliques e definir as ações a serem rastreadas, clique no segundo ícone no painel à esquerda, conforme mostrado abaixo:

   ![](assets/web-campaign-click.png)

   Use o botão **Adicionar Componente** para selecionar uma nova ação a ser monitorada. Saiba mais sobre o uso do rastreamento de cliques em [esta seção](monitor-web-experiences.md#use-click-tracking).
