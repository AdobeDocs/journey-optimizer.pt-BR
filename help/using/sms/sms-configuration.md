---
solution: Journey Optimizer
product: journey optimizer
title: Configurar o canal de SMS
description: Saiba como configurar seu ambiente para enviar SMS com o Journey Optimizer
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: a6b2c1585867719a48f9abc4bf0eb81558855d85
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 16%

---

# Configurar canal de SMS {#sms-configuration}

[!DNL Journey Optimizer] O permite criar suas jornadas e enviar mensagens para o público-alvo direcionado.

Antes de enviar SMS, configure sua instância. Você precisa [integrar as configurações do provedor](#create-api) com o Journey Optimizer e [criar uma superfície de SMS](#message-preset-sms) (ou seja, predefinição de SMS). Essas etapas devem ser executadas por um [administrador do sistema do Adobe Journey Optimizer](../start/path/administrator.md).

## Pré-requisitos{#sms-prerequisites}

Atualmente, o Adobe Journey Optimizer está integrado a provedores de terceiros, como Sinch, Twilio e Infobip, que oferecem serviços SMS independentes do Adobe Journey Optimizer.

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
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/sms/sms-configuration.html?lang=pt-BR#message-preset-sms" text="Criar uma superfície de canal SMS"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="Selecionar a configuração do fornecedor de SMS"
>abstract="Selecione as credenciais da API configuradas para seu fornecedor de SMS."

Para configurar seu fornecedor de SMS com o Journey Optimizer, siga estas etapas:

1. No painel esquerdo, navegue até **[!UICONTROL Administração]** > **[!UICONTROL Canais]** e selecione o **[!UICONTROL Credenciais da API]** menu. Clique em **[!UICONTROL Criar novas credenciais de API]** botão.

   ![](assets/sms_6.png)

1. Configurar suas credenciais da API de SMS:

   * Para **[!DNL Sinch]**:

      * **[!UICONTROL Nome]**: escolha um nome para a credencial da API.

      * **[!UICONTROL ID do serviço]** e **[!UICONTROL Token de API]**: para acessar a página APIs, você pode encontrar suas credenciais na guia SMS.  [Saiba mais](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"}.

      * **[!UICONTROL Mensagem de Opt-in]**: digite a resposta personalizada que é enviada automaticamente como **[!UICONTROL Mensagem de Opt-in]**.

      * **[!UICONTROL Mensagem de ajuda]**: digite a resposta personalizada que é enviada automaticamente como **Mensagem de ajuda**.

   * Para **[!DNL Sinch MMS]**:

      * **[!UICONTROL Nome]**: escolha um nome para a credencial da API.

      * **[!UICONTROL ID do projeto]**, **[!UICONTROL ID do aplicativo]** e **[!UICONTROL Token de API]**: no menu da API de conversa, você pode encontrar suas credenciais no menu Aplicativo.  [Saiba mais](https://docs.cc.sinch.com/cloud/service-configuration/en/oxy_ex-1/common/wln1620131604643.html)

   * Para **[!DNL Twilio]**:

      * **[!UICONTROL Nome]**: escolha um nome para a credencial da API.

      * **[!UICONTROL SID da conta]** e **[!UICONTROL Token de autenticação]**: acesse o painel Informações da conta da página Painel do Twilio Console para encontrar suas credenciais.

      * **[!UICONTROL SID da Mensagem]**: digite o identificador exclusivo atribuído a cada mensagem criada pela API do Twilio. [Saiba mais](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}.

   * Para **[!DNL Infobip]**:

      * **[!UICONTROL Nome]**: escolha um nome para a credencial da API.

      * **[!UICONTROL URL de base da API]** e **[!UICONTROL Token de API]**: acesse a página inicial da interface da Web ou a página de gerenciamento de chaves da API para encontrar suas credenciais. [Saiba mais](https://www.infobip.com/docs/api){target="_blank"}.

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

   ![](assets/sms-create-surface.png)

   >[!NOTE]
   >
   > Os nomes devem começar com uma letra (A-Z). Ele só pode conter caracteres alfanuméricos. Também é possível usar sublinhado `_`, ponto`.` e hífen `-` caracteres.

1. Defina o **Configurações de SMS**.

   ![](assets/sms-surface-settings.png)

   Comece selecionando o **[!UICONTROL Tipo de SMS]** que serão enviados com a superfície: **[!UICONTROL Transacional]** ou **[!UICONTROL Marketing]**.

   * Escolher **Marketing** para SMS promocional: essas mensagens exigem o consentimento do usuário.
   * Escolher **Transacional** para mensagens não comerciais, como confirmação de pedidos, notificações de redefinição de senha ou informações de entrega, por exemplo.

   Ao criar uma mensagem SMS, você deve escolher uma superfície de canal válida que corresponda à categoria selecionada para a mensagem.

   >[!CAUTION]
   >
   >**Transacional** Mensagens SMS podem ser enviadas a perfis que cancelaram a assinatura de comunicações de marketing. Essas mensagens só podem ser enviadas em contextos específicos.

1. Selecione o **[!UICONTROL Configuração de SMS]** para associar à superfície.

   Para obter mais informações sobre como configurar o seu ambiente para enviar mensagens SMS, consulte [nesta seção](#create-api).

1. Insira o **[!UICONTROL Número do remetente]** &#x200B;que você deseja usar para suas comunicações.

1. Selecione o **[!UICONTROL Campo de execução do SMS]** para selecionar o **[!UICONTROL Atributo de perfil]** associados aos números de telefone dos perfis.

1. Se quiser usar a função de redução de URL em suas mensagens SMS, selecione um item na lista suspensa **[!UICONTROL Subdomínio]** lista.

   >[!NOTE]
   >
   >Para selecionar um subdomínio, verifique se você configurou anteriormente pelo menos um subdomínio SMS. [Saiba como](sms-subdomains.md)

1. Insira o **[!UICONTROL Número de recusa]** que você deseja usar para esta superfície. Quando os perfis optam por não participar desse número, você ainda pode enviar mensagens de outros números com os quais possa estar usando para enviar mensagens SMS [!DNL Journey Optimizer].

   >[!NOTE]
   >
   >Entrada [!DNL Journey Optimizer], o cancelamento de SMS não é mais gerenciado no nível do canal. Agora é específico de um número.

1. Após configurar todos os parâmetros, clique em **[!UICONTROL Enviar]** para confirmar. Você também pode salvar a superfície de canal como rascunho e retomar sua configuração posteriormente.

   ![](assets/sms-submit-surface.png)

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

