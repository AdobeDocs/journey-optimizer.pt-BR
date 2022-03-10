---
title: Configuração da página de aterrissagem
description: Saiba como configurar seu ambiente para criar e usar landing pages com o Journey Optimizer
role: Admin
level: Intermediate
exl-id: 7cf1f083-bef0-40b5-8ddd-920a9d108eca
source-git-commit: 8f0e85a08a0ab510f02aab3787f30933e430e3e4
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 2%

---

# Configurar páginas de aterrissagem {#lp-configuration}

## Configurar subdomínios de página de aterrissagem {#lp-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_configure_subdomain"
>title="Configurar subdomínios de página de aterrissagem"
>abstract="Para selecionar um subdomínio, verifique se você configurou anteriormente pelo menos um subdomínio de página de aterrissagem."

Para poder [criar predefinições de página de aterrissagem](#lp-create-preset), é necessário configurar os subdomínios que serão usados para as landing pages.

Você pode usar um subdomínio que já tenha sido delegado ao Adobe ou pode configurar outro subdomínio. Saiba mais sobre como delegar subdomínios ao Adobe [esta seção](delegate-subdomain.md).

### Usar um subdomínio existente {#lp-use-existing-subdomain}

Para usar um subdomínio que já tenha sido delegado ao Adobe, siga as etapas abaixo.

1. Acesse o **[!UICONTROL Administration]** > **[!UICONTROL Channels]** e selecione **[!UICONTROL Email configuration]** > **[!UICONTROL Landing page subdomains]**.

   ![](assets/lp_access-subdomains.png)

1. Clique em **[!UICONTROL Set up subdomain]**.

   ![](assets/lp_set-up-subdomain.png)

1. Selecionar **[!UICONTROL Use delegated domain]** do **[!UICONTROL Configuration type]** seção.

   ![](assets/lp_use-delegated-subdomain.png)

1. Insira o prefixo que será exibido no URL da página inicial.

   >[!NOTE]
   >
   >Somente caracteres alfanuméricos e hifens são permitidos.

1. Selecione um subdomínio delegado na lista.

   >[!NOTE]
   >
   >Não é possível selecionar um subdomínio que já esteja sendo usado como subdomínio de página de aterrissagem.

   ![](assets/lp_prefix-and-subdomain.png)

   >[!CAUTION]
   >
   >Se você selecionar um domínio que foi delegado ao Adobe usando a variável [método CNAME](delegate-subdomain.md#cname-subdomain-delegation), você deve criar o registro DNS na plataforma de hospedagem. Para gerar o registro DNS, o processo é o mesmo que ao configurar um novo subdomínio de página de aterrissagem. Saiba mais sobre como [esta seção](#lp-configure-new-subdomain).

1. Clique em **[!UICONTROL Submit]**.

1. Depois de enviado, o subdomínio é exibido na lista com a variável **[!UICONTROL Processing]** status. Para obter mais informações sobre os status dos subdomínios, consulte [esta seção](access-subdomains.md).<!--Same statuses?-->

   ![](assets/lp_subdomain-processing.png)

   >[!NOTE]
   >
   >Antes de poder usar esse subdomínio para enviar mensagens, você deve aguardar até que o Adobe execute as verificações necessárias, que podem levar até 4 horas.<!--Learn more in [this section](delegate-subdomain.md#subdomain-validation).-->

1. Depois que as verificações são bem-sucedidas, o subdomínio recebe o **[!UICONTROL Success]** status. Ele está pronto para ser usado para criar predefinições de página de aterrissagem.

### Configurar um novo subdomínio {#lp-configure-new-subdomain}

Para configurar um novo subdomínio, siga as etapas abaixo.

1. Acesse o **[!UICONTROL Administration]** > **[!UICONTROL Channels]** e selecione **[!UICONTROL Email configuration]** > **[!UICONTROL Landing page subdomains]**.

1. Clique em **[!UICONTROL Set up subdomain]**.

1. Selecionar **[!UICONTROL Add your own domain]** do **[!UICONTROL Configuration type]** seção.

   ![](assets/lp_add-your-own-subdomain.png)

1. Especifique o subdomínio que será delegado.

   >[!CAUTION]
   >
   >Não é possível usar um subdomínio de página de aterrissagem existente.

   Não é permitido delegar um subdomínio inválido para Adobe. Certifique-se de inserir um subdomínio válido que seja de propriedade de sua organização, como marketing.suaempresa.com.

   Subdomínios de vários níveis, como &quot;email.marketing.suaempresa.com&quot;, não são suportados no momento.

1. O registro a ser colocado em seus servidores DNS é exibido. Copie esse registro ou baixe um arquivo CSV e navegue até a solução de hospedagem de domínio para gerar o registro DNS correspondente.

1. Certifique-se de que o registro DNS foi gerado em sua solução de hospedagem de domínio. Se tudo estiver configurado corretamente, marque a caixa &quot;I confirm...&quot; e clique em **[!UICONTROL Submit]**.

   ![](assets/lp_add-your-own-subdomain-confirm.png)

   >[!NOTE]
   >
   >Ao configurar um novo subdomínio de página de aterrissagem, ele sempre apontará para um registro CNAME.

1. Depois que a delegação de subdomínio for enviada, o subdomínio será exibido na lista com a variável **[!UICONTROL Processing]** status. Para obter mais informações sobre os status dos subdomínios, consulte [esta seção](access-subdomains.md).<!--Same statuses?-->

   >[!NOTE]
   >
   >Antes de poder usar esse subdomínio para enviar mensagens, você deve aguardar até que o Adobe execute as verificações necessárias, que podem levar até 4 horas.<!--Learn more in [this section](#subdomain-validation).-->

1. Depois que as verificações são bem-sucedidas, o subdomínio recebe o **[!UICONTROL Success]** status. Ele está pronto para ser usado para criar predefinições de página de aterrissagem.

   Observe que o subdomínio será marcado como **[!UICONTROL Failed]** se você não criar o registro de validação em sua solução de hospedagem.

## Definir predefinições da landing page {#lp-define-preset}

When [criação de uma landing page](../landing-pages/create-lp.md#create-a-lp), você deve selecionar uma predefinição de página de aterrissagem para criar a página de aterrissagem e aproveitá-la **[!DNL Journey Optimizer]**.

### Acessar predefinições da página de aterrissagem {#lp-presets}

Para acessar as predefinições da landing page, siga as etapas abaixo.

1. Acesse o **[!UICONTROL Administration]** > **[!UICONTROL Channels]** menu.

1. Selecione **[!UICONTROL Branding]** > **[!UICONTROL Landing page presets]**.

   ![](assets/lp_presets-access.png)

1. Clique em qualquer rótulo predefinido para acessar os detalhes predefinidos da landing page.

   ![](assets/lp_preset-details.png)

### Criar uma predefinição de página de aterrissagem {#lp-create-preset}

Para criar uma predefinição de página de aterrissagem, siga as etapas abaixo.

>[!NOTE]
>
>Para criar uma predefinição, verifique se você configurou anteriormente pelo menos um subdomínio de página de aterrissagem. [Saiba como](#lp-subdomains)

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

1. Se desejar selecionar o subdomínio da página de aterrissagem como o URL de rastreamento, verifique a variável **[!UICONTROL Same as landing page subdomain]** opção. [Saiba mais sobre o rastreamento](../messages/message-tracking.md)

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
