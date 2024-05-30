---
solution: Journey Optimizer
product: journey optimizer
title: Salvar conteúdo como fragmento
description: Saiba como salvar conteúdo como fragmentos para reutilizar conteúdo em campanhas e jornadas do Journey Optimizer
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
source-git-commit: 83997271d16e15fb0d7ccdd21aa8ac8b8221a0d5
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 2%

---

# Salvar conteúdo como fragmento {#save-as-fragment}

Ao editar conteúdo no [!DNL Journey Optimizer], você pode salvar todo o conteúdo ou parte dele como fragmento para futura reutilização.

## Salvar conteúdo como fragmento visual {#save-as-visual-fragment}

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

## Salvar fragmento de expressão do conteúdo {#save-as-expression-fragment}

>[!CONTEXTUALHELP]
>id="ajo_perso_library"
>title="Salvar como fragmento de expressão"
>abstract="A variável [!DNL Journey Optimizer] o editor de personalização permite salvar o conteúdo como fragmentos de expressão. Essas expressões ficam disponíveis para criar conteúdo personalizado."

A variável [!DNL Journey Optimizer] o editor de personalização permite salvar o conteúdo como fragmentos de expressão. Essas expressões ficam disponíveis para criar conteúdo personalizado.

Para salvar o conteúdo como um fragmento de expressão, siga as etapas abaixo.

1. No [editor de personalização](../personalization/personalization-build-expressions.md) , crie uma expressão e clique em **[!UICONTROL Salvar como fragmento]**.

1. No painel direito, insira um nome e uma descrição para a expressão para ajudar os usuários a encontrá-la mais facilmente.

   ![](assets/expression-fragment-save-as.png)

1. Clique em **[!UICONTROL Salvar fragmento]**.

   <!--An expression fragment cannot be nested inside another fragment.-->

1. O fragmento de expressão é adicionado à variável [lista de fragmentos](#access-manage-fragments). Agora você pode usá-lo para criar conteúdo personalizado.

>[!NOTE]
>
>As expressões não podem exceder 200 KB.
