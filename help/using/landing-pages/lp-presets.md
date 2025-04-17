---
solution: Journey Optimizer
product: journey optimizer
title: Definir predefinições da página de destino
description: Aprenda a configurar seus ambiente para criar e usar páginas de aterrissagem com o Journey Optimizer
feature: Landing Pages, Channel Configuration
role: Admin
level: Experienced
keywords: landing, landing page, configurar, ambiente, subdomínio, predefinições
exl-id: 7cf1f083-bef0-40b5-8ddd-920a9d108eca
source-git-commit: 8e5a904f9310385f5a8186159dedde9942624268
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 15%

---

# Definir predefinições da página de destino {#lp-presets}

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain_header"
>title="Criar uma predefinição de página de destino"
>abstract="Para criar uma página de destino e aproveitá-la no Journey Optimizer, você deve criar uma predefinição de página de destino que inclua o subdomínio a ser usado."

## Introdução às predefinições do landing page {#gs-lp-presets}

Ao [criar um landing page](../landing-pages/create-lp.md#create-a-lp), você deve selecionar uma predefinição landing page para poder build o landing page e usar-lo **[!DNL Journey Optimizer]**. A predefinição inclui o subdomínio a ser usado para as páginas de aterrissagem com base nessa predefinição.

Antes de criar uma predefinição, verifique se você configurou anteriormente pelo menos um subdomínio landing page. [Aprenda a criar um subdomínio](lp-subdomains.md) landing page.

## Acessar predefinições de landing page {#access-lp-presets}

Para acessar landing page predefinições, seguir as etapas abaixo:

1. Acesse o **[!UICONTROL menu Administração]** > **[!UICONTROL Canais]** .

1. Selecione **[!UICONTROL Configurações]** de página inicial > **[!UICONTROL predefinições de página inicial.]**

   ![](assets/lp_presets-access.png)

1. Clique em qualquer rótulo predefinido para acessar os detalhes da predefinição landing page.

   ![](assets/lp_preset-details.png)

## Criar uma predefinição de página de destino {#lp-create-preset}

Para criar uma predefinição landing page, seguir as etapas abaixo:

1. Navegue pelo **[!UICONTROL menu Administração]** > **[!UICONTROL Canais]** e selecione **[!UICONTROL Configurações]** de aterrissagem página > **[!UICONTROL predefinições de página inicial.]**

1. Selecione **[!UICONTROL Criar landing page predefinição]**.

   ![](assets/lp_create-preset-temp.png)

1. Insira um nome e uma descrição para a predefinição.

   Os nomes devem começar com uma letra (A-Z) e conter apenas caracteres alfa-numérico, sublinhado `_`, ponto`.` e caracteres de hífen `-` .

1. Selecione um subdomínio landing page no lista suspenso.

   ![](assets/lp_preset-subdomain.png)

   Para poder selecionar um subdomínio, verifique se você configurou anteriormente pelo menos um subdomínio landing page. [Saiba como](#lp-subdomains)

   As configurações correspondentes ao subdomínio selecionado são exibidas.

1. Você pode selecionar o subdomínio da página de aterrissagem para a URL de rastreamento marcando a opção **[!UICONTROL Igual ao subdomínio da página de aterrissagem]**. [Saiba mais sobre a rastreamento](../email/message-tracking.md)

   ![](assets/lp_preset-subdomain-settings-same.png)

   Por exemplo, se o URL da página de aterrissagem for &quot;pages.mail.luma.com&quot; e o URL de rastreamento for &quot;data.mail.luma.com&quot;, você poderá escolher &quot;pages.mail.luma.com&quot; para ser usado como o subdomínio de rastreamento.

1. Clique **[!UICONTROL em Enviar]** para confirmar a criação landing page predefinição. <!--You can also save the preset as draft and resume its configuration later on.-->

   <!--![](assets/lp_preset-subdomain-settings-submit.png)-->

1. Depois que a predefinição landing page for criada, ela será exibida no lista com o **[!UICONTROL status Ativo]** . Ela está pronta para ser usada para suas páginas iniciais.

Agora você está pronto para [criar páginas](../landing-pages/create-lp.md) iniciais.[!DNL Journey Optimizer]
<!--
>[!NOTE]
>
>Learn how to create channel configurations for push notifications and emails in [this section](channel-surfaces.md).-->

**Tópicos relacionados**:

* [Introdução às páginas de destino](../landing-pages/get-started-lp.md)
* [Criar uma página de destino](../landing-pages/create-lp.md#create-a-lp)
