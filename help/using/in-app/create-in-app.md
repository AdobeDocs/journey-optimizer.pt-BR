---
title: Criar uma notificação no aplicativo
description: Saiba como criar uma mensagem no aplicativo no Journey Otimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 0%

---

# Criar uma mensagem no aplicativo {#create-in-app}

## Criar uma campanha e uma mensagem no aplicativo{#create-in-app-in-a-campaign}

Para criar uma mensagem no aplicativo, siga as etapas abaixo:

1. Acesse o **[!UICONTROL Campaigns]** , em seguida, clique em **[!UICONTROL Create campaign]**.

1. No **[!UICONTROL Properties]** especifique quando deseja executar a campanha.

1. No **[!UICONTROL Actions]** escolha a **[!UICONTROL In-app message]** e **[!UICONTROL App surface]** configurado anteriormente para a mensagem no aplicativo. Em seguida, clique em **[!UICONTROL Create]**.

   [Saiba mais sobre a configuração no aplicativo](inapp-configuration.md).

   ![](assets/in_app_create_1.png)

1. No **[!UICONTROL Properties]** edite o **[!UICONTROL Title]** e **[!UICONTROL Description]**.

1. Para atribuir rótulos de uso de dados personalizados ou principais à página inicial, selecione **[!UICONTROL Manage access]**. [Saiba mais](../administration/object-based-access.md).

1. Clique no botão **[!UICONTROL Select audience]** para definir o público-alvo a ser direcionado a partir da lista de segmentos disponíveis da Adobe Experience Platform. [Saiba mais](../segment/about-segments.md).

   ![](assets/in_app_create_2.png)

1. No **[!UICONTROL Identity namespace]** , escolha o namespace a ser usado para identificar os indivíduos do segmento selecionado. [Saiba mais](../event/about-creating.md#select-the-namespace).

1. Escolha a frequência do acionador quando a mensagem no aplicativo estiver ativa:

   * **[!UICONTROL Show every time]**: Sempre mostrar a mensagem quando os eventos selecionados no **[!UICONTROL Mobile app trigger]** ocorre.
   * **[!UICONTROL Show once]**: Mostrar esta mensagem somente na primeira vez que os eventos selecionados no **[!UICONTROL Mobile app trigger]** ocorre.
   * **[!UICONTROL Show until click through]**: Mostrar esta mensagem quando os eventos forem selecionados no **[!UICONTROL Mobile app trigger]** ocorre até que um evento de interação seja enviado pelo SDK com uma ação &quot;clicada&quot;.

1. No **[!UICONTROL Mobile app trigger]** selecione os eventos e critérios que acionarão sua mensagem:

   1. Na lista suspensa esquerda, selecione o evento necessário para acionar a mensagem.
   1. Na lista suspensa direita, selecione a validação necessária no evento selecionado.
   1. Clique no botão **[!UICONTROL Add]** se desejar que o acionador considere vários eventos ou critérios. Em seguida, repita as etapas acima.
   1. Selecione como seus eventos são vinculados, por exemplo, escolha **[!UICONTROL And]** se desejar **both** aciona como true para que uma mensagem seja exibida ou escolha **[!UICONTROL Or]** se quiser que a mensagem seja exibida, se **ou** dos acionadores são verdadeiros.

   ![](assets/in_app_create_3.png)

1. Escolha o evento que aciona sua mensagem do **[!UICONTROL Mobile app trigger]**
lista suspensa.

   Ao escolher um acionador, você escolhe qual ação do usuário faz com que a mensagem no aplicativo seja exibida.

   ![](assets/in_app_create_3.png)

1. As campanhas são projetadas para serem executadas em uma data específica ou em uma frequência recorrente. Saiba como configurar o **[!UICONTROL Schedule]** da sua campanha em [esta seção](../campaigns/create-campaign.md#schedule).

   ![](assets/in-app-schedule.png)

1. Agora você pode começar a projetar seu conteúdo com a variável **[!UICONTROL Edit content]** botão.

   ![](assets/in_app_create_4.png)

## Enviar mensagens no aplicativo{#in-app-send}

### Visualizar no dispositivo {#preview-device}

Você pode visualizar a notificação no aplicativo em um dispositivo específico.

1. Clique em **[!UICONTROL Preview on device]**.

   ![](assets/in_app_create_6.png)

1. No **[!UICONTROL Connect to device]** , clique em **[!UICONTROL Start]**.

1. Digite no **[!UICONTROL Base URL]** do seu aplicativo e clique em **[!UICONTROL Next]**.

   ![](assets/in_app_create_7.png)

1. Verifique o código QR com seu dispositivo e insira o código PIN exibido.

A mensagem no aplicativo agora pode ser acionada diretamente no dispositivo, permitindo que você visualize e revise a mensagem em um dispositivo real.

### Revisar e ativar sua notificação no aplicativo{#in-app-review}

Depois que a mensagem no aplicativo é criada e o conteúdo é definido e personalizado, é possível revisá-la e ativá-la.

Para fazer isso, siga as etapas abaixo:

1. Use o **[!UICONTROL Review to activate]** para exibir um resumo da mensagem.

   O resumo permite modificar sua campanha, se necessário, e verificar se algum parâmetro está incorreto ou ausente.

   ![](assets/in_app_create_5.png)

1. Verifique se a campanha está configurada corretamente e clique em **[!UICONTROL Activate]**.

Sua campanha agora está ativada. A notificação no aplicativo configurada na campanha é enviada imediatamente ou na data especificada.

Depois de enviado, você pode medir o impacto de suas mensagens no aplicativo no relatório de Campanha. Para obter mais informações, consulte [esta seção](inapp-report.md).

**Tópicos relacionados:**

* [Criar mensagem no aplicativo](design-in-app.md)
* [Relatório no aplicativo](inapp-report.md)
* [Configuração no aplicativo](inapp-configuration.md)
