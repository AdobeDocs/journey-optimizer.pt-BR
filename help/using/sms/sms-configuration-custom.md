---
solution: Journey Optimizer
product: journey optimizer
title: Configurar o provedor personalizado
description: Saiba como configurar seu ambiente para enviar mensagens de texto com o Journey Optimizer com um provedor personalizado
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: fd713864-96b9-4687-91bd-84e3533273ff
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '1032'
ht-degree: 9%

---

# Configurar um provedor personalizado {#sms-configuration-custom}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_provider_url"
>title="URL do provedor"
>abstract="Especifique o URL da API externa à qual você planeja se conectar. Esse URL serve como ponto de acesso para acessar os recursos e funcionalidades da API."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_header_parameters"
>title="Parâmetros de cabeçalho"
>abstract="Especifique o rótulo, o tipo e o valor dos cabeçalhos adicionais para habilitar a autenticação adequada, a formatação de conteúdo e a comunicação eficaz da API. "

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_provider_payload"
>title="Conteúdo do provedor"
>abstract="Forneça o conteúdo da solicitação para garantir que os dados corretos sejam enviados para processamento e geração de resposta."

Esse recurso permite integrar e configurar seus próprios provedores de mensagens, oferecendo flexibilidade além das opções padrão (Sinch, Twilio e Infobip). Isso permite a criação, entrega, relatórios e gerenciamento de consentimento perfeitos para mensagens SMS e RCS.

Com a configuração personalizada do provedor, você pode conectar serviços de mensagens de terceiros diretamente no Journey Optimizer, personalizar cargas de mensagem para conteúdo dinâmico e gerenciar preferências de aceitação/recusa para garantir a conformidade entre os canais SMS e RCS.

Para configurar seu provedor personalizado, siga as etapas abaixo:

1. [Criar credencial de API](#api-credential)
1. [Criar Webhook](#webhook)
1. [Criar configuração de canal](sms-configuration-surface.md)
1. [Criar Jornada ou Campanha com ação de canal SMS](create-sms.md)

## Criar a credencial da API {#api-credential}

Para enviar mensagens SMS e RCS no Journey Optimizer usando um provedor personalizado não disponível imediatamente pela Adobe (por exemplo, Sinch, Infobip, Twilio), siga estas etapas:

1. No painel à esquerda, navegue até **[!UICONTROL Administração]** `>` **[!UICONTROL Canais]**, selecione o menu **[!UICONTROL Credenciais da API]** em **[!UICONTROL Configurações de SMS]** e clique no botão **[!UICONTROL Criar novas credenciais de API]**.

   ![](assets/sms_byo_1.png)

1. Configure suas credenciais da API de SMS, conforme detalhado abaixo:

   * **[!UICONTROL Fornecedor de SMS]**: personalizado.

   * **[!UICONTROL Nome]**: digite um nome para a credencial da API.

   * **[!UICONTROL AppId do Provedor]**: insira a ID do aplicativo fornecida pelo seu provedor de SMS.

   * **[!UICONTROL Nome do Provedor]**: insira o nome do seu provedor de SMS.

   * **[!UICONTROL URL do Provedor]**: Insira a URL do seu provedor de SMS.

   * **[!UICONTROL Tipo de Autenticação&#x200B;]**: selecione seu tipo de autorização e [preencha os campos correspondentes](#auth-options) com base no método de autenticação escolhido.

     ![](assets/sms-byop.png)

1. Na seção **[!UICONTROL Cabeçalhos]**, clique em **[!UICONTROL Adicionar novo parâmetro]** para especificar os cabeçalhos HTTP para a mensagem de solicitação que será enviada para o serviço externo.

   Os campos de cabeçalho **Content-Type** e **Charset** estão definidos por padrão e não podem ser excluídos.

   ![](assets/sms_byo_2.png)

1. Adicione a **[!UICONTROL Carga do provedor]** para validar e personalizar as cargas da solicitação.

   Para mensagens RCS, essa carga é usada posteriormente durante [design de conteúdo](create-sms.md#sms-content).

1. Clique em **[!UICONTROL Enviar]** quando terminar de configurar suas credenciais de API.

1. No menu **[!UICONTROL Credenciais da API]**, clique no ![ícone bin](assets/do-not-localize/Smock_Delete_18_N.svg) para excluir suas credenciais da API.

   ![](assets/sms_byo_3.png)

1. Para modificar as credenciais existentes, localize as credenciais de API desejadas e clique na opção **[!UICONTROL Editar]** para fazer as alterações necessárias.

   ![](assets/sms_byo_4.png)

Depois de criar e configurar sua credencial de API, agora é necessário definir [as configurações de entrada para o Webhook](#webhook) para mensagens SMS.

### Opções de autenticação para Provedores de SMS personalizados {#auth-options}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_auth_type"
>title="Tipo de autenticação"
>abstract="Especifique o método de autenticação necessário para acessar a API, garantindo uma comunicação segura e autorizada com o serviço externo."

>[!BEGINTABS]

>[!TAB Chave de API]

Depois que a credencial da API for criada, preencha os campos necessários para autenticação da chave de API:

* **[!UICONTROL Nome]**&#x200B;: digite um nome para a configuração da chave de API.
* **[!UICONTROL Token de API]**&#x200B;: insira o Token de API fornecido pelo seu provedor de SMS.

![](assets/sms-byop-api-key.png)

>[!TAB Autenticação do MAC]

Depois que a credencial da API for criada, preencha os campos necessários para autenticação da MAC:

* **[!UICONTROL Nome]**&#x200B;: digite um nome para a configuração de autenticação do MAC.
* **[!UICONTROL Token de API]**&#x200B;: insira o Token de API fornecido pelo seu provedor de SMS.
* **[!UICONTROL Chave secreta de API]**: insira a Chave secreta de API fornecida pelo seu provedor de SMS. Essa chave é usada para gerar o MAC (Message Authentication Code) para comunicação segura.
* **[!UICONTROL Formato de hash de autorização do Mac]**: escolha o formato de hash para a autenticação do MAC.

![](assets/sms-byop-mac.png)

>[!TAB Autenticação OAuth]

Depois que a credencial da API for criada, preencha os campos necessários para autenticação OAuth:

* **[!UICONTROL Nome]**&#x200B;: insira um nome para a configuração de autenticação do OAuth.

* **[!UICONTROL Token de API]**&#x200B;: insira o Token de API fornecido pelo seu provedor de SMS.

* **[!UICONTROL URL do OAuth]**&#x200B;: insira a URL para obter o token do OAuth.

* **[!UICONTROL Corpo de OAuth]**&#x200B;: forneça o corpo da solicitação de OAuth no formato JSON, incluindo parâmetros como `grant_type`, `client_id` e `client_secret`.

![](assets/sms-byop-oauth.png)

>[!TAB Autenticação JWT]

Depois que a credencial da API for criada, preencha os campos necessários para autenticação JWT:

* **[!UICONTROL Nome]**&#x200B;: insira um nome para a configuração de autenticação JWT.

* **[!UICONTROL Token de API]**&#x200B;: insira o Token de API fornecido pelo seu provedor de SMS.

* **[!UICONTROL Carga JWT]**&#x200B;: insira a carga JSON que contém as declarações necessárias para o JWT, como emissor, assunto, público-alvo e expiração.

![](assets/sms-byop-jwt.png)

>[!ENDTABS]

## Criar Webhook {#webhook}

>[!BEGINSHADEBOX]

Se as palavras-chave de aceitação ou recusa não forem fornecidas, as mensagens de consentimento padrão serão usadas para honrar a privacidade do usuário. A adição de palavras-chave personalizadas substitui automaticamente os padrões.

**Palavras-chave padrão:**

* **Aceitar**: ASSINAR, SIM, REINICIAR, INICIAR, CONTINUAR, RETOMAR, INICIAR
* **Recusar**: PARAR, SAIR, CANCELAR, ENCERRAR, CANCELAR INSCRIÇÃO, NÃO
* **Ajuda**: AJUDA

>[!ENDSHADEBOX]

Depois que as credenciais da API forem criadas com êxito, a próxima etapa é criar um webhook e definir as configurações de entrada. Essa configuração garante que seu sistema possa receber e processar corretamente mensagens ou dados recebidos.

1. No painel à esquerda, navegue até **[!UICONTROL Administração]** `>` **[!UICONTROL Canais]**, selecione o menu **[!UICONTROL Webhooks de SMS]** em **[!UICONTROL Configurações de SMS]** e clique no botão **[!UICONTROL Criar Webhook]**.

   ![](assets/sms_byo_5.png)

1. Defina as configurações do Webhook, conforme detalhado abaixo:

   * **[!UICONTROL Nome]**: digite um nome para o seu Webhook.

   * **[!UICONTROL Selecionar fornecedor de SMS]**: personalizado.

   * **[!UICONTROL Selecionar credenciais de API]**: escolha no menu suspenso suas [credenciais de API configuradas anteriormente](#api-credential).

   * **[!UICONTROL Palavras-chave de aceitação]**: insira as palavras-chave padrão ou personalizadas que dispararão automaticamente sua mensagem de aceitação. Para várias palavras-chave, use valores separados por vírgulas.

   * **[!UICONTROL Mensagem de aceitação]**: digite a resposta personalizada que é enviada automaticamente como sua Mensagem de aceitação.

   * **[!UICONTROL Palavras-chave de recusa]**: insira as palavras-chave padrão ou personalizadas que dispararão automaticamente sua mensagem de recusa. Para várias palavras-chave, use valores separados por vírgulas.

   * **[!UICONTROL Mensagem de recusa]**: digite a resposta personalizada que é enviada automaticamente como sua Mensagem de recusa.

   ![](assets/sms_byo_6.png)

1. Clique em **[!UICONTROL Exibir editor de carga]** para validar e personalizar suas cargas de solicitação.

   Você pode personalizar dinamicamente seu conteúdo usando atributos de perfil do e garantir que dados precisos sejam enviados para processamento e geração de resposta com a ajuda de funções auxiliares integradas.

1. Clique em **[!UICONTROL Enviar]** quando terminar a configuração do seu Webhook.

1. No menu **[!UICONTROL Webhooks]**, clique no ![ícone bin](assets/do-not-localize/Smock_Delete_18_N.svg) para excluir seu Webhook.

1. Para modificar a configuração existente, localize o Webhook desejado e clique na opção **[!UICONTROL Editar]** para fazer as alterações necessárias.

1. Acesse e copie sua nova **[!UICONTROL URL do Webhook]** do **[!UICONTROL Webhook]** enviado anteriormente.

   ![](assets/sms_byo_7.png)

Depois de criar e definir as configurações de entrada para o Webhook, agora é necessário criar uma [configuração de canal](sms-configuration-surface.md) para mensagens SMS.

Depois de configurado, você pode aproveitar todos os recursos de canal prontos para uso, como criação de mensagens, personalização, rastreamento de links e relatórios.

## Vídeo tutorial {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3431625)

