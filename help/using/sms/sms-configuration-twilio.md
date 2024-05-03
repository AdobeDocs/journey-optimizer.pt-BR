---
solution: Journey Optimizer
product: journey optimizer
title: Configurar o provedor do Twilio
description: Saiba como configurar seu ambiente para enviar mensagens de texto com o Journey Optimizer com Twilio
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 1%

---

# Configurar o provedor do Twilio {#sms-configuration-twilio}

Para configurar o Twilio com o Journey Optimizer, é necessário criar uma nova credencial de API usada para o Twilio:

1. No painel esquerdo, navegue até **[!UICONTROL Administração]** > **[!UICONTROL Canais]** e selecione o **[!UICONTROL Credenciais da API]** menu. Clique em **[!UICONTROL Criar novas credenciais de API]** botão.

   ![](assets/sms_6.png)

1. Configure suas credenciais da API de SMS, conforme detalhado abaixo:

   * **[!UICONTROL Nome]**: escolha um nome para a credencial da API.

   * **[!UICONTROL SID da conta]** e **[!UICONTROL Token de autenticação]**: acesse o **Informações da conta** painel da página Painel do Twilio Console para encontrar suas credenciais.

   * **[!UICONTROL SID da Mensagem]**: digite o identificador exclusivo atribuído a cada mensagem criada pela API do Twilio. Saiba mais em [Documentação do Twilio](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}.

1. Clique em **[!UICONTROL Enviar]** quando você concluiu a configuração das credenciais da API.

Depois de criar e configurar sua credencial de API, agora é necessário criar uma superfície de canal para mensagens SMS e MMS. [Saiba mais](sms-configuration-surface.md)

