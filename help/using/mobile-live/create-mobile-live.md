---
solution: Journey Optimizer
product: journey optimizer
title: Criar uma mensagem de atividade ao vivo
description: Saiba como criar uma atividade ao vivo no Journey Optimizer
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 9864a136-e129-4279-bb09-081b72f584df
source-git-commit: 6b4e3a6c32d24861f1ea8df54fc2e4fbb19d0ce7
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 3%

---

# Criar uma Atividade em tempo real {#create-mobile-live}

Após definir a configuração móvel e implementar o Adobe Experience Platform mobile SDK, você pode começar a criar sua atividade Live no Journey Optimizer:

1. Acesse o menu **[!UICONTROL Campanhas]** e clique em **[!UICONTROL Criar campanha]**.

1. Selecione o tipo de campanha **API acionada**.

   * Selecione **Marketing acionado por API** para campanhas baseadas em público-alvo

   * Selecione **Transacional acionado por API** para campanhas individuais.

   >[!IMPORTANT]
   >
   > Observe que para a **Transacional acionada por API**, a opção **[!UICONTROL Alta Taxa de Transferência]** não deve estar habilitada.

   ![](assets/create-live-1.png)

1. Na seção **[!UICONTROL Propriedades]**, edite o **[!UICONTROL Título]** e a **[!UICONTROL Descrição]** da sua campanha.

1. Na seção **[!UICONTROL Actions]**, escolha **[!UICONTROL Atividade online]** e selecione ou crie uma nova configuração.

   Saiba mais sobre a configuração de atividade do Live em [esta página](mobile-live-configuration.md).

   ![](assets/create-live-2.png)

1. Clique em **[!UICONTROL Criar experimento]** para começar a configurar seu experimento de conteúdo e criar tratamentos para medir seu desempenho e identificar a melhor opção para seu público-alvo. [Saiba mais](../content-management/content-experiment.md)

1. Na guia **[!UICONTROL Público]**, escolha seu **[!UICONTROL Tipo de identidade]** [Saiba mais](../audience/about-audiences.md).

   >[!NOTE]
   >
   >Para campanhas de **Marketing acionado por API**, você pode selecionar um público existente que atue como a primeira segmentação antes de verificar a assinatura de channelID APNs da carga da API.

1. As campanhas são projetadas para serem executadas em uma data específica ou em uma frequência recorrente. Saiba como configurar o **[!UICONTROL Cronograma]** da sua campanha no [nesta seção](../campaigns/create-campaign.md#schedule).

1. Após a configuração, clique em **[!UICONTROL Revisar para ativar]** e em **[!UICONTROL Ativar]**.

1. Depois que a campanha for ativada, use a **cURL request** fornecida como um modelo para acionar os eventos de início, atualização ou término da Atividade em tempo real. Atualize o payload de amostra com seus dados específicos antes da execução.

   Copie também os identificadores da **[!UICONTROL ID da campanha]** para incluir em sua carga.

   ➡️ Consulte a [Documentação de Campanhas acionadas por API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/) para obter os requisitos de autenticação, incluindo tokens OAuth e chaves de API.

   ![](assets/create-live-3.png)

   +++ Exemplo de carga para casos de uso unitários (campanha transacional acionada por API)

   Este exemplo de conteúdo é para campanhas individuais que usam o tipo de campanha **Transacional** acionado por API. Observe que a maioria dos campos do exemplo de carga a seguir são obrigatórios, somente `requestId`, `dismissal-date` e `alert` são opcionais.

   ```json
   {
       "requestId": "your-request-id",
       "campaignId": "your-campaign-id",
       "recipients": [
   {
       "type": "aep",
       "userId": "testemail@gmail.com",
       "namespace": "email",
       "context": {
        "requestPayload": {
       "aps": {
       "content-available": 1,
       "timestamp": 1756984054,              // current epoch time
       "dismissal-date": 1756984084,         // optional – auto remove when event="end"
       "event": "update",                    // start | update | end
   
       // Fields from FoodDeliveryLiveActivityAttributes
       "content-state": {
         "orderStatus": "Delivered"
       },
   
       "attributes-type": "FoodDeliveryLiveActivityAttributes",
       "attributes": {
         "restaurantName": "Pizza",
         "liveActivityData": {
           "liveActivityID": "orderId1"       // customer reference ID
         }
       },
   
       "alert": {
         "title": "Order Delivered!",
         "body": "Your pizza has arrived."
       }
     }
   }
   }
   }
   ]
   }
   ```

   +++

   +++ Exemplo de uma carga para casos de uso de transmissão (campanha de marketing acionada por API)

   Este exemplo de conteúdo é para campanhas baseadas em público usando o tipo de campanha **Marketing acionado por API**.

   ```json
   {
       "requestId": "123400000",
       "campaignId": "d32e6f6c-56df-4a98-a2c0-6db6008f8f32",
       "audience": {
           "id": "508f9416-52d0-4898-ba47-08baaa22e9c7"
       },
       "context": {
           "requestPayload": {
               "aps": {
                   "input-push-channel": "V+8UslywEfAAAOq9SbTrLg==",  //apns-channel-id
                   "content-available": 1,
                   "timestamp": 1770808339,
                   "event": "update",   // start | update | end
   
                   // Fields from GameScoreLiveActivityAttributes
                   "content-state": {
                       "homeTeamScore": 33,
                       "awayTeamScore": 49,
                       "statusText": "Wingdom keeps scoring!"
                   },
                   "attributes-type": "GameScoreLiveActivityAttributes",
                   "attributes": {
                       "liveActivityData": {
                           "channelID": "V+8UslywEfAAAOq9SbTrLg=="   //apns-channel-id, must match the "input-push-channel" value
                       }
                   },
                   "alert": {
                       "title": "This is the title for game",
                       "body": "This is the body for body"
                   }
               }
           }
       }
   }
   ```

   +++

Depois de projetar sua atividade Live, você pode acompanhar a medição do impacto da atividade Live com [relatórios internos](../reports/campaign-global-report-cja-activity.md).

## Vídeo tutorial

Descubra como configurar as atividades do iOS Live com o Adobe Journey Optimizer para fornecer atualizações avançadas em tempo real na Tela de bloqueio do iPhone e no Dynamic Island.

>[!VIDEO](https://video.tv.adobe.com/v/3479864)
