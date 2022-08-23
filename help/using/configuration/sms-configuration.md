---
title: Configuração de SMS
description: Saiba como configurar seu ambiente para enviar mensagens SMS com o Journey Optimizer
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: f44638ac7cfb078b6914635433feedb0f48ef099
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 7%

---

# Configurar canal de SMS {#sms-configuration}

[!DNL Journey Optimizer] O permite criar suas jornadas e enviar mensagens para o público-alvo.

Antes de enviar SMS, configure sua instância. Você precisa [integrar as configurações do provedor](#create-api) com a Journey Optimizer e [criar uma superfície de SMS](#message-preset-sms) (ou seja, predefinição de SMS). Essas etapas devem ser executadas por um [Administrador de sistema da Adobe Journey Optimizer](../start/path/administrator.md).

>[!AVAILABILITY]
>
>No momento, o canal SMS está disponível apenas para algumas organizações (disponibilidade limitada). Para obter mais informações, entre em contato com o seu representante da Adobe.

## Criar nova credencial da API {#create-api}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="Configurar seu fornecedor de SMS"
>abstract="Selecione o fornecedor e preencha as credenciais da API de SMS."

Para configurar seu fornecedor de SMS com o Journey Optimizer, siga estas etapas:

1. Acesse o **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL API Credentials]** , em seguida, clique em **[!UICONTROL Create API credential]**.

   ![](assets/sms_4.png)

1. Selecione seu **[!UICONTROL SMS vendor]**:

   * [!DNL Sinch]. Para encontrar seu **[!UICONTROL Service ID]** e **[!UICONTROL API Token]**, acesse o menu SMS > APIs em sua conta do Sinch .
   * [!DNL Twilio]. Para encontrar seu **[!UICONTROL Service ID]** e **[!UICONTROL API Token]**, acesse o painel Informações da conta da página Painel do console .

1. Insira um **[!UICONTROL Name]** para sua Credencial da API.

1. Insira seu **[!UICONTROL Service ID]** e **[!UICONTROL API Token]**.

   ![](assets/sms_5.png)

1. Clique em **[!UICONTROL Submit]** ao concluir a configuração das credenciais da API.

Depois de criar e configurar sua credencial de API, agora é necessário criar uma superfície de canal (ou seja, predefinição de mensagem) para mensagens SMS.

## Criar uma superfície de canal para mensagens SMS {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="Definir a categoria SMS"
>abstract="Selecione o tipo de mensagens SMS que serão enviadas ao usar esta superfície: Marketing para mensagens SMS promocionais, que exigem consentimento do usuário, ou Transacional para mensagens SMS não comerciais, que também podem ser enviadas para perfis sem assinatura em contextos específicos."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/messages/create-sms.html#sms-opt-in-out" text="Recusar em mensagens SMS de marketing"

Após configurar o canal SMS, é necessário criar uma superfície de canal para enviar mensagens SMS de **[!DNL Journey Optimizer]**.

Para criar uma superfície de canal, siga estas etapas:

1. Acesse o **[!UICONTROL Channels]** > **[!UICONTROL Branding]** > **[!UICONTROL Channel surfaces]** , em seguida, clique em **[!UICONTROL Create channel surface]**.

   ![](assets/preset-create.png)

1. Insira um nome e uma descrição (opcional) para a superfície e selecione o canal SMS.

   ![](assets/sms_preset.png)

   >[!NOTE]
   >
   > Os nomes devem começar com uma letra (A-Z). Ela só pode conter caracteres alfanuméricos. Você também pode usar o sublinhado `_`, ponto`.` e hífen `-` caracteres.

1. Configure o **SMS** configurações.

   ![](assets/preset-sms.png)

   * Selecione o **[!UICONTROL SMS Type]** que será enviado com a superfície: **[!UICONTROL Transactional]** ou **[!UICONTROL Marketing]**.

   * Selecione o **[!UICONTROL SMS configuration]** para associar com a superfície.

      Para obter mais informações sobre como configurar seu ambiente para enviar mensagens SMS, consulte [esta seção](#create-api).

   * Insira o **[!UICONTROL Sender number]** &#x200B; você deseja usar para suas comunicações.

   * Selecione seu **[!UICONTROL SMS Execution Field]** para selecionar o **[!UICONTROL Profile attribute]** associado aos números de telefone dos perfis.

1. Depois que todos os parâmetros tiverem sido configurados, clique em **[!UICONTROL Submit]** para confirmar. Você também pode salvar a superfície do canal como rascunho e retomar sua configuração posteriormente.

   ![](assets/sms_preset_2.png)

1. Depois que a superfície do canal for criada, ela será exibida na lista com a variável **[!UICONTROL Processing]** status.

   >[!NOTE]
   >
   >Se as verificações não forem bem-sucedidas, saiba mais sobre os possíveis motivos de falha em [esta seção](#monitor-channel-surfaces).

1. Depois que as verificações são bem-sucedidas, a superfície do canal recebe a variável **[!UICONTROL Active]** status. Ele está pronto para ser usado para entregar mensagens.

   ![](assets/preset-active.png)

Agora você está pronto para enviar mensagens SMS com o Journey Optimizer.

**Tópicos relacionados**

* [Criar uma mensagem de SMS.](../messages/create-sms.md)
* [Adicionar uma mensagem em uma jornada](../building-journeys/journeys-message.md)
