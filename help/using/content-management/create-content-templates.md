---
solution: Journey Optimizer
product: journey optimizer
title: Criar modelos de conteúdo
description: Saiba como criar modelos para reutilizar conteúdo em campanhas e jornadas do Journey Optimizer
feature: Templates
topic: Content Management
role: User
level: Beginner
exl-id: a205539b-b7ea-4832-92b0-49637c4dac47
source-git-commit: a9f2eae6398f92a40accb62b1d4544bda031559c
workflow-type: tm+mt
source-wordcount: '626'
ht-degree: 11%

---

# Criar modelos de conteúdo {#create-content-templates}

>[!CONTEXTUALHELP]
>id="ajo_create_template"
>title="Definir seu próprio modelo de conteúdo"
>abstract="Crie um modelo personalizado independente partindo do zero para tornar seu conteúdo reutilizável em várias jornadas e campanhas."

Há duas maneiras de criar modelos de conteúdo:

* Crie um modelo de conteúdo do zero, usando o painel esquerdo **[!UICONTROL Modelos de conteúdo]**. [Saiba como](#create-template-from-scratch)

* Ao criar o conteúdo em uma campanha ou jornada, salve-o como template. [Saiba como](#save-as-template)

Depois de salvo, seu template de conteúdo fica disponível para uso em uma campanha ou jornada. Seja criado do zero ou de conteúdo anterior, você pode usar este modelo ao criar qualquer conteúdo dentro de [!DNL Journey Optimizer]. [Saiba como](#use-content-templates)

>[!NOTE]
>
>* As alterações feitas em modelos de conteúdo não são propagadas para campanhas ou jornadas, estejam elas ativas ou em rascunho.
>
>* Da mesma forma, quando os modelos são usados em uma campanha ou jornada, as edições feitas na campanha e no conteúdo da jornada não afetam o modelo de conteúdo usado anteriormente.

## Criar modelo do zero {#create-template-from-scratch}

>[!NOTE]
>
>A partir de março de 2025, os modelos de conteúdo do tipo HTML serão descontinuados. Os modelos de conteúdo do HTML existentes criados anteriormente no [!DNL Journey Optimizer] ainda podem ser usados.

Para criar um template de conteúdo do zero, siga as etapas abaixo.

1. Acesse a lista de modelos de conteúdo por meio do menu esquerdo **[!UICONTROL Gerenciamento de Conteúdo]** > **[!UICONTROL Modelos de Conteúdo]**.

1. Selecione **[!UICONTROL Criar modelo]**.

1. Preencha os detalhes do modelo e selecione o canal desejado.

   ![](assets/content-template-channels.png)

   >[!NOTE]
   >
   >Atualmente, todos os canais estão disponíveis, exceto a Web.

1. Selecione ou crie tags Adobe Experience Platform a partir do campo **[!UICONTROL Tags]** para categorizar seu modelo para pesquisa aprimorada. [Saiba mais](../start/search-filter-categorize.md#tags)

1. Para atribuir rótulos de uso de dados principais ou personalizados ao modelo, selecione **[!UICONTROL Gerenciar acesso]**. [Saiba mais sobre o OLAC (Controle de Acesso em Nível de Objeto)](../administration/object-based-access.md).

1. Clique em **[!UICONTROL Criar]** e crie o conteúdo conforme necessário, da mesma forma que faria para qualquer conteúdo dentro de uma jornada ou campanha, de acordo com o canal selecionado.

   ![](assets/content-template-edition.png)

   Saiba como criar conteúdo para os diferentes canais nas seguintes seções:
   * [Definir conteúdo do email](../email/get-started-email-design.md)
   * [Definir conteúdo de push](../push/design-push.md)
   * [Definir conteúdo de SMS](../sms/create-sms.md#sms-content)
   * [Definir conteúdo da correspondência direta](../direct-mail/create-direct-mail.md)
   * [Definir conteúdo no aplicativo](../in-app/design-in-app.md)
   * [Definir conteúdo da Web](../web/create-web.md#edit-web-content)
   * [Definir conteúdo de experiência baseado em código](../code-based/create-code-based.md)

     >[!NOTE]
     >
     >Você pode adicionar políticas de decisão a modelos de conteúdo de experiência baseados em código. [Saiba mais](../experience-decisioning/create-decision.md#add-decision)

1. Você pode testar seu conteúdo. [Saiba como](#test-template)

1. Quando o modelo estiver pronto, clique em **[!UICONTROL Salvar]**.

1. Clique na seta ao lado do nome do modelo para retornar à tela **[!UICONTROL Detalhes]**.

   ![](assets/content-template-back.png)

Este modelo agora está pronto para ser usado na compilação de qualquer conteúdo em [!DNL Journey Optimizer]. [Saiba como](#use-content-templates)

>[!NOTE]
>
>Ao criar um modelo de conteúdo de email, você pode aplicar rapidamente um estilo específico que se ajuste à sua marca e design aplicando um tema ao seu conteúdo. [Saiba mais](../email/apply-email-themes.md)

## Salvar conteúdo como modelo de conteúdo {#save-as-template}

Ao criar qualquer conteúdo em uma campanha ou jornada, você pode salvá-lo para futura reutilização. Para fazer isso, siga as etapas abaixo.

1. Na tela da mensagem **[!UICONTROL Editar conteúdo]**, clique no botão **[!UICONTROL Modelo de conteúdo]**.

1. Selecione **[!UICONTROL Salvar como modelo de conteúdo]** no menu suspenso.

   ![](assets/content-template-button-save.png)

   Se você estiver na [Designer de Email](../email/get-started-email-design.md), também poderá selecionar essa opção na lista suspensa **[!UICONTROL Mais]**, no canto superior direito da tela.

   ![](assets/content-template-more-button-save.png)

1. Adicione um nome e uma descrição para este template.

   ![](assets/content-template-name.png)

   >[!NOTE]
   >
   >O canal atual é preenchido automaticamente e não pode ser editado.

1. Selecione ou crie uma marca Adobe Experience Platform do campo **Marcas** para categorizar seu modelo. [Saiba mais](../start/search-filter-categorize.md#tags)

1. Para atribuir rótulos de uso de dados principais ou personalizados ao modelo, selecione **[!UICONTROL Gerenciar acesso]**. [Saiba mais](../administration/object-based-access.md).

1. Clique em **[!UICONTROL Salvar]**.

1. O modelo é salvo na lista **[!UICONTROL Modelos de conteúdo]**, acessível no menu dedicado [!DNL Journey Optimizer]. Ele se torna um modelo de conteúdo independente que pode ser acessado, editado e excluído como qualquer outro item nessa lista. [Saiba mais](#access-manage-templates)

Agora você pode usar este modelo ao criar qualquer conteúdo dentro de [!DNL Journey Optimizer]. [Saiba como](#use-content-templates)

>[!NOTE]
>
>Qualquer alteração no novo modelo não será propagada para o conteúdo do qual se origina. Da mesma forma, quando o conteúdo original é editado, o novo modelo não é modificado.

