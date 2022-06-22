---
title: Criar uma campanha
description: Saiba como criar campanhas no [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: b9fa6bff926eb8cee476fa53feb38ed783e048fc
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 3%

---


# Criar uma campanha {#create-campaign}

>[!NOTE]
>
>Antes de criar uma nova campanha, verifique se você tem uma predefinição de mensagem e um segmento do Adobe Experience Platform pronto para uso. Saiba mais nestas seções:
>
>* [Criar predefinições de mensagem](../configuration/message-presets.md)
>* [Introdução aos segmentos](../segment/about-segments.md)


## Configurar uma campanha {#configure}

As etapas para criar uma campanha são as seguintes:

1. Acesse o **[!UICONTROL Campaigns]** , em seguida, clique em **[!UICONTROL Create campaign]**.

   ![](assets/create-campaign.png)

<!--1. In the **[!UICONTROL Properties]** section, specify when you want to execute the campaign:

    * **[!UICONTROL Scheduled]**: execute the campaign immediately or on a specified date,
    * **[!UICONTROL API-triggered]**: execute the campaign using an API call. In this case, profiles to be targeted and triggers for actions need to be set via the API call.-->

1. No **[!UICONTROL Actions]** escolha o canal e a superfície da mensagem (ou seja, a predefinição de mensagem) a serem usados para enviar a mensagem.

   ![](assets/create-campaign-action.png)

1. Especifique um título e uma descrição para a campanha.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

   ![](assets/create-campaign-properties.png)

1. No **[!UICONTROL Actions]** , configure a mensagem a ser enviada com a campanha:

   1. Clique no botão **[!UICONTROL Edit content]** , em seguida, configure e crie a mensagem. [Saiba como configurar mensagens](../messages/get-started-content.md).

      Quando o conteúdo estiver pronto, clique na seta para voltar à tela de criação da campanha.

      ![](assets/create-campaign-design.png)

   1. No **[!UICONTROL Actions tracking]** , especifique se deseja rastrear como os recipients reagem ao seu delivery.

      Os resultados do rastreamento serão acessíveis no relatório da campanha após a execução da campanha. [Saiba mais sobre relatórios de campanha](campaign-global-report.md)

      ![](assets/create-campaign-action-properties.png)

1. Defina o público-alvo como meta. Para fazer isso, clique no botão **[!UICONTROL Select audience]** para exibir a lista de segmentos disponíveis do Adobe Experience Platform. [Saiba mais sobre segmentos](../segment/about-segments.md)

   ![](assets/create-campaign-audience.png)

   <!--By default, the targeted audience for in-app messages includes all the users of the selected mobile application.-->

   No **[!UICONTROL Identity namespace]** , escolha o namespace a ser usado para identificar os indivíduos do segmento selecionado. [Saiba mais sobre namespaces](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   >[!NOTE]
   >
   >Os indivíduos pertencentes a um segmento que não tem a identidade (namespace) selecionada entre suas diferentes identidades não serão direcionados pela campanha. <!--info vue dans section journeys, read segment-->

   <!--If you are creating a campaign to send an in-app message, you can choose how and when the message will be shown to the audience using existing mobile app triggers.-->
   <!-- where are triggers configured?-->

1. Configure as datas de início e término da campanha.

   Por padrão, as Campanhas são configuradas para serem iniciadas manualmente e para terminarem assim que a mensagem for enviada uma vez.

1. Além disso, é possível configurar uma frequência para a execução da ação configurada na campanha.

   ![](assets/create-campaign-schedule.png)

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

1. A campanha agora está ativada e tem a variável **[!UICONTROL Live]** status (ou **[!UICONTROL Scheduled]**  se você especificou uma data de início). [Saiba mais sobre status de campanhas](get-started-with-campaigns.md#statuses)

   A mensagem configurada na campanha é executada imediatamente ou na data especificada.

   >[!NOTE]
   >
   >Depois que uma campanha é ativada, ela manterá o status &quot;Ao vivo&quot; mesmo após a execução da mensagem. Para alterar seu status, você precisa interrompê-lo manualmente. [Saiba como parar uma campanha](modify-stop-campaign.md)

1. Depois que uma campanha é ativada, você pode verificar as informações a qualquer momento abrindo-a. O resumo permite obter estatísticas sobre o número de perfis segmentados e ações entregues e com falha.

   Você também pode obter estatísticas adicionais em relatórios dedicados clicando no botão **[!UICONTROL Reports]** botão. [Saiba mais](campaign-global-report.md)

   ![](assets/create-campaign-summary.png)

   >[!IMPORTANT]
   >
   >As mensagens criadas em campanhas são específicas para [!DNL Journey Optimizer] recursos da campanha. Uma vez criados, eles serão acessíveis somente em campanhas e não serão exibidos na variável **[!UICONTROL Messages]** menu.