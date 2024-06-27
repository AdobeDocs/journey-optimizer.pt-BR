---
solution: Journey Optimizer
product: journey optimizer
title: Salvar conteúdo como fragmento
description: Saiba como salvar conteúdo como fragmentos para reutilizar conteúdo em campanhas e jornadas do Journey Optimizer
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 70e88ea0-f2b0-4c13-8693-619741762429
source-git-commit: e6924928e03d494817a2368b33997029ca2eca1c
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 11%

---

# Salvar conteúdo como fragmento {#save-as-fragment}

Ao editar conteúdo no [!DNL Journey Optimizer], você pode salvar todo o conteúdo ou parte dele como fragmento para futura reutilização. É possível salvar o conteúdo como fragmento [no Designer de email](#save-as-visual-fragment)ou [no editor de expressão](#save-as-expression-fragment).

## Salvar como fragmento visual {#save-as-visual-fragment}

Para salvar o conteúdo do Designer de email como fragmento, siga estas etapas:

1. No [Designer de email](../email/get-started-email-design.md), clique nas reticências na parte superior direita da tela.

1. Selecionar **[!UICONTROL Salvar como fragmento]** no menu suspenso.

   ![](assets/fragment-save-as.png)

1. A variável **[!UICONTROL Salvar como fragmento]** é exibida. Lá, selecione os elementos que deseja incluir no fragmento, incluindo campos de personalização e conteúdo dinâmico. Observe que os atributos contextuais não são suportados em fragmentos.

   ![](assets/fragment-save-as-screen.png)

   >[!CAUTION]
   >
   >Você só pode selecionar seções adjacentes entre si. Não é possível selecionar uma estrutura vazia ou outro fragmento.

1. Clique em **[!UICONTROL Criar]** e preencha o nome e a descrição do fragmento (se necessário).

1. Para atribuir rótulos de uso de dados personalizados ou principais ao fragmento, clique no **[!UICONTROL Gerenciar acesso]** na seção superior da tela. [Saiba mais sobre o OLAC (Object Level Access Control)](../administration/object-based-access.md).

1. Selecione ou crie tags do Adobe Experience Platform na **Tags** para categorizar seu modelo para pesquisa aprimorada. [Saiba mais](../start/search-filter-categorize.md#tags)

1. Clique em **[!UICONTROL Criar]**. O fragmento é adicionado à variável [lista de fragmentos](#access-manage-fragments) com o **Rascunho** status. Ele se torna um fragmento independente que pode ser usado como qualquer outro fragmento visual dessa lista.

   >[!NOTE]
   >
   >Qualquer alteração nesse novo fragmento não é propagada para o email ou modelo de onde vem. Da mesma forma, quando o conteúdo original é editado nesse email ou modelo, o novo fragmento não é modificado.

1. Para poder usar o fragmento em suas jornadas e campanhas, é necessário ativá-lo. [Saiba como visualizar e publicar um fragmento](../content-management/create-fragments.md#publish)

## Salvar como fragmento de expressão {#save-as-expression-fragment}

>[!CONTEXTUALHELP]
>id="ajo_perso_library"
>title="Salvar como fragmento de expressão"
>abstract="O editor de personalização do [!DNL Journey Optimizer] permite salvar o conteúdo como fragmentos de expressão. Essas expressões são disponibilizadas na criação de conteúdo personalizado."

O editor de personalização do [!DNL Journey Optimizer] permite salvar o conteúdo como fragmentos de expressão. Essas expressões são disponibilizadas na criação de conteúdo personalizado.

Para salvar o conteúdo como um fragmento de expressão, siga as etapas abaixo.

1. No [editor de personalização](../personalization/personalization-build-expressions.md) , crie uma expressão e clique em **[!UICONTROL Salvar como fragmento]**.

   >[!NOTE]
   >
   >As expressões não podem exceder 200 KB.

1. No painel direito, insira um nome e uma descrição para a expressão para ajudar os usuários a encontrá-la mais facilmente.

   ![](assets/expression-fragment-save-as.png)

1. Clique em **[!UICONTROL Salvar fragmento]**.

   <!--An expression fragment cannot be nested inside another fragment.-->

1. O fragmento é adicionado à variável [lista de fragmentos](#access-manage-fragments) com o **Rascunho** status. Ele se torna um fragmento independente que pode ser usado como qualquer outro fragmento de expressão dessa lista.

1. Para poder usar o fragmento em suas jornadas e campanhas, é necessário ativá-lo. [Saiba como visualizar e publicar um fragmento](../content-management/create-fragments.md#publish)
