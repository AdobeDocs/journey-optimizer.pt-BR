---
solution: Journey Optimizer
product: journey optimizer
title: Trabalhar com fragmentos
description: Saiba como criar fragmentos para reutilizar conteúdo em campanhas e jornadas do Journey Optimizer
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 7131a953-baca-4e7c-a8df-97c0bd6ac567
source-git-commit: 08f3fc1837a4daa1ecaa7afcd53c80381177efb0
workflow-type: tm+mt
source-wordcount: '1569'
ht-degree: 13%

---

# Trabalhar com fragmentos {#fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_fragment"
>title="Definir seus próprios fragmentos"
>abstract="Crie e gerencie fragmentos independentes para tornar o conteúdo reutilizável em várias jornadas e campanhas."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/reusable-content/fragments.html?lang=pt-BR#create-fragments" text="Criar fragmentos"

Um fragmento é um componente reutilizável que pode ser referenciado em um ou mais emails [!DNL Journey Optimizer] campanhas e jornadas.

Essa funcionalidade permite pré-criar vários blocos de conteúdo personalizados que podem ser usados por usuários de marketing para reunir rapidamente o conteúdo de email em um processo de design aprimorado.

![](../rn/assets/do-not-localize/fragments.gif)

➡️ [Saiba como gerenciar, criar e usar fragmentos nestes vídeos](#video-fragments)

Para aproveitar ao máximo os fragmentos:

* Crie seus próprios fragmentos. Você pode criar fragmentos visuais ou fragmentos de expressão. [Saiba mais](#create-fragments)

* Use-as quantas vezes forem necessárias em seu conteúdo. Consulte [Adicionar fragmentos visuais](../email/use-visual-fragments.md) e [Aproveitar fragmentos de expressão](../personalization/use-expression-fragments.md)

>[!NOTE]
>
>**Fragmentos visuais** pode ser usada na [Email Designer](../email/get-started-email-design.md), enquanto **fragmentos de expressão** são acessíveis através do [Editor de expressão](../personalization/personalization-build-expressions.md).

Além disso, você pode aproveitar o Journey Optimizer **API REST de conteúdo** para gerenciar fragmentos de conteúdo. Para obter mais informações, consulte [Documentação das APIs do Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/content/){target="_blank"}.

## Antes de começar {#fragment-prerequisites}

>[!CAUTION]
>
>Para criar, editar e arquivar fragmentos, você deve ter a **[!DNL Manage library items]** permissão incluída na **[!DNL Content Library Manager]** perfil do produto. [Saiba mais](../administration/ootb-product-profiles.md#content-library-manager)

Nesta versão, as seguintes limitações se aplicam:

* Os fragmentos visuais só estão disponíveis para o canal de email

* Os fragmentos de expressão não estão disponíveis para os canais na Web e no aplicativo

## Acessar e gerenciar fragmentos {#access-manage-fragments}

Para acessar a lista de fragmentos, selecione **[!UICONTROL Gestão de conteúdo]** > **[!UICONTROL Fragmentos]** no menu esquerdo.

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

* Copie um fragmento para outra sandbox. <!--Learn more?-->

* Arquivar um fragmento. [Saiba mais](#archive-fragments)

* Editar o de um fragmento [tags](../start/search-filter-categorize.md#tags).

![](assets/fragment-list-more-actions.png)

### Editar fragmentos {#edit-fragments}

Para editar um fragmento, siga as etapas abaixo.

1. Clique no item desejado na guia **[!UICONTROL Fragmentos]** lista.
1. Nas propriedades do fragmento, é possível [explorar referências](#explore-references), [gerenciar seu acesso](../administration/object-based-access.md)e atualize os detalhes do fragmento, incluindo [tags](../start/search-filter-categorize.md#tags).

   ![](../email/assets/fragment-edit-content.png)

1. Selecione o botão correspondente para editar o conteúdo da mesma forma que faria ao criar um fragmento do zero. [Saiba mais](#create-from-scratch)

>[!NOTE]
>
>Ao editar um fragmento, as alterações são propagadas automaticamente para todo o conteúdo usando esse fragmento, exceto o conteúdo usado em **[!UICONTROL Ao vivo]** jornadas ou campanhas. Também é possível quebrar a herança do fragmento original. Saiba mais na [Adicionar fragmentos visuais aos seus emails](../email/use-visual-fragments.md#break-inheritance) e [Aproveitar fragmentos de expressão](../personalization/use-expression-fragments.md#break-inheritance) seções.

### Explorar referências {#explore-references}

Você pode exibir a lista de jornadas, campanhas e modelos de conteúdo que estão usando um fragmento no momento.

Para fazer isso, selecione **[!UICONTROL Explorar referências]** na caixa **[!UICONTROL Mais ações]** na lista de fragmentos ou na tela propriedades do fragmento.

![](assets/fragment-explore-references.png)

Selecione uma guia para alternar entre jornadas, campanhas, modelos e fragmentos. Você pode ver o status e clicar em um nome a ser redirecionado para o item correspondente onde o fragmento é referenciado.

![](assets/fragment-usage-screen.png)

>[!NOTE]
>
>Se o fragmento for usado em uma jornada, campanha ou modelo que tenha um rótulo que o impeça de acessá-lo, você verá uma mensagem de alerta na parte superior da guia selecionada. [Saiba mais sobre o OLAC (Object Level Access Control)](../administration/object-based-access.md)

### Arquivar fragmentos {#archive-fragments}

Você pode limpar a lista de fragmentos dos itens que não são mais relevantes para sua marca.

Para fazer isso, clique no link **[!UICONTROL Mais ações]** ao lado do fragmento desejado e selecione **[!UICONTROL Arquivar]**. Ele desaparecerá da lista de fragmentos, o que impede que os usuários o usem em emails ou modelos futuros.

![](assets/fragment-list-archive.png)

>[!NOTE]
>
>Se você arquivar um fragmento usado em um conteúdo, <!--it will remain in the email or template, but you won't be able to select it from the fragment list to edit it-->que o conteúdo não será afetado.

Para desarquivar um fragmento, filtre na variável **[!UICONTROL Arquivado]** itens e selecione **[!UICONTROL Desarquivar]** do **[!UICONTROL Mais ações]** menu. Agora ele pode ser acessado novamente na lista de fragmentos e pode ser usado em qualquer email ou modelo.

![](assets/fragment-list-unarchive.png)

## Criar fragmentos {#create-fragments}

Há duas maneiras de criar fragmentos:

* Criar um fragmento do zero, usando o **[!UICONTROL Fragmentos]** menu dedicado. [Saiba como](#create-from-scratch)

* Ao criar o conteúdo, salve uma parte do conteúdo como fragmento. [Saiba como](#save-as-fragment)

Depois de salvo, o fragmento fica disponível para uso em uma jornada, campanha ou template. Seja criado do zero ou a partir de um conteúdo existente, agora é possível usar esse fragmento ao criar qualquer conteúdo no [!DNL Journey Optimizer]. Consulte [Adicionar fragmentos visuais](../email/use-visual-fragments.md) e [Aproveitar fragmentos de expressão](../personalization/use-expression-fragments.md)

### Criar do zero {#create-from-scratch}

Para criar um fragmento do zero, siga as etapas abaixo.

1. [Acessar a lista de fragmentos](#access-manage-fragments) por meio da **[!UICONTROL Gestão de conteúdo]** > **[!UICONTROL Fragmentos]** menu esquerdo.

1. Selecionar **[!UICONTROL Criar fragmento]**.

1. Preencha os detalhes do fragmento, ou seja, nome e descrição (se necessário).

   ![](assets/fragment-details.png)

1. Selecione o tipo de fragmento: [Fragmento visual](#create-visual-fragment) ou [Fragmento da expressão](#create-expression-fragment).

1. Para atribuir rótulos de uso de dados personalizados ou principais ao fragmento, selecione **[!UICONTROL Gerenciar acesso]**. [Saiba mais sobre o OLAC (Object Level Access Control)](../administration/object-based-access.md).

1. Selecione ou crie tags do Adobe Experience Platform na **[!UICONTROL Tags]** para categorizar seu fragmento para pesquisa aprimorada. [Saiba mais](../start/search-filter-categorize.md#tags)

1. Clique em **[!UICONTROL Criar]**.

### Criar um fragmento visual {#create-visual-fragment}

>[!CONTEXTUALHELP]
>id="ajo_create_visual_fragment"
>title="Selecione o tipo “Visual”"
>abstract="Crie um fragmento visual independente para tornar o conteúdo reutilizável em um email de uma jornada ou campanha ou em um modelo de conteúdo."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/email/design-email/add-content/use-visual-fragments.html?lang=pt-BR" text="Adicionar fragmentos visuais aos emails"

1. [Criar um fragmento](#create-from-scratch) do **[!UICONTROL Gestão de conteúdo]** > **[!UICONTROL Fragmentos]** e selecione a opção **[!UICONTROL Fragmento visual]** tipo.

   >[!NOTE]
   >
   >Atualmente, para fragmentos visuais, somente a variável **E-mail** canal é compatível.

1. A variável [Email Designer](../email/get-started-email-design.md) é exibido. Edite seu conteúdo conforme necessário, da mesma forma que faria para qualquer email dentro de uma jornada ou campanha.

   >[!NOTE]
   >
   >Você pode adicionar campos de personalização e conteúdo dinâmico, mas os atributos contextuais não são compatíveis com fragmentos.

   ![](assets/fragment-designer.png)

1. Quando o fragmento estiver pronto, clique em **[!UICONTROL Salvar]**. Ele é adicionado à guia [lista de fragmentos](#access-manage-fragments).

1. Se necessário, clique na seta ao lado do nome do fragmento para voltar para a **[!UICONTROL Detalhes]** tela e editá-la.

   ![](assets/fragment-designer-back.png)

Este fragmento agora está pronto para ser usado ao criar qualquer [email](../email/get-started-email-design.md) ou [template de conteúdo](content-templates.md) no prazo de [!DNL Journey Optimizer]. [Saiba como](../email/use-visual-fragments.md)

### Criar um fragmento de expressão {#create-expression-fragment}

>[!CONTEXTUALHELP]
>id="ajo_create_expression_fragment"
>title="Selecione o tipo “Expressão”"
>abstract="Crie um fragmento de expressão independente para tornar seu conteúdo reutilizável em várias jornadas e campanhas. Ao usar o editor de expressão, você pode aproveitar todos os fragmentos de expressão que foram criados na sandbox atual."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/personalization/expression-editor/use-expression-fragments.html?lang=pt-BR" text="Aproveitar fragmentos de expressão"

1. [Criar um fragmento](#create-from-scratch) do **[!UICONTROL Gestão de conteúdo]** > **[!UICONTROL Fragmentos]** e selecione a opção **[!UICONTROL Fragmento da expressão]** tipo.

1. Selecione o tipo de código que deseja usar: **[!UICONTROL HTML]**, **[!UICONTROL JSON]** ou **[!UICONTROL Texto]**.

   ![](assets/fragment-expression-type.png)

   <!--Expression fragments can be used in any channel.-->

1. Clique em **[!UICONTROL Criar]**. O editor de expressão se abre.

1. Você pode aproveitar o [!DNL Journey Optimizer] Editor de expressão com todos os seus recursos de personalização e criação. [Saiba mais](../personalization/personalization-build-expressions.md)

   ![](assets/fragment-expression-editor.png)

1. Quando o fragmento estiver pronto, clique em **[!UICONTROL Salvar]**. Ele é adicionado à guia [lista de fragmentos](#access-manage-fragments).

1. Se necessário, clique na seta ao lado do nome do fragmento para voltar para a **[!UICONTROL Detalhes]** tela e editá-la.

Este fragmento agora está pronto para ser usado ao criar qualquer conteúdo no [!DNL Journey Optimizer] Editor de expressão. [Saiba como](../personalization/use-expression-fragments.md)

## Salvar como fragmento {#save-as-fragment}

Ao editar conteúdo no [!DNL Journey Optimizer], você pode salvar todo o conteúdo ou parte dele como fragmento para futura reutilização.

### Salvar como fragmento visual {#save-as-visual-fragment}

Ao projetar um [template de conteúdo](content-templates.md) ou um [email](../email/get-started-email-design.md) em uma campanha ou jornada, você pode salvar uma parte do conteúdo como fragmento visual. Para fazer isso, siga as etapas abaixo.

1. No [Email Designer](../email/get-started-email-design.md), clique nas reticências na parte superior direita da tela.

1. Selecionar **[!UICONTROL Salvar como fragmento]** no menu suspenso.

   ![](assets/fragment-save-as.png)

1. A variável **[!UICONTROL Salvar como fragmento]** é exibida. Lá, selecione os elementos que deseja incluir no fragmento, incluindo campos de personalização e conteúdo dinâmico. Observe que os atributos contextuais não são suportados em fragmentos.

   >[!CAUTION]
   >
   >Você só pode selecionar seções adjacentes entre si. Não é possível selecionar uma estrutura vazia ou outro fragmento.

   ![](assets/fragment-save-as-screen.png)

1. Clique em **[!UICONTROL Criar]**. Preencha os detalhes do fragmento, ou seja, nome e descrição (se necessário).

1. Para atribuir rótulos de uso de dados personalizados ou principais ao fragmento, selecione **[!UICONTROL Gerenciar acesso]**. [Saiba mais sobre o OLAC (Object Level Access Control)](../administration/object-based-access.md).

1. Selecione ou crie tags do Adobe Experience Platform na **Tags** para categorizar seu modelo para pesquisa aprimorada. [Saiba mais](../start/search-filter-categorize.md#tags)

1. Clique em **[!UICONTROL Criar]** novamente. O fragmento é salvo em adicionado à variável [lista de fragmentos](#access-manage-fragments), acessível pelo [!DNL Journey Optimizer] menu dedicado.

   Ele se torna um fragmento independente que pode ser [acessado](#access-manage-fragments), [editado](#edit-fragments) e [arquivado](#archive-fragments) como qualquer outro item dessa lista.

Agora você pode usar esse fragmento ao criar qualquer [email](../email/get-started-email-design.md) ou [template de conteúdo](content-templates.md) no prazo de [!DNL Journey Optimizer]. [Saiba como](../email/use-visual-fragments.md)

>[!NOTE]
>
>Qualquer alteração nesse novo fragmento não é propagada para o email ou modelo de onde vem. Da mesma forma, quando o conteúdo original é editado nesse email ou modelo, o novo fragmento não é modificado.

### Salvar como fragmento de expressão {#save-as-expression-fragment}

>[!CONTEXTUALHELP]
>id="ajo_perso_library"
>title="Salvar como fragmento de expressão"
>abstract="O editor de expressão do [!DNL Journey Optimizer] permite salvar o conteúdo como fragmentos de expressão. Essas expressões são disponibilizadas na criação de conteúdo personalizado."

O editor de expressão do [!DNL Journey Optimizer] permite salvar o conteúdo como fragmentos de expressão. Essas expressões são disponibilizadas na criação de conteúdo personalizado.

Para salvar o conteúdo como um fragmento de expressão, siga as etapas abaixo.

1. No [Editor de expressão](../personalization/personalization-build-expressions.md) , crie uma expressão e clique em **[!UICONTROL Salvar como fragmento]**.

1. No painel direito, insira um nome e uma descrição para a expressão para ajudar os usuários a encontrá-la mais facilmente.

   ![](assets/expression-fragment-save-as.png)

1. Clique em **[!UICONTROL Salvar fragmento]**.

   <!--An expression fragment cannot be nested inside another fragment.-->

1. O fragmento de expressão é adicionado à variável [lista de fragmentos](#access-manage-fragments). Agora você pode usá-lo para criar conteúdo personalizado.

>[!NOTE]
>
>As expressões não podem exceder 200 KB.

## Vídeo explicativo {#video-fragments}

Saiba como gerenciar, criar e usar fragmentos visuais no [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3419932/?quality=12)

Saiba como gerenciar, criar e usar fragmentos de expressão no [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3424587/?quality=12)
