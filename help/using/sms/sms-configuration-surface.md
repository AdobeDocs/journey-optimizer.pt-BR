---
solution: Journey Optimizer
product: journey optimizer
title: Configurar a superfície de SMS
description: Saiba como configurar sua superfície SMS/MMS para enviar mensagens de texto com o Journey Optimizer
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 0d541520-016e-468f-b011-808712847556
source-git-commit: 080928d14a9d6ec116286386748b77a6a25e76f8
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 10%

---

# Criar uma superfície de SMS/MMS {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="Definição da categoria da mensagem"
>abstract="Selecione o tipo de mensagens de texto usando esta superfície: Marketing para mensagens promocionais, que exigem consentimento do usuário, ou Transacional para mensagens não comerciais, como redefinição de senha."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=pt-BR#sms-opt-out-management" text="Recusar mensagens de texto de marketing"

Depois que o canal SMS/MMS for configurado, você deverá criar uma superfície de canal para enviar mensagens SMS e MMS do **[!DNL Journey Optimizer]**.

Para criar uma superfície de canal, siga estas etapas:

1. No painel à esquerda, vá para **[!UICONTROL Administração]** > **[!UICONTROL Canais]** e selecione **[!UICONTROL Identidade Visual]** > **[!UICONTROL Superfícies de canal]**. Clique no botão **[!UICONTROL Criar superfície de canal]**.

   ![](assets/preset-create.png)

1. Insira um nome e uma descrição (opcional) para a superfície e selecione o canal SMS.

   ![](assets/sms-create-surface.png)

   >[!NOTE]
   >
   > Os nomes devem começar com uma letra (A-Z). Ele só pode conter caracteres alfanuméricos. Também é possível usar sublinhado `_`, ponto`.` e hífen `-` caracteres.

1. Defina as **configurações de SMS**.

   ![](assets/sms-surface-settings.png)

   Comece selecionando o **[!UICONTROL Tipo de SMS]** que será enviado com a superfície: **[!UICONTROL Transacional]** ou **[!UICONTROL Marketing]**.

   * Escolha **Marketing** para mensagens de texto promocionais: essas mensagens exigem o consentimento do usuário.
   * Escolha **Transacional** para mensagens não comerciais, como confirmações de pedidos, notificações de redefinição de senha ou informações de entrega, por exemplo.

   Ao criar um SMS/MMS, você deve escolher uma superfície de canal válida que corresponda à categoria selecionada para sua mensagem.

   >[!CAUTION]
   >
   >As mensagens **Transacionais** podem ser enviadas a perfis que cancelaram a assinatura de comunicações de marketing. Essas mensagens só podem ser enviadas em contextos específicos.

1. Selecione a **[!UICONTROL configuração de SMS]** para associar à superfície.

   Para obter mais informações sobre como configurar seu ambiente para enviar mensagens SMS, consulte [esta seção](#create-api).

1. Digite o **[!UICONTROL Número do remetente]** &#x200B;que você deseja usar para suas comunicações.

1. Selecione o **[!UICONTROL Campo de Execução do SMS]** para selecionar o **[!UICONTROL atributo de perfil]** associado aos números de telefone dos perfis.

1. Se você quiser usar a função de redução de URL em suas mensagens SMS, selecione um item na lista **[!UICONTROL Subdomínio]**.

   >[!NOTE]
   >
   >Para selecionar um subdomínio, verifique se você configurou anteriormente pelo menos um subdomínio SMS/MMS. [Saiba como](sms-subdomains.md)

1. Depois que todos os parâmetros tiverem sido configurados, clique em **[!UICONTROL Enviar]** para confirmar. Você também pode salvar a superfície de canal como rascunho e retomar sua configuração posteriormente.

   ![](assets/sms-submit-surface.png)

1. Após criar a superfície de canal, ela é exibida na lista com o status **[!UICONTROL Processando]**.

   >[!NOTE]
   >
   >Se as verificações não forem bem-sucedidas, saiba mais sobre os possíveis motivos de falha em [esta seção](#monitor-channel-surfaces).

1. Depois que as verificações forem bem-sucedidas, a superfície de canal obterá o status **[!UICONTROL Ativo]**. Ele está pronto para ser usado para enviar mensagens.

   ![](assets/preset-active.png)

Agora você está pronto para enviar mensagens de texto com o Journey Optimizer.
