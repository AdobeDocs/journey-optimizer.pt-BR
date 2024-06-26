---
solution: Journey Optimizer
product: journey optimizer
title: Criar modelos de conteúdo
description: Saiba como criar modelos para reutilizar conteúdo em campanhas e jornadas do Journey Optimizer
feature: Templates
topic: Content Management
role: User
level: Beginner
source-git-commit: 59c675dd2ac94b6967cfb3a93f74b2016a090190
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 14%

---


# Criar modelos de conteúdo {#create-content-templates}

>[!CONTEXTUALHELP]
>id="ajo_create_template"
>title="Definir seu próprio modelo de conteúdo"
>abstract="Crie um modelo personalizado independente partindo do zero para tornar seu conteúdo reutilizável em várias jornadas e campanhas."

Há duas maneiras de criar modelos de conteúdo:

* Criar um modelo de conteúdo do zero, usando o painel esquerdo **[!UICONTROL Modelos de conteúdo]** menu. [Saiba como](#create-template-from-scratch)

* Ao criar o conteúdo em uma campanha ou jornada, salve-o como template. [Saiba como](#save-as-template)

Depois de salvo, seu template de conteúdo fica disponível para uso em uma campanha ou jornada. Seja criado do zero ou de um conteúdo anterior, agora é possível usar esse modelo ao criar qualquer conteúdo dentro [!DNL Journey Optimizer]. [Saiba como](#use-content-templates)

>[!NOTE]
>
>* As alterações feitas em modelos de conteúdo não são propagadas para campanhas ou jornadas, estejam elas ativas ou em rascunho.
>
>* Da mesma forma, quando os modelos são usados em uma campanha ou jornada, as edições feitas na campanha e no conteúdo da jornada não afetam o modelo de conteúdo usado anteriormente.

## Criar modelo do zero {#create-template-from-scratch}

Para criar um template de conteúdo do zero, siga as etapas abaixo.

1. Acesse a lista de templates de conteúdo por meio da **[!UICONTROL Gestão de conteúdo]** > **[!UICONTROL Modelos de conteúdo]** menu esquerdo.

1. Selecionar **[!UICONTROL Criar modelo]**.

1. Preencha os detalhes do modelo e selecione o canal desejado.

   ![](assets/content-template-channels.png)

   >[!NOTE]
   >
   >Atualmente, todos os canais estão disponíveis, exceto a Web.

1. Escolha um **[!UICONTROL Tipo]** para o canal selecionado.

   ![](assets/content-template-type.png)

   * Para **[!UICONTROL E-mail]**, se você selecionar **[!UICONTROL Conteúdo]**, você pode definir a variável [Linha de assunto](../email/create-email.md#define-email-content) como parte do modelo. Se você selecionar **[!UICONTROL HTML]**, você só poderá definir o conteúdo do corpo do email.

   * Para **[!UICONTROL SMS]**, **[!UICONTROL Push]**, **[!UICONTROL No aplicativo]** e **[!UICONTROL Correspondência direta]**, somente o tipo padrão está disponível para o canal atual. Você ainda precisa selecioná-lo.

1. Selecione ou crie tags do Adobe Experience Platform na **[!UICONTROL Tags]** para categorizar seu modelo para pesquisa aprimorada. [Saiba mais](../start/search-filter-categorize.md#tags)

1. Para atribuir rótulos de uso de dados personalizados ou principais ao modelo, você pode selecionar **[!UICONTROL Gerenciar acesso]**. [Saiba mais sobre o OLAC (Object Level Access Control)](../administration/object-based-access.md).

1. Clique em **[!UICONTROL Criar]** e crie seu conteúdo conforme necessário, da mesma forma que faria com qualquer conteúdo de uma jornada ou campanha, de acordo com o canal selecionado.

   ![](assets/content-template-edition.png)

   Saiba como criar conteúdo para os diferentes canais nas seguintes seções:
   * [Definir conteúdo do email](../email/get-started-email-design.md)
   * [Definir conteúdo de push](../push/design-push.md)
   * [Definir conteúdo de SMS](../sms/create-sms.md#sms-content)
   * [Definir conteúdo da correspondência direta](../direct-mail/create-direct-mail.md)
   * [Definir conteúdo no aplicativo](../in-app/design-in-app.md)

1. Se você estiver criando uma **[!UICONTROL E-mail]** modelo com o **[!UICONTROL HTML]** digite, você pode testar o conteúdo. [Saiba como](#test-template)

1. Quando o modelo estiver pronto, clique em **[!UICONTROL Salvar]**.

1. Clique na seta ao lado do nome do modelo para voltar para a **[!UICONTROL Detalhes]** tela.

   ![](assets/content-template-back.png)

Este template agora está pronto para ser usado ao criar qualquer conteúdo dentro de [!DNL Journey Optimizer]. [Saiba como](#use-content-templates)

## Salvar conteúdo como modelo de conteúdo {#save-as-template}

>[!CONTEXTUALHELP]
>id="ajo_messages_depecrated_inventory"
>title="Saiba como migrar as mensagens"
>abstract="Em 25 de julho de 2022, o menu Mensagens desapareceu e as mensagens agora são criadas diretamente na jornada. Se você quiser reutilizar as mensagens herdadas nas jornadas, é necessário salvá-las como modelos."

Ao criar qualquer conteúdo em uma campanha ou jornada, você pode salvá-lo para futura reutilização. Para fazer isso, siga as etapas abaixo.

1. Da mensagem **[!UICONTROL Editar conteúdo]** clique na guia **[!UICONTROL Modelo de conteúdo]** botão.

1. Selecionar **[!UICONTROL Salvar como modelo de conteúdo]** no menu suspenso.

   ![](assets/content-template-button-save.png)

   Se você estiver na [Designer de email](../email/get-started-email-design.md), você também pode selecionar essa opção na **[!UICONTROL Mais]** na parte superior direita da tela.

   ![](assets/content-template-more-button-save.png)

1. Adicione um nome e uma descrição para este template.

   ![](assets/content-template-name.png)

   >[!NOTE]
   >
   >O canal e o tipo atuais são preenchidos automaticamente e não podem ser editados. Para modelos de email criados na [Designer de email](../email/get-started-email-design.md), o **[!UICONTROL HTML]** O tipo é selecionado automaticamente.

1. Selecione ou crie uma tag do Adobe Experience Platform na **Tags** para categorizar seu modelo. [Saiba mais](../start/search-filter-categorize.md#tags)

1. Para atribuir rótulos de uso de dados personalizados ou principais ao modelo, você pode selecionar **[!UICONTROL Gerenciar acesso]**. [Saiba mais](../administration/object-based-access.md).

1. Clique em **[!UICONTROL Salvar]**.

1. O modelo é salvo na variável **[!UICONTROL Modelos de conteúdo]** , acessível na [!DNL Journey Optimizer] menu dedicado. Ele se torna um modelo de conteúdo independente que pode ser acessado, editado e excluído como qualquer outro item nessa lista. [Saiba mais](#access-manage-templates)

Agora você pode usar este template ao criar qualquer conteúdo dentro de [!DNL Journey Optimizer]. [Saiba como](#use-content-templates)

>[!NOTE]
>
>Qualquer alteração nesse novo modelo não será propagada para o conteúdo de onde vem. Da mesma forma, quando o conteúdo original é editado dentro desse conteúdo, o novo modelo não é modificado.
