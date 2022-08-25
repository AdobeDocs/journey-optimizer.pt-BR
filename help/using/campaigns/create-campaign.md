---
title: Criar uma campanha
description: Saiba como criar campanhas no [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 7c4afc98-0d79-4e26-90f8-558bac037169
source-git-commit: 711fdf1dce0688d2e21d405a4e3e8777612b2f3b
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 4%

---

# Criar uma campanha {#create-campaign}

>[!NOTE]
>
>Antes de criar uma nova campanha, verifique se você tem um canal de superfície (ou seja, uma predefinição de mensagem) e um segmento do Adobe Experience Platform pronto para uso. Saiba mais nestas seções:
>
>* [Criar superfícies de canal](../configuration/channel-surfaces.md)
>* [Introdução aos segmentos](../segment/about-segments.md)


## Configurar uma campanha {#configure}

As etapas para criar uma campanha são as seguintes:

1. Acesse o **[!UICONTROL Campaigns]** , em seguida, clique em **[!UICONTROL Create campaign]**.

   ![](assets/create-campaign.png)

   >[!NOTE]
   >
   >Você também pode duplicar uma campanha ao vivo existente para criar uma nova.[Saiba mais](modify-stop-campaign.md#duplicate) <!-- check if only live campaigns-->

<!--1. In the **[!UICONTROL Properties]** section, specify when you want to execute the campaign:

    * **[!UICONTROL Scheduled]**: execute the campaign immediately or on a specified date. Scheduled campaigns are aimed at sending **marketing** type messages.
    * **[!UICONTROL API-triggered]**: execute the campaign using an API call. API-triggered campaigns are aimed at sending **transactional** messages, i.e. messages sent out following an action performed by an individual: password reset, card abandonment etc. [Learn how to trigger a campaign using APIs](api-triggered-campaigns.md)-->

1. No **[!UICONTROL Actions]** escolha o canal e a superfície do canal a serem usados para enviar a mensagem e clique em **[!UICONTROL Create]**.

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >Somente superfícies de canal compatíveis com o tipo de campanha (marketing ou transacional) são listadas na lista suspensa.

1. Especifique um título e uma descrição para a campanha.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. No **[!UICONTROL Actions]** , configure a mensagem a ser enviada com a campanha:

   1. Clique no botão **[!UICONTROL Edit content]** , em seguida, configure e crie o conteúdo da mensagem. [Saiba mais sobre mensagens](../messages/get-started-content.md)

      >[!NOTE]
      >
      >O **[!UICONTROL Simulate content]** permite usar perfis de teste para visualizar e testar o conteúdo. [Saiba mais](../design/preview.md)

   1. Quando o conteúdo estiver pronto, clique na seta para voltar à tela de criação da campanha.

      ![](assets/create-campaign-design.png)

   1. No **[!UICONTROL Actions tracking]** , especifique se deseja rastrear como os recipients reagem ao seu delivery.

      Os resultados do rastreamento serão acessíveis no relatório da campanha após a execução da campanha. [Saiba mais sobre relatórios de campanha](../reports/campaign-global-report.md)

1. Defina o público-alvo como meta. Para fazer isso, clique no botão **[!UICONTROL Select audience]** para exibir a lista de segmentos disponíveis do Adobe Experience Platform. [Saiba mais sobre segmentos](../segment/about-segments.md)

   <!-- NOTE For API-triggered campaigns, the audience needs to be set via API call. [Learn more](api-triggered-campaigns.md)-->

   No **[!UICONTROL Identity namespace]** , escolha o namespace a ser usado para identificar os indivíduos do segmento selecionado. [Saiba mais sobre namespaces](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   >[!NOTE]
   >
   >Os indivíduos pertencentes a um segmento que não tem a identidade (namespace) selecionada entre suas diferentes identidades não serão direcionados pela campanha.

1. Configure as datas de início e término da campanha. Por padrão, as Campanhas são configuradas para serem iniciadas manualmente e para terminarem assim que a mensagem for enviada uma vez.

1. Além disso, você pode especificar uma frequência para a execução da ação configurada na campanha.

   <!-- NOTE For API-triggered campaigns, scheduling at a specific date and time with recurrence is not available as action is triggered via API. However, start and end date are relevant to ensure that, if an API call is made prior of after the window, then those get errored.-->

   ![](assets/create-campaign-schedule.png)

<!--1. If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

Quando a campanha estiver pronta, você poderá revisá-la e publicá-la (consulte [Revisar e ativar uma campanha](#review-activate)).

## Revisar e ativar uma campanha {#review-activate}

Após a configuração da campanha, é necessário revisar o parâmetro e o conteúdo antes de ativá-los. Para fazer isso, siga estes passos:

1. Na tela de configuração da campanha, clique em **[!UICONTROL Review to activate]** para exibir um resumo da campanha.

   O resumo permite modificar sua campanha, se necessário, e verificar se algum parâmetro está incorreto ou ausente.

   >[!IMPORTANT]
   >
   >Em caso de erro, você não poderá ativar a campanha. Resolva os erros antes de continuar.

   ![](assets/create-campaign-alerts.png)

1. Verifique se a campanha está configurada corretamente e clique em **[!UICONTROL Activate]**.

   ![](assets/create-campaign-review.png)

1. A campanha agora está ativada e tem a variável **[!UICONTROL Live]** status (ou **[!UICONTROL Scheduled]**  se você especificou uma data de início). [Saiba mais sobre status de campanhas](get-started-with-campaigns.md#statuses). A mensagem configurada na campanha é executada imediatamente ou na data especificada.

   >[!NOTE]
   >
   >O **[!UICONTROL Completed]** é automaticamente atribuído a uma campanha 3 dias após ter sido ativado ou na data final da campanha, se tiver uma execução recorrente.
   >
   >Se nenhuma data final tiver sido especificada, a campanha manterá o status &quot;Ao vivo&quot;. Para alterá-la, você precisa interromper a campanha manualmente. [Saiba como parar uma campanha](modify-stop-campaign.md)

1. Depois que uma campanha é ativada, você pode verificar as informações a qualquer momento abrindo-a. O resumo permite obter estatísticas sobre o número de perfis segmentados e ações entregues e com falha.

   Você também pode obter estatísticas adicionais em relatórios dedicados clicando no botão **[!UICONTROL Reports]** botão. [Saiba mais](../reports/campaign-global-report.md)

   ![](assets/create-campaign-summary.png)
