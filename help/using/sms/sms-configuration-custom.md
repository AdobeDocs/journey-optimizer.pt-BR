---
solution: Journey Optimizer
product: journey optimizer
title: Configurar o provedor personalizado
description: Saiba como configurar seu ambiente para enviar mensagens de texto com o Journey Optimizer com um provedor personalizado
feature: SMS, Channel Configuration
badge: label="Beta" type="Informative"
role: Admin
level: Intermediate
exl-id: fd713864-96b9-4687-91bd-84e3533273ff
source-git-commit: 201d7d367540f7b36f27ca4a09b6f0ce12e3e22f
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 27%

---

# Configurar um provedor personalizado {#sms-configuration-custom}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_provider_url"
>title="URL do provedor"
>abstract="Especifique o URL da API externa à qual você planeja se conectar. Esse URL serve como ponto de acesso para acessar os recursos e funcionalidades da API."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_auth_type"
>title="Tipo de autenticação"
>abstract="Especifique o método de autenticação necessário para acessar a API, como os tokens OAuth ou Bearer. Isso garante a comunicação segura e autorizada com o serviço externo."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_header_parameters"
>title="Parâmetros de cabeçalho"
>abstract="Especifique o rótulo, o tipo e o valor dos cabeçalhos adicionais para habilitar a autenticação adequada, a formatação de conteúdo e a comunicação eficaz da API. "

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_provider_payload"
>title="Conteúdo do provedor"
>abstract="Forneça o conteúdo da solicitação para garantir que os dados corretos sejam enviados para processamento e geração de resposta."

>[!AVAILABILITY]
>
>Os provedores personalizados estão disponíveis atualmente como uma versão beta somente para usuários selecionados. Entre em contato com seu representante da Adobe para ser incluído na Beta.
>
>Observe que esse Beta não é compatível com mensagens de entrada para gerenciamento de consentimento de aceitação/recusa e relatórios de entrega.

Para enviar mensagens no Journey Optimizer usando um provedor personalizado não disponível imediatamente pela Adobe (por exemplo, Sinch, Infobip, Twilio), siga estas etapas:

1. No painel à esquerda, vá para **[!UICONTROL Administração]** > **[!UICONTROL Canais]** e selecione o menu **[!UICONTROL Credenciais de API]**.

1. Clique no botão **[!UICONTROL Criar novas credenciais de API]**.

   ![](assets/sms_byo_1.png)

1. Configure suas credenciais da API de SMS, conforme detalhado abaixo:

   * **[!UICONTROL Fornecedor de SMS]**: personalizado.

   * **[!UICONTROL Nome]**: digite um nome para a credencial da API.

   * **[!UICONTROL AppId do Provedor]**: digite a ID do aplicativo fornecida pelo seu provedor de SMS.

   * **[!UICONTROL Nome do Provedor]**: digite o nome do seu provedor de SMS.

   * **[!UICONTROL URL do Provedor]**: digite a URL do seu provedor de SMS.

   * **[!UICONTROL Tipo de Autenticação&#x200B;]**: selecione seu tipo de Autorização. Os tipos de Autorização com suporte são **Aplicativo de Portador** ou **Básico**.

   * **[!UICONTROL Token de API]**: insira o Token de API fornecido pelo seu provedor de SMS.

   * **[!UICONTROL Carga do provedor]**: adicione a carga do provedor, por exemplo, `{"from": "+1234XXXXXX", "to": "+1374XXXXXX", "content": "This is a test message", "contentType": "TEXT"}`.

     Verifique se a carga inclui `{{toNumber}}`, `{{fromNumber}}`, `{{message}}`.

1. Clique em **[!UICONTROL Enviar]** quando terminar de configurar suas credenciais de API.

1. No menu **[!UICONTROL Credenciais da API]**, clique no ícone de compartimento para excluir suas credenciais da API.

1. Para modificar as credenciais existentes, localize as credenciais de API desejadas e clique na opção **[!UICONTROL Editar]** para fazer as alterações necessárias.

Depois de criar e configurar sua credencial de API, agora é necessário criar uma superfície de canal para mensagens SMS. [Saiba mais](sms-configuration-surface.md)

Depois de configurado, você pode aproveitar todos os recursos de canal prontos para uso, como criação de mensagens, personalização, rastreamento de links e relatórios.

## Vídeo tutorial {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3431625)
