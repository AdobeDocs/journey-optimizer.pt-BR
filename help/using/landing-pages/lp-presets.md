---
solution: Journey Optimizer
product: journey optimizer
title: Definir predefinições da página de destino
description: Saiba como configurar seu ambiente para criar e usar landing pages com o Journey Optimizer
feature: Landing Pages, Channel Configuration
role: Admin
level: Experienced
keywords: landing page, landing page, configurar, ambiente, subdomínio, predefinições
exl-id: 7cf1f083-bef0-40b5-8ddd-920a9d108eca
source-git-commit: 8579acfa881f29ef3947f6597dc11d4c740c3d68
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 17%

---

# Definir predefinições da página de destino {#lp-presets}

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain_header"
>title="Criar uma predefinição de página de destino"
>abstract="Para criar uma página de destino e aproveitá-la no Journey Optimizer, você deve criar uma predefinição de página de destino que inclua o subdomínio a ser usado."

Ao [criar uma página de aterrissagem](../landing-pages/create-lp.md#create-a-lp), você deve selecionar uma predefinição de página de aterrissagem para poder criar a página de aterrissagem e aproveitá-la até **[!DNL Journey Optimizer]**.

## Acessar predefinições de página de destino {#access-lp-presets}

Para acessar as predefinições da página de aterrissagem, siga as etapas abaixo.

1. Acesse o menu **[!UICONTROL Administração]** > **[!UICONTROL Canais]**.

1. Selecione **[!UICONTROL Marcas]** > **[!UICONTROL Predefinições de página de aterrissagem]**.

   ![](assets/lp_presets-access.png)

1. Clique em qualquer rótulo predefinido para acessar os detalhes da predefinição de página de aterrissagem.

   ![](assets/lp_preset-details.png)

## Criar uma predefinição de página de destino {#lp-create-preset}

Para criar uma predefinição de página de aterrissagem, siga as etapas abaixo.

>[!NOTE]
>
>Para criar uma predefinição, verifique se você configurou anteriormente pelo menos um subdomínio de página de destino. [Saiba como](lp-subdomains.md)

1. Acesse o menu **[!UICONTROL Administração]** > **[!UICONTROL Canais]** e selecione **[!UICONTROL Identidade Visual]** > **[!UICONTROL Predefinições de página de aterrissagem]**.

1. Selecione **[!UICONTROL Criar predefinição de página de destino]**.

   ![](assets/lp_create-preset-temp.png)

1. Insira um nome e uma descrição para a predefinição.

   >[!NOTE]
   >
   > Os nomes devem começar com uma letra (A-Z). Ele só pode conter caracteres alfanuméricos. Também é possível usar sublinhado `_`, ponto`.` e hífen `-` caracteres.

1. Selecione um subdomínio de landing page na lista suspensa.

   ![](assets/lp_preset-subdomain.png)

   >[!NOTE]
   >
   >Para selecionar um subdomínio, verifique se você configurou anteriormente pelo menos um subdomínio de página de destino. [Saiba como](#lp-subdomains)

   As configurações correspondentes ao subdomínio selecionado são exibidas.

1. Se quiser selecionar o subdomínio da página de aterrissagem para a URL de rastreamento, marque a opção **[!UICONTROL Igual ao subdomínio da página de aterrissagem]**. [Saiba mais sobre rastreamento](../email/message-tracking.md)

   ![](assets/lp_preset-subdomain-settings-same.png)

   Por exemplo, se o URL da página de aterrissagem for &quot;pages.mail.luma.com&quot; e o URL de rastreamento for &quot;data.mail.luma.com&quot;, você poderá escolher &quot;pages.mail.luma.com&quot; para ser usado como o subdomínio de rastreamento.

1. Clique em **[!UICONTROL Enviar]** para confirmar a criação da predefinição de página de destino. <!--You can also save the preset as draft and resume its configuration later on.-->

   <!--![](assets/lp_preset-subdomain-settings-submit.png)-->

1. Após criar a predefinição de página de aterrissagem, ela é exibida na lista com o status **[!UICONTROL Ativo]**. Ele está pronto para ser usado nas páginas de aterrissagem.

   ![](assets/lp-preset-active-temp.png)

Agora você está pronto para [criar páginas de aterrissagem](../landing-pages/create-lp.md) em [!DNL Journey Optimizer].
<!--
>[!NOTE]
>
>Learn how to create channel surfaces for push notifications and emails in [this section](channel-surfaces.md).-->

**Tópicos relacionados**:

* [Introdução às páginas de destino](../landing-pages/get-started-lp.md)
* [Criar uma página de destino](../landing-pages/create-lp.md#create-a-lp)
