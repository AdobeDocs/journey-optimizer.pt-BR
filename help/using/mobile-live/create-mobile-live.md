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
source-git-commit: bfd36dddb5795cd8b6eeb164f70b6cf3fdcb5750
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 1%

---

# Criar uma atividade ao vivo {#create-mobile-live}

>[!BEGINSHADEBOX]

* [Introdução à atividade Live](get-started-mobile-live.md)
* [Configuração de atividade online](mobile-live-configuration.md)
* [Integração da atividade ao vivo com o Adobe Experience Platform Mobile SDK](mobile-live-configuration-sdk.md)
* **[Criar uma atividade online](create-mobile-live.md)**
* [Perguntas frequentes](mobile-live-faq.md)
* [Relatório de campanha de atividade ao vivo](../reports/campaign-global-report-cja-activity.md)

>[!ENDSHADEBOX]

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

1. As campanhas são projetadas para serem executadas em uma data específica ou em uma frequência recorrente. Saiba como configurar o **[!UICONTROL Cronograma]** da sua campanha no [nesta seção](../campaigns/create-campaign.md#schedule).

1. Após a configuração, clique em **[!UICONTROL Revisar para ativar]** e em **[!UICONTROL Ativar]**.

1. Depois que a campanha for ativada, use a **cURL request** fornecida como um modelo para acionar os eventos de início, atualização ou término da Atividade em tempo real. Atualize o payload de amostra com seus dados específicos antes da execução.

   Copie também os identificadores da **[!UICONTROL ID da campanha]** para incluir em sua carga.

   ➡️ Consulte a [Documentação de Campanhas acionadas por API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/) para obter os requisitos de autenticação, incluindo tokens OAuth e chaves de API.

   ![](assets/create-live-3.png)

   +++ Exemplo de uma carga individual

   Observe que a maioria dos campos do exemplo de carga a seguir são obrigatórios, somente `requestId`, `dismissal-date` e `alert` são opcionais.

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

Depois de projetar sua atividade Live, você pode acompanhar a medição do impacto da atividade Live com [relatórios internos](../reports/campaign-global-report-cja-activity.md).
