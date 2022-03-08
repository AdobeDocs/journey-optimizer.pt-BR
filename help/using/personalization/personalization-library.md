---
title: Trabalhar com expressões salvas
description: Saiba como trabalhar com expressões salvas do [!DNL Journey Optimizer] biblioteca.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# Trabalhar com expressões salvas {#expression-library}

>[!CONTEXTUALHELP]
>id="ajo_perso_library"
>title="Sobre a Biblioteca de expressões"
>abstract="[!DNL Journey Optimizer] O fornece uma biblioteca onde você pode acessar expressões de personalização salvas que foram configuradas por usuários administradores. "

[!DNL Journey Optimizer] O fornece uma biblioteca onde você pode acessar expressões de personalização salvas anteriormente que foram adicionadas por usuários administradores.

1. Para acessar as expressões salvas, clique no botão **[!UICONTROL Library]** no painel esquerdo. A lista exibe todas as expressões que foram salvas por usuários administradores (consulte [Salvar expressões na biblioteca](#save-expressions)).

   >[!NOTE]
   >
   >Você pode usar o botão info para obter mais informações sobre o conteúdo de uma expressão salva. Se você tiver as permissões apropriadas para gerenciar itens de biblioteca, o botão de informações será exibido no menu da elipse.

   ![](assets/library-list.png)

1. Clique em + para inserir a expressão no editor. Em seguida, você pode personalizar e validar seu conteúdo de personalização como de costume. [Saiba mais](../personalization/personalization-build-expressions.md)

   ![](assets/library-add.png)

## Salvar uma expressão na biblioteca {#save-expressions}

[!DNL Journey Optimizer] permite que usuários administradores salvem expressões de personalização na biblioteca. Essas expressões serão disponibilizadas para todos os usuários para criar conteúdo de personalização.

Para salvar uma expressão na biblioteca, siga estas etapas:

1. Na interface do editor, crie a expressão e clique em **[!UICONTROL Add to library]**.

   >[!NOTE]
   >
   >Se o botão não estiver visível, verifique no Admin Console se você tem as permissões necessárias (consulte [Níveis de permissões](../administration/high-low-permissions.md)).

   ![](assets/library-save.png)

1. No painel direito, insira um título e uma descrição para a expressão para ajudar os usuários a encontrá-la mais facilmente, em seguida, clique em **[!UICONTROL Add]**.

   ![](assets/add-expression.png)

1. A expressão é adicionada à biblioteca. Agora os usuários podem usá-lo para criar o conteúdo de personalização.


>[!NOTE]
>
>* Você salva até 40 expressões na biblioteca do .
>
>* As expressões não podem exceder 200 KB.
>
>* As expressões salvas são classificadas por data de criação: a expressão adicionada recentemente será mostrada primeiro na lista.



Para editar uma expressão existente, adicione-a ao editor e, em seguida, modifique-a de acordo com suas necessidades. Clique em **[!UICONTROL Add to library]** para validar a sintaxe e salvar a expressão.

Para excluir uma expressão, clique no botão de elipse e clique em **[!UICONTROL Delete]**.
