---
solution: Journey Optimizer
product: journey optimizer
title: Configurar provedor Sinch
description: Saiba como configurar seu ambiente para enviar mensagens de texto com o Journey Optimizer com Sinch
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 85412a85-edf0-4069-8bc7-b80371375f1f
source-git-commit: 8f045e1b709c0059ce21cda68c21e8732f58e51e
workflow-type: tm+mt
source-wordcount: '557'
ht-degree: 4%

---

# Configurar provedor Sinch {#sms-configuration-sinch}

Ao usar o provedor Sinch com o Journey Optimizer, você pode encontrar duas opções distintas:

* **Configuração de SMS**: configure suas credenciais da API do Sinch para enviar mensagens SMS sem problemas.

* **Configuração do MMS**: Para mensagens multimídia (MMS), configure as credenciais da API do Sinch MMS. Observe que o rastreamento e a resposta às mensagens de entrada são manipulados pela configuração do SMS. A configuração do MMS é somente para entrega de saída da mensagem MMS.

## Credenciais da API Sinch{#create-api}

Para configurar seu provedor Sinch para enviar mensagens SMS e MMS com o Journey Optimizer, siga estas etapas:

1. No painel esquerdo, navegue até **[!UICONTROL Administração]** > **[!UICONTROL Canais]** e selecione o **[!UICONTROL Credenciais da API]** menu. Clique em **[!UICONTROL Criar novas credenciais de API]** botão.

1. Configure suas credenciais da API de SMS, conforme detalhado abaixo:

   * **[!UICONTROL Fornecedor de SMS]**: Sinch.

   * **[!UICONTROL Nome]**: escolha um nome para a credencial da API.

   * **[!UICONTROL ID do serviço]** e **[!UICONTROL Token de API]**: para acessar a página APIs, você pode encontrar suas credenciais na guia SMS. Saiba mais em [Documentação da Sinch](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"}.

   * **[!UICONTROL Palavras-chave de Opt-in]**: digite as palavras-chave padrão ou personalizadas que acionarão automaticamente o **[!UICONTROL Mensagem de Opt-in]**. Para várias palavras-chave, use valores separados por vírgulas.

   * **[!UICONTROL Mensagem de Opt-in]**: digite a resposta personalizada que é enviada automaticamente como **[!UICONTROL Mensagem de Opt-in]**.

   * **[!UICONTROL Palavras-chave de recusa]**: digite as palavras-chave padrão ou personalizadas que acionarão automaticamente o **[!UICONTROL Mensagem de recusa]**. Para várias palavras-chave, use valores separados por vírgulas.

   * **[!UICONTROL Mensagem de recusa]**: digite a resposta personalizada que é enviada automaticamente como **[!UICONTROL Mensagem de recusa]**.

   * **[!UICONTROL Palavras-chave da Ajuda]**: digite as palavras-chave padrão ou personalizadas que acionarão automaticamente o **Mensagem de ajuda**. Para várias palavras-chave, use valores separados por vírgulas.

   * **[!UICONTROL Mensagem de ajuda]**: digite a resposta personalizada que é enviada automaticamente como **Mensagem de ajuda**.

   * **[!UICONTROL Palavras-chave de aceitação dupla]**: digite as palavras-chave que acionam o processo de aceitação dupla. Se um perfil de usuário não existir, ele será criado após a confirmação bem-sucedida. Para várias palavras-chave, use valores separados por vírgulas. [Saiba mais sobre o Double Opt-in de SMS](https://video.tv.adobe.com/v/3427129/?learn=on).

   * **[!UICONTROL Mensagem de aceitação dupla]**: digite a resposta personalizada que é enviada automaticamente em resposta à confirmação de aceitação dupla.

1. Clique em **[!UICONTROL Enviar]** quando você concluiu a configuração das credenciais da API.

Depois de criar e configurar sua credencial de API, agora é necessário criar uma superfície de canal para mensagens SMS. [Saiba mais](sms-configuration-surface.md)

## Credenciais da API do MMS Sinch {#sinch-mms}

>[!IMPORTANT]
>
> Juntamente com a configuração do MMS, também é necessário criar credenciais da API Sinch especificamente para rastrear mensagens de entrada e gerenciar solicitações de consentimento.

Para configurar o Sinch MMS para enviar o MMS com o Journey Optimizer, siga estas etapas:

1. No painel esquerdo, navegue até **[!UICONTROL Administração]** > **[!UICONTROL Canais]** e selecione o **[!UICONTROL Credenciais da API]** menu. Clique em **[!UICONTROL Criar novas credenciais de API]** botão.

1. Configure suas credenciais da API do MMS, conforme detalhado abaixo:

   * **[!UICONTROL Fornecedor de SMS]**: Sinch MMS.

   * **[!UICONTROL Nome]**: escolha um nome para a credencial da API.

   * **[!UICONTROL ID do projeto]**, **[!UICONTROL ID do aplicativo]** e **[!UICONTROL Token de API]**: siga as etapas abaixo para coletar suas credenciais da API do MMS.

      * Para **[!UICONTROL ID do projeto]** e **[!UICONTROL ID do aplicativo]**: Acesse o **Visão geral da API de conversa** página do seu projeto Sinch no seu Painel Sinch.
      * Para **[!UICONTROL Token de API]**: Obtenha o **Chaves de acesso** para seu projeto Sinch e gerar um **Token de API Base64** do seu projeto Sinch **Chaves de acesso**.

   * **[!UICONTROL ID do Plano de Serviço]** e **[!UICONTROL Token da API de SMS]**: seu **[!UICONTROL ID do Plano de Serviço]** e **[!UICONTROL Token da API de SMS]** estão localizados na guia SMS da página APIs.

1. Clique em **[!UICONTROL Enviar]** quando você concluiu a configuração das credenciais da API.

Depois de criar e configurar sua credencial de API, agora é necessário criar uma superfície de canal para mensagens MMS. [Saiba mais](sms-configuration-surface.md)
