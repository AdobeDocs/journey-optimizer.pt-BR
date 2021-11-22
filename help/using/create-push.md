---
title: Configurar uma notificação por push
description: Saiba como criar uma notificação por push no Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 2ebbcd7d-dcfc-4528-974d-6230fc0dca3d
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '1192'
ht-degree: 13%

---

# Criar uma notificação por push {#create-push-notification}

Uma vez [criou uma mensagem](create-message.md), clique no botão **[!UICONTROL Push Notification]** para definir as configurações e o conteúdo da notificação por push.

![](assets/create-content-push.png)

Use as guias dedicadas para definir as configurações de notificação por push para **iOS** e **Android** sistemas operacionais.

>[!NOTE]
>
>O **[!UICONTROL Compose Message]** é comum a **[!UICONTROL iOS]** e **[!UICONTROL Android]** guias. Qualquer alteração nesta seção será aplicada a ambas as guias.

## Título e corpo

Para compor sua mensagem, clique no botão **[!UICONTROL Title]** e **[!UICONTROL Body]** campos. Use o Editor de expressão para definir dados de conteúdo e personalização. Saiba mais sobre a personalização no Editor de expressão em [esta seção](personalization/personalize.md)

Use a seção de visualização do dispositivo para visualizar como a notificação por push é exibida em dispositivos iOS e Android.

## No comportamento do clique {#on-click-behavior}

Selecione o comportamento quando um recipient clicar no corpo da notificação por push.

![](assets/title-body-push.png)

* Use o **[!UICONTROL Open app]** opção para abrir o aplicativo associado à mensagem **[!UICONTROL Preset]**.
* Use o **[!UICONTROL Deeplink]** para redirecionar o recipient para um conteúdo específico localizado dentro do aplicativo. Insira o deeplink no campo associado.
* Use o **[!UICONTROL Web URL]** para redirecionar o recipient para um URL externo. Insira o URL no campo associado.

## Adicionar mídia

Na versão iOS da notificação por push, é possível adicionar uma imagem, um vídeo ou um GIF que será exibido dentro da sua notificação.

Na versão do Android, você só pode adicionar um ícone de imagem e uma imagem para notificações expandidas.

![](assets/push-config-add-media.png)

Estão disponíveis duas opções. É possível:

* Clique no botão **[!UICONTROL Add media]** botão para selecionar um ativo em **[!DNL Adobe Experience Manager Assets Essentials]**.

   Saiba como usar **[!DNL Adobe Experience Manager Assets Essentials]** em [esta página](assets-essentials.md).

* Ou insira o URL da mídia clicando em **[!UICONTROL Add media]** campo. Nesse caso, é possível adicionar personalização.

Depois de adicionada, a mídia é exibida à direita do corpo da notificação.

## Botões Adicionar

Você pode criar uma notificação acionável adicionando botões ao seu conteúdo de push.

Se a tela do dispositivo estiver bloqueada, esses botões não serão exibidos: somente a variável **Título** e **Mensagem** da notificação estão visíveis. Se o dispositivo estiver desbloqueado, os destinatários verão os botões.

Na versão do iOS, é possível adicionar até 4 botões. Na versão do Android, é possível adicionar até 3 botões.

>[!NOTE]
>
>No iOS, use a variável **[!UICONTROL iOS category]** campo para associar ações a uma categoria de notificação.

Clique em **[!UICONTROL Add button]** para definir configurações: o rótulo e a ação associada. As ações possíveis são as mesmas do [comportamento ao clicar](#on-click-behavior).

Clique em **[!UICONTROL Expand view]** para visualizar os botões personalizados.

![](assets/push_buttons.png)

## Enviar uma notificação silenciosa

Uma notificação por push silenciosa (ou notificação em segundo plano) é uma instrução oculta fornecida ao aplicativo. É usado para, por exemplo, notificar seu aplicativo sobre a disponibilidade de novo conteúdo ou iniciar um download em segundo plano.

Selecione o **[!UICONTROL Silent Notification]** opção para notificar silenciosamente o aplicativo: neste caso, a notificação é transferida diretamente para o pedido. Nenhum alerta é exibido na tela do dispositivo.

Use o **[!UICONTROL Custom data]** para adicionar pares de valores chave.

## Dados personalizados

No **[!UICONTROL Custom data]** , você pode adicionar variáveis personalizadas ao payload, dependendo da configuração do aplicativo móvel. Para obter mais informações sobre como configurar notificações por push no Adobe Experience Platform e no Adobe Launch, consulte [esta seção](push-gs.md)

## Opções avançadas

Você pode configurar **[!UICONTROL Advanced options]** para sua notificação por push. Os parâmetros disponíveis estão listados abaixo:

| Parâmetro | Descrição |
|---------|---------|
| **[!UICONTROL Collapsible]** (iOS/Android) | Uma mensagem que pode ser recolhida é uma mensagem que pode ser substituída por uma nova mensagem se tiver ficado desatualizada. Um caso de uso comum de mensagens que podem ser recolhidas são mensagens usadas para informar um aplicativo móvel para sincronizar dados do servidor. Um exemplo seria um aplicativo esportivo que atualiza os usuários com a pontuação mais recente. Somente a mensagem mais recente é relevante. Por outro lado, com uma mensagem que não pode ser recolhida, toda mensagem é importante para o aplicativo do cliente e precisa ser entregue. |
| **[!UICONTROL Custom sound]** (iOS/Android) | O som a ser reproduzido pelo terminal móvel quando a notificação for recebida. O som precisa ser empacotado no aplicativo. |
| **[!UICONTROL Badges]** (iOS/Android) | Um selo é usado para exibir diretamente no ícone do aplicativo o número de novas informações não lidas. <br/>O valor do selo desaparecerá assim que o usuário abrir ou ler o novo conteúdo do aplicativo. Quando uma notificação é recebida em um dispositivo, ela pode atualizar ou adicionar um valor de selo para o aplicativo relacionado.<br/>Por exemplo, se estiver armazenando o número de artigos não lidos de seus clientes, você pode aproveitar a personalização para enviar o valor de selo de artigos não lidos exclusivo para cada cliente. Para obter mais personalizações, consulte [esta seção](personalization/personalize.md). |
| **[!UICONTROL Notification group]**  (Somente iOS) | Associe um grupo de notificação à notificação por push.<br/>A partir do iOS 12, os grupos de notificação permitem consolidar os threads de mensagem e os tópicos de notificação nas IDs de thread. Por exemplo, uma marca pode enviar notificações de marketing sob uma ID de grupo, mantendo mais notificações de tipo operacional sob uma ou mais IDs diferentes.<br/>Para ilustrar isso, é possível ter groupID: 123 &quot;confira a nova coleção de primavera de suéteres&quot; e groupID: 456 Grupos de notificação &quot;o pacote foi entregue&quot;. Neste exemplo, todas as notificações de delivery seriam agrupadas sob a ID do grupo: 456. |
| **[!UICONTROL Notification channel]** (Somente Android) | Associe um canal de notificação à notificação por push.<br/>A partir do Android 8.0 (nível de API 26), todas as notificações devem ser atribuídas a um canal para serem exibidas. Para obter mais informações, consulte [Documentação do desenvolvedor do Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels). |
| **[!UICONTROL Add content-availability flag]** (Somente iOS) | Envia o sinalizador de conteúdo disponível na carga de push para garantir que o aplicativo seja reativado assim que receber a notificação por push, o que significa que o aplicativo poderá acessar os dados da carga.<br/> Isso funciona mesmo se o aplicativo estiver sendo executado em segundo plano e sem precisar de nenhuma interação do usuário (por exemplo, ao tocar na notificação por push). No entanto, isso não se aplica se o aplicativo não estiver em execução. Para obter mais informações, consulte a [documentação para desenvolvedores da Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html). |
| **[!UICONTROL Add mutable-content flag]** (Somente iOS) | Envia o sinalizador de conteúdo mutável no payload por push e permitirá que o conteúdo da notificação por push seja modificado por uma extensão de aplicativo de serviço de notificação fornecida no iOS SDK. Para saber mais, consulte a [documentação para desenvolvedores da Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html).<br/>Em seguida, você poderá otimizar suas extensões de aplicativo móvel para modificar ainda mais o conteúdo ou a apresentação das notificações por push de entrada enviadas pelo [!DNL Journey Optimizer]. Por exemplo, os usuários podem aproveitar essa opção para descriptografar dados, alterar o corpo ou o texto do título de uma notificação, adicionar um identificador de thread a uma notificação etc. |
| **[!UICONTROL Notification visibility]** (Somente Android) | Define a visibilidade da notificação por push. <br/><b>Privado</b> mostrará a notificação em todas as telas de bloqueio, mas ocultará informações confidenciais ou privadas em telas de bloqueio seguras. <br/><b>Público</b> mostrará a notificação em sua totalidade em todas as telas de bloqueio. <br/><b>Segredo</b> não revelará nenhuma parte da notificação em uma tela de bloqueio segura. <br/>Para obter mais informações, consulte [Documentação do desenvolvedor do Android](https://developer.android.com/reference/android/app/Notification). |
| **[!UICONTROL Notification priority]** (Somente Android) | Define a importância da notificação por push de Baixa para Máx. Isso determina como a notificação por push será &quot;intrusiva&quot; ao ser entregue. Para obter mais informações, consulte [Documentação do desenvolvedor do Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL Delivery priority]** (Somente Android) | Define uma prioridade alta ou normal para suas notificações por push. Para obter mais informações sobre a prioridade da mensagem, consulte a [documentação para desenvolvedor do Google](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message). |

**Tópicos relacionados**

<!--
* [Understand push notification flow](push-gs.md)
-->

* [Configurar canal de push](push-gs.md)
* [Criar uma nova mensagem](create-message.md)
* [Adicionar uma mensagem em uma jornada](building-journeys/journeys-message.md)
