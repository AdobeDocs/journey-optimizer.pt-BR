---
solution: Journey Optimizer
product: journey optimizer
title: Configurar provedor Sinch
description: Saiba como configurar seu ambiente para enviar mensagens de texto com o Journey Optimizer com Sinch
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 85412a85-edf0-4069-8bc7-b80371375f1f
source-git-commit: 7dfedb1b66101204b4923ddeb7793c80887ebdc0
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 3%

---

# Configurar provedor Sinch {#sms-configuration-sinch}

Ao usar o provedor Sinch com o Journey Optimizer, você pode encontrar duas opções distintas:

* **Configuração de SMS**: configure suas credenciais da API Sinch para enviar mensagens SMS facilmente.

* **Configuração do MMS**: para mensagens multimídia (MMS), configure suas credenciais da API do Sinch MMS. Observe que o rastreamento e a resposta às mensagens de entrada são manipulados pela configuração do SMS. A configuração do MMS é somente para entrega de saída da mensagem MMS.

## Credenciais da API Sinch{#create-api}

Para configurar seu provedor Sinch para enviar mensagens SMS e MMS com o Journey Optimizer, siga estas etapas:

1. No painel à esquerda, vá para **[!UICONTROL Administração]** > **[!UICONTROL Canais]** e selecione o menu **[!UICONTROL Credenciais de API]**. Clique no botão **[!UICONTROL Criar novas credenciais de API]**.

1. Configure suas credenciais da API de SMS, conforme detalhado abaixo:

   * **[!UICONTROL Fornecedor de SMS]**: Sinch.

   * **[!UICONTROL Nome]**: escolha um nome para a credencial de API.

   * **[!UICONTROL ID de Serviço]** e **[!UICONTROL Token de API]**: para acessar a página APIs, encontre suas credenciais na guia SMS. Saiba mais em [Documentação da Sinch](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"}.

   * **[!UICONTROL Palavras-chave de aceitação]**: digite as palavras-chave padrão ou personalizadas que dispararão automaticamente sua **[!UICONTROL Mensagem de aceitação]**. Para várias palavras-chave, use valores separados por vírgulas.

   * **[!UICONTROL Mensagem de aceitação]**: digite a resposta personalizada que é enviada automaticamente como sua **[!UICONTROL Mensagem de aceitação]**.

   * **[!UICONTROL Palavras-chave de recusa]**: digite as palavras-chave padrão ou personalizadas que dispararão automaticamente sua **[!UICONTROL Mensagem de recusa]**. Para várias palavras-chave, use valores separados por vírgulas.

   * **[!UICONTROL Mensagem de recusa]**: digite a resposta personalizada que é enviada automaticamente como sua **[!UICONTROL Mensagem de recusa]**.

   * **[!UICONTROL Palavras-chave da Ajuda]**: digite as palavras-chave padrão ou personalizadas que dispararão automaticamente sua **Mensagem da Ajuda**. Para várias palavras-chave, use valores separados por vírgulas.

   * **[!UICONTROL Mensagem de Ajuda]**: digite a resposta personalizada que é enviada automaticamente como sua **Mensagem de Ajuda**.

   * **[!UICONTROL Palavras-chave de Aceitação Dupla]**: digite as palavras-chave que disparam o processo de aceitação dupla. Se um perfil de usuário não existir, ele será criado após a confirmação bem-sucedida. Para várias palavras-chave, use valores separados por vírgulas. [Saiba mais sobre a Aceitação dupla de SMS](https://video.tv.adobe.com/v/3427129/?learn=on).

   * **[!UICONTROL Mensagem de aceitação dupla]**: digite a resposta personalizada que é enviada automaticamente em resposta à confirmação de aceitação dupla.

   * **[!UICONTROL Número de Entrada]**: adicione seu número de entrada exclusivo ou código curto. Isso permite usar as mesmas credenciais de API em diferentes sandboxes, cada uma com seu próprio número de entrada ou código curto.

1. Clique em **[!UICONTROL Enviar]** quando terminar de configurar suas credenciais de API.

Depois de criar e configurar sua credencial de API, agora é necessário criar uma superfície de canal para mensagens SMS. [Saiba mais](sms-configuration-surface.md)

## Credenciais da API do MMS Sinch {#sinch-mms}

>[!IMPORTANT]
>
> Juntamente com a configuração do MMS, também é necessário criar credenciais da API Sinch especificamente para rastrear mensagens de entrada e gerenciar solicitações de consentimento.

Para configurar o Sinch MMS para enviar o MMS com o Journey Optimizer, siga estas etapas:

1. No painel à esquerda, vá para **[!UICONTROL Administração]** > **[!UICONTROL Canais]** e selecione o menu **[!UICONTROL Credenciais de API]**. Clique no botão **[!UICONTROL Criar novas credenciais de API]**.

1. Configure suas credenciais da API do MMS, conforme detalhado abaixo:

   * **[!UICONTROL Fornecedor de SMS]**: Sinch MMS.

   * **[!UICONTROL Nome]**: escolha um nome para a credencial de API.

   * **[!UICONTROL ID do Projeto]**, **[!UICONTROL ID do Aplicativo]** e **[!UICONTROL Token da API]**: siga as etapas abaixo para coletar suas credenciais de API do MMS.

      * Para **[!UICONTROL ID do Projeto]** e **[!UICONTROL ID do Aplicativo]**: Acesse a página [Visão Geral da API de Conversa](https://dashboard.sinch.com/convapi/overview) do seu projeto Sinch no Painel Sinch.
      * Para **[!UICONTROL Token de API]**: obtenha as [Chaves de acesso](https://community.sinch.com/t5/Customer-Dashboard/Sinch-Access-Keys/ta-p/12638) para o seu Projeto Sinch e gere um **Token de API Base64** do seu Projeto Sinch **Chaves de acesso**.

   * **[!UICONTROL ID do Plano de Serviço]** e **[!UICONTROL Token de API de SMS]**: suas **[!UICONTROL ID do Plano de Serviço]** e **[!UICONTROL Token de API de SMS]** estão localizadas na guia SMS da página APIs.

1. Clique em **[!UICONTROL Enviar]** quando terminar de configurar suas credenciais de API.

Depois de criar e configurar sua credencial de API, agora é necessário criar uma superfície de canal para mensagens MMS. [Saiba mais](sms-configuration-surface.md)
