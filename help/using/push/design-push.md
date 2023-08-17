---
solution: Journey Optimizer
product: journey optimizer
title: Criar uma notificação por push
description: Saiba como criar uma notificação por push no Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 6f6d693d-11f2-48b7-82a8-171829bf8045
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '1260'
ht-degree: 14%

---

# Criar uma notificação por push {#design-push-notification}

## Título e corpo {#push-title-body}

Para redigir a mensagem, clique no link **[!UICONTROL Título]** e **[!UICONTROL Corpo]** campos. Use o Editor de expressão para definir o conteúdo, personalizar os dados e adicionar conteúdo dinâmico. Saiba mais sobre [personalização](../personalization/personalize.md) e [conteúdo dinâmico](../personalization/get-started-dynamic-content.md) no Editor de expressão.

Use a seção de visualização de dispositivo para visualizar como a notificação por push é exibida em dispositivos iOS e Android.

## Comportamento ao clicar {#on-click-behavior}

>[!CONTEXTUALHELP]
>id="ajo-message-push-onclick"
>title="Sobre o comportamento ao clicar"
>abstract="Selecione o comportamento quando um recipient clicar no corpo da notificação por push."

Você pode selecionar o comportamento quando um usuário clicar no corpo da notificação por push.

![](assets/title-body-push.png)

* Para abrir o aplicativo, selecione a variável **[!UICONTROL Abrir aplicativo]** opção. O aplicativo associado à notificação é definido na variável [superfície de canal](../configuration/channel-surfaces.md) (ou seja, predefinição de mensagem).
* Para redirecionar o usuário para um conteúdo específico em um aplicativo, selecione a variável **[!UICONTROL Deeplink]** opção.  O conteúdo específico pode ser uma exibição específica, uma seção específica de uma página ou uma determinada guia. Depois que a opção for selecionada, insira o deep link no campo associado.
* Para redirecionar o usuário para um URL externo, use o **[!UICONTROL URL da Web]** opção. Depois que a opção for selecionada, insira o URL no campo associado.

## Adicionar mídia {#add-media-push}

Na versão para iOS da sua notificação por push, você pode adicionar uma imagem, um vídeo ou um GIF que será exibido na notificação.

Na versão do Android, só é possível adicionar um ícone de imagem e uma imagem para notificações expandidas.

![](assets/push-config-add-media.png)

Estão disponíveis duas opções. É possível:

* Use o **[!UICONTROL Adicionar mídia]** botão para selecionar um ativo no **[!DNL Adobe Experience Manager Assets Essentials]**.

  Saiba como usar o **[!DNL Adobe Experience Manager Assets Essentials]** in [esta página](../email/assets-essentials.md).

* Ou insira o URL da mídia no campo **[!UICONTROL Adicionar mídia]** campo. Nesse caso, você pode adicionar personalização ao URL.

Depois de adicionada, a mídia é exibida à direita do corpo de notificação.

## Adicionar botões {#add-buttons-push}

Crie uma notificação acionável adicionando botões ao seu conteúdo de push.

Se a tela do dispositivo estiver bloqueada, esses botões não serão exibidos: somente a **Título** e a variável **Mensagem** da notificação estão visíveis. Se o dispositivo estiver desbloqueado, os recipients verão os botões.

Na versão do iOS, é possível adicionar até quatro botões. Na versão Android, é possível adicionar até três botões.

>[!NOTE]
>
>Para o iOS, use o **[!UICONTROL Categoria do iOS]** para associar ações a uma categoria de notificação.

1. Use o **[!UICONTROL Botão Adicionar]** para definir configurações: o rótulo e a ação associada. As ações possíveis são as mesmas de [comportamento ao clicar](#on-click-behavior).

1. Use o **[!UICONTROL Expandir visualização]** ícone na imagem de visualização central para visualizar os botões personalizados.

![](assets/push_buttons.png)

## Enviar uma notificação silenciosa {#silent-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push_silent_notification"
>title="Sobre notificação silenciosa"
>abstract="Enviar notificações sem perturbar o usuário. As notificações não são mostradas no centro de notificações ou na barra de notificação."

Uma notificação por push silenciosa (ou notificação em segundo plano) é uma instrução oculta entregue ao aplicativo. Ele é usado, por exemplo, para notificar seu aplicativo sobre a disponibilidade de novo conteúdo ou iniciar um download em segundo plano.

Selecione o **[!UICONTROL Notificação silenciosa]** opção para notificar silenciosamente o aplicativo: nesse caso, a notificação é transferida diretamente para o aplicativo. Nenhum alerta é exibido na tela do dispositivo.

Use o **[!UICONTROL Dados personalizados]** seção para adicionar pares de valor-chave.

## Dados personalizados

No **[!UICONTROL Dados personalizados]** você pode adicionar variáveis personalizadas à carga, dependendo da configuração do seu aplicativo móvel. Para obter mais informações sobre como configurar notificações por push no Adobe Experience Platform e no Adobe Launch, consulte [nesta seção](push-gs.md)

## Opções avançadas {#advanced-options-push}

Você pode configurar **[!UICONTROL Opções avançadas]** para sua notificação por push. Os parâmetros disponíveis estão listados abaixo:

| Parâmetro | Descrição |
|---------|---------|
| **[!UICONTROL Recolhível]** (iOS/Android) | Uma mensagem recolhível é uma mensagem que pode ser substituída por uma nova mensagem se ela se tornar desatualizada. Casos de uso comuns de mensagens recolhíveis são mensagens usadas para informar um aplicativo móvel para sincronizar dados do servidor. Um exemplo seria um aplicativo de esportes que atualiza os usuários com a pontuação mais recente. Somente a mensagem mais recente é relevante. Por outro lado, com mensagens não recolhíveis, cada mensagem é importante para o aplicativo cliente e precisa ser entregue. |
| **[!UICONTROL Som personalizado]** (iOS/Android) | O som a ser reproduzido pelo terminal móvel quando a notificação for recebida. O som precisa ser incluído no aplicativo. |
| **[!UICONTROL Medalhas]** (iOS/Android) | Um selo é usado para exibir diretamente no ícone do aplicativo o número de novas informações não lidas. <br/>O valor do selo desaparecerá assim que o usuário abrir ou ler o novo conteúdo do aplicativo. Quando uma notificação é recebida em um dispositivo, ela pode atualizar ou adicionar um valor de selo para o aplicativo relacionado.<br/>Por exemplo, se estiver armazenando o número de artigos não lidos dos clientes, você pode aproveitar a personalização para enviar o valor exclusivo do selo de artigos não lidos para cada cliente. Para obter mais personalizações, consulte [nesta seção](../personalization/personalize.md). |
| **[!UICONTROL Grupo de notificação]**  (somente iOS) | Associe um grupo de notificação à notificação por push.<br/>A partir do iOS 12, os grupos de notificação permitem consolidar threads de mensagem e tópicos de notificação em IDs de thread. Por exemplo, uma marca pode enviar notificações de marketing em uma ID de grupo, enquanto mantém mais notificações de tipo operacional em uma ou mais IDs diferentes.<br/>Para ilustrar isso, você pode ter grupos de notificação groupID: 123 &quot;confira a nova coleção de primavera de blusas&quot; e groupID: 456 &quot;seu pacote foi entregue&quot;. Neste exemplo, todas as notificações de delivery seriam agrupadas na ID de grupo: 456. |
| **[!UICONTROL Canal de notificação]** (Somente Android) | Associe um canal de notificação à notificação por push.<br/>A partir do Android 8.0 (nível de API 26), todas as notificações devem ser atribuídas a um canal para serem exibidas. Para obter mais informações, consulte [Documentação do desenvolvedor do Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels). |
| **[!UICONTROL Adicionar sinalizador de disponibilidade de conteúdo]** (somente iOS) | Envia o sinalizador de conteúdo disponível na carga de push para garantir que o aplicativo seja reativado assim que receber a notificação por push, o que significa que o aplicativo poderá acessar os dados da carga.<br/> Isso funciona mesmo se o aplicativo estiver sendo executado em segundo plano e sem precisar de nenhuma interação do usuário (por exemplo, ao tocar na notificação por push). No entanto, isso não se aplica se o aplicativo não estiver em execução. Para obter mais informações, consulte a [documentação para desenvolvedores da Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html). |
| **[!UICONTROL Adicionar sinalizador de conteúdo mutável]** (somente iOS) | Envia o sinalizador de conteúdo mutável no payload por push e permitirá que o conteúdo da notificação por push seja modificado por uma extensão de aplicativo de serviço de notificação fornecida no SDK do iOS. Para saber mais, consulte a [documentação para desenvolvedores da Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html).<br/>Em seguida, você poderá otimizar suas extensões de aplicativo móvel para modificar ainda mais o conteúdo ou a apresentação das notificações por push de entrada enviadas pelo [!DNL Journey Optimizer]. Por exemplo, os usuários podem aproveitar essa opção para descriptografar dados, alterar o texto do corpo ou do título de uma notificação, adicionar um identificador de thread a uma notificação etc. |
| **[!UICONTROL Visibilidade de notificação]** (Somente Android) | Define a visibilidade da notificação por push. <br/><b>Privado</b> mostrará a notificação em todas as telas de bloqueio, mas ocultará informações confidenciais ou privadas nas telas de bloqueio seguras. <br/><b>Público</b> mostrará a notificação na íntegra em todas as telas de bloqueio. <br/><b>Segredo</b> não revelarão nenhuma parte da notificação em uma tela de bloqueio segura. <br/>Para obter mais informações, consulte [Documentação do desenvolvedor do Android](https://developer.android.com/reference/android/app/Notification). |
| **[!UICONTROL Prioridade de notificação]** (Somente Android) | Define a importância da notificação por push de Baixo para Máximo. Isso determina o quão &quot;intrusiva&quot; será a notificação por push quando for entregue. Para obter mais informações, consulte [Documentação do desenvolvedor do Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL Prioridade de entrega]** (Somente Android) | Configura uma prioridade alta ou normal para suas notificações por push. Para obter mais informações sobre a prioridade da mensagem, consulte a [documentação para desenvolvedor do Google](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message). |
