---
title: Editar conteúdo usando o editor não visual
description: Saiba como criar uma página da Web e editar seu conteúdo usando o editor não visual do Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Experienced
exl-id: 00d2fc73-3ac8-421c-982a-0f3ec7e3dacd
TQID: https://experienceleague.adobe.com/AVN9LN-KzTpcMx-dexxN7i1i2nB4496dzSZ473a3NJE
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: c618a0dc-1818-4c6d-9916-0d92e6796f24
  - id: d056adbe-402d-4f42-9746-f3d424e598b1
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e9001ce2-5245-4a8e-8601-dd958009072f
source-git-commit: 4bae03291d44603ab1648416f34dd1a8b414a07a
workflow-type: tm+mt
source-wordcount: 427
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

1. Na lista suspensa, selecione o tipo de modificação.

   Dois tipos estão disponíveis. Eles vêm com opções diferentes. Consulte os links abaixo para obter mais detalhes:

   * **[!UICONTROL Seletor de CSS]** - [Saiba mais](manage-web-modifications.md#css-selector)
   * **[!UICONTROL Página`<head>`]** - [Saiba mais](manage-web-modifications.md#page-head)

1. Clique no botão **[!UICONTROL Adicionar personalização]**. O editor de personalização é aberto.

   Você pode aproveitar o editor de personalização do [!DNL Journey Optimizer] com todos os seus recursos de personalização e criação. [Saiba mais](../personalization/personalization-build-expressions.md)

1. Insira seu conteúdo e **[!UICONTROL Salve]** suas alterações.

   ![](assets/web-non-visual-editor-ex-save.png)

1. Sua primeira modificação é exibida na parte superior do painel **[!UICONTROL Modificações]**.

   Clique no botão **[!UICONTROL Mais ações]** ao lado da sua modificação e selecione **[!UICONTROL Informações]** para exibir seus detalhes. Você também pode **[!UICONTROL Excluir a modificação]**, se necessário.

   ![](assets/web-non-visual-editor-ex-more.png){width="50%"}

   >[!NOTE]
   >
   >O painel **[!UICONTROL Modificações]** é igual ao usado com o [web designer](web-visual-editor.md). Todas as ações que você pode executar com ele estão detalhadas em [esta seção](manage-web-modifications.md#use-modifications-pane).

1. Clique no botão **[!UICONTROL Adicionar]** na parte superior do painel **[!UICONTROL Modificações]** para adicionar outra modificação e repita as etapas acima.


1. Além disso, você pode selecionar qualquer elemento do site e rastrear os cliques nesse elemento. Para ativar o rastreamento de cliques e definir as ações a serem rastreadas, clique no segundo ícone no painel à esquerda, conforme mostrado abaixo:

   ![](assets/web-campaign-click.png){width="50%"}

   Use o botão **Adicionar Componente** para selecionar uma nova ação a ser monitorada. Saiba mais sobre o uso do rastreamento de cliques em [esta seção](monitor-web-experiences.md#use-click-tracking).


1. Clique na seta na parte superior esquerda da tela para navegar de volta para a tela de edição de jornada ou campanha. Você pode ver o número atual de alterações e adicionar mais modificações.

   ![](assets/web-campaign-modifications.png)

   Você também pode alternar para o web designer, se desejar. Todas as modificações serão preservadas.
