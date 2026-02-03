---
solution: Journey Optimizer
product: journey optimizer
title: Configurar o Webhook de SMS
description: Saiba como configurar Webhooks para capturar respostas de entrada para gerenciar o consentimento de aceitação e recusa
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: 4278d8c8294b1413788402cd8eac5959996ad3f5
workflow-type: tm+mt
source-wordcount: '1290'
ht-degree: 0%

---

# Criar webhook {#webhook}

>[!BEGINSHADEBOX]

Se as palavras-chave de aceitação ou recusa não forem fornecidas, as mensagens de consentimento padrão serão usadas para honrar a privacidade do usuário. A adição de palavras-chave personalizadas substitui automaticamente os padrões.

**Palavras-chave padrão:**

* **Aceitar**: ASSINAR, SIM, REINICIAR, INICIAR, CONTINUAR, RETOMAR, INICIAR
* **Recusar**: PARAR, SAIR, CANCELAR, ENCERRAR, CANCELAR INSCRIÇÃO, NÃO
* **Ajuda**: AJUDA

>[!ENDSHADEBOX]

Depois que suas credenciais de API forem criadas com êxito, você poderá configurar Webhooks para capturar respostas de entrada para gerenciar o consentimento de aceitação e recusa e para receber relatórios do delivery, incluindo confirmações de leitura, quando disponíveis.

Ao configurar um webhook, você pode definir sua finalidade com base no tipo de dados que deseja capturar:

* **[!UICONTROL Entrada]**: use esta opção se desejar capturar respostas de consentimento, como aceitação ou recusa, e coletar preferências do usuário.

* **[!UICONTROL Feedback]**: escolha esta opção para rastrear eventos de entrega e participação, incluindo confirmações de leitura e interações de usuário, para oferecer suporte a relatórios e análises.

Navegue pelas guias abaixo, dependendo dos seus provedores de SMS:

>[!BEGINTABS]

>[!TAB Personalizado]

1. No painel à esquerda, navegue até **[!UICONTROL Administração]** `>` **[!UICONTROL Canais]**, selecione o menu **[!UICONTROL Webhooks de SMS]** em **[!UICONTROL Configurações de SMS]** e clique no botão **[!UICONTROL Criar Webhook]**.

   ![](assets/sms_byo_5.png){zoomable="yes"}

1. Defina as configurações do Webhook, conforme detalhado abaixo:

   * **[!UICONTROL Nome]**: digite um nome para o seu Webhook.

   * **[!UICONTROL Selecionar fornecedor de SMS]**: personalizado.

   * **[!UICONTROL Tipo]**: Entrada.

   * **[!UICONTROL Credenciais da API]**: escolha no menu suspenso suas [credenciais de API configuradas anteriormente](sms-configuration-custom.md#api-credential).

   * **[!UICONTROL Número de Telefone do Remetente &#x200B;]**: digite o número de telefone do Remetente &#x200B;que você deseja usar para suas comunicações.

     ![](assets/webhook-inbound.png){zoomable="yes"}

1. Clique em ![](assets/do-not-localize/Smock_Add_18_N.svg) para adicionar categorias de palavras-chave e, em seguida, configure-as dependendo do seu provedor de SMS:

   * **[!UICONTROL Categoria de Palavra-chave de Entrada]**: Escolha suas categorias de palavra-chave: **[!UICONTROL Aceitação]**, **[!UICONTROL Recusa]**, **[!UICONTROL Aceitação Dupla]**, **[!UICONTROL Ajuda]** ou **[!UICONTROL Personalizado]**.

   * **[!UICONTROL Inserir uma palavra-chave]**: insira as palavras-chave padrão ou personalizadas que dispararão automaticamente sua mensagem. Clique em ![](assets/do-not-localize/Smock_Add_18_N.svg) para adicionar várias palavras-chave.

     Para **[!UICONTROL Palavra-chave personalizada]**, use palavras-chave não relacionadas a consentimento para ações baseadas em lote em uma jornada.

   * **[!UICONTROL Mensagem de resposta]**: selecione no menu suspenso a resposta personalizada que é enviada automaticamente.

   * **[!UICONTROL Recusa difusa]**: habilite esta opção para enviar uma resposta automática quando uma palavra-chave de recusa quase correspondente for detectada.

   ![](assets/sms_byo_6.png){zoomable="yes"}

1. Digite uma **[!UICONTROL Mensagem de Resposta Padrão]** enviada automaticamente quando uma mensagem de entrada não corresponde a nenhuma palavra-chave ou categoria configurada.

1. Clique em **[!UICONTROL Exibir editor de carga]** para validar e personalizar suas cargas de solicitação.

   Você pode personalizar dinamicamente seu conteúdo usando atributos de perfil do e garantir que dados precisos sejam enviados para processamento e geração de resposta com a ajuda de funções auxiliares integradas.

1. Clique em **[!UICONTROL Enviar]** quando terminar a configuração do seu Webhook.

1. Para criar um webhook **[!UICONTROL Feedback]**, siga as mesmas etapas descritas acima, selecionando **[!UICONTROL Feedback]** como seu webhook **[!UICONTROL Type]**.

1. No menu **[!UICONTROL Webhooks]**, você pode editar ou excluir webhooks existentes, ou acessar e copiar a **[!UICONTROL URL do Webhook]** para integração com o provedor de SMS.

   ![](assets/sms_byo_7.png){zoomable="yes"}

Depois de criar e definir as configurações do Webhook, agora é necessário criar uma [configuração de canal](sms-configuration-surface.md) para mensagens SMS.

Depois de configurado, você pode aproveitar todos os recursos de canal prontos para uso, como criação de mensagens, personalização, rastreamento de links e relatórios.

>[!TAB Infobip]

1. No painel à esquerda, navegue até **[!UICONTROL Administração]** `>` **[!UICONTROL Canais]**, selecione o menu **[!UICONTROL Webhooks de SMS]** em **[!UICONTROL Configurações de SMS]** e clique no botão **[!UICONTROL Criar Webhook]**.

   ![](assets/sms_byo_5.png){zoomable="yes"}

1. Defina as configurações do Webhook, conforme detalhado abaixo:

   * **[!UICONTROL Nome]**: digite um nome para o seu Webhook.

   * **[!UICONTROL Selecionar fornecedor de SMS]**: Infobip.

   * **[!UICONTROL Tipo]**: Entrada.

   * **[!UICONTROL Credenciais da API]**: escolha no menu suspenso suas [credenciais de API configuradas anteriormente](sms-configuration-infobip.md#api-credential).

   * **[!UICONTROL Número de Telefone do Remetente &#x200B;]**: digite o número de telefone do Remetente &#x200B;que você deseja usar para suas comunicações.

     ![](assets/webhook-infobip-1.png){zoomable="yes"}

1. Clique em ![](assets/do-not-localize/Smock_Add_18_N.svg) para adicionar categorias de palavras-chave e, em seguida, configure-as dependendo do seu provedor de SMS:

   * **[!UICONTROL Categoria de Palavra-chave de Entrada]**: Escolha suas categorias de palavra-chave: **[!UICONTROL Aceitação]**, **[!UICONTROL Recusa]**, **[!UICONTROL Aceitação Dupla]**, **[!UICONTROL Ajuda]** ou **[!UICONTROL Personalizado]**.

   * **[!UICONTROL Inserir uma palavra-chave]**: insira as palavras-chave padrão ou personalizadas que dispararão automaticamente sua mensagem. Clique em ![](assets/do-not-localize/Smock_Add_18_N.svg) para adicionar várias palavras-chave.

     Para **[!UICONTROL Palavra-chave personalizada]**, use palavras-chave não relacionadas a consentimento para ações baseadas em lote em uma jornada.

   * **[!UICONTROL Mensagem de resposta]**: selecione no menu suspenso a resposta personalizada que é enviada automaticamente.

   * **[!UICONTROL Recusa difusa]**: habilite esta opção para enviar uma resposta automática quando uma palavra-chave de recusa quase correspondente for detectada.

   ![](assets/webhook-infobip-2.png){zoomable="yes"}

1. Digite uma **[!UICONTROL Mensagem de Resposta Padrão]** enviada automaticamente quando uma mensagem de entrada não corresponde a nenhuma palavra-chave ou categoria configurada.

1. Clique em **[!UICONTROL Enviar]** quando terminar a configuração do seu Webhook.

1. Para criar um webhook **[!UICONTROL Feedback]**, siga as mesmas etapas descritas acima, selecionando **[!UICONTROL Feedback]** como seu webhook **[!UICONTROL Type]**.

1. No menu **[!UICONTROL Webhooks]**, você pode editar ou excluir webhooks existentes, ou acessar e copiar a **[!UICONTROL URL do Webhook]** para integração com o provedor de SMS.

   ![](assets/sms_byo_7.png){zoomable="yes"}

Depois de criar e definir as configurações de entrada para o Webhook, agora é necessário criar uma [configuração de canal](sms-configuration-surface.md) para mensagens SMS.

Depois de configurado, você pode aproveitar todos os recursos de canal prontos para uso, como criação de mensagens, personalização, rastreamento de links e relatórios.

>[!TAB Sinch]

1. No painel à esquerda, navegue até **[!UICONTROL Administração]** `>` **[!UICONTROL Canais]**, selecione o menu **[!UICONTROL Webhooks de SMS]** em **[!UICONTROL Configurações de SMS]** e clique no botão **[!UICONTROL Criar Webhook]**.

   ![](assets/sms_byo_5.png){zoomable="yes"}

1. Defina as configurações do Webhook, conforme detalhado abaixo:

   * **[!UICONTROL Nome]**: digite um nome para o seu Webhook.

   * **[!UICONTROL Selecionar fornecedor de SMS]**: Sinch.

   * **[!UICONTROL Tipo]**: Entrada.

   * **[!UICONTROL Credenciais da API]**: escolha no menu suspenso suas [credenciais de API configuradas anteriormente](sms-configuration-sinch.md#create-api).

   * **[!UICONTROL Número de Telefone do Remetente &#x200B;]**: digite o número de telefone do Remetente &#x200B;que você deseja usar para suas comunicações.

     ![](assets/webhook-sinch-1.png){zoomable="yes"}

1. Clique em ![](assets/do-not-localize/Smock_Add_18_N.svg) para adicionar categorias de palavras-chave e, em seguida, configure-as dependendo do seu provedor de SMS:

   * **[!UICONTROL Categoria de Palavra-chave de Entrada]**: Escolha suas categorias de palavra-chave: **[!UICONTROL Aceitação]**, **[!UICONTROL Recusa]**, **[!UICONTROL Aceitação Dupla]**, **[!UICONTROL Ajuda]** ou **[!UICONTROL Personalizado]**.

   * **[!UICONTROL Inserir uma palavra-chave]**: insira as palavras-chave padrão ou personalizadas que dispararão automaticamente sua mensagem. Clique em ![](assets/do-not-localize/Smock_Add_18_N.svg) para adicionar várias palavras-chave.

     Para **[!UICONTROL Palavra-chave personalizada]**, use palavras-chave não relacionadas a consentimento para ações baseadas em lote em uma jornada.

   * **[!UICONTROL Mensagem de resposta]**: selecione no menu suspenso a resposta personalizada que é enviada automaticamente.

   * **[!UICONTROL Recusa difusa]**: habilite esta opção para enviar uma resposta automática quando uma palavra-chave de recusa quase correspondente for detectada.

   ![](assets/webhook-sinch-2.png){zoomable="yes"}

1. Digite uma **[!UICONTROL Mensagem de Resposta Padrão]** enviada automaticamente quando uma mensagem de entrada não corresponde a nenhuma palavra-chave ou categoria configurada.

1. Clique em **[!UICONTROL Enviar]** quando terminar a configuração do seu Webhook.

1. No menu **[!UICONTROL Webhooks]**, clique no ![ícone bin](assets/do-not-localize/Smock_Delete_18_N.svg) para excluir seu Webhook.

1. Para modificar a configuração existente, localize o Webhook desejado e clique na opção **[!UICONTROL Editar]** para fazer as alterações necessárias.

1. Acesse e copie sua nova **[!UICONTROL URL do Webhook]** do **[!UICONTROL Webhook]** enviado anteriormente.

   ![](assets/sms_byo_7.png){zoomable="yes"}

Depois de criar e definir as configurações de entrada para o Webhook, agora é necessário criar uma [configuração de canal](sms-configuration-surface.md) para mensagens SMS.

Depois de configurado, você pode aproveitar todos os recursos de canal prontos para uso, como criação de mensagens, personalização, rastreamento de links e relatórios.

>[!TAB Twilio]

1. No painel à esquerda, navegue até **[!UICONTROL Administração]** `>` **[!UICONTROL Canais]**, selecione o menu **[!UICONTROL Webhooks de SMS]** em **[!UICONTROL Configurações de SMS]** e clique no botão **[!UICONTROL Criar Webhook]**.

   ![](assets/sms_byo_5.png){zoomable="yes"}

1. Defina as configurações do Webhook, conforme detalhado abaixo:

   * **[!UICONTROL Nome]**: digite um nome para o seu Webhook.

   * **[!UICONTROL Selecionar fornecedor de SMS]**: Twilio.

   * **[!UICONTROL Tipo]**: Entrada.

   * **[!UICONTROL Credenciais da API]**: escolha no menu suspenso suas [credenciais de API configuradas anteriormente](sms-configuration-twilio.md#create-api).

   * **[!UICONTROL Número de Telefone do Remetente &#x200B;]**: digite o número de telefone do Remetente &#x200B;que você deseja usar para suas comunicações.

1. Clique em ![](assets/do-not-localize/Smock_Add_18_N.svg) para adicionar categorias de palavras-chave e, em seguida, configure-as dependendo do seu provedor de SMS:

   * **[!UICONTROL Categoria de Palavra-chave de Entrada]**: Escolha suas categorias de palavra-chave: **[!UICONTROL Aceitação]**, **[!UICONTROL Recusa]**, **[!UICONTROL Aceitação Dupla]**, **[!UICONTROL Ajuda]** ou **[!UICONTROL Personalizado]**.

   * **[!UICONTROL Inserir uma palavra-chave]**: insira as palavras-chave padrão ou personalizadas que dispararão automaticamente sua mensagem. Clique em ![](assets/do-not-localize/Smock_Add_18_N.svg) para adicionar várias palavras-chave.

     Para **[!UICONTROL Palavra-chave personalizada]**, use palavras-chave não relacionadas a consentimento para ações baseadas em lote em uma jornada.

   * **[!UICONTROL Mensagem de resposta]**: selecione no menu suspenso a resposta personalizada que é enviada automaticamente.

   * **[!UICONTROL Recusa difusa]**: habilite esta opção para enviar uma resposta automática quando uma palavra-chave de recusa quase correspondente for detectada.

1. Digite uma **[!UICONTROL Mensagem de Resposta Padrão]** enviada automaticamente quando uma mensagem de entrada não corresponde a nenhuma palavra-chave ou categoria configurada.

1. Clique em **[!UICONTROL Enviar]** quando terminar a configuração do seu Webhook.

1. No menu **[!UICONTROL Webhooks]**, clique no ![ícone bin](assets/do-not-localize/Smock_Delete_18_N.svg) para excluir seu Webhook.

1. Para modificar a configuração existente, localize o Webhook desejado e clique na opção **[!UICONTROL Editar]** para fazer as alterações necessárias.

1. Acesse e copie sua nova **[!UICONTROL URL do Webhook]** do **[!UICONTROL Webhook]** enviado anteriormente.

Depois de criar e definir as configurações de entrada para o Webhook, agora é necessário criar uma [configuração de canal](sms-configuration-surface.md) para mensagens SMS.

Depois de configurado, você pode aproveitar todos os recursos de canal prontos para uso, como criação de mensagens, personalização, rastreamento de links e relatórios.


>[!ENDTABS]


## Vídeo tutorial {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3431625)

