---
title: Criar aplicativos de página única
description: Saiba como criar SPAs e aplicar modificações a diferentes exibições no Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Intermediate
exl-id: b33e4bca-d2e9-4610-9f04-008d47f686d0
TQID: https://experienceleague.adobe.com/clX0VeCEzwDOgxyFrzVaBIx-eH90KEYaHGTMzf2xvQc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2:
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e9001ce2-5245-4a8e-8601-dd958009072f
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 500
ht-degree: 27%

---

# Criar aplicativos de página única {#web-author-spas}

## Sobre visualizações {#about-views}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications_views"
>title="Aplicar alterações às exibições selecionadas"
>abstract="As alterações serão aplicadas somente às exibições selecionadas. As exibições podem ser descobertas usando o modo **Procurar**. Não consegue localizar uma exibição específica?"
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR" text="Saiba mais"

**Aplicativos de página única** (SPAs) agora podem ser criados no editor visual do designer da Web. Isso permite selecionar a quais **exibições** específicas você deseja aplicar as modificações da página da Web.

[Saiba como criar aplicativos de página única neste vídeo](#video)

Uma exibição pode ser definida como um site inteiro ou um grupo de elementos visuais de um site, como a página inicial, a totalidade do site de produtos ou o quadro de preferências de entrega em todas as páginas de check-out.

É necessária uma configuração de desenvolvedor única para definir as exibições na implementação do Adobe Experience Platform Web SDK. Isso permite criar e executar campanhas da Web do Adobe Journey Optimizer em SPAs.

## Definir exibições na implementação do Web SDK {#define-views}

As exibições XDM podem ser usadas no Adobe [!DNL Journey Optimizer] para capacitar os profissionais de marketing a executar campanhas de personalização e experimentação da Web em SPAs por meio do editor visual da Web. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-spa-implementation.html?lang=pt-BR){target="_blank"}

Para acessar e criar exibições na interface do usuário do [!DNL Journey Optimizer], siga as etapas listadas em [esta seção](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-spa-implementation.html?lang=pt-BR#implement-xdm-views){target="_blank"}.

## Descobrir exibições no web designer {#discover-views}

Depois que a configuração do SPAs for concluída na implementação do Adobe Experience Platform Web SDK, será necessário navegar por todas as exibições do site às quais deseja aplicar modificações. Siga as etapas abaixo.

1. [Crie uma jornada da Web ou campanha](create-web.md) e acesse o [web designer](web-visual-editor.md).

   A visualização em que você está no momento é exibida no canto superior esquerdo.

   ![](assets/web-designer-view-home.png)

1. Mudar para o modo **[!UICONTROL Procurar]**. [Saiba mais](web-visual-editor.md#browse-mode)

   ![](assets/web-designer-view-browse.png)

1. Navegue entre as diferentes páginas do site para descobrir todas elas. O nome da exibição exibido na parte superior muda quando você passa por outra página.

   ![](assets/web-designer-other-view.png)

## Aplicar modificações a outras exibições {#apply-modifications-views}

Após adicionar uma modificação enquanto estiver em uma exibição específica, você pode aplicá-la a outras exibições selecionadas. Siga as etapas abaixo.

>[!CAUTION]
>
>Se você não descobriu modos de exibição usando o modo de **[!UICONTROL Navegação]**, não poderá selecioná-los para aplicar suas modificações. [Saiba mais](#discover-views)

1. Selecione o ícone **[!UICONTROL Modificações]** para exibir o painel correspondente à esquerda.

   ![](assets/web-designer-view-modifications-pane.png)

1. Selecione qualquer modificação e clique no botão **[!UICONTROL Mais ações]** ao lado dela. Selecione **[!UICONTROL Aplicar a mais exibições]**.

   ![](assets/web-designer-modifications-more-actions.png)

1. Selecione as exibições às quais deseja aplicar as alterações.

   ![](assets/web-designer-modifications-apply-to.png)

1. Clique em **[!UICONTROL Aplicar]**.

1. Mude para o modo **[!UICONTROL Procurar]** para verificar se as modificações foram aplicadas nas páginas desejadas.

   ![](assets/web-designer-modifications-applied-view.png)

## Vídeo tutorial{#video}

Este vídeo explica como:

* Descobrir exibições SPA usando o modo **[!UICONTROL Procurar]**
* Criar na visualização atual
* Aplicar modificações de site em várias exibições ou em todas as que foram descobertas
* Realizar ações em massa em modificações

>[!VIDEO](https://video.tv.adobe.com/v/3424536/?quality=12&learn=on)
