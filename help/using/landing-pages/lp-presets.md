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
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 13%

---

# Definir predefinições da página de destino {#lp-presets}

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain_header"
>title="Criar uma predefinição de página de destino"
>abstract="Para criar uma página de destino e aproveitá-la no Journey Optimizer, você deve criar uma predefinição de página de destino que inclua o subdomínio a ser usado."

## Introdução às predefinições de página de destino {#gs-lp-presets}

Ao [criar uma página de aterrissagem](../landing-pages/create-lp.md#create-lp), você deve selecionar uma predefinição de página de aterrissagem para poder criar a página de aterrissagem e aproveitá-la até **[!DNL Journey Optimizer]**. A predefinição inclui o subdomínio a ser usado para as páginas de aterrissagem com base nessa predefinição.

Antes de criar uma predefinição, verifique se você configurou anteriormente pelo menos um subdomínio de página de destino. [Saiba como criar um subdomínio de página de destino](lp-subdomains.md).

## Acessar predefinições de página de destino {#access-lp-presets}

Para acessar predefinições de páginas de aterrissagem, siga as etapas abaixo:

1. Acesse o menu **[!UICONTROL Administração]** > **[!UICONTROL Canais]**.

1. Selecione **[!UICONTROL Configurações da página de aterrissagem]** > **[!UICONTROL Predefinições da página de aterrissagem]**.

   ![](assets/lp_presets-access.png)

1. Clique em qualquer rótulo predefinido para acessar os detalhes da predefinição de página de aterrissagem.

   ![](assets/lp_preset-details.png)

## Criar uma predefinição de página de destino {#lp-create-preset}

Para criar uma predefinição de página de aterrissagem, siga as etapas abaixo:

1. Navegue pelo menu **[!UICONTROL Administração]** > **[!UICONTROL Canais]** e selecione **[!UICONTROL Configurações da página de aterrissagem]** > **[!UICONTROL Predefinições da página de aterrissagem]**.

1. Selecione **[!UICONTROL Criar predefinição de página de destino]**.

   ![](assets/lp_create-preset-temp.png)

1. Insira um nome e uma descrição para a predefinição.

   Os nomes devem começar com uma letra (A-Z) e conter apenas caracteres alfanuméricos, sublinhado `_`, ponto `.` e hífen `-` caracteres.

1. Selecione um subdomínio de landing page na lista suspensa.

   ![](assets/lp_preset-subdomain.png)

   >[!NOTE]
   >
   >Para selecionar um subdomínio, verifique se você configurou anteriormente pelo menos um subdomínio de página de destino. [Saiba como](lp-subdomains.md)

   As configurações correspondentes ao subdomínio selecionado são exibidas.

1. Você pode selecionar o subdomínio da página de aterrissagem para a **[!UICONTROL URL de rastreamento]** marcando a opção **[!UICONTROL Igual ao subdomínio da página de aterrissagem]**. [Saiba mais sobre o rastreamento](../email/message-tracking.md)

   ![](assets/lp_preset-subdomain-settings-same.png)

   Por exemplo, se o URL da página de aterrissagem for &quot;pages.mail.luma.com&quot; e o URL de rastreamento for &quot;data.mail.luma.com&quot;, você poderá escolher &quot;pages.mail.luma.com&quot; para ser usado como o subdomínio de rastreamento.

   >[!CAUTION]
   >
   >O subdomínio de página de aterrissagem selecionado é usado para especificar a **[!UICONTROL URL de Acompanhamento]** do <!--and **[!UICONTROL Image Delivery URL]** -->se esse subdomínio foi criado usando um [subdomínio existente](lp-subdomains.md#lp-use-existing-subdomain).
   >
   >Se o subdomínio tiver sido criado com a opção [Adicionar seu próprio domínio](lp-subdomains.md#lp-configure-new-subdomain), o subdomínio primário (ou seja, o primeiro subdomínio delegado) será usado.

1. Clique em **[!UICONTROL Enviar]** para confirmar a criação da predefinição de página de destino. <!--You can also save the preset as draft and resume its configuration later on.-->

   <!--![](assets/lp_preset-subdomain-settings-submit.png)-->

1. Após criar a predefinição de página de aterrissagem, ela é exibida na lista com o status **[!UICONTROL Ativo]**. Ele está pronto para ser usado nas páginas de aterrissagem.

Agora você está pronto para [criar páginas de aterrissagem](../landing-pages/create-lp.md) em [!DNL Journey Optimizer].
<!--
>[!NOTE]
>
>Learn how to create channel configurations for push notifications and emails in [this section](channel-surfaces.md).-->

**Tópicos relacionados**:

* [Introdução às páginas de destino](../landing-pages/get-started-lp.md)
* [Criar uma página de destino](../landing-pages/create-lp.md#create-lp)
