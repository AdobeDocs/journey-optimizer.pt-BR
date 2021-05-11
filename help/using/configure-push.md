---
title: Configurar uma notificação por push
description: Saiba como criar uma notificação por push no Journey Optimizer
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '934'
ht-degree: 13%

---

# Configurar uma notificação por push {#create-push-notification}

![](assets/do-not-localize/badge.png)

A notificação por push é configurada ao criar uma mensagem, na guia **[!UICONTROL Push Notification]** (consulte [Criar uma mensagem](create-message.md)).

É possível configurar o conteúdo da notificação por push para sistemas operacionais iOS ou Android usando as guias dedicadas.

![](assets/create-content-push.png)

## Título e corpo

Para compor sua mensagem, clique nos campos **[!UICONTROL Title]** e **[!UICONTROL Body]**. Use o Editor de expressão para definir dados de conteúdo e personalização.

Saiba mais sobre a personalização [nesta seção](personalization/personalize.md)

Use a seção central para visualizar como a notificação por push é exibida em terminais iOS e Android.

>[!NOTE]
>
>A seção **[!UICONTROL Compose Message]** é comum às guias **[!UICONTROL iOS]** e **[!UICONTROL Android]**. Qualquer alteração nesta seção será aplicada a ambos os sistemas operacionais.

## No comportamento do clique {#on-click-behavior}

Selecione o comportamento quando um recipient clicar no corpo da notificação por push:

* Use a opção **[!UICONTROL Open app]** para abrir o aplicativo associado à mensagem **[!UICONTROL Preset]**.
* Use a opção **[!UICONTROL Deeplink]** para redirecionar o recipient para um conteúdo específico localizado dentro do aplicativo. Insira o deeplink no campo associado.
* Use a opção **[!UICONTROL Web URL]** para redirecionar o recipient para um URL externo. Insira o URL no campo associado.

## Enviar uma notificação silenciosa

Uma notificação por push silenciosa (ou notificação em segundo plano) é uma instrução oculta fornecida ao aplicativo. É usado para, por exemplo, notificar seu aplicativo sobre a disponibilidade de novo conteúdo ou iniciar um download em segundo plano.

Selecione a opção **[!UICONTROL Silent Notification]** para notificar silenciosamente o aplicativo: neste caso, a notificação é transferida diretamente para o pedido. Nenhum alerta é exibido na tela do dispositivo.

Use a seção **[!UICONTROL Custom data]** para adicionar pares de chave/valor.

## Opções avançadas

Configure o **[!UICONTROL Advanced options]**. Os parâmetros disponíveis são:

| Parâmetro | Disponibilidade | Descrição |
|---------|----------|---------|
| **[!UICONTROL Collapsible]** | iOS/Android | Uma mensagem que pode ser reduzida é uma mensagem que pode ser substituída por uma nova. Por exemplo, um aplicativo que atualiza os usuários com as últimas notícias sobre um tópico. Nesse caso, somente a mensagem mais recente é relevante. Por outro lado, com mensagens não recolhidas, todas as mensagens são importantes para o aplicativo do cliente e precisam ser entregues. |
| **[!UICONTROL Custom sound]** | iOS/Android | O som a ser reproduzido pelo terminal móvel quando a notificação for recebida. O som precisa ser empacotado no aplicativo. |
| **[!UICONTROL Badges]** | iOS/Android | Um selo é usado para exibir diretamente no ícone do aplicativo o número de novas informações não lidas. <br/>O valor do selo desaparecerá assim que o usuário abrir ou ler o novo conteúdo do aplicativo. Quando uma notificação é recebida em um dispositivo, ela pode atualizar ou adicionar um valor de selo para o aplicativo relacionado.<br/>Por exemplo, se estiver armazenando o número de artigos não lidos de seus clientes, você pode aproveitar a personalização para enviar o valor de selo de artigos não lidos exclusivo para cada cliente. Para obter mais personalização, consulte [esta seção](personalization/personalize.md). |
| **[!UICONTROL Notification group]** / | iOS | Associe um grupo de notificação à notificação por push.<br/>A partir do iOS 12, os grupos de notificação permitem consolidar threads de mensagem e tópicos de notificação em IDs de thread. Por exemplo, uma marca pode enviar notificações de marketing sob uma ID de grupo, mantendo mais notificações de tipo operacional sob uma ou mais IDs diferentes.<br/>Para ilustrar isso, é possível ter groupID: 123 &quot;confira a nova coleção de primavera de suéteres&quot; e groupID: 456 Grupos de notificação &quot;o pacote foi entregue&quot;. Neste exemplo, todas as notificações de delivery seriam agrupadas sob a ID do grupo: 456. |
| **[!UICONTROL Notification channel]** | Android | Associe um canal de notificação à notificação por push.<br/>A partir do Android 8.0 (nível de API 26), todas as notificações devem ser atribuídas a um canal para serem exibidas. Para obter mais informações, consulte a [documentação do desenvolvedor do Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels). |
| **[!UICONTROL Add content-availability flag]** | iOS | Envia o sinalizador de conteúdo disponível na carga de push para garantir que o aplicativo seja reativado assim que receber a notificação por push, o que significa que o aplicativo poderá acessar os dados da carga.<br/> Isso funciona mesmo se o aplicativo estiver sendo executado em segundo plano e sem precisar de nenhuma interação do usuário (por exemplo, ao tocar na notificação por push). No entanto, isso não se aplica se o aplicativo não estiver em execução. Para obter mais informações, consulte a [documentação para desenvolvedores da Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html). |
| **[!UICONTROL Add mutable-content flag]** | iOS | Envia o sinalizador de conteúdo mutável no payload por push e permitirá que o conteúdo da notificação por push seja modificado por uma extensão de aplicativo de serviço de notificação fornecida no SDK do iOS. Para saber mais, consulte a [documentação para desenvolvedores da Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html).<br/>Você pode aproveitar suas extensões de aplicativo móvel para modificar ainda mais o conteúdo ou a apresentação das notificações por push de entrada enviadas por  [!DNL Journey Optimizer] Por exemplo, os usuários podem aproveitar essa opção para descriptografar dados, alterar o texto do corpo ou do título de uma notificação, adicionar um identificador de thread a uma notificação etc. |
| **[!UICONTROL Notification visibility]** | Android | Define a visibilidade da notificação por push. <b></b> privatemostrará a notificação em todas as telas de bloqueio, mas ocultará informações confidenciais ou privadas em telas de bloqueio seguras. <b></b> O Publicará mostrará a notificação em sua totalidade em todas as telas de bloqueio. <b></b> Os secretários não revelarão qualquer parte da notificação num ecrã de bloqueio seguro. Para obter mais informações, consulte a [documentação do desenvolvedor do Android](https://developer.android.com/reference/android/app/Notification). |
| **[!UICONTROL Notification priority]** | Android | Define a importância da notificação por push de Baixa para Máx. Isso determina como a notificação por push será &quot;intrusiva&quot; ao ser entregue. Para obter mais informações, consulte a [documentação do desenvolvedor do Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL Delivery priority]** | Android | Define uma prioridade alta ou normal para suas notificações por push. Para obter mais informações sobre a prioridade da mensagem, consulte a [documentação para desenvolvedor do Google](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message). |

## Dados personalizados

Na seção **[!UICONTROL Custom data]**, é possível adicionar variáveis personalizadas ao payload, dependendo da configuração do aplicativo móvel. Para obter mais informações sobre como configurar notificações por push no Adobe Experience Platform e no Adobe Launch, consulte [esta seção](push-configuration.md)

