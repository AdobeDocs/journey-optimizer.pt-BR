---
solution: Journey Optimizer
product: journey optimizer
title: Criar uma notificação por push
description: Saiba como criar uma notificação por push no Journey Optimizer
feature: Push
topic: Content Management
role: User
level: Beginner
exl-id: 6f6d693d-11f2-48b7-82a8-171829bf8045
source-git-commit: 083545ff7b2dc5ce45ef3766321fdf12e1b96c5c
workflow-type: tm+mt
source-wordcount: '1831'
ht-degree: 13%

---

# Criar uma notificação por push {#design-push-notification}

Depois de criar uma notificação por push, você pode projetar o conteúdo para plataformas iOS e Android. Esta página orienta você na redação da mensagem, configuração do comportamento ao clicar, adição de mídia e botões e configuração de opções avançadas para criar notificações por push envolventes que repercutem com seu público-alvo.

## Título e corpo {#push-title-body}

>[!CONTEXTUALHELP]
>id="ajo-message-push-compose"
>title="Personalizar a notificação por push."
>abstract="Para compor a mensagem, insira o conteúdo nos campos **Título** e **Corpo**. Para incluir tokens de personalização, abra a caixa de diálogo de personalização."

![](assets/title-body.png)

Para redigir a mensagem, clique nos campos **[!UICONTROL Título]** e **[!UICONTROL Corpo]**. Use o editor de personalização para definir conteúdo, personalizar dados e adicionar conteúdo dinâmico. Saiba mais sobre [personalização](../personalization/personalize.md) e [conteúdo dinâmico](../personalization/get-started-dynamic-content.md) no editor de personalização.

Use a seção de visualização de dispositivo para visualizar como a notificação por push é exibida no iOS e no Android.

Acelere sua criação de conteúdo com o AI Assistant e gere textos convincentes de notificação por push com o [AI Assistant para geração de texto](../content-management/generative-text.md) ou crie notificações por push completas com o [AI Assistant para geração de conteúdo completa](../content-management/generative-full-content.md).

## Comportamento ao clicar {#on-click-behavior}

>[!CONTEXTUALHELP]
>id="ajo-message-push-onclick"
>title="Sobre o comportamento ao clicar"
>abstract="Selecione o comportamento quando um recipient clicar no corpo da notificação por push."

Configure a ação que ocorre quando os destinatários tocam no corpo da notificação por push. Escolha entre as seguintes opções:

![](assets/title-body-push.png)

* **[!UICONTROL Abrir aplicativo]**: inicia o aplicativo associado à notificação. O aplicativo é especificado na sua [configuração de canal](../configuration/channel-surfaces.md) (ou seja, predefinição de mensagem).
* **[!UICONTROL Deeplink]**: direciona os usuários para conteúdo específico no seu aplicativo, como uma exibição, seção de página ou guia específica. Insira o URL do deep link no campo fornecido.
* **[!UICONTROL URL da Web]**: direciona os usuários para uma página da Web externa. Insira o URL de destino no campo fornecido.

## Adicionar mídia {#add-media-push}

>[!CONTEXTUALHELP]
>id="ajo-message-push-media"
>title="Adicionar mídias à notificação por push"
>abstract="É possível adicionar uma imagem, um vídeo ou um GIF que será exibido na notificação."

Aprimore sua notificação por push adicionando mídia visual. Os tipos de mídia disponíveis e os métodos de implementação variam de acordo com o sistema operacional, conforme detalhado nas guias abaixo.

>[!BEGINTABS]

>[!TAB Android]

Para o Android, você só pode adicionar um ícone de imagem e uma imagem para notificações expandidas.

![](assets/push-config-add-media.png)

Você pode adicionar mídia usando um dos seguintes métodos:

* Botão **[!UICONTROL Adicionar mídia]**: Selecione um ativo do [Adobe Experience Manager Assets](../integrations/assets.md) ou acesse o Assistente de IA para gerar [imagens envolventes](../content-management/generative-image.md) para notificações por push.

* Campo **[!UICONTROL Adicionar mídia]**: insira a URL da mídia diretamente. Você pode incluir tokens de personalização no URL.

Depois de adicionada, a mídia é exibida à direita do corpo de notificação.

>[!NOTE]
>
>Ao incluir anexos de mídia na carga de notificação por push (como imagens em campos de dados personalizados como `adb_media`), seu aplicativo móvel deve implementar um tratamento específico do lado do cliente para que as imagens sejam renderizadas em dispositivos. Seu aplicativo deve implementar o [fluxo de trabalho automático de exibição e rastreamento](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/push-notification/android/automatic-display-and-tracking/){target="_blank"} para lidar com anexos de imagem da carga.

>[!TAB iOS]

Para o iOS, você pode adicionar uma imagem, vídeo ou GIF para exibir na notificação.

![](assets/push-config-add-media-ios.png)

Você pode adicionar mídia usando um dos seguintes métodos:

* Botão **[!UICONTROL Adicionar mídia]**: Selecione um ativo de **[!DNL Adobe Experience Manager Assets]**. Saiba mais sobre como usar o **[!DNL Adobe Experience Manager Assets]** em [esta página](../integrations/assets.md).

* Campo **[!UICONTROL Adicionar mídia]**: insira a URL da mídia diretamente. Você pode incluir tokens de personalização no URL.

Depois de adicionada, a mídia é exibida à direita do corpo de notificação.

>[!NOTE]
>
>Ao incluir anexos de mídia na carga de notificação por push (como imagens em campos de dados personalizados como `adb_media`), seu aplicativo móvel deve implementar um tratamento específico do lado do cliente para que as imagens sejam renderizadas em dispositivos. Seu aplicativo deve implementar uma [Extensão de Serviço de Notificação](https://developer.apple.com/documentation/usernotifications/modifying_content_in_newly_delivered_notifications){target="_blank"} para baixar e processar conteúdo de mídia da carga. Além disso, a opção **[!UICONTROL Adicionar sinalizador de conteúdo mutável]** deve ser habilitada na seção [Opções avançadas](#advanced-options-push).

<!--
>[!TAB Web]

Enter the media URL in the **[!UICONTROL Add media]** field. You can also include personalization tokens in the URL to customize the content for each user.

Click ![Edit text with the AI assistant](assets/do-not-localize/Smock_ImageAdd_18_N.svg) to quickly generate media using the Journey Optimizer AI Assistant.

![](assets/web-media.png)
-->

>[!ENDTABS]

## Adicionar botões {#add-buttons-push}

>[!CONTEXTUALHELP]
>id="ajo-message-push-buttons"
>title="Adicione botões para a interação com a notificação por push."
>abstract="Nesta seção, adicione botões de chamada para ação à mensagem. Para Apple iOS, especifique um identificador de categoria de notificação. Para Google Android, é possível incluir texto e destinos personalizados para cada botão."

Crie uma notificação acionável adicionando botões ao seu conteúdo de push. Navegue pelas guias a seguir com base em seu sistema operacional.

Se a tela do dispositivo estiver bloqueada, esses botões não serão exibidos: somente então o **Título** e a **Mensagem** da notificação estarão visíveis. Se o dispositivo estiver desbloqueado, os recipients verão os botões.

>[!BEGINTABS]

>[!TAB Android]

Para o Android, você pode adicionar até três botões.

1. Use o **[!UICONTROL Botão Adicionar]** para definir as configurações: o rótulo e a ação associada. As ações possíveis são as mesmas de [comportamento ao clicar](#on-click-behavior).

   ![](assets/push_buttons.png)

1. Use o ícone **[!UICONTROL Expandir exibição]** sob a imagem de visualização central para visualizar seus botões personalizados.

>[!TAB iOS]

![](assets/push_buttons-ios.png)

Para o iOS, é especificado um identificador de categoria de notificação. As categorias de notificação precisam ser pré-configuradas no aplicativo iOS, que definirá os botões a serem exibidos e as ações executadas. Consulte a [documentação do Apple](https://developer.apple.com/documentation/usernotifications/declaring_your_actionable_notification_types) para obter mais detalhes.

<!--
>[!TAB Web]

![](assets/push_buttons-web.png)

Use the **[!UICONTROL Add Button]** option to define each button's label and associated action, as detailed below:

* **[!UICONTROL Deeplink]**: Redirect users to a specific view, section, or tab within your app. Enter the deeplink URL in the associated field.

* **[!UICONTROL Web URL]**: Redirect users to an external webpage. Enter the URL in the associated field.
-->

>[!ENDTABS]

## Enviar uma notificação silenciosa {#silent-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push_silent_notification"
>title="Sobre notificação silenciosa"
>abstract="Enviar notificações sem perturbar o usuário. As notificações não são mostradas no centro de notificações ou na barra de notificação."

<!--
>[!AVAILABILITY]
>
>Web push notifications in Journey Optimizer do not support the **Silent Notification** feature.
-->

Uma notificação por push silenciosa (ou notificação em segundo plano) é uma instrução oculta entregue ao aplicativo. Ele é usado, por exemplo, para notificar seu aplicativo sobre a disponibilidade de novo conteúdo ou iniciar um download em segundo plano.

Selecione a opção **[!UICONTROL Notificação silenciosa]** para notificar silenciosamente o aplicativo: nesse caso, a notificação é transferida diretamente para o aplicativo. Nenhum alerta é exibido na tela do dispositivo.

Use a seção **[!UICONTROL Dados personalizados]** para adicionar pares de valor chave.

## Dados personalizados {#custom-data}

>[!CONTEXTUALHELP]
>id="ajo-message-push-custom"
>title="Configurar dados personalizados para a notificação por push."
>abstract="Adicione variáveis personalizadas ao conteúdo, dependendo da configuração do aplicativo móvel."

Na seção **[!UICONTROL Dados personalizados]**, você pode adicionar variáveis personalizadas à carga, dependendo da configuração do seu aplicativo móvel. Para obter mais informações sobre como configurar notificações por push no Adobe Experience Platform, consulte [esta seção](push-gs.md)

## Personalizar com o Experience Decisioning {#decisioning-push}

Você pode personalizar e otimizar o conteúdo de suas notificações por push com o **Experience Decisioning**. Esse recurso permite usar Pontuações de prioridade, Fórmulas ou Modelos de IA para selecionar e exibir dinamicamente o melhor conteúdo para seus clientes.

Para obter mais informações sobre como criar e usar políticas de decisão em notificações por push, consulte [esta seção](../experience-decisioning/create-decision.md).

## Opções avançadas {#advanced-options-push}

>[!CONTEXTUALHELP]
>id="ajo-message-push-advanced"
>title="Configurar opções avançadas para a notificação por push."
>abstract="Esta seção permite aprimorar a personalização da notificação por push."

Você pode configurar **[!UICONTROL opções avançadas]** para sua notificação por push. Os parâmetros disponíveis estão listados abaixo:

| Parâmetro | Descrição |
|---------|---------|
| **[!UICONTROL Recolhível]** (iOS / Android) | Uma mensagem recolhível é uma mensagem que pode ser substituída por uma nova mensagem se ela se tornar desatualizada. Casos de uso comuns de mensagens recolhíveis são mensagens usadas para informar um aplicativo móvel para sincronizar dados do servidor. Um exemplo seria um aplicativo de esportes que atualiza os usuários com a pontuação mais recente. Somente a mensagem mais recente é relevante. Por outro lado, com mensagens não recolhíveis, cada mensagem é importante para o aplicativo cliente e precisa ser entregue. |
| **[!UICONTROL Som personalizado]** (iOS/Android) | O som a ser reproduzido pelo terminal móvel quando a notificação for recebida. O som precisa ser incluído no aplicativo. |
| **[!UICONTROL Medalhas]** (iOS/Android) | Um selo é usado para exibir diretamente no ícone do aplicativo o número de novas informações não lidas. <br/>O valor do selo desaparecerá assim que o usuário abrir ou ler o novo conteúdo do aplicativo. Quando uma notificação é recebida em um dispositivo, ela pode atualizar ou adicionar um valor de selo para o aplicativo relacionado.<br/>Por exemplo, se estiver armazenando o número de artigos não lidos dos clientes, você poderá aproveitar a personalização para enviar o valor exclusivo do selo de artigos não lidos para cada cliente. Para mais personalizações, consulte [esta seção](../personalization/personalize.md). |
| **[!UICONTROL Grupo de notificação]** (somente iOS) | Associe um grupo de notificação à notificação por push.<br/>A partir do iOS 12, os grupos de notificação permitem consolidar threads de mensagens e tópicos de notificação em IDs de thread. Por exemplo, uma marca pode enviar notificações de marketing em uma ID de grupo, enquanto mantém mais notificações de tipo operacional em uma ou mais IDs diferentes.<br/>Para ilustrar isso, você pode ter grupos de notificações groupID: 123 &quot;confira a nova coleção de primavera de blusas&quot; e groupID: 456 &quot;seu pacote foi entregue&quot;. Neste exemplo, todas as notificações de delivery seriam agrupadas na ID de grupo: 456. |
| **[!UICONTROL Canal de notificação]** (somente Android) | Associe um canal de notificação à notificação por push.<br/>A partir do Android 8.0 (nível de API 26), todas as notificações devem ser atribuídas a um canal para serem exibidas. Para obter mais informações, consulte a [documentação para desenvolvedores do Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels). |
| **[!UICONTROL Adicionar sinalizador de disponibilidade de conteúdo]** (somente iOS) | Envia o sinalizador de conteúdo disponível na carga de push para garantir que o aplicativo seja reativado assim que receber a notificação por push, o que significa que o aplicativo poderá acessar os dados da carga.<br/> Isso funciona mesmo se o aplicativo estiver sendo executado em segundo plano e sem precisar de nenhuma interação do usuário (por exemplo, ao tocar na notificação por push). No entanto, isso não se aplica se o aplicativo não estiver em execução. Para obter mais informações, consulte a [documentação para desenvolvedores da Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html). |
| **[!UICONTROL Adicionar sinalizador de conteúdo mutável]** (somente iOS) | Envia o sinalizador de conteúdo mutável no payload por push e permitirá que o conteúdo da notificação por push seja modificado por uma extensão de aplicativo de serviço de notificação fornecida no iOS SDK. Para saber mais, consulte a [documentação para desenvolvedores da Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html).<br/>Você poderá aproveitar suas extensões de aplicativo móvel para modificar ainda mais o conteúdo ou a apresentação das notificações por push de entrada enviadas de [!DNL Journey Optimizer]. Por exemplo, os usuários podem aproveitar essa opção para descriptografar dados, alterar o texto do corpo ou do título de uma notificação, adicionar um identificador de thread a uma notificação etc.<br/>**Importante**: esse sinalizador deve ser habilitado ao incluir anexos de mídia (imagens, vídeos) por meio de campos de carga (como `adb_media`) para que eles sejam renderizados em dispositivos iOS. Seu aplicativo também deve implementar uma Extensão de Serviço de Notificação para baixar e processar o conteúdo de mídia da carga. |
| **[!UICONTROL Adicionar expiração de push]** (somente iOS) | Escolha a **Data e hora** da expiração de push. No iOS, a expiração da notificação é imposta como uma parada permanente, o que significa que qualquer mensagem que chegue ao Apple Push Notification Service (APNS) após a hora de expiração não é entregue, garantindo que os clientes nunca recebam notificações desatualizadas ou irrelevantes. Para obter mais informações, consulte a [documentação para desenvolvedores da Apple](https://developer.apple.com/documentation/usernotifications/sending-notification-requests-to-apns). |
| **[!UICONTROL Visibilidade de notificação]** (somente Android) | Define a visibilidade da notificação por push. <br/><b>Particular</b> mostrará a notificação em todas as telas de bloqueio, mas ocultará informações confidenciais ou privadas nas telas de bloqueio seguras. <br/><b>Public</b> mostrará a notificação em sua totalidade em todas as telas de bloqueio. <br/><b>Segredo</b> não revelará nenhuma parte da notificação em uma tela de bloqueio segura. <br/>Para obter mais informações, consulte a [documentação para desenvolvedores do Android](https://developer.android.com/reference/android/app/Notification). |
| **[!UICONTROL Prioridade de notificação]** (somente Android) | Define a importância da notificação por push de Baixo para Máximo. Isso determina o quão &quot;intrusiva&quot; será a notificação por push quando for entregue. Para obter mais informações, consulte a [documentação para desenvolvedores do Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL Prioridade de entrega]** (somente Android) | Configura uma prioridade alta ou normal para suas notificações por push. Para obter mais informações sobre a prioridade da mensagem, consulte a [documentação para desenvolvedor do Google](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message). |
| **[!UICONTROL Tempo de vida]** (somente Android) | Defina o número de segundos após os quais sua mensagem expirará. No Android, a expiração é tratada como uma janela de entrega: o Firebase Cloud Messaging (FCM) converte o tempo de expiração em um valor de TTL (time-to-live), começando quando a mensagem é recebida, o que significa que as campanhas não entregues podem ser enviadas depois do esperado ou até mesmo fora do período desejado. Para obter mais informações, consulte a [documentação para desenvolvedores do Android](https://firebase.google.com/docs/cloud-messaging/concept-options#ttl). |
