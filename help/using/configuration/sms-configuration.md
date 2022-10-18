---
solution: Journey Optimizer
product: journey optimizer
title: Configuração de SMS
description: Saiba como configurar seu ambiente para enviar SMS com o Journey Optimizer
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 2%

---

# Configurar canal de SMS {#sms-configuration}

[!DNL Journey Optimizer] O permite criar suas jornadas e enviar mensagens para o público-alvo.

Antes de enviar SMS, configure sua instância. Você precisa [integrar as configurações do provedor](#create-api) com a Journey Optimizer e [criar uma superfície de SMS](#message-preset-sms) (ou seja, predefinição de SMS). Essas etapas devem ser executadas por um [Administrador de sistema da Adobe Journey Optimizer](../start/path/administrator.md).

>[!IMPORTANT]
>
>Atualmente, a Adobe Journey Optimizer integra-se com provedores de terceiros, como Sinch e Twilio, que oferecem serviços SMS independentes da Adobe Journey Optimizer.  Antes da configuração do SMS, você deve criar uma conta com um desses provedores de SMS para receber o Token de API e a ID de serviço que permitirá estabelecer a conexão entre o Adobe Journey Optimizer e o provedor de SMS aplicável. O uso de serviços de SMS estará sujeito aos termos e condições adicionais do provedor de SMS aplicável. Como o Sinch e o Twilio são produtos de terceiros disponíveis para os usuários do Adobe Journey Optimizer por meio de uma integração, para quaisquer problemas ou consultas relacionadas aos serviços SMS, os usuários do Sinch ou do Twilio precisarão entrar em contato com o provedor de SMS aplicável para obter assistência. O Adobe não controla e não é responsável por produtos de terceiros.

## Criar nova credencial da API {#create-api}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="Configure seu fornecedor de SMS com o Journey Optimizer"
>abstract="Selecione o fornecedor e preencha as credenciais da API de SMS."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="Configure seu fornecedor de SMS com o Journey Optimizer"
>abstract="Antes de enviar SMS, você deve integrar as configurações do provedor com o Journey Optimizer. Depois de concluído, você precisará criar uma superfície de SMS. Essas etapas devem ser executadas por um administrador de sistema do Adobe Journey Optimizer."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/configuration-message/sms-configuration.html#message-preset-sms" text="Criar uma superfície de canal SMS"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="Selecione a configuração do fornecedor de SMS"
>abstract="Selecione as credenciais da API configuradas para seu fornecedor de SMS."

Para configurar seu fornecedor de SMS com o Journey Optimizer, siga estas etapas:

1. Acesse o **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Credenciais da API]** , em seguida, clique em **[!UICONTROL Criar credencial da API]**.

   ![](assets/sms_4.png)

1. Selecione seu **[!UICONTROL Fornecedor de SMS]**:

   * [!DNL Sinch]. Para encontrar seu **[!UICONTROL ID do serviço]** e **[!UICONTROL Token de API]**, acesse o menu SMS > APIs em sua conta do Sinch .
   * [!DNL Twilio]. Para encontrar seu **[!UICONTROL ID do serviço]** e **[!UICONTROL Token de API]**, acesse o painel Informações da conta da página Painel do console .

1. Insira um **[!UICONTROL Nome]** para sua Credencial da API.

1. Insira seu **[!UICONTROL ID do serviço]** e **[!UICONTROL Token de API]**.

   ![](assets/sms_5.png)

1. Clique em **[!UICONTROL Enviar]** ao concluir a configuração das credenciais da API.

Depois de criar e configurar sua credencial de API, agora é necessário criar uma superfície de canal (ou seja, predefinição de mensagem) para mensagens SMS.

## Criar uma superfície de canal para mensagens SMS {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="Definir a categoria SMS"
>abstract="Selecione o tipo de mensagens SMS que serão enviadas ao usar esta superfície: Marketing para mensagens SMS promocionais, que exigem consentimento do usuário, ou Transacional para mensagens SMS não comerciais, que também podem ser enviadas para perfis sem assinatura em contextos específicos."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/messages/create-sms.html#sms-opt-in-out" text="Recusar em mensagens SMS de marketing"

Após configurar o canal SMS, é necessário criar uma superfície de canal para enviar mensagens SMS de **[!DNL Journey Optimizer]**.

Para criar uma superfície de canal, siga estas etapas:

1. Acesse o **[!UICONTROL Canais]** > **[!UICONTROL Marca]** > **[!UICONTROL Superfícies do canal]** , em seguida, clique em **[!UICONTROL Criar superfície de canal]**.

   ![](assets/preset-create.png)

1. Insira um nome e uma descrição (opcional) para a superfície e selecione o canal SMS.

   ![](assets/sms_preset.png)

   >[!NOTE]
   >
   > Os nomes devem começar com uma letra (A-Z). Ela só pode conter caracteres alfanuméricos. Você também pode usar o sublinhado `_`, ponto`.` e hífen `-` caracteres.

1. Configure o **SMS** configurações.

   ![](assets/preset-sms.png)

   * Selecione o **[!UICONTROL Tipo de SMS]** que será enviado com a superfície: **[!UICONTROL Transacional]** ou **[!UICONTROL Marketing]**.

   * Selecione o **[!UICONTROL Configuração de SMS]** para associar com a superfície.

      Para obter mais informações sobre como configurar seu ambiente para enviar mensagens SMS, consulte [esta seção](#create-api).

   * Insira o **[!UICONTROL Número do remetente]** &#x200B; você deseja usar para suas comunicações.

   * Selecione seu **[!UICONTROL Campo de execução do SMS]** para selecionar o **[!UICONTROL Atributo de perfil]** associado aos números de telefone dos perfis.

1. Depois que todos os parâmetros tiverem sido configurados, clique em **[!UICONTROL Enviar]** para confirmar. Você também pode salvar a superfície do canal como rascunho e retomar sua configuração posteriormente.

   ![](assets/sms_preset_2.png)

1. Depois que a superfície do canal for criada, ela será exibida na lista com a variável **[!UICONTROL Processamento]** status.

   >[!NOTE]
   >
   >Se as verificações não forem bem-sucedidas, saiba mais sobre os possíveis motivos de falha em [esta seção](#monitor-channel-surfaces).

1. Depois que as verificações são bem-sucedidas, a superfície do canal recebe a variável **[!UICONTROL Ativo]** status. Ele está pronto para ser usado para entregar mensagens.

   ![](assets/preset-active.png)

Agora você está pronto para enviar mensagens SMS com o Journey Optimizer.

**Tópicos relacionados**

* [Criar uma mensagem de SMS.](../messages/create-sms.md)
* [Adicionar uma mensagem em uma jornada](../building-journeys/journeys-message.md)
