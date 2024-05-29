---
solution: Journey Optimizer
product: journey optimizer
title: Configurar provedor Twilio
description: Saiba como configurar seu ambiente para enviar mensagens de texto com o Journey Optimizer com Twilio
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: d6f74566-c913-4727-83b9-473a798a0158
source-git-commit: 8f045e1b709c0059ce21cda68c21e8732f58e51e
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 5%

---

# Configurar provedor Twilio {#sms-configuration-twilio}

Para configurar o Twilio com o Journey Optimizer, é necessário criar uma nova credencial de API usada para o Twilio:

1. No painel esquerdo, navegue até **[!UICONTROL Administração]** > **[!UICONTROL Canais]** e selecione o **[!UICONTROL Credenciais da API]** menu. Clique em **[!UICONTROL Criar novas credenciais de API]** botão.

1. Configure suas credenciais da API de SMS, conforme detalhado abaixo:

   * **[!UICONTROL Fornecedor de SMS]**: Twilio.

   * **[!UICONTROL Nome]**: escolha um nome para a credencial da API.

   * **[!UICONTROL SID da conta]** e **[!UICONTROL Token de autenticação]**: acesse o **Informações da conta** painel da página Painel do Twilio Console para encontrar suas credenciais.

   * **[!UICONTROL SID da Mensagem]**: digite o identificador exclusivo atribuído a cada mensagem criada pela API do Twilio. Saiba mais em [Documentação do Twilio](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}.

1. Clique em **[!UICONTROL Enviar]** quando você concluiu a configuração das credenciais da API.

Depois de criar e configurar sua credencial de API, agora é necessário criar uma superfície de canal para mensagens SMS e MMS. [Saiba mais](sms-configuration-surface.md)
