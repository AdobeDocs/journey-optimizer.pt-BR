---
solution: Journey Optimizer
product: journey optimizer
title: Criar um fragmento
description: Saiba como criar fragmentos para reutilizar conteúdo em campanhas e jornadas do Journey Optimizer
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: da3ffe9c-a244-4246-b4b5-a3a1d0508676
source-git-commit: f47160f40abd9427cb9b9c793ee0ab402bf9f65b
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 23%

---

# Criar um fragmento do zero {#create-fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_visual_fragment"
>title="Selecione o tipo “Visual”"
>abstract="Crie um fragmento visual independente para tornar o conteúdo reutilizável em um email de uma jornada ou campanha ou em um modelo de conteúdo."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/email/design-email/add-content/use-visual-fragments.html?lang=pt-BR" text="Adicionar fragmentos visuais aos emails"

>[!CONTEXTUALHELP]
>id="ajo_create_expression_fragment"
>title="Selecione o tipo “Expressão”"
>abstract="Crie um fragmento de expressão independente para tornar seu conteúdo reutilizável em várias jornadas e campanhas. Ao usar o editor de personalização, é possível aproveitar todos os fragmentos de expressão criados na sandbox atual."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/personalization/expression-editor/use-expression-fragments.html?lang=pt-BR" text="Aproveitar fragmentos de expressão"

Fragmentos são criados a partir do **[!UICONTROL Fragmentos]** menu esquerdo. Além disso, também é possível salvar uma parte do conteúdo existente como fragmento ao projetar o conteúdo. [Saiba como](#save-as-fragment)

Depois de salvo, o fragmento fica disponível para uso em uma jornada, campanha ou template. Agora você pode usar este fragmento ao criar qualquer conteúdo no [!DNL Journey Optimizer]. Consulte [Adicionar fragmentos visuais](../email/use-visual-fragments.md) e [Aproveitar fragmentos de expressão](../personalization/use-expression-fragments.md)

Para criar um fragmento do zero, siga as etapas abaixo.

1. [Acessar a lista de fragmentos](#access-manage-fragments) por meio da **[!UICONTROL Gestão de conteúdo]** > **[!UICONTROL Fragmentos]** menu esquerdo.

1. Selecionar **[!UICONTROL Criar fragmento]**.

1. Preencha os detalhes do fragmento, ou seja, nome e descrição (se necessário).

   ![](assets/fragment-details.png)

1. Selecione ou crie tags do Adobe Experience Platform na **[!UICONTROL Tags]** para categorizar seu fragmento para pesquisa aprimorada. [Saiba mais](../start/search-filter-categorize.md#tags)

1. Selecione o tipo de fragmento: [Fragmento visual](#create-visual-fragment) ou [Fragmento da expressão](#create-expression-fragment).

   >[!NOTE]
   >
   >Atualmente, para fragmentos visuais, somente a variável **E-mail** canal é compatível.

1. Se estiver criando um fragmento de expressão, selecione o tipo de código que deseja usar: **[!UICONTROL HTML]**, **[!UICONTROL JSON]** ou **[!UICONTROL Texto]**.

   ![](assets/fragment-expression-type.png)

1. Para atribuir rótulos de uso de dados personalizados ou principais ao fragmento, selecione **[!UICONTROL Gerenciar acesso]**. [Saiba mais sobre o OLAC (Object Level Access Control)](../administration/object-based-access.md).

1. Clique em **[!UICONTROL Criar]**.

1. A variável [Email Designer](../email/get-started-email-design.md) ou o editor de personalização se abre, dependendo do tipo de fragmento que você está criando.

   * Para fragmentos visuais, edite o conteúdo conforme necessário, da mesma forma que faria para qualquer email dentro de uma jornada ou campanha.

     >[!NOTE]
     >
     >Você pode adicionar campos de personalização e conteúdo dinâmico, mas os atributos contextuais não são compatíveis com fragmentos.

     ![](assets/fragment-designer.png)

   * Para fragmentos de expressão, utilize o [!DNL Journey Optimizer] o editor de personalização com todos os seus recursos de personalização e criação para criar o conteúdo do fragmento. [Saiba mais](../personalization/personalization-build-expressions.md)

     ![](assets/fragment-expression-editor.png)

1. Quando o fragmento estiver pronto, clique em **[!UICONTROL Salvar]**.

O fragmento é adicionado à variável [lista de fragmentos](#access-manage-fragments). Agora ele está pronto para ser usado ao criar qualquer conteúdo na [!DNL Journey Optimizer] Designer de email ou editor de personalização.

* [Saiba como usar fragmentos visuais](../email/use-visual-fragments.md)
* [Saiba como usar fragmentos de expressão](../personalization/use-expression-fragments.md)
