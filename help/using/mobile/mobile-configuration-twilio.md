---
solution: Journey Optimizer
product: journey optimizer
title: Configurar provedor Twilio
description: Saiba como configurar seu ambiente para enviar mensagens de texto com o Journey Optimizer com Twilio
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: d6f74566-c913-4727-83b9-473a798a0158
TQID: https://experienceleague.adobe.com/EbPWXkbbXG4zazPUQsqaEeXx5wUi6VzFGrEeYmlAASY
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32id: d556b755-390a-43f0-be32-a08cf6236126
subfeature_v2: id: d2e8a157-b3b0-4143-9ff3-809bf400be56
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: a4c92daab69394e6a736517f2e23a941135f7eb4
workflow-type: tm+mt
source-wordcount: 606
ht-degree: 1%

---

# Configurar provedor Twilio {#sms-configuration-twilio}

Ao integrar o Twilio ao Adobe Journey Optimizer, você pode enviar mensagens de texto para seus perfis como parte de suas jornadas e campanhas.

Para configurar o Twilio como seu provedor de SMS, siga as etapas abaixo:

1. [Criar credencial de API](#api-credential)
1. [Criar webhook](mobile-webhook.md)
1. [Criar configuração de canal](mobile-configuration-surface.md)
1. [Criar Jornada ou Campanha com ação de canal SMS](create-mobile-message.md)

## Configurar credencial de API para SMS/MMS {#api-credential}

Para configurar o Twilio com o Journey Optimizer, você precisa criar novas credenciais de API para o Twilio:

1. No painel à esquerda, vá para **[!UICONTROL Administração]** > **[!UICONTROL Canais]** `>` **[!UICONTROL Configurações de SMS]** e selecione o menu **[!UICONTROL Credenciais de API]**. Clique no botão **[!UICONTROL Criar novas credenciais de API]**.

1. Configure suas credenciais da API de SMS, conforme detalhado abaixo:

   * **[!UICONTROL Fornecedor de SMS]**: Twilio.

   * **[!UICONTROL Nome]**: escolha um nome para a credencial de API.

   * **[!UICONTROL SID da Conta]** e **[!UICONTROL Token de Autenticação]**: acesse o painel **Informações da Conta** da página Painel do Console do Twilio para encontrar suas credenciais.

   * **[!UICONTROL SID da Mensagem]**: digite o identificador exclusivo atribuído a cada mensagem criada pela API do Twilio. Saiba mais em [Documentação do Twilio](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}.

   * **[!UICONTROL Número de Entrada]**: adicione seu número de entrada exclusivo. Isso permite usar as mesmas credenciais de API em diferentes sandboxes, cada uma com seu próprio número de entrada.

1. Selecione **[!UICONTROL Usar conjunto de dados personalizado para entrada]** para rotear o SMS de entrada desta credencial para um conjunto de dados pré-criado que você escolher na lista suspensa. [Saiba mais sobre como usar um conjunto de dados personalizado para palavras-chave de entrada](custom-dataset-inbound-keywords.md)

   >[!NOTE]
   >
   >O esquema do conjunto de dados deve ser **[!UICONTROL XDM ExperienceEvent]** e incluir pelo menos estes grupos de campos:
   >* Adobe CJM ExperienceEvent - Detalhes de interação da mensagem
   >* Adobe CJM ExperienceEvent - Detalhes da execução da mensagem
   >* Adobe CJM ExperienceEvent - Detalhes do perfil da mensagem
   >
   >O esquema e o conjunto de dados devem ser habilitados para o Perfil.

1. Clique em **[!UICONTROL Enviar]** quando terminar de configurar suas credenciais de API.

1. No menu **[!UICONTROL Credenciais da API]**, clique no ícone de compartimento para excluir suas credenciais da API.

1. Para modificar as credenciais existentes, localize as credenciais de API desejadas e clique na opção **[!UICONTROL Editar]** para fazer as alterações necessárias.

1. Clique em **[!UICONTROL Verificar conexão de SMS]**, a partir de suas credenciais de API existentes, para testar e verificar suas credenciais de API de SMS enviando uma mensagem de exemplo para um dispositivo designado.

1. Preencha os campos **Número** e **Mensagem** e clique em **[!UICONTROL Verificar conexão]**.

   >[!IMPORTANT]
   >
   >A mensagem deve ser estruturada para se alinhar ao formato de carga do provedor.

   ![](assets/verify-connection.png)

Depois de criar e configurar a credencial da API, agora é necessário criar uma configuração de canal para mensagens SMS e MMS. [Saiba mais](mobile-configuration-surface.md)

## Configurar credencial de API para RCS

O Adobe Journey Optimizer oferece suporte a mensagens RCS por meio do Twilio usando o recurso [Provedor de SMS personalizado](mobile-configuration-custom.md). Isso permite a entrega de mensagens avançadas e interativas por meio de perfis empresariais verificados, incorporando elementos como carrosséis, botões e conteúdo multimídia.

➡️ [Saiba como o Twilio oferece suporte ao RCS na documentação do Twilio](https://www.twilio.com/docs/rcs)

Para habilitar mensagens RCS com Twilio, novas credenciais de API devem ser configuradas por meio de um Provedor de SMS Personalizado. As credenciais SMS do Twilio existentes não são compatíveis, pois o RCS requer um formato de carga distinto.

Para configurar o RCS com Twilio:

1. **Registrar para Mensagens RCS no Twilio**

   Comece concluindo o processo de registro do RCS na plataforma Twilio. Isso inclui configurar seu perfil comercial e habilitar recursos RCS para sua conta.

1. **Criar um Webhook de SMS**

   [Configurar um Webhook de SMS](mobile-configuration-custom.md#webhook) que pode receber respostas de mensagens RCS de entrada ou atualizações de entrega. Este webhook deve estar vinculado corretamente à configuração do Twilio para comunicação bidirecional.

1. **Criar credencial de API usando Personalizado como fornecedor de SMS**

   No Journey Optimizer, [defina novas credenciais de API](mobile-configuration-custom.md#api-credential) especificamente para o RCS usando &quot;Personalizado&quot; como fornecedor de SMS. Use o método de autenticação de ponto de extremidade RCS, o URL base e os cabeçalhos apropriados.

Depois de criar e configurar a credencial da API, agora é necessário criar uma configuração de canal para suas mensagens RCS. [Saiba mais](mobile-configuration-surface.md)







