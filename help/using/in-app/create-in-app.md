---
title: Criar uma notificação no aplicativo
description: Saiba como criar uma mensagem no aplicativo no Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: no aplicativo, mensagem, criação, iniciar
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: dc48cc6d95e4af288727961fd9f7761dee4f2552
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 6%

---

# Criação de uma mensagem no aplicativo {#create-in-app}

<!--
>[!BEGINTABS]

>[!TAB Add an In-app message to a journey]

>[!AVAILABILITY]
>
>The In-app activity is currently available as a beta to select users only. To join the beta program, contact Adobe Customer Care.

1. Open your journey, then drag and drop an **[!UICONTROL In-app]** activity from the **[!UICONTROL Actions]** section of the palette.

    When a profile reaches the end of their journey, any in-app messages displayed to them will automatically expire. For that reason, a Wait activity is automatically added after your In-app activity to ensure proper timing.

    ![](assets/in_app_journey_1.png)

1. Enter a **[!UICONTROL Label]** and **[!UICONTROL Description]** for your message.

1. Choose the [In-app surface](inapp-configuration.md) to use.

    ![](assets/in_app_journey_2.png)

1. You can now start designing your content with the **[!UICONTROL Edit content]** button. [Learn more](design-in-app.md)

1. Click **[!UICONTROL Edit trigger]** to configure your Trigger. 

    ![](assets/in_app_journey_4.png)

1. Choose the frequency of your trigger when your In-app message is active:

    * **[!UICONTROL Show every time]**: Always show the message when the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur.
    * **[!UICONTROL Show once]**: Only show this message the first time the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur.
    * **[!UICONTROL Show until click through]**: Show this message when the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur until an interact event is sent by the SDK with an action of "clicked".

1. From the **[!UICONTROL Mobile app trigger]** dropdown(s), choose the event(s) and criteria that will trigger your message:

    1. From the left drop-down, select the event required to trigger the message.
    1. From the right drop-down, select the validation required on the selected event.
    1. Click the **[!UICONTROL Add]** button if you want the trigger to consider multiple events or criteria. Then, repeat the steps above.
    1. Select how your events are linked, e.g. choose **[!UICONTROL And]** if you want **both** triggers to be true in order for a message to be shown or choose **[!UICONTROL Or]** if you want the message to be shown if **either** of the triggers are true.
    1. Click **[!UICONTROL Save]** when your Triggers have been configured.

    ![](assets/in_app_journey_3.png)
    
1. If necessary, complete your journey flow by dragging and dropping additional actions or events. [Learn more](../building-journeys/about-journey-activities.md)

1. Once your In-app message is ready, finalize the configuration and publish your journey to activate it.

For more information on how to configure a journey, refer to [this page](../building-journeys/journey-gs.md).

>[!TAB Add an In-app message to a campaign]
-->

1. Acesse o **[!UICONTROL Campanhas]** e clique em **[!UICONTROL Criar campanha]**.

1. No **[!UICONTROL Propriedades]** selecione quando o tipo de execução da campanha: Scheduled ou API-trigger. Saiba mais sobre tipos de campanha no [esta página](../campaigns/create-campaign.md#campaigntype).

1. No **[!UICONTROL Ações]** escolha a opção **[!UICONTROL Mensagem no aplicativo]** e a variável **[!UICONTROL Superfície do aplicativo]** previamente configurada para sua mensagem no aplicativo. Em seguida, clique em **[!UICONTROL Criar]**.

   Saiba mais sobre Configuração no aplicativo em [esta página](inapp-configuration.md).

   ![](assets/in_app_create_1.png)

1. No **[!UICONTROL Propriedades]** , insira o **[!UICONTROL Título]** e a variável **[!UICONTROL Descrição]** descrição.

1. Para atribuir rótulos de uso de dados personalizados ou principais à mensagem no aplicativo, selecione **[!UICONTROL Gerenciar acesso]**. [Saiba mais](../administration/object-based-access.md).

1. Clique em **[!UICONTROL Selecionar público]** botão para definir o público-alvo a ser direcionado na lista de segmentos disponíveis do Adobe Experience Platform. [Saiba mais](../segment/about-segments.md).

   ![](assets/in_app_create_2.png)

1. No **[!UICONTROL Namespace de identidade]** escolha o namespace a ser usado para identificar os indivíduos do segmento selecionado. [Saiba mais](../event/about-creating.md#select-the-namespace).

1. Clique em **[!UICONTROL Criar experimento]** para começar a configurar seu experimento de conteúdo e criar tratamentos para medir seu desempenho e identificar a melhor opção para seu público-alvo. [Saiba mais](../campaigns/content-experiment.md)

1. Clique em **[!UICONTROL Editar acionadores]** para escolher os eventos e critérios que acionarão sua mensagem:

   1. Clique em **Adicionar condição** se desejar que o acionador considere vários eventos ou critérios.
   1. Selecione como seus eventos são vinculados, por exemplo, escolha **[!UICONTROL E]** se desejar **ambos** será verdadeiro para que uma mensagem seja exibida ou escolha **[!UICONTROL Ou]** se quiser que a mensagem seja exibida se **ou** dos acionadores são verdadeiros.
   1. Clique em **[!UICONTROL Criar grupo]** para agrupar acionadores.

   ![](assets/in_app_create_3.png)

1. Escolha a frequência do acionador quando a mensagem no aplicativo estiver ativa. As opções disponíveis são as seguintes:

   * **[!UICONTROL Todas as vezes]**: sempre mostrar a mensagem quando os eventos selecionados no **[!UICONTROL Acionador do aplicativo móvel]** lista suspensa.
   * **[!UICONTROL Uma vez]**: mostrar esta mensagem somente na primeira vez que os eventos forem selecionados na **[!UICONTROL Acionador do aplicativo móvel]** lista suspensa.
   * **[!UICONTROL Até o click-through]**: mostrar esta mensagem quando os eventos selecionados no **[!UICONTROL Acionador do aplicativo móvel]** As listas suspensas ocorrem até que um evento de interação seja enviado pelo SDK com uma ação de &quot;clicado&quot;.
   * **[!UICONTROL X número de vezes]**: Mostrar esta mensagem X vez.

1. Se necessário, escolha qual **[!UICONTROL Dia da semana]** ou **[!UICONTROL Hora do dia]** a mensagem no aplicativo será exibida.

1. As campanhas são projetadas para serem executadas em uma data específica ou em uma frequência recorrente. Saiba como configurar o **[!UICONTROL Agendar]** da sua campanha no [nesta seção](../campaigns/create-campaign.md#schedule).

   ![](assets/in-app-schedule.png)

1. Agora é possível começar a projetar o conteúdo com o **[!UICONTROL Editar conteúdo]** botão. [Saiba mais](design-in-app.md)

   ![](assets/in_app_create_4.png)

<!--
>[!ENDTABS]
-->

## Vídeos tutoriais{#video}

O vídeo abaixo mostra como criar, configurar e publicar mensagens no aplicativo em suas campanhas.

>[!VIDEO](https://video.tv.adobe.com/v/3410430?quality=12&learn=on)

O vídeo abaixo mostra como configurar e analisar experimentos de conteúdo para testar mensagens no aplicativo A/B.

>[!VIDEO](https://video.tv.adobe.com/v/3419898)

**Tópicos relacionados:**

* [Criar mensagem no aplicativo](design-in-app.md)
* [Teste e envie sua mensagem no aplicativo](send-in-app.md)
* [Relatório no aplicativo](../reports/campaign-global-report.md#inapp-report)
* [Configuração no aplicativo](inapp-configuration.md)