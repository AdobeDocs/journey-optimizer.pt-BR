---
title: Configuração de SMS
description: Saiba como configurar seu ambiente para enviar mensagens SMS com o Journey Optimizer
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: a60afd8a2948da5386b75421ffdb36735ed091e6
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 4%

---

# Configurar canal de SMS {#sms-configuration}

[!DNL Journey Optimizer] O permite criar suas jornadas e enviar mensagens para o público-alvo.

>[!NOTE]
>
>No momento, o canal SMS está disponível apenas para um conjunto de organizações (Disponibilidade limitada). Para obter mais informações, entre em contato com o representante do Adobe.

## Criar nova credencial da API {#create-api}

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

Depois de criar e configurar sua credencial de API, agora é necessário criar uma predefinição de mensagem para mensagens SMS.

## Criar uma predefinição de mensagem para mensagens SMS {#message-preset-sms}

Após configurar o canal SMS, é necessário criar uma predefinição de mensagem para enviar mensagens SMS de **[!DNL Journey Optimizer]**.

Para criar uma predefinição de mensagem, siga estas etapas:

1. Acesse o **[!UICONTROL Channels]** > **[!UICONTROL Branding]** > **[!UICONTROL Message presets]** , em seguida, clique em **[!UICONTROL Create Message preset]**.

   ![](assets/preset-create.png)

1. Insira um nome e uma descrição (opcional) para a predefinição, depois selecione o canal SMS.

   ![](assets/sms_preset.png)

   >[!NOTE]
   >
   > Os nomes devem começar com uma letra (A-Z). Ela só pode conter caracteres alfanuméricos. Você também pode usar o sublinhado `_`, ponto`.` e hífen `-` caracteres.

1. Configure o **SMS** configurações.

   ![](assets/preset-sms.png)

   * Selecione o **[!UICONTROL SMS Type]** que será enviado com a predefinição: **[!UICONTROL Transactional]** ou **[!UICONTROL Marketing]**.

   * Selecione o **[!UICONTROL SMS configuration]** para associar com a predefinição.

      Para obter mais informações sobre como configurar seu ambiente para enviar mensagens SMS, consulte [esta seção](sms-configuration.md).

   * Insira o **[!UICONTROL Sender number]** &#x200B; você deseja usar para suas comunicações.

   * Selecione seu **[!UICONTROL SMS Execution Field]** para selecionar o **[!UICONTROL Profile attribute]** associado aos números de telefone dos perfis.

1. Depois que todos os parâmetros tiverem sido configurados, clique em **[!UICONTROL Submit]** para confirmar. Você também pode salvar a predefinição de mensagem como rascunho e retomar sua configuração posteriormente.

   ![](assets/sms_preset_2.png)

1. Depois que a predefinição de mensagem tiver sido criada, ela será exibida na lista com a variável **[!UICONTROL Processing]** status.

   >[!NOTE]
   >
   >Se as verificações não forem bem-sucedidas, saiba mais sobre os possíveis motivos de falha em [esta seção](#monitor-message-presets).

1. Depois que as verificações são bem-sucedidas, a predefinição de mensagem recebe a variável **[!UICONTROL Active]** status. Ele está pronto para ser usado para entregar mensagens.

   ![](assets/preset-active.png)

Agora você está pronto para enviar mensagens SMS com o Journey Optimizer.

**Tópicos relacionados**

* [Criar uma mensagem de SMS.](../messages/create-sms.md)
* [Adicionar uma mensagem em uma jornada](../building-journeys/journeys-message.md)
