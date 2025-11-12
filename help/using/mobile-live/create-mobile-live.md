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
source-git-commit: ce6bfca78d097588b5958c10c721b29b7013b3e2
workflow-type: tm+mt
source-wordcount: '379'
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

       &quot;json
       &lbrace;
       &quot;requestId&quot;: &quot;your-request-id&quot;,
       &quot;campaignId&quot;: &quot;your-campaign-id&quot;,
       &quot;destinatários&quot;: &lbrack;
       &lbrace;
       &quot;tipo&quot;: &quot;aep&quot;,
       &quot;userId&quot;: &quot;testemail@gmail.com&quot;,
       &quot;namespace&quot;: &quot;email&quot;,
       &quot;contexto&quot;: &lbrace;
       &quot;requestPayload&quot;: &lbrace;
       &quot;aps&quot;: &lbrace;
       &quot;conteúdo-disponível&quot;: 1,
       &quot;carimbo de data/hora&quot;: 1756984054,              // hora atual da época
       &quot;data de demissão&quot;: 1756984084,         // opcional - remover automaticamente quando event=&quot;end&quot;
       &quot;event&quot;: &quot;update&quot;,                    // iniciar | atualizar | fim
       
       // Campos de FoodDeliveryLiveActivityAttributes
       &quot;content-state&quot;: &lbrace;
       &quot;orderStatus&quot;: &quot;Entregue&quot;
       ,
       
       &quot;attributes-type&quot;: &quot;FoodDeliveryLiveActivityAttributes&quot;,
       &quot;atributos&quot;: &lbrace;
       &quot;RestaurantName&quot;: &quot;Pizza&quot;,
       &quot;liveActivityData&quot;: &lbrace;
       &quot;liveActivityID&quot;: &quot;orderId1&quot;       // ID de referência do cliente
       
       ,
       
       &quot;alerta&quot;: &lbrace;
       &quot;título&quot;: &quot;Pedido entregue!&quot;,
       &quot;body&quot;: &quot;Sua pizza chegou.&quot;
       
       
       
       
       
       &rbrack;
       
       &quot;
   +++

Depois de projetar sua atividade Live, você pode acompanhar a medição do impacto da atividade Live com [relatórios internos](../reports/campaign-global-report-cja-activity.md).
