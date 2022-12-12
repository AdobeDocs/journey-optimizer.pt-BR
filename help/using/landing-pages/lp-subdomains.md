---
solution: Journey Optimizer
product: journey optimizer
title: Configurar subdomínios de página de aterrissagem
description: Saiba como configurar subdomínios de página de aterrissagem com o Journey Otimizer
role: Admin
level: Intermediate
exl-id: dd1af8dc-3920-46cb-ae4d-a8f4d4c26e89
source-git-commit: 61c90f39fa2bddb384e5581e3935c43d4691c355
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 0%

---

# Configurar subdomínios de página de aterrissagem {#lp-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_lp_header"
>title="Delegar um subdomínio de página de aterrissagem"
>abstract="Você configurará seu subdomínio para um uso de página de aterrissagem. Você pode usar um subdomínio que já tenha sido delegado à Adobe ou configurar outro subdomínio."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_lp"
>title="Delegar um subdomínio de página de aterrissagem"
>abstract="Você deve configurar um subdomínio para usar nas landing pages, pois ele precisará para criar uma predefinição de landing page. Você pode usar um subdomínio já delegado à Adobe ou configurar um novo subdomínio."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-presets.html#lp-create-preset" text="Criar predefinições de página de aterrissagem"

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain"
>title="Criar uma predefinição de página de aterrissagem"
>abstract="Para criar uma predefinição de página de aterrissagem, verifique se você configurou anteriormente pelo menos um subdomínio de página de aterrissagem para escolher na lista Nome de subdomínio ."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-presets.html#lp-create-preset" text="Criar predefinições de página de aterrissagem"

Para poder [criar predefinições de página de aterrissagem](lp-presets.md), você deve configurar os subdomínios que serão usados para as landing pages.

Você pode usar um subdomínio que já tenha sido delegado à Adobe ou pode configurar outro subdomínio. Saiba mais sobre como delegar subdomínios à Adobe no [esta seção](../configuration/delegate-subdomain.md).

>[!CAUTION]
>
>A configuração do subdomínio da página de aterrissagem é comum a todos os ambientes. Portanto, qualquer modificação em um subdomínio de página de aterrissagem também afetará as sandboxes de produção.

Observe que letras maiúsculas não devem ser permitidas em um subdomínio

## Usar um subdomínio existente {#lp-use-existing-subdomain}

Para usar um subdomínio já delegado à Adobe, siga as etapas abaixo.

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

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

   ![](assets/lp_prefix-and-subdomain.png)

   Observe que não é possível usar vários subdomínios delegados do mesmo domínio pai. Por exemplo, se &#39;marketing1.suaempresa.com&#39; já estiver delegado à Adobe para suas páginas de aterrissagem, você não poderá usar &#39;marketing2.suaempresa.com&#39;. No entanto, subdomínios de vários níveis que são compatíveis com landing pages, você pode continuar usando um subdomínio de &#39;marketing1.suaempresa.com&#39; (como &#39;email.marketing1.suaempresa.com&#39;) ou um domínio pai diferente.

   >[!CAUTION]
   >
   >Se você selecionar um domínio que foi delegado à Adobe usando a variável [método CNAME](../configuration/delegate-subdomain.md#cname-subdomain-delegation), você deve criar o registro DNS na plataforma de hospedagem. Para gerar o registro DNS, o processo é o mesmo que ao configurar um novo subdomínio de página de aterrissagem. Saiba mais sobre como [esta seção](#lp-configure-new-subdomain).

1. Clique em **[!UICONTROL Submit]**.

1. Depois de enviado, o subdomínio é exibido na lista com a variável **[!UICONTROL Processing]** status. Para obter mais informações sobre os status dos subdomínios, consulte [esta seção](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

   ![](assets/lp_subdomain-processing.png)

   >[!NOTE]
   >
   >Antes de poder usar esse subdomínio para enviar mensagens, você deve aguardar até que a Adobe execute as verificações necessárias, que podem levar até 4 horas.<!--Learn more in [this section](delegate-subdomain.md#subdomain-validation).-->

1. Depois que as verificações são bem-sucedidas, o subdomínio recebe o **[!UICONTROL Success]** status. Ele está pronto para ser usado para criar predefinições de página de aterrissagem.

## Configurar um novo subdomínio {#lp-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_lp_subdomain_dns"
>title="Gerar o registro DNS correspondente"
>abstract="Para configurar um novo subdomínio de página de aterrissagem, você precisa copiar as informações do servidor de nomes da Adobe exibidas na interface do Journey Otimizer e colá-las em sua solução de hospedagem de domínio para gerar o registro DNS correspondente. Depois que as verificações forem bem-sucedidas, o subdomínio estará pronto para ser usado para criar predefinições de páginas de aterrissagem."

Para configurar um novo subdomínio, siga as etapas abaixo.

1. Acesse o **[!UICONTROL Administration]** > **[!UICONTROL Channels]** e selecione **[!UICONTROL Email configuration]** > **[!UICONTROL Landing page subdomains]**.

1. Clique em **[!UICONTROL Set up subdomain]**.

1. Selecionar **[!UICONTROL Add your own domain]** do **[!UICONTROL Configuration type]** seção.

   ![](assets/lp_add-your-own-subdomain.png)

1. Especifique o subdomínio que será delegado.

   >[!CAUTION]
   >
   >Não é possível usar um subdomínio de página de aterrissagem existente.
   >
   >Letras maiúsculas não são permitidas em subdomínios.

   Não é permitido delegar um subdomínio inválido à Adobe. Certifique-se de inserir um subdomínio válido que seja de propriedade de sua organização, como marketing.yourcompany.com.

   >[!NOTE]
   >
   >Para páginas de aterrissagem, subdomínios de vários níveis são compatíveis. Por exemplo, você pode usar &#39;email.marketing.suaempresa.com&#39;.

1. O registro a ser colocado em seus servidores DNS é exibido. Copie esse registro ou baixe um arquivo CSV e navegue até a solução de hospedagem de domínio para gerar o registro DNS correspondente.

1. Certifique-se de que o registro DNS foi gerado em sua solução de hospedagem de domínio. Se tudo estiver configurado corretamente, marque a caixa &quot;I confirm...&quot; e clique em **[!UICONTROL Submit]**.

   ![](assets/lp_add-your-own-subdomain-confirm.png)

   >[!NOTE]
   >
   >Ao configurar um novo subdomínio de página de aterrissagem, ele sempre apontará para um registro CNAME.

1. Depois que a delegação de subdomínio for enviada, o subdomínio será exibido na lista com a variável **[!UICONTROL Processing]** status. Para obter mais informações sobre os status dos subdomínios, consulte [esta seção](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

   >[!NOTE]
   >
   >Antes de poder usar esse subdomínio para enviar mensagens, você deve aguardar até que a Adobe execute as verificações necessárias, que podem levar até 4 horas.<!--Learn more in [this section](#subdomain-validation).-->

1. Depois que as verificações são bem-sucedidas, o subdomínio recebe o **[!UICONTROL Success]** status. Ele está pronto para ser usado para criar predefinições de página de aterrissagem.

   Observe que o subdomínio será marcado como **[!UICONTROL Failed]** se você não criar o registro de validação em sua solução de hospedagem.
