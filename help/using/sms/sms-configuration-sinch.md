---
solution: Journey Optimizer
product: journey optimizer
title: Configurar provedor Sinch
description: Saiba como configurar seu ambiente para enviar mensagens de texto com o Journey Optimizer com Sinch
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 85412a85-edf0-4069-8bc7-b80371375f1f
source-git-commit: 5beaf2b7dc339cb94352cd7503dd86a97a6db6bd
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 1%

---

# Configurar provedor Sinch {#sms-configuration-sinch}

Ao usar o provedor Sinch com o Journey Optimizer, você pode encontrar três opções distintas:

* **Configuração de SMS**: configure suas credenciais da API Sinch para enviar mensagens SMS facilmente.

* **Configuração do MMS**: para mensagens multimídia (MMS), configure suas credenciais da API do Sinch MMS. Observe que o rastreamento e a resposta às mensagens de entrada são manipulados pela configuração do SMS. A configuração do MMS é somente para entrega de saída da mensagem MMS.

* **Configuração do RCS**: configure suas credenciais da API Sinch para enviar mensagens do RCS sem problemas.

Para configurar seu provedor Sinch, siga as etapas abaixo:

1. [Criar credencial de API](#create-api)
1. [Criar webhook](sms-webhook.md)
1. [Criar configuração de canal](sms-configuration-surface.md)
1. [Criar Jornada ou Campanha com ação de canal SMS](create-sms.md)

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

1. Selecione **[!UICONTROL Usar conjunto de dados personalizado para entrada]** para rotear o SMS de entrada desta credencial para um conjunto de dados pré-criado que você escolher na lista suspensa. [Saiba mais sobre como criar conjuntos de dados](../experience-decisioning/data-collection/create-dataset.md)

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

Depois de criar e configurar sua credencial de API, agora é necessário criar [seu Webhook](sms-webhook.md) e uma configuração de canal para suas mensagens RCS. [Saiba mais](sms-configuration-surface.md)

## Configurar credenciais de API para MMS{#sinch-mms}

>[!IMPORTANT]
>
> Juntamente com a configuração do MMS, também é necessário criar credenciais da API Sinch especificamente para rastrear mensagens de entrada e gerenciar solicitações de consentimento.

Para configurar o Sinch MMS para enviar o MMS com o Journey Optimizer, siga estas etapas:

1. No painel à esquerda, vá para **[!UICONTROL Administração]** > **[!UICONTROL Canais]** `>` **[!UICONTROL Configurações de SMS]** e selecione o menu **[!UICONTROL Credenciais de API]**. Clique no botão **[!UICONTROL Criar novas credenciais de API]**.

1. Configure suas credenciais da API do MMS, conforme detalhado abaixo:

   * **[!UICONTROL Fornecedor de SMS]**: Sinch MMS.

   * **[!UICONTROL Nome]**: escolha um nome para a credencial de API.

   * **[!UICONTROL ID do Projeto]**, **[!UICONTROL ID do Aplicativo]** e **[!UICONTROL Token da API]**: siga as etapas abaixo para coletar suas credenciais de API do MMS.

      * Para **[!UICONTROL ID do Projeto]** e **[!UICONTROL ID do Aplicativo]**: Acesse a página [Visão Geral da API de Conversa](https://dashboard.sinch.com/convapi/overview) do seu projeto Sinch no Painel Sinch.
      * Para **[!UICONTROL Token de API]**: obtenha as [Chaves de acesso](https://community.sinch.com/t5/Customer-Dashboard/Sinch-Access-Keys/ta-p/12638) para o seu Projeto Sinch e gere um **Token de API Base64** do seu Projeto Sinch **Chaves de acesso**.

1. Clique em **[!UICONTROL Enviar]** quando terminar de configurar suas credenciais de API.

1. No menu **[!UICONTROL Credenciais da API]**, clique no ícone de compartimento para excluir suas credenciais da API.

1. Para modificar as credenciais existentes, localize as credenciais de API desejadas e clique na opção **[!UICONTROL Editar]** para fazer as alterações necessárias.

Depois de criar e configurar sua credencial de API, agora é necessário criar [seu Webhook](sms-webhook.md) e uma configuração de canal para suas mensagens RCS. [Saiba mais](sms-configuration-surface.md)

## Configurar credencial de API para RCS

<!--![](assets/do-not-localize/rcs-sms.png)-->

As mensagens do RCS (Rich Communication Services) são compatíveis com o Journey Optimizer por meio do Sinch, permitindo o envio de mensagens básicas usando perfis empresariais verificados com elementos de marca, como logotipos e nomes de remetentes.

Observe que as mensagens retornam automaticamente para SMS quando o dispositivo do perfil não é compatível com RCS ou está temporariamente inacessível via RCS.

<!--
### Basic RCS Messages

>[!AVAILABILITY]
>
> Basic RCS messages is only available upon Adobe RCS add-on offering.

1. **Set up your branded RCS agent**

    Create a branded RCS agent in the Sinch Dashboard. [Learn more on branded RCS agent](https://community.sinch.com/t5/RCS/Getting-Started-with-RCS-using-Conversation-API/ta-p/17844)

1. **Set up your [Custom API credentials](sms-configuration-custom.md)**
    
    Once your RCS agent is approved, you need to set up your Sinch API credentials, which include your access key, secret, and service plan ID. These credentials will be used by Journey Optimizer to authenticate and send messages through Sinch's platform.

1. **Create a [channel configuration](sms-configuration-surface.md) for your RCS messages**

    Configure a channel surface in Journey Optimizer by linking your Sinch credentials and defining the messaging parameters. This setup enables you to compose and send RCS messages from Journey Optimizer.

1. **Create and personalize your [SMS message](../sms/create-sms.md)**

    Your messages automatically falls back to SMS when the profile's device does not support RCS or is temporarily unreachable via RCS.
-->

### Mensagens multimídia RCS

>[!AVAILABILITY]
>
> As mensagens RCS avançadas só estão disponíveis com uma conta direta gerenciada pela Sinch.

1. **Configurar o agente RCS da sua marca**

   Crie um agente RCS com marca no Sinch Dashboard. [Saiba mais sobre o agente RCS da marca](https://community.sinch.com/t5/RCS/Getting-Started-with-RCS-using-Conversation-API/ta-p/17844)

1. **Configurar as [Credenciais da API personalizada](sms-configuration-custom.md)**

   Depois que o agente RCS for aprovado, será necessário configurar as credenciais da API personalizada, que incluem AppId, Nome, URL e Tipo de autenticação.

1. **Configure seu RCS com a carga do Provedor.**

   Em suas [Credenciais de API personalizadas](sms-configuration-custom.md), adicione sua Carga do provedor para validar e personalizar suas mensagens do RCS.

1. **Criar uma [configuração de canal](sms-configuration-surface.md) para suas mensagens RCS**

   Configure uma superfície de canal no Journey Optimizer vinculando suas credenciais do Sinch e definindo os parâmetros de mensagens. Essa configuração permite redigir e enviar mensagens RCS do Journey Optimizer.

1. **Criar e personalizar sua [mensagem SMS](../sms/create-sms.md)**

   Cole seu conteúdo diretamente no conteúdo do SMS para incorporar e entregar suas mensagens do RCS (Serviços de Comunicação Avançada).

   ➡️ [Saiba como a Sinch oferece suporte ao RCS na documentação da Sinch](https://sinch.com/blog/rcs-api-guide/)


