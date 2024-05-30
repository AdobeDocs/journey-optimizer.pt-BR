---
solution: Journey Optimizer
product: journey optimizer
title: Gerenciar fragmentos
description: Saiba como gerenciar os fragmentos de conteúdo
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
source-git-commit: 83997271d16e15fb0d7ccdd21aa8ac8b8221a0d5
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 2%

---


# Gerenciar fragmentos {#manage-fragments}

Para gerenciar os fragmentos, acesse a lista de fragmentos na **[!UICONTROL Gestão de conteúdo]** > **[!UICONTROL Fragmentos]** menu esquerdo.

![](assets/fragment-list.png)

Todos os fragmentos criados na sandbox atual - ou [do **[!UICONTROL Fragmentos]** menu](#create-fragments), utilizando o [Salvar como fragmento](#save-as-fragment) opção - são exibidas.

Você pode filtrar fragmentos em:

* Tipo: **[!UICONTROL Visual]** ou **[!UICONTROL Expressão]**
* Tags
* Data de criação ou modificação

Você pode optar por mostrar todos os fragmentos ou somente os itens que o usuário atual criou ou modificou.

Também é possível exibir a variável **[!UICONTROL Arquivado]** fragmentos. [Saiba mais](#archive-fragments)

![](assets/fragment-list-filters.png)

No **[!UICONTROL Mais ações]** ao lado de cada fragmento, é possível:

* Duplique um fragmento.

* Use o **[!UICONTROL Explorar referências]** opção para ver as jornadas, campanhas ou templates onde são usados. [Saiba mais](#explore-references)

* Arquivar um fragmento. [Saiba mais](#archive-fragments)

* Editar o de um fragmento [tags](../start/search-filter-categorize.md#tags).

![](assets/fragment-list-more-actions.png)

## Editar fragmentos {#edit-fragments}

Para editar um fragmento, siga as etapas abaixo.

1. Clique no item desejado na guia **[!UICONTROL Fragmentos]** lista.
1. Nas propriedades do fragmento, é possível [explorar referências](#explore-references), [gerenciar seu acesso](../administration/object-based-access.md)e atualize os detalhes do fragmento, incluindo [tags](../start/search-filter-categorize.md#tags).

   ![](../email/assets/fragment-edit-content.png)

1. Selecione o botão correspondente para editar o conteúdo da mesma forma que faria ao criar um fragmento do zero. [Saiba mais](#create-from-scratch)

>[!NOTE]
>
>Ao editar um fragmento, as alterações são propagadas automaticamente para todo o conteúdo usando esse fragmento, exceto o conteúdo usado em **[!UICONTROL Ao vivo]** jornadas ou campanhas. Também é possível quebrar a herança do fragmento original. Saiba mais na [Adicionar fragmentos visuais aos seus emails](../email/use-visual-fragments.md#break-inheritance) e [Aproveitar fragmentos de expressão](../personalization/use-expression-fragments.md#break-inheritance) seções.

## Explorar referências {#explore-references}

Você pode exibir a lista de jornadas, campanhas e modelos de conteúdo que estão usando um fragmento no momento.

Para fazer isso, selecione **[!UICONTROL Explorar referências]** na caixa **[!UICONTROL Mais ações]** na lista de fragmentos ou na tela propriedades do fragmento.

![](assets/fragment-explore-references.png)

Selecione uma guia para alternar entre jornadas, campanhas, modelos e fragmentos. Você pode ver o status e clicar em um nome a ser redirecionado para o item correspondente onde o fragmento é referenciado.

![](assets/fragment-usage-screen.png)

>[!NOTE]
>
>Se o fragmento for usado em uma jornada, campanha ou modelo que tenha um rótulo que o impeça de acessá-lo, você verá uma mensagem de alerta na parte superior da guia selecionada. [Saiba mais sobre o OLAC (Object Level Access Control)](../administration/object-based-access.md)

## Arquivar fragmentos {#archive-fragments}

Você pode limpar a lista de fragmentos dos itens que não são mais relevantes para sua marca.

Para fazer isso, clique no link **[!UICONTROL Mais ações]** ao lado do fragmento desejado e selecione **[!UICONTROL Arquivar]**. Ele desaparecerá da lista de fragmentos, o que impede que os usuários o usem em emails ou modelos futuros.

![](assets/fragment-list-archive.png)

>[!NOTE]
>
>Se você arquivar um fragmento usado em um conteúdo, <!--it will remain in the email or template, but you won't be able to select it from the fragment list to edit it-->que o conteúdo não será afetado.

Para desarquivar um fragmento, filtre na variável **[!UICONTROL Arquivado]** itens e selecione **[!UICONTROL Desarquivar]** do **[!UICONTROL Mais ações]** menu. Agora ele pode ser acessado novamente na lista de fragmentos e pode ser usado em qualquer email ou modelo.

![](assets/fragment-list-unarchive.png)
