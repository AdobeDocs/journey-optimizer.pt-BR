---
solution: Journey Optimizer
product: journey optimizer
title: Criar um email
description: Saiba como criar um email no Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: b7b333e96e0f4b32a0f94c3f1e67f0f3d3fc2816
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 5%

---

# Criar um email {#create-email-bis}

Para criar um email, siga as etapas abaixo.

## 1. Crie um email em uma jornada ou campanha

Adicione um **[!UICONTROL Email]** para uma jornada ou campanha e siga as etapas abaixo de acordo com seu caso.

>[!BEGINTABS]

>[!TAB Adicionar um email a uma jornada]

1. Abra a jornada e arraste e solte uma **[!UICONTROL Email]** da **[!UICONTROL Ações]** da paleta.

1. Forneça informações básicas sobre sua mensagem (rótulo, descrição, categoria).

1. Escolha a [superfície do email] para usar.

   ![](assets/email_journey.png)

Para obter mais informações sobre como configurar uma jornada, consulte [esta página](../building-journeys/journey-gs.md).

>[!TAB Adicionar um email a uma campanha]

1. Crie uma nova campanha agendada ou acionada por API e selecione **[!UICONTROL Email]** como sua ação.

1. Escolha a [superfície do email] para usar.

   ![](assets/email_campaign.png)

1. Clique em **[!UICONTROL Criar]**.

1. Complete as etapas para criar uma campanha por email.

   ![](assets/email_campaign_steps.png)

<!--
From the **[!UICONTROL Action]** section, specify if you want to track how your recipients react to your delivery: you can track email opens, and/or clicks on links and buttons in your email.

![](assets/email_campaign_tracking.png)
-->

Para obter mais informações sobre como configurar uma campanha, consulte [esta página](../campaigns/get-started-with-campaigns.md).

>[!ENDTABS]

## Definir o conteúdo do email

1. Na tela de configuração da jornada ou campanha, clique no botão **[!UICONTROL Editar conteúdo]** para configurar o conteúdo do email. [Saiba mais]

   ![](assets/email_campaign_edit_content.png)

1. No **[!UICONTROL Cabeçalho]** da seção **[!UICONTROL Editar conteúdo]** , a **[!UICONTROL Nome de origem]**, **[!UICONTROL Do email]** e **[!UICONTROL CCO]** O campo vem da superfície de email selecionada. [Saiba mais] <!--check if same for journey-->

   ![](assets/email_designer_edit_content_header.png)

1. Você pode adicionar uma linha de assunto. Digite o texto simples diretamente no campo correspondente ou use o [Editor de expressão](../personalization/personalization-build-expressions.md) para personalizar a linha de assunto.

1. Clique no botão **[!UICONTROL Editar corpo do email]** botão para começar a criar o conteúdo usando o [!DNL Journey Optimizer] Email Designer. [Saiba mais]

   ![](assets/email_designer_edit_email_body.png)

   Você também pode clicar no botão **[!UICONTROL Editor de códigos]** botão para codificar seu próprio conteúdo no plain HTML usando a janela pop-up exibida.

   ![](assets/email_designer_edit_code_editor.png)

   >[!NOTE]
   >
   >Se você já criou ou importou conteúdo por meio do Designer de email, esse conteúdo será exibido no HTML.

## Pré-visualizar seu email

Após definir o conteúdo da mensagem, é possível pré-visualizá-lo para controlar a renderização do email e verificar as configurações de personalização com perfis de teste. [Saiba mais]

![](assets/email_designer_edit_simulate.png)

Você também deve verificar os alertas na seção superior do editor.  Alguns deles são avisos simples, mas outros podem impedir que você use a mensagem. [Saiba mais](alerts.md).

## Validar seu conteúdo de email

Quando o email estiver pronto, conclua a configuração do [jornada](../building-journeys/journey-gs.md) ou [campanha](../campaigns/create-campaign.md) e ative para enviar a mensagem.

>[!NOTE]
>
>Para rastrear o comportamento dos recipients por meio de aberturas e/ou interações de email, verifique se as opções dedicadas na variável **[!UICONTROL Rastreamento]** estão ativadas na jornada [atividade de email](../building-journeys/journeys-message.md) ou no email [campanha](../campaigns/create-campaign.md).

Você também deve verificar os alertas na seção superior do editor.  Alguns deles são avisos simples, mas outros podem impedir que você use a mensagem. [Saiba mais](alerts.md)

