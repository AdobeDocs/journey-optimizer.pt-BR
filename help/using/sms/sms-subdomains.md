---
solution: Journey Optimizer
product: journey optimizer
title: Configurar subdomínios para mensagens de texto (SMS/MMS)
description: Saiba como configurar subdomínios SMS com o Journey Optimizer
role: Admin
feature: SMS, Channel Configuration
level: Intermediate
keywords: SMS, subdomínios, configuração
exl-id: 08a546d1-060c-43e8-9eac-4c38945cc3e1
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 24%

---

# Configuração de subdomínios de SMS {#sms-mms-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_sms_header"
>title="Delegar um subdomínio de SMS/MMS"
>abstract="Configure seu subdomínio para mensagens de texto (SMS/MMS). Você pode usar um subdomínio já delegado à Adobe ou configurar um novo subdomínio."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_sms"
>title="Delegar um subdomínio de SMS/MMS"
>abstract="Você deve configurar um subdomínio para usar com as mensagens de texto, pois ele será necessário para criar uma configuração de SMS. Você pode usar um subdomínio já delegado à Adobe ou configurar um novo subdomínio."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/channels/sms/configure-sms/sms-configuration-surface" text="Criar uma configuração de SMS"

>[!CONTEXTUALHELP]
>id="ajo_admin_config_sms_subdomain"
>title="Selecionar um subdomínio de SMS/MMS"
>abstract="Para criar uma configuração de SMS, verifique se você configurou anteriormente pelo menos um subdomínio de SMS que possa ser selecionado na lista Nome de subdomínio."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/channels/sms/configure-sms/sms-configuration-surface" text="Criar uma configuração de SMS"

Para encurtar URLs adicionadas às suas mensagens SMS/MMS, você deve configurar o subdomínio que selecionará ao [criar uma configuração de SMS](sms-configuration.md#message-preset-sms).

Você pode usar um subdomínio que já foi delegado à Adobe ou configurar outro subdomínio. Saiba mais sobre como delegar subdomínios à Adobe em [esta seção](../configuration/delegate-subdomain.md).

>[!CAUTION]
>
>* A configuração do subdomínio SMS é compartilhada entre todos os ambientes. Portanto, qualquer modificação em um subdomínio SMS também afeta outras sandboxes de produção.
>
>* Para acessar e editar subdomínios SMS, você deve ter a permissão **[!UICONTROL Gerenciar subdomínios SMS]** na sandbox de produção. Saiba mais sobre permissões [nesta seção](../administration/high-low-permissions.md).
>

## Usar um subdomínio existente {#sms-use-existing-subdomain}

Para usar um subdomínio que já está delegado à Adobe, siga as etapas abaixo.

1. Navegue até o menu **[!UICONTROL Administração]** > **[!UICONTROL Canais]** e selecione **[!UICONTROL Configurações de SMS]** > **[!UICONTROL Subdomínios de SMS]**.

1. Clique em **[!UICONTROL Configurar subdomínio]**.

   ![](assets/sms_set-up-subdomain.png)

1. Selecione **[!UICONTROL Usar subdomínio delegado]** na seção **[!UICONTROL Tipo de configuração]**.

   ![](assets/sms_use-delegated-subdomain.png)

1. Insira o prefixo que será exibido no URL do SMS.

   >[!NOTE]
   >
   >Somente caracteres alfanuméricos e hifens são permitidos.

1. Selecione um subdomínio delegado na lista.

   >[!NOTE]
   >
   >Não é possível selecionar um subdomínio que já esteja sendo usado como subdomínio de SMS.

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

   ![](assets/sms_prefix-and-subdomain.png)

   <!--Note that you cannot use multiple delegated subdomains of the same parent domain. For example, if 'marketing1.yourcompany.com' is already delegated to Adobe for your SMS messages, you will not be able to use 'marketing2.yourcompany.com'. However, multi-level subdomains being supported for SMS, you may proceed using a subdomain of 'marketing1.yourcompany.com' (such as 'email.marketing1.yourcompany.com'), or a different parent domain.-->

   >[!CAUTION]
   >
   >Se você selecionar um domínio que foi delegado à Adobe usando o [método CNAME](../configuration/delegate-subdomain.md#cname-subdomain-delegation), deverá criar o registro DNS na sua plataforma de hospedagem. Para gerar o registro DNS, o processo é o mesmo de quando você configura um novo subdomínio SMS. Saiba mais em [esta seção](#sms-configure-new-subdomain).

1. Clique em **[!UICONTROL Enviar]**.

1. Depois de enviado, o subdomínio é exibido na lista com o status **[!UICONTROL Processando]**. Para obter mais informações sobre os status dos subdomínios, consulte [esta seção](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

   >[!NOTE]
   >
   >Antes de poder usar esse subdomínio para enviar mensagens, você deve aguardar até que o Adobe execute as verificações necessárias, que podem levar até 4 horas.<!--Learn more in [this section](delegate-subdomain.md#subdomain-validation).-->

1. Depois que as verificações forem bem-sucedidas, o subdomínio obterá o status **[!UICONTROL Success]**. Ele está pronto para ser usado para criar configurações de canal SMS.

## Configurar um novo subdomínio {#sms-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_subdomain_dns"
>title="Gerar o registro DNS correspondente"
>abstract="Para configurar um novo subdomínio de SMS, é necessário copiar as informações do servidor de nomes da Adobe exibidas na interface do Journey Optimizer e colá-las em sua solução de hospedagem de domínio para gerar o registro DNS correspondente. Depois que as verificações forem bem-sucedidas, o subdomínio estará pronto para criar configurações de SMS."

Para configurar um novo subdomínio, siga as etapas abaixo.

1. Navegue até o menu **[!UICONTROL Administração]** > **[!UICONTROL Canais]** e selecione **[!UICONTROL Configurações de SMS]** > **[!UICONTROL Subdomínios de SMS]**.

1. Clique em **[!UICONTROL Configurar subdomínio]**.

   ![](assets/sms_set-up-subdomain.png)

1. Selecione **[!UICONTROL Adicionar seu próprio domínio]** na seção **[!UICONTROL Tipo de configuração]**.

   ![](assets/sms_add-your-own-subdomain.png)

1. Especifique o subdomínio que será delegado.

   >[!CAUTION]
   >
   >* Não é possível usar um subdomínio SMS existente.
   >
   >* Letras maiúsculas não são permitidas em subdomínios.

   Não é permitido delegar um subdomínio inválido à Adobe. Insira um subdomínio válido de propriedade de sua organização, como marketing.yourcompany.com.

   >[!NOTE]
   >
   >Subdomínios de vários níveis (do mesmo domínio pai) são suportados. Por exemplo, você pode usar &quot;sms.marketing.yourcompany.com&quot;.

1. O registro a ser colocado em seus servidores DNS é exibido. Copie esse registro ou baixe um arquivo CSV e navegue até a solução de hospedagem de domínio para gerar o registro DNS correspondente.

1. Verifique se o registro DNS foi gerado na solução de hospedagem de domínio. Se tudo estiver configurado corretamente, marque a caixa &quot;Eu confirmo...&quot; e clique em **[!UICONTROL Enviar]**.

   ![](assets/sms_add-your-own-subdomain-confirm.png)

   >[!NOTE]
   >
   >Ao configurar um novo subdomínio SMS, ele sempre apontará para um registro CNAME.

1. Depois que a delegação de subdomínio for enviada, o subdomínio será exibido na lista com o status **[!UICONTROL Processando]**. Para obter mais informações sobre os status dos subdomínios, consulte [esta seção](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

Antes de usar um subdomínio para enviar mensagens SMS, você deve aguardar até que o Adobe execute as verificações necessárias, que podem levar até 4 horas.<!--Learn more in [this section](#subdomain-validation).--> Depois que as verificações forem bem-sucedidas, o subdomínio obterá o status **[!UICONTROL Sucesso]**. Ele está pronto para ser usado para criar configurações de canal SMS.

Observe que o subdomínio será marcado como **[!UICONTROL Falha]** se você não criar o registro de validação na solução de hospedagem.
