---
title: Criar um email
description: Saiba como criar um email no Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: c77dc420-a375-4376-ad86-ac740e214c3c
source-git-commit: 711fdf1dce0688d2e21d405a4e3e8777612b2f3b
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 9%

---

# Criar um email {#configure-email}

>[!CONTEXTUALHELP]
>id="ajo_message_email"
>title="Criação de email"
>abstract="Defina seus parâmetros de email em apenas três etapas simples."

Emails podem ser criados:

* Em um **Jornada**: Depois de adicionar uma atividade Email na jornada e definir as configurações básicas, use a **[!UICONTROL Actions: Email]** painel direito para criar o conteúdo das notificações por push.

   Para obter mais informações sobre como configurar a jornada, consulte esta seção [página](../building-journeys/journey-gs.md).

   ![](assets/email-edit-content.png)

* Em um **Campanha**: Depois de criar uma campanha, selecione Email como sua ação e defina as configurações básicas.

   Para obter mais informações sobre como configurar sua campanha, consulte esta seção [página](../campaigns/create-campaign.md#configure).

   ![](assets/email_campaign.png)

## Definir o conteúdo do email{#email-content}

Use [!DNL Journey Optimizer] Email Designer para [crie seu email do zero](../design/create-email-content.md). Se tiver um conteúdo existente, é possível [importe-o no Email Designer](../design/existing-content.md)ou [codificar seu próprio conteúdo](../design/code-content.md) em [!DNL Journey Optimizer].

[!DNL Journey Optimizer] vem com um conjunto de [modelos incorporados](../design/email-templates.md) para ajudá-lo a começar. Qualquer email também pode ser salvo como um modelo.

Use [!DNL Journey Optimizer] Editor de expressão para personalizar suas mensagens com dados de perfis. Para saber mais sobre personalizações, consulte [esta seção](../personalization/personalize.md).

## Acompanhamento de email{#email-tracking}

Se você quiser rastrear o comportamento dos recipients por meio de aberturas e/ou cliques em links, ative as seguintes opções: **[!UICONTROL Email opens]** e **[!UICONTROL Click on email]**.

Saiba mais sobre como rastrear no [esta seção](../design/message-tracking.md).

## Validar seu conteúdo de email{#email-content-validate}

Controle a renderização do email e verifique as configurações de personalização com perfis de teste, usando a seção preview no lado esquerdo. Para obter mais informações, consulte [esta seção](../design/preview.md).

![](assets/messages-simple-preview.png)


Você também deve verificar os alertas na seção superior do editor.  Alguns deles são avisos simples, mas outros podem impedir que você use a mensagem. Saiba mais [nesta seção](alerts.md).


>[!NOTE]
>
>O **[!UICONTROL From email]** e **[!UICONTROL From name]** são determinadas pela **[!UICONTROL Surface]** que foi selecionado quando [criação da mensagem](get-started-content.md).

