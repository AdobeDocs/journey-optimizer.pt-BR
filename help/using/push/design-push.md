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
source-git-commit: ccfc0870a8d59d16c7f5b6b02856785aa28dd307
workflow-type: tm+mt
source-wordcount: '1365'
ht-degree: 17%

---

# Criar uma notificação por push {#design-push-notification}

## Título e corpo {#push-title-body}

>[!CONTEXTUALHELP]
>id="ajo-message-push-compose"
>title="Personalizar a notificação por push."
>abstract="Para compor a mensagem, insira o conteúdo nos campos Título e Corpo. Para incluir tokens de personalização, abra a caixa de diálogo de personalização."

Para redigir a mensagem, clique nos campos **[!UICONTROL Título]** e **[!UICONTROL Corpo]**. Use o editor de personalização para definir conteúdo, personalizar dados e adicionar conteúdo dinâmico. Saiba mais sobre [personalização](../personalization/personalize.md) e [conteúdo dinâmico](../personalization/get-started-dynamic-content.md) no editor de personalização.

Use a seção de visualização de dispositivo para visualizar como a notificação por push é exibida em dispositivos iOS e Android.

## Comportamento ao clicar {#on-click-behavior}

>[!CONTEXTUALHELP]
>id="ajo-message-push-onclick"
>title="Sobre o comportamento ao clicar"
>abstract="Selecione o comportamento quando um recipient clicar no corpo da notificação por push."

Você pode selecionar o comportamento quando um usuário clicar no corpo da notificação por push.

![](assets/title-body-push.png)

* Para abrir o aplicativo, selecione a opção **[!UICONTROL Abrir aplicativo]**. O aplicativo associado à notificação é definido na [configuração de canal](../configuration/channel-surfaces.md) (ou seja, predefinição de mensagem).
* Para redirecionar o usuário para um conteúdo específico em um aplicativo, selecione a opção **[!UICONTROL Deeplink]**.  O conteúdo específico pode ser uma exibição específica, uma seção específica de uma página ou uma determinada guia. Depois que a opção for selecionada, insira o deep link no campo associado.
* Para redirecionar o usuário para uma URL externa, use a opção **[!UICONTROL URL da Web]**. Depois que a opção for selecionada, insira o URL no campo associado.

## Adicionar mídia {#add-media-push}

>[!CONTEXTUALHELP]
>id="ajo-message-push-media"
>title="Adicionar mídias à notificação por push"
>abstract="É possível adicionar uma imagem, um vídeo ou um GIF que será exibido na notificação."

Na versão para iOS da sua notificação por push, você pode adicionar uma imagem, um vídeo ou um GIF que são exibidos na sua notificação.

Na versão do Android, só é possível adicionar um ícone de imagem e uma imagem para notificações expandidas.

![](assets/push-config-add-media.png)

Duas opções estão disponíveis. É possível:

* Use o botão **[!UICONTROL Adicionar mídia]** para selecionar um ativo em **[!DNL Adobe Experience Manager Assets]**.

  Saiba como usar **[!DNL Adobe Experience Manager Assets]** em [esta página](../integrations/assets.md).

* Ou insira a URL da mídia no campo **[!UICONTROL Adicionar mídia]**. Nesse caso, você pode adicionar personalização ao URL.

Depois de adicionada, a mídia é exibida à direita do corpo de notificação.

## Adicionar botões {#add-buttons-push}

>[!CONTEXTUALHELP]
>id="ajo-message-push-buttons"
>title="Adicione botões para a interação com a notificação por push."
>abstract="Esta seção permite adicionar botões de “chamada para ação” à mensagem. Para iOS, especifique um identificador de categoria de notificação. Para Android, é possível incluir texto e destinos personalizados para cada botão."

Crie uma notificação acionável adicionando botões ao seu conteúdo de push.

Se a tela do dispositivo estiver bloqueada, esses botões não serão exibidos: somente o **Título** e a **Mensagem** da notificação estarão visíveis. Se o dispositivo estiver desbloqueado, os recipients verão os botões.

Na versão do Android, é possível adicionar até três botões.

Na versão do iOS, um identificador de categoria de notificação é especificado. As categorias de notificação precisam ser pré-configuradas no aplicativo iOS, que definirá os botões a serem exibidos e as ações executadas. Consulte a [documentação do Apple](https://developer.apple.com/documentation/usernotifications/declaring_your_actionable_notification_types) para obter mais detalhes.

1. Use o **[!UICONTROL Botão Adicionar]** para definir as configurações: o rótulo e a ação associada. As ações possíveis são as mesmas de [comportamento ao clicar](#on-click-behavior).

1. Use o ícone **[!UICONTROL Expandir exibição]** sob a imagem de visualização central para visualizar seus botões personalizados.

   ![](assets/push_buttons.png)

## Enviar uma notificação silenciosa {#silent-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push_silent_notification"
>title="Sobre notificação silenciosa"
>abstract="Enviar notificações sem perturbar o usuário. As notificações não são mostradas no centro de notificações ou na barra de notificação."

Uma notificação por push silenciosa (ou notificação em segundo plano) é uma instrução oculta entregue ao aplicativo. Ele é usado, por exemplo, para notificar seu aplicativo sobre a disponibilidade de novo conteúdo ou iniciar um download em segundo plano.

Selecione a opção **[!UICONTROL Notificação silenciosa]** para notificar silenciosamente o aplicativo: nesse caso, a notificação é transferida diretamente para o aplicativo. Nenhum alerta é exibido na tela do dispositivo.

Use a seção **[!UICONTROL Dados personalizados]** para adicionar pares de valor chave.

## Dados personalizados {#custom-data}

>[!CONTEXTUALHELP]
>id="ajo-message-push-custom"
>title="Configurar dados personalizados para a notificação por push."
>abstract="Adicione variáveis personalizadas ao conteúdo, dependendo da configuração do aplicativo móvel."

Na seção **[!UICONTROL Dados personalizados]**, você pode adicionar variáveis personalizadas à carga, dependendo da configuração do seu aplicativo móvel. Para obter mais informações sobre como configurar notificações por push no Adobe Experience Platform e no Adobe Launch, consulte [esta seção](push-gs.md)

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
| **[!UICONTROL Adicionar sinalizador de conteúdo mutável]** (somente iOS) | Envia o sinalizador de conteúdo mutável no payload por push e permitirá que o conteúdo da notificação por push seja modificado por uma extensão de aplicativo de serviço de notificação fornecida no iOS SDK. Para saber mais, consulte a [documentação para desenvolvedores da Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html).<br/>Você poderá aproveitar suas extensões de aplicativo móvel para modificar ainda mais o conteúdo ou a apresentação das notificações por push de entrada enviadas de [!DNL Journey Optimizer]. Por exemplo, os usuários podem aproveitar essa opção para descriptografar dados, alterar o texto do corpo ou do título de uma notificação, adicionar um identificador de thread a uma notificação etc. |
| **[!UICONTROL Visibilidade de notificação]** (somente Android) | Define a visibilidade da notificação por push. <br/><b>Particular</b> mostrará a notificação em todas as telas de bloqueio, mas ocultará informações confidenciais ou privadas nas telas de bloqueio seguras. <br/><b>Public</b> mostrará a notificação em sua totalidade em todas as telas de bloqueio. <br/><b>Segredo</b> não revelará nenhuma parte da notificação em uma tela de bloqueio segura. <br/>Para obter mais informações, consulte a [documentação para desenvolvedores do Android](https://developer.android.com/reference/android/app/Notification). |
| **[!UICONTROL Prioridade de notificação]** (somente Android) | Define a importância da notificação por push de Baixo para Máximo. Isso determina o quão &quot;intrusiva&quot; será a notificação por push quando for entregue. Para obter mais informações, consulte a [documentação para desenvolvedores do Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL Prioridade de entrega]** (somente Android) | Configura uma prioridade alta ou normal para suas notificações por push. Para obter mais informações sobre a prioridade da mensagem, consulte a [documentação para desenvolvedor do Google](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message). |
