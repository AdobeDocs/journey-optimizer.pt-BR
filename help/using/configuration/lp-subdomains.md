---
title: Configurar subdomínios de página de aterrissagem
description: Saiba como configurar subdomínios de página de aterrissagem com o Journey Optimizer
role: Admin
level: Intermediate
source-git-commit: a485c58366f0690fb2515139658224d59468a24f
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---

# Configurar subdomínios de página de aterrissagem {#lp-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain"
>title="Criar uma predefinição de página de aterrissagem"
>abstract="Para criar uma predefinição de página de aterrissagem, verifique se você configurou anteriormente pelo menos um subdomínio de página de aterrissagem para escolher na lista Nome de subdomínio ."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/lp-configuration.html#lp-create-preset" text="Criar predefinições de página de aterrissagem"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_lp"
>title="Delegar um subdomínio de página de aterrissagem"
>abstract="Você deve configurar um subdomínio para usar nas landing pages, pois ele precisará para criar uma predefinição de landing page. Você pode usar um subdomínio já delegado ao Adobe ou configurar um novo subdomínio."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/lp-configuration.html#lp-create-preset" text="Criar predefinições de página de aterrissagem"

Para poder [criar predefinições de página de aterrissagem](lp-presets.md), você deve configurar os subdomínios que serão usados para as landing pages.

Você pode usar um subdomínio que já tenha sido delegado ao Adobe ou pode configurar outro subdomínio. Saiba mais sobre como delegar subdomínios ao Adobe [esta seção](delegate-subdomain.md).

## Usar um subdomínio existente {#lp-use-existing-subdomain}

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

## Configurar um novo subdomínio {#lp-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_lp_subdomain_dns"
>title="Gerar o registro DNS correspondente"
>abstract="Para configurar um novo subdomínio de página de aterrissagem, você precisa copiar as informações do servidor de nomes do Adobe exibidas na interface do Journey Optimizer e colá-las em sua solução de hospedagem de domínio para gerar o registro DNS correspondente. Depois que as verificações forem bem-sucedidas, o subdomínio estará pronto para ser usado para criar predefinições de páginas de aterrissagem."

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
