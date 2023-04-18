---
title: Criar uma notificação no aplicativo
description: Saiba como criar uma mensagem no aplicativo no Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: no aplicativo, mensagem, criação, iniciar
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: 0c32248d13c08a98e9298ddc932aa2e547ab2acd
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 4%

---

# Criação de uma mensagem no aplicativo {#create-in-app}

As mensagens no aplicativo são criadas no contexto de uma campanha.

>[!BEGINTABS]

>[!TAB Adicionar uma mensagem no aplicativo a uma jornada]

>[!AVAILABILITY]
>
>A atividade no aplicativo está disponível atualmente como um beta para selecionar somente usuários. Para participar do programa beta, entre em contato com o Atendimento ao cliente da Adobe.

1. Abra a jornada e arraste e solte uma **[!UICONTROL No aplicativo]** da **[!UICONTROL Ações]** da paleta.

   Quando um perfil atingir o fim de sua jornada, todas as mensagens no aplicativo exibidas a ele expirarão automaticamente. Por esse motivo, uma atividade Wait é adicionada automaticamente após a atividade In-app para garantir o tempo adequado.

   ![](assets/in_app_journey_1.png)

1. Insira um **[!UICONTROL Rótulo]** e **[!UICONTROL Descrição]** para sua mensagem.

1. Escolha a [Superfície do aplicativo](inapp-configuration.md) para usar.

   ![](assets/in_app_journey_2.png)

1. Agora você pode começar a projetar seu conteúdo com a variável **[!UICONTROL Editar conteúdo]** botão. [Saiba mais](design-in-app.md)

1. Clique em **[!UICONTROL Editar acionador]** para configurar o Acionador.

   ![](assets/in_app_journey_4.png)

1. Escolha a frequência do acionador quando a mensagem no aplicativo estiver ativa:

   * **[!UICONTROL Mostrar sempre]**: Sempre mostrar a mensagem quando os eventos selecionados no **[!UICONTROL Acionador do aplicativo móvel]** ocorre.
   * **[!UICONTROL Mostrar uma vez]**: Mostrar esta mensagem somente na primeira vez que os eventos selecionados no **[!UICONTROL Acionador do aplicativo móvel]** ocorre.
   * **[!UICONTROL Mostrar até o click-through]**: Mostrar esta mensagem quando os eventos forem selecionados no **[!UICONTROL Acionador do aplicativo móvel]** ocorre até que um evento de interação seja enviado pelo SDK com uma ação &quot;clicada&quot;.

1. No **[!UICONTROL Acionador do aplicativo móvel]** selecione os eventos e critérios que acionarão sua mensagem:

   1. Na lista suspensa esquerda, selecione o evento necessário para acionar a mensagem.
   1. Na lista suspensa direita, selecione a validação necessária no evento selecionado.
   1. Clique no botão **[!UICONTROL Adicionar]** se desejar que o acionador considere vários eventos ou critérios. Em seguida, repita as etapas acima.
   1. Selecione como seus eventos são vinculados, por exemplo, escolha **[!UICONTROL E]** se desejar **both** aciona como true para que uma mensagem seja exibida ou escolha **[!UICONTROL Ou]** se quiser que a mensagem seja exibida, se **ou** dos acionadores são verdadeiros.
   1. Clique em **[!UICONTROL Salvar]** quando os Triggers tiverem sido configurados.

   ![](assets/in_app_journey_3.png)

1. Se necessário, conclua o fluxo de jornada arrastando e soltando ações ou eventos adicionais. [Saiba mais](../building-journeys/about-journey-activities.md)

1. Quando a mensagem no aplicativo estiver pronta, finalize a configuração e publique a jornada para ativá-la.

Para obter mais informações sobre como configurar uma jornada, consulte [esta página](../building-journeys/journey-gs.md).

>[!TAB Adicionar uma mensagem no aplicativo a uma campanha]

1. Acesse o **[!UICONTROL Campanhas]** , em seguida, clique em **[!UICONTROL Criar campanha]**.

1. No **[!UICONTROL Propriedades]** selecione quando o tipo de execução da campanha: Programado ou acionado por API. Saiba mais sobre os tipos de campanha no [esta página](../campaigns/create-campaign.md#campaigntype).

1. No **[!UICONTROL Ações]** escolha a **[!UICONTROL Mensagem no aplicativo]** e **[!UICONTROL Superfície do aplicativo]** configurado anteriormente para a mensagem no aplicativo. Em seguida, clique em **[!UICONTROL Criar]**.

   Saiba mais sobre a configuração no aplicativo em [esta página](inapp-configuration.md).

   ![](assets/in_app_create_1.png)

1. No **[!UICONTROL Propriedades]** digite o **[!UICONTROL Título]** e **[!UICONTROL Descrição]** descrição.

1. Para atribuir rótulos de uso de dados personalizados ou principais à mensagem no aplicativo, selecione **[!UICONTROL Gerenciar acesso]**. [Saiba mais](../administration/object-based-access.md).

1. Clique no botão **[!UICONTROL Seleção do público-alvo]** para definir o público-alvo a ser direcionado a partir da lista de segmentos disponíveis do Adobe Experience Platform. [Saiba mais](../segment/about-segments.md).

   ![](assets/in_app_create_2.png)

1. No **[!UICONTROL Namespace de identidade]** , escolha o namespace a ser usado para identificar os indivíduos do segmento selecionado. [Saiba mais](../event/about-creating.md#select-the-namespace).

1. Clique em **[!UICONTROL Editar acionadores]** para escolher os eventos e critérios que acionarão sua mensagem:

   1. Clique em **Adicionar condição** se desejar que o acionador considere vários eventos ou critérios.
   1. Selecione como seus eventos são vinculados, por exemplo, escolha **[!UICONTROL E]** se desejar **both** aciona como true para que uma mensagem seja exibida ou escolha **[!UICONTROL Ou]** se quiser que a mensagem seja exibida, se **ou** dos acionadores são verdadeiros.
   1. Clique em **[!UICONTROL Criar grupo]** para agrupar acionadores.

   ![](assets/in_app_create_3.png)

1. Escolha a frequência do acionador quando a mensagem no aplicativo estiver ativa. As opções disponíveis são as seguintes:

   * **[!UICONTROL Todas as vezes]**: Sempre mostrar a mensagem quando os eventos selecionados no **[!UICONTROL Acionador do aplicativo móvel]** ocorre.
   * **[!UICONTROL Uma vez]**: Mostrar esta mensagem somente na primeira vez que os eventos selecionados no **[!UICONTROL Acionador do aplicativo móvel]** ocorre.
   * **[!UICONTROL Até o click-through]**: Mostrar esta mensagem quando os eventos forem selecionados no **[!UICONTROL Acionador do aplicativo móvel]** ocorre até que um evento de interação seja enviado pelo SDK com uma ação &quot;clicada&quot;.
   * **[!UICONTROL X número de vezes]**: Mostrar esta mensagem X hora.

1. Se necessário, escolha qual **[!UICONTROL Dia da semana]** ou **[!UICONTROL Hora do dia]** a mensagem no aplicativo será exibida.

1. As campanhas são projetadas para serem executadas em uma data específica ou em uma frequência recorrente. Saiba como configurar o **[!UICONTROL Agendar]** da sua campanha em [esta seção](../campaigns/create-campaign.md#schedule).

   ![](assets/in-app-schedule.png)

1. Agora você pode começar a projetar seu conteúdo com a variável **[!UICONTROL Editar conteúdo]** botão. [Saiba mais](design-in-app.md)

   ![](assets/in_app_create_4.png)

>[!ENDTABS]

## Vídeo tutorial{#video}

O vídeo abaixo mostra como criar, configurar e publicar mensagens no aplicativo em suas campanhas.

>[!VIDEO](https://video.tv.adobe.com/v/3410430?quality=12&learn=on)


**Tópicos relacionados:**

* [Criar mensagem no aplicativo](design-in-app.md)
* [Teste e envie a mensagem no aplicativo](send-in-app.md)
* [Relatório no aplicativo](../reports/campaign-global-report.md#inapp-report)
* [Configuração no aplicativo](inapp-configuration.md)