---
solution: Journey Optimizer
product: journey optimizer
title: Configurar provedor Sinch
description: Saiba como configurar seu ambiente para enviar mensagens móveis com o Journey Optimizer com Sinch
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 85412a85-edf0-4069-8bc7-b80371375f1f
TQID: https://experienceleague.adobe.com/24n9GhVTfQ9y4hlvY6g67dyL0FHqNOJW0aP-WIpzRqs
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
subfeature_v2:
  - id: d2e8a157-b3b0-4143-9ff3-809bf400be56
  - id: fdac7813-bd56-47ae-9f6d-fa94ad1c5dee
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: a4c92daab69394e6a736517f2e23a941135f7eb4
workflow-type: tm+mt
source-wordcount: 1007
ht-degree: 1%

---

# Configurar provedor Sinch {#sms-configuration-sinch}

Ao usar o provedor Sinch com o Journey Optimizer, você pode encontrar três opções distintas:

* **Configuração de SMS**: configure suas credenciais da API Sinch para enviar mensagens SMS facilmente.

* **Configuração do MMS**: para mensagens multimídia (MMS), configure suas credenciais da API do Sinch MMS. Observe que o rastreamento e a resposta às mensagens de entrada são manipulados pela configuração do SMS. A configuração do MMS é somente para entrega de saída da mensagem MMS.

* **Configuração do RCS**: configure suas credenciais da API Sinch para enviar mensagens do RCS sem problemas.

Para configurar seu provedor Sinch, siga as etapas abaixo:

1. [Criar credencial de API](#create-api)
1. [Criar webhook](mobile-webhook.md)
1. [Criar configuração de canal](mobile-configuration-surface.md)
1. [Criar Jornada ou Campanha com ação de canal SMS](create-mobile-message.md)

## Configurar credenciais de API para SMS{#create-api}

Para configurar seu provedor Sinch para enviar mensagens SMS e MMS com o Journey Optimizer, siga estas etapas:

1. No painel à esquerda, vá para **[!UICONTROL Administração]** > **[!UICONTROL Canais]** `>` **[!UICONTROL Configurações de SMS]** e selecione o menu **[!UICONTROL Credenciais de API]**. Clique no botão **[!UICONTROL Criar novas credenciais de API]**.

1. Configure suas credenciais da API de SMS, conforme detalhado abaixo:

   +++ Lista de credenciais SMS para configuração

   | Campos de configuração | Descrição |
   |---|---|
   | Fornecedor de SMS | Sinch |
   | Nome | Escolha um nome para a credencial da API. |
   | ID de serviço e token de API | Para acessar a página APIs, você pode encontrar suas credenciais na guia SMS. Saiba mais em [Documentação da Sinch](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"}. |
   | Número de entrada | Adicione seu número de entrada exclusivo ou código curto. Isso permite usar as mesmas credenciais de API em diferentes sandboxes, cada uma com seu próprio número de entrada ou código curto. |
   | Substituir URL | Insira seu URL personalizado para substituir os endpoints padrão para relatórios do delivery de SMS, dados de feedback, mensagens de entrada ou notificações de eventos. A Sinch enviará todas as atualizações relevantes para esse URL em vez das predefinidas. |

   +++

<!--
1. Choose how user consent should be tracked for messaging:

    * **[!UICONTROL Sender short code]**: Inbound keyword consent is keyed to your **sender short code** only. Use when one inbound number is enough to represent consent.

    * **[!UICONTROL Sender short code + profile number]**: Consent is keyed to the **sender short code** and the profile **mobile number**. Use when profiles can have several numbers, or when opt-in/out must apply per sender and recipient pair.
-->

1. Selecione **[!UICONTROL Usar conjunto de dados personalizado para entrada]** para rotear o SMS de entrada desta credencial para um conjunto de dados pré-criado que você escolher na lista suspensa. [Saiba mais sobre como usar um conjunto de dados personalizado para palavras-chave de entrada](../mobile/custom-dataset-inbound-keywords.md)

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

Depois de criar e configurar sua credencial de API, agora é necessário criar [seu Webhook](mobile-webhook.md) e uma configuração de canal para suas mensagens RCS. [Saiba mais](mobile-configuration-surface.md)

## Configurar credenciais de API para MMS{#sinch-mms}

>[!IMPORTANT]
>
> Juntamente com a configuração do MMS, também é necessário criar credenciais da API Sinch especificamente para rastrear mensagens de entrada e gerenciar solicitações de consentimento.

Para configurar o Sinch MMS para enviar o MMS com o Journey Optimizer, siga estas etapas:

1. No painel à esquerda, vá para **[!UICONTROL Administração]** > **[!UICONTROL Canais]** `>` **[!UICONTROL Configurações de SMS]** e selecione o menu **[!UICONTROL Credenciais de API]**. Clique no botão **[!UICONTROL Criar novas credenciais de API]**.

1. Configure suas credenciais da API do MMS, conforme detalhado abaixo:

   * **[!UICONTROL Fornecedor de SMS]**: Sinch MMS.

   * **[!UICONTROL Nome]**: digite um nome para a credencial da API.

   * **[!UICONTROL ID do Projeto]**, **[!UICONTROL ID do Aplicativo]** e **[!UICONTROL Token da API]**: siga as etapas abaixo para coletar suas credenciais de API do MMS.

      * Para **[!UICONTROL ID do Projeto]** e **[!UICONTROL ID do Aplicativo]**: Acesse a página [Visão Geral da API de Conversa](https://dashboard.sinch.com/convapi/overview) do seu projeto Sinch no Painel Sinch.
      * Para **[!UICONTROL Token de API]**: obtenha as [Chaves de acesso](https://community.sinch.com/t5/Customer-Dashboard/Sinch-Access-Keys/ta-p/12638) para o seu Projeto Sinch e gere um **Token de API Base64** do seu Projeto Sinch **Chaves de acesso**.

1. Clique em **[!UICONTROL Enviar]** quando terminar de configurar suas credenciais de API.

1. No menu **[!UICONTROL Credenciais da API]**, clique no ícone de compartimento para excluir suas credenciais da API.

1. Para modificar as credenciais existentes, localize as credenciais de API desejadas e clique na opção **[!UICONTROL Editar]** para fazer as alterações necessárias.

Depois de criar e configurar sua credencial de API, agora é necessário criar [seu Webhook](mobile-webhook.md) e uma configuração de canal para suas mensagens RCS. [Saiba mais](mobile-configuration-surface.md)

## Configurar credencial de API para RCS

<!--![](assets/do-not-localize/rcs-sms.png)-->

As mensagens do RCS (Rich Communication Services) são compatíveis com o Journey Optimizer por meio do Sinch, permitindo o envio de mensagens básicas usando perfis empresariais verificados com elementos de marca, como logotipos e nomes de remetentes.

A criação de RCS nativo requer Sinch RCS. Twilio, Infobip e outros provedores devem usar uma [integração de provedor personalizada](mobile-configuration-custom.md).

Observe que as mensagens retornam automaticamente para SMS quando o dispositivo do perfil não é compatível com RCS ou está temporariamente inacessível via RCS.

Para configurar o Sinch RCS para enviar o RCS com o Journey Optimizer, siga estas etapas:

1. No painel à esquerda, vá para **[!UICONTROL Administração]** > **[!UICONTROL Canais]** `>` **[!UICONTROL Configurações de SMS]** e selecione o menu **[!UICONTROL Credenciais de API]**. Clique no botão **[!UICONTROL Criar novas credenciais de API]**.

1. Configure suas credenciais da API RCS, conforme detalhado abaixo:

   * **[!UICONTROL Fornecedor de SMS]**: Sinch RCS.

   * **[!UICONTROL Nome]**: digite um nome para a credencial da API.

   * **[!UICONTROL ID do Projeto]**, **[!UICONTROL ID do Aplicativo]** e **[!UICONTROL Token da API]**: insira a ID do projeto, a ID do aplicativo e o token da API da sua conta Sinch RCS.

   * **[!UICONTROL ID do Plano de Serviço]**: insira a ID do plano de serviço associada à sua conta Sinch.

   * **[!UICONTROL Token da API de SMS]**: digite o token da API de SMS da sua conta Sinch.

   ![](assets/rcs-config.png)

1. Opcionalmente, habilite a opção **[!UICONTROL Usar conjunto de dados personalizado para entrada]** para armazenar mensagens RCS de entrada em um conjunto de dados personalizado. [Saiba mais](../mobile/custom-dataset-inbound-keywords.md)

1. Defina o **[!UICONTROL limite de taxa de API (solicitações por segundo)]** para limitar o número máximo de chamadas de API por segundo, use o valor recomendado do seu provedor para evitar limitação ou deixe-o em 0 para solicitações ilimitadas.

1. Clique em **[!UICONTROL Enviar]** quando terminar de configurar suas credenciais de API.

1. No menu **[!UICONTROL Credenciais da API]**, clique no ícone de compartimento para excluir suas credenciais da API.

1. Para modificar as credenciais existentes, localize as credenciais de API desejadas e clique na opção **[!UICONTROL Editar]** para fazer as alterações necessárias.

Depois de criar e configurar sua credencial de API, agora é necessário criar [seu Webhook](mobile-webhook.md) e uma configuração de canal para suas mensagens RCS. [Saiba mais](mobile-configuration-surface.md)


<!--
### Basic RCS Messages

>[!AVAILABILITY]
>
> Basic RCS messages is only available upon Adobe RCS add-on offering.

1. **Set up your branded RCS agent**

    Create a branded RCS agent in the Sinch Dashboard. [Learn more on branded RCS agent](https://community.sinch.com/t5/RCS/Getting-Started-with-RCS-using-Conversation-API/ta-p/17844)

1. **Set up your [Custom API credentials](mobile-configuration-custom.md)**
    
    Once your RCS agent is approved, you need to set up your Sinch API credentials, which include your access key, secret, and service plan ID. These credentials will be used by Journey Optimizer to authenticate and send messages through Sinch's platform.

1. **Create a [channel configuration](mobile-configuration-surface.md) for your RCS messages**

    Configure a channel surface in Journey Optimizer by linking your Sinch credentials and defining the messaging parameters. This setup enables you to compose and send RCS messages from Journey Optimizer.

1. **Create and personalize your [SMS message](../mobile/create-mobile-message.md)**

    Your messages automatically falls back to SMS when the profile's device does not support RCS or is temporarily unreachable via RCS.
-->



