---
solution: Journey Optimizer
product: journey optimizer
title: Configurar provedor Infobip
description: Saiba como configurar seu ambiente para enviar mensagens de texto e MMS com o Journey Optimizer com Infobip
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
source-git-commit: 8f045e1b709c0059ce21cda68c21e8732f58e51e
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 5%

---

# Configurar provedor Infobip {#sms-configuration-infobip}

Para configurar o Infobip com o Journey Optimizer, siga estas etapas:

1. No painel esquerdo, navegue até **[!UICONTROL Administração]** `>` **[!UICONTROL Canais]** e selecione o **[!UICONTROL Credenciais da API]** menu. Clique em **[!UICONTROL Criar novas credenciais de API]** botão.

1. Configure suas credenciais de API, conforme detalhado abaixo.

   * **[!UICONTROL Fornecedor de SMS]**: Infobip.

   * **[!UICONTROL Nome]**: escolha um nome para a credencial da API.

   * **[!UICONTROL URL de base da API]** e **[!UICONTROL Chave de API]**: acesse a página inicial da interface da Web ou a página de gerenciamento de chaves da API para encontrar suas credenciais. Saiba mais em [Documentação do Infobip](https://www.infobip.com/docs/api){target="_blank"}.

   * **[!UICONTROL Palavras-chave de Opt-in]**: digite as palavras-chave padrão ou personalizadas que acionarão automaticamente o **[!UICONTROL Mensagem de Opt-in]**. Para várias palavras-chave, use valores separados por vírgulas.

   * **[!UICONTROL Mensagem de Opt-in]**: digite a resposta personalizada que é enviada automaticamente como **[!UICONTROL Mensagem de Opt-in]**.

   * **[!UICONTROL Palavras-chave de recusa]**: digite as palavras-chave ou padrão que acionarão automaticamente o **[!UICONTROL Mensagem de recusa]**. Para várias palavras-chave, use valores separados por vírgulas.

   * **[!UICONTROL Mensagem de recusa]**: digite a resposta personalizada que é enviada automaticamente como **[!UICONTROL Mensagem de recusa]**.

   * **[!UICONTROL Palavras-chave da Ajuda]**: digite as palavras-chave padrão ou personalizadas que acionarão automaticamente o **Mensagem de ajuda**. Para várias palavras-chave, use valores separados por vírgulas.

   * **[!UICONTROL Mensagem de ajuda]**: digite a resposta personalizada que é enviada automaticamente como **Mensagem de ajuda**.

   * **[!UICONTROL Palavras-chave de aceitação dupla]**: digite as palavras-chave que acionam o processo de aceitação dupla. Se um perfil de usuário não existir, ele será criado após a confirmação bem-sucedida. Para várias palavras-chave, use valores separados por vírgulas.

   * **[!UICONTROL Mensagem de aceitação dupla]**: digite a resposta personalizada que é enviada automaticamente em resposta à confirmação da Aceitação dupla.

   * **[!UICONTROL ID da entidade principal]**: digite a ID de entidade principal DLT atribuída.

   * **[!UICONTROL ID do modelo de conteúdo]**: digite a ID do modelo de conteúdo DLT registrado.

   * **[!UICONTROL Período de validade]**: digite o período de validade da mensagem em horas. Caso as mensagens não possam ser entregues dentro desse período, o sistema fará tentativas adicionais para reenviá-las. O período de validade padrão é definido como 48 horas.

   * **[!UICONTROL Dados de Retorno]**: digite os dados adicionais do cliente que serão enviados no URL de notificação.

1. Clique em **[!UICONTROL Enviar]** quando você concluiu a configuração das credenciais da API.

Depois de criar e configurar sua credencial de API, agora é necessário criar uma superfície de canal para mensagens SMS e MMS. [Saiba mais](sms-configuration-surface.md)
