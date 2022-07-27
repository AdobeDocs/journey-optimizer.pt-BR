---
title: Criar uma campanha
description: Saiba como criar campanhas no [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 7c4afc98-0d79-4e26-90f8-558bac037169
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 5%

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

1. No **[!UICONTROL Properties]** , especifique quando deseja executar a campanha:

   * **[!UICONTROL Scheduled]**: execute a campanha imediatamente ou em uma data especificada. As campanhas programadas têm como objetivo enviar **marketing** digite mensagens.
   * **[!UICONTROL API-triggered]**: execute a campanha usando uma chamada de API . As campanhas acionadas por API são destinadas ao envio de **transacional** mensagens, ou seja, mensagens enviadas após uma ação executada por um indivíduo: redefinição de senha, abandono de cartão etc. [Saiba como acionar uma campanha usando APIs](api-triggered-campaigns.md)

1. No **[!UICONTROL Actions]** escolha o canal e a superfície do canal a serem usados para enviar a mensagem e clique em **[!UICONTROL Create]**.

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >Somente superfícies de canal compatíveis com o tipo de campanha (marketing ou transacional) são listadas na lista suspensa.

1. Especifique um título e uma descrição para a campanha.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. No **[!UICONTROL Actions]** , configure a mensagem a ser enviada com a campanha:

   1. Clique no botão **[!UICONTROL Edit content]** , em seguida, configure e crie o conteúdo da mensagem. [Saiba mais sobre mensagens](../messages/get-started-content.md).

      Quando o conteúdo estiver pronto, clique na seta para voltar à tela de criação da campanha.

      ![](assets/create-campaign-design.png)

   1. No **[!UICONTROL Actions tracking]** , especifique se deseja rastrear como os recipients reagem ao seu delivery.

      Os resultados do rastreamento serão acessíveis no relatório da campanha após a execução da campanha. [Saiba mais sobre relatórios de campanha](campaign-global-report.md)

1. Defina o público-alvo como meta. Para fazer isso, clique no botão **[!UICONTROL Select audience]** para exibir a lista de segmentos disponíveis do Adobe Experience Platform. [Saiba mais sobre segmentos](../segment/about-segments.md)

   >[!NOTE]
   >
   >Para campanhas acionadas por API, o público-alvo precisa ser definido por meio de uma chamada de API. [Saiba mais](api-triggered-campaigns.md)

   No **[!UICONTROL Identity namespace]** , escolha o namespace a ser usado para identificar os indivíduos do segmento selecionado. [Saiba mais sobre namespaces](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   >[!NOTE]
   >
   >Os indivíduos pertencentes a um segmento que não tem a identidade (namespace) selecionada entre suas diferentes identidades não serão direcionados pela campanha.

1. Configure as datas de início e término da campanha. Por padrão, as Campanhas são configuradas para serem iniciadas manualmente e para terminarem assim que a mensagem for enviada uma vez.

1. Além disso, você pode especificar uma frequência para a execução da ação configurada na campanha.

   >[!NOTE]
   >
   >Para campanhas acionadas por API, a programação em uma data e hora específica com recorrência não está disponível, pois a ação é acionada por meio da API. No entanto, as datas de início e de término são relevantes para garantir que, se uma chamada de API for feita antes da janela , elas serão erradas.

   ![](assets/create-campaign-schedule.png)

1. Se você estiver criando uma campanha acionada por API, a variável **[!UICONTROL cURL request]** permite recuperar a variável **[!UICONTROL Campaign ID]** para usar na chamada da API . [Saiba mais](api-triggered-campaigns.md)

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

## Recursos adicionais

* [Introdução às campanhas](get-started-with-campaigns.md)
* [Criar campanhas acionadas por API](api-triggered-campaigns.md)
* [Modificar ou interromper uma campanha](modify-stop-campaign.md)
* [Relatório em tempo real da campanha](campaign-live-report.md)
* [Relatório global da campanha](campaign-global-report.md)
