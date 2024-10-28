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
source-git-commit: bcccc7b385f031fba2c2b57ec62cae127eda8466
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 14%

---

# Criar um fragmento {#create-fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_visual_fragment"
>title="Selecione o tipo “Visual”"
>abstract="Crie um fragmento visual independente para tornar o conteúdo reutilizável em um email de uma jornada ou campanha ou em um modelo de conteúdo."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/email/design-email/add-content/use-visual-fragments" text="Adicionar fragmentos visuais aos emails"

>[!CONTEXTUALHELP]
>id="ajo_create_expression_fragment"
>title="Selecione o tipo “Expressão”"
>abstract="Crie um fragmento de expressão independente para tornar seu conteúdo reutilizável em várias jornadas e campanhas. Ao usar o editor de personalização, é possível aproveitar todos os fragmentos de expressão criados na sandbox atual."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/content-management/personalization/expression-editor/use-expression-fragments" text="Aproveitar fragmentos de expressão"

Os fragmentos podem ser criados do zero no menu esquerdo **[!UICONTROL Fragmentos]**. Além disso, também é possível salvar uma parte do conteúdo existente como fragmento ao projetar o conteúdo. [Saiba como](#save-as-fragment)

Depois de salvo, o fragmento fica disponível para uso em uma jornada, campanha ou template. Você pode usar esse fragmento ao criar qualquer conteúdo em jornadas e campanhas. Consulte [Adicionar fragmentos visuais](../email/use-visual-fragments.md) e [Aproveitar fragmentos de expressão](../personalization/use-expression-fragments.md)

Para criar um fragmento, siga as etapas abaixo.

## Definir as propriedades do fragmento {#properties}

1. Acesse a lista de fragmentos por meio do menu esquerdo **[!UICONTROL Gerenciamento de conteúdo]** > **[!UICONTROL Fragmentos]**.

1. Selecione **[!UICONTROL Criar fragmento]** e preencha o nome e a descrição do fragmento (se necessário).

   ![](assets/fragment-details.png)

1. Selecione ou crie tags do Adobe Experience Platform a partir do campo **[!UICONTROL Tags]** para categorizar seu fragmento para pesquisa aprimorada. [Saiba como trabalhar com Marcas Unificadas](../start/search-filter-categorize.md#tags)

1. Selecione o tipo de fragmento: **Fragmento visual** ou **Fragmento de expressão**. [Saiba mais sobre fragmentos visuais e de expressão](../content-management/fragments.md#visual-expression)

   >[!NOTE]
   >
   >Por enquanto, os fragmentos visuais estão disponíveis somente para o canal **Email**.

1. Se você estiver criando um fragmento de expressão, selecione o tipo de código que deseja usar: **[!UICONTROL HTML]**, **[!UICONTROL JSON]** ou **[!UICONTROL Text]**.

   ![](assets/fragment-expression-type.png)

1. Para atribuir rótulos de uso de dados personalizados ou principais ao fragmento, clique no botão **[!UICONTROL Gerenciar acesso]** na seção superior da tela. [Saiba mais sobre OLAC (Controle de Acesso em Nível de Objeto)](../administration/object-based-access.md).

1. Clique em **[!UICONTROL Criar]** para criar o conteúdo do fragmento.

## Criar o conteúdo do fragmento {#content}

Após configurar as propriedades do fragmento, o Designer de email ou o editor de personalização é aberto, dependendo do tipo de fragmento que você está criando.

* Para fragmentos visuais, edite o conteúdo conforme necessário, da mesma forma que faria para qualquer email dentro de uma jornada ou campanha. [Saiba mais](../email/get-started-email-design.md)

  ![](assets/fragment-designer.png)

* Para fragmentos de expressão, aproveite o editor de personalização do [!DNL Journey Optimizer] com todos os seus recursos de personalização e criação para criar o conteúdo do fragmento. [Saiba mais](../personalization/personalization-build-expressions.md)

  ![](assets/fragment-expression-editor.png)

Quando o conteúdo estiver pronto, clique no botão **Salvar**. O fragmento é criado e adicionado à lista de fragmentos com o status **Rascunho**. Você pode visualizá-la e publicá-la para torná-la disponível em jornadas e campanhas.

## Pré-visualizar e publicar o fragmento {#publish}

>[!NOTE]
>
>Para publicar um fragmento, você deve ter a permissão de usuário [Fragmento do Publish](../administration/ootb-product-profiles.md#content-library-manager).

Se o fragmento estiver pronto para entrar no ar, você poderá visualizá-lo e publicá-lo para disponibilizá-lo em suas jornadas e campanhas. Para fazer isso, siga estes passos:

1. Volte para a tela de criação do fragmento depois de criar o conteúdo ou abra-o a partir da lista de fragmentos.

1. Uma visualização do fragmento está disponível no campo **Tags**, permitindo verificar sua renderização. Se precisar fazer alguma alteração, clique no botão **Editar** na seção superior da tela para abrir o Designer de email ou o editor de personalização, dependendo do tipo de fragmento.

   ![](assets/fragment-preview.png)

1. Clique no botão **Publish** no canto superior direito para publicar o fragmento.

   Se o fragmento estiver sendo usado em uma jornada ou campanha em tempo real, uma mensagem é aberta para informá-lo. Clique no link **Ver mais** para acessar a lista de jornadas e/ou campanhas às quais ele é referenciado. [Saiba como explorar referências de um fragmento](../content-management/manage-fragments.md#explore-references)

   Clique em **Confirmar** para publicar o fragmento e atualizá-lo nas jornadas/campanhas ativas que o estão usando.

   ![](assets/fragment-publish.png){width="70%" align="center"}

O fragmento agora está **Ativo** e fica disponível ao criar qualquer conteúdo no [!DNL Journey Optimizer] Email Designer ou no editor de personalização:

* [Saiba como usar fragmentos visuais](../email/use-visual-fragments.md)
* [Saiba como usar fragmentos de expressão](../personalization/use-expression-fragments.md)
