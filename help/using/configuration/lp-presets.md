---
title: Definir predefinições da landing page
description: Saiba como configurar seu ambiente para criar e usar landing pages com o Journey Optimizer
role: Admin
level: Intermediate
exl-id: 7cf1f083-bef0-40b5-8ddd-920a9d108eca
source-git-commit: a036f53b88425d64281d2ac530016d638e2d13c9
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 4%

---

# Definir predefinições da landing page {#lp-presets}

When [criação de uma landing page](../landing-pages/create-lp.md#create-a-lp), você deve selecionar uma predefinição de página de aterrissagem para criar a página de aterrissagem e aproveitá-la **[!DNL Journey Optimizer]**.

## Acessar predefinições da página de aterrissagem {#access-lp-presets}

Para acessar as predefinições da landing page, siga as etapas abaixo.

1. Acesse o **[!UICONTROL Administration]** > **[!UICONTROL Channels]** menu.

1. Selecione **[!UICONTROL Branding]** > **[!UICONTROL Landing page presets]**.

   ![](assets/lp_presets-access.png)

1. Clique em qualquer rótulo predefinido para acessar os detalhes predefinidos da landing page.

   ![](assets/lp_preset-details.png)

## Criar uma predefinição de página de aterrissagem {#lp-create-preset}

Para criar uma predefinição de página de aterrissagem, siga as etapas abaixo.

>[!NOTE]
>
>Para criar uma predefinição, verifique se você configurou anteriormente pelo menos um subdomínio de página de aterrissagem. [Saiba como](lp-subdomains.md)

1. Acesse o **[!UICONTROL Administration]** > **[!UICONTROL Channels]** e selecione **[!UICONTROL Branding]** > **[!UICONTROL Landing page presets]**.

1. Selecione **[!UICONTROL Create landing page preset]**.

   ![](assets/lp_create-preset-temp.png)

1. Insira um nome e uma descrição para a predefinição.

   >[!NOTE]
   >
   > Os nomes devem começar com uma letra (A-Z). Ela só pode conter caracteres alfanuméricos. Você também pode usar o sublinhado `_`, ponto`.` e hífen `-` caracteres.

1. Selecione um subdomínio de página de aterrissagem na lista suspensa.

   ![](assets/lp_preset-subdomain.png)

   >[!NOTE]
   >
   >Para selecionar um subdomínio, verifique se você configurou anteriormente pelo menos um subdomínio de página de aterrissagem. [Saiba como](#lp-subdomains)

   As configurações correspondentes ao subdomínio selecionado são exibidas.

1. Se desejar selecionar o subdomínio da página de aterrissagem como o URL de rastreamento, verifique a variável **[!UICONTROL Same as landing page subdomain]** opção. [Saiba mais sobre o rastreamento](../design/message-tracking.md)

   ![](assets/lp_preset-subdomain-settings-same.png)

   Por exemplo, se o URL da página de aterrissagem for &#39;pages.mail.luma.com&#39; e o URL de rastreamento for &#39;data.mail.luma.com&#39;, você poderá escolher &#39;pages.mail.luma.com&#39; para ser usado como o subdomínio de rastreamento.

1. Clique em **[!UICONTROL Submit]** para confirmar a criação da predefinição de landing page. Também é possível salvar a predefinição como rascunho e retomar a configuração posteriormente.

   ![](assets/lp_preset-subdomain-settings-submit.png)

1. Depois que a predefinição de landing page for criada, ela será exibida na lista com a variável **[!UICONTROL Active]** status. Ele está pronto para ser usado em suas landing pages.

   ![](assets/lp-preset-active-temp.png)

Agora você está pronto para [criar landing pages](../landing-pages/create-lp.md) em [!DNL Journey Optimizer].

>[!NOTE]
>
>Saiba como criar predefinições de mensagens para notificações por push e emails em [esta seção](message-presets.md).

**Tópicos relacionados**:

* [Introdução às páginas de aterrissagem](../landing-pages/get-started-lp.md)
* [Criar uma página de aterrissagem](../landing-pages/create-lp.md#create-a-lp)
