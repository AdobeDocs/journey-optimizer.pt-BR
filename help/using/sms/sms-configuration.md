---
solution: Journey Optimizer
product: journey optimizer
title: Configurar o canal de SMS
description: Saiba como configurar seu ambiente para enviar SMS com o Journey Optimizer
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 33dccf32b60a6afb58931823016821fc1effcbd8
workflow-type: tm+mt
source-wordcount: '848'
ht-degree: 19%

---

# Configurar canal de SMS {#sms-configuration}

[!DNL Journey Optimizer] O permite criar suas jornadas e enviar mensagens para o público-alvo direcionado.

Antes de enviar SMS, configure sua instância. Você precisa [integrar as configurações do provedor](#create-api) com o Journey Optimizer e [criar uma superfície de SMS](#message-preset-sms) (ou seja, predefinição de SMS). Essas etapas devem ser executadas por um [administrador do sistema do Adobe Journey Optimizer](../start/path/administrator.md).

## Pré-requisitos{#sms-prerequisites}

Atualmente, o Adobe Journey Optimizer está integrado a provedores de terceiros, como Sinch e Twilio, que oferecem serviços SMS independentes do Adobe Journey Optimizer.

Antes da configuração do SMS, você deve criar uma conta com um desses provedores de SMS para receber o token da API e a ID de serviço que permitirá estabelecer a conexão entre o Adobe Journey Optimizer e o provedor de SMS aplicável.

Seu uso de serviços SMS estará sujeito a termos e condições adicionais do provedor de SMS aplicável. Como a Sinch e a Twilio são produtos de terceiros disponíveis para os usuários do Adobe Journey Optimizer por meio de uma integração, para quaisquer problemas ou consultas relacionadas aos serviços SMS, os usuários da Sinch ou da Twilio precisarão entrar em contato com o provedor de SMS aplicável para obter assistência. A Adobe não controla e não é responsável por produtos de terceiros.

>[!CAUTION]
>
>Para acessar e editar subdomínios SMS, você deve ter a **[!UICONTROL Gerenciar subdomínios de SMS]** permissão na sandbox de produção.

## Criar nova credencial de API {#create-api}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="Configurar o fornecedor de SMS com o Journey Optimizer"
>abstract="Selecione o fornecedor e preencha as credenciais da API de SMS."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="Configurar o fornecedor de SMS com o Journey Optimizer"
>abstract="Antes de enviar SMS, você deve integrar as configurações do provedor com o Journey Optimizer. Depois de concluído, você precisará criar uma superfície de SMS. Essas etapas devem ser executadas por um administrador do sistema do Adobe Journey Optimizer."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/sms/sms-configuration.html?lang=br#message-preset-sms" text="Criar uma superfície de canal SMS"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="Selecionar a configuração do fornecedor de SMS"
>abstract="Selecione as credenciais da API configuradas para seu fornecedor de SMS."

Para configurar seu fornecedor de SMS com o Journey Optimizer, siga estas etapas:

1. No painel esquerdo, navegue até **[!UICONTROL Administração]** > **[!UICONTROL Canais]** e selecione o **[!UICONTROL Credenciais da API]** menu. Clique em **[!UICONTROL Criar novas credenciais de API]** botão.

   ![](assets/sms_6.png)

1. Selecione o **[!UICONTROL Fornecedor de SMS]**:

   * **[!DNL Sinch]**

      Para encontrar o **[!UICONTROL ID do serviço]** e **[!UICONTROL Token de API]**, acesse o menu SMS > APIs na sua conta Sinch.

   * **[!DNL Twilio]**

      Para encontrar o **[!UICONTROL ID do serviço]** e **[!UICONTROL Token de API]**, acesse o painel Informações da conta da página Painel de controle do console.


1. Insira um **[!UICONTROL Nome]** para a credencial da API.

1. Insira seu **[!UICONTROL ID do serviço]** e **[!UICONTROL Token de API]**.

   ![](assets/sms_7.png)

1. Clique em **[!UICONTROL Enviar]** quando você concluiu a configuração das credenciais da API.

Depois de criar e configurar a credencial de API, agora é necessário criar uma superfície de canal (ou seja, predefinição de mensagem) para mensagens SMS.

## Criar uma superfície de SMS {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="Definir a categoria de SMS"
>abstract="Selecione o tipo de mensagens SMS usando esta superfície: Marketing para mensagens SMS promocionais, que exigem consentimento do usuário, ou Transacional para mensagens SMS não comerciais, como redefinição de senha."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html#sms-opt-out-management" text="Recusa em mensagens SMS de marketing"

Depois que o canal SMS for configurado, você deverá criar uma superfície de canal para enviar mensagens SMS do **[!DNL Journey Optimizer]**.

Para criar uma superfície de canal, siga estas etapas:

1. No painel esquerdo, navegue até **[!UICONTROL Administração]** > **[!UICONTROL Canais]** e selecione **[!UICONTROL Marcas]** > **[!UICONTROL Superfícies de canal]**. Clique em **[!UICONTROL Criar superfície de canal]** botão.

   ![](assets/preset-create.png)

1. Insira um nome e uma descrição (opcional) para a superfície e selecione o canal SMS.

   ![](assets/sms_preset.png)

   >[!NOTE]
   >
   > Os nomes devem começar com uma letra (A-Z). Ele só pode conter caracteres alfanuméricos. Também é possível usar sublinhado `_`, ponto`.` e hífen `-` caracteres.

1. Defina o **Configurações de SMS**.

   ![](assets/preset-sms.png)

   * Selecione o **[!UICONTROL Tipo de SMS]** que serão enviados com a superfície: **[!UICONTROL Transacional]** ou **[!UICONTROL Marketing]**.

      * Escolher **Marketing** para SMS promocional: essas mensagens exigem o consentimento do usuário.
      * Escolher **Transacional** para mensagens não comerciais, como confirmação de pedidos, notificações de redefinição de senha ou informações de entrega, por exemplo.

      >[!CAUTION]
      >
      >**Transacional** Mensagens SMS podem ser enviadas a perfis que cancelaram a assinatura de comunicações de marketing. Essas mensagens só podem ser enviadas em contextos específicos.

      Ao criar uma mensagem SMS, você deve escolher uma superfície de canal válida que corresponda à categoria selecionada para a mensagem.

   * Selecione o **[!UICONTROL Configuração de SMS]** para associar à superfície.

      Para obter mais informações sobre como configurar o seu ambiente para enviar mensagens SMS, consulte [nesta seção](#create-api).

   * Insira o **[!UICONTROL Número do remetente]** &#x200B;que você deseja usar para suas comunicações.

   * Selecione o **[!UICONTROL Campo de execução do SMS]** para selecionar o **[!UICONTROL Atributo de perfil]** associados aos números de telefone dos perfis.


1. Se quiser usar a função de redução de URL em suas mensagens SMS, selecione um item na lista suspensa **[!UICONTROL Subdomínio]** lista.

   >[!NOTE]
   >
   >Para selecionar um subdomínio, verifique se você configurou anteriormente pelo menos um subdomínio SMS. [Saiba como](sms-subdomains.md)

1. Após configurar todos os parâmetros, clique em **[!UICONTROL Enviar]** para confirmar. Você também pode salvar a superfície de canal como rascunho e retomar sua configuração posteriormente.

   ![](assets/sms_preset_2.png)

1. Depois que a superfície de canal é criada, ela é exibida na lista com o **[!UICONTROL Processando]** status.

   >[!NOTE]
   >
   >Se as verificações não forem bem-sucedidas, saiba mais sobre os possíveis motivos de falha no [nesta seção](#monitor-channel-surfaces).

1. Depois que as verificações forem bem-sucedidas, a superfície de canal obterá a variável **[!UICONTROL Ativo]** status. Ele está pronto para ser usado para enviar mensagens.

   ![](assets/preset-active.png)

Agora você está pronto para enviar mensagens SMS com o Journey Optimizer.

**Tópicos relacionados**

* [Criar uma mensagem de SMS.](create-sms.md)
* [Adicionar uma mensagem em uma jornada](../building-journeys/journeys-message.md)
* [Adicionar uma mensagem em uma campanha](../campaigns/create-campaign.md)

