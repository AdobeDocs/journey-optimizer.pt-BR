---
solution: Journey Optimizer
product: journey optimizer
title: Enviar sua notificação por push
description: Saiba como visualizar e testar sua notificação por push no Journey Otimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: aad4e08a-3369-454d-9e32-974347a3b393
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Enviar sua notificação por push {#send-push}

## Visualizar sua notificação por push {#preview-push}

Após definir o conteúdo da mensagem, é possível usar perfis de teste para pré-visualizá-lo e testá-lo. Se você inseriu conteúdo personalizado, é possível verificar como esse conteúdo é exibido na mensagem, aproveitando os dados do perfil de teste.

1. Clique em **[!UICONTROL Simulate content]**.

1. Clique em **[!UICONTROL Manage test profiles]** para adicionar um perfil de teste.

1. Encontre seu perfil de teste com a **[!UICONTROL Identity namespace]** e **[!UICONTROL Identity value]** campos. Em seguida, clique em **[!UICONTROL Add profile]**.

   ![](assets/push_preview_1.png)

1. Siga as mesmas etapas descritas acima para selecionar um perfil de teste e

   ![](assets/push_preview_2.png)

1. Na visualização por push, os dados do perfil de teste são aproveitados no conteúdo da mensagem.

   Selecione o tipo de dispositivo para visualizar o conteúdo: **[!UICONTROL iOS]** ou **[!UICONTROL Android]**.

   ![](assets/push_preview_3.png)

## Validar sua notificação por push {#push-validate}

>[!NOTE]
>
> Para melhorar o deliverability, você sempre deve usar os números de telefone nos formatos compatíveis com o provedor. Por exemplo, Twilio e Sinch suportam apenas números de telefone no formato E.164.

Você também deve verificar os alertas na seção superior do editor.  Alguns deles são avisos simples, mas outros podem impedir que você use a mensagem. Dois tipos de alertas podem acontecer:

* **Avisos** consulte recomendações e práticas recomendadas.

* **Erros** impedir que você teste ou ative a jornada, desde que elas não sejam resolvidas, como:

   * **[!UICONTROL The push version of the message is empty]**: esse erro é exibido quando o corpo ou o título da notificação por push está ausente. Saiba como definir o conteúdo de notificação por push em [esta seção](create-push.md).

   * **[!UICONTROL Surface doesn't exist]**: não será possível usar a mensagem se a superfície selecionada for excluída após a criação da mensagem. Se este erro ocorrer, selecione outra superfície na mensagem **[!UICONTROL Properties]**. Saiba mais sobre as superfícies dos canais em [esta seção](../configuration/channel-surfaces.md).

   * **[!UICONTROL Push iOS/Android payload has exceeded limit of 4KB]**: o tamanho da notificação por push não pode exceder 4 KB. Para respeitar esse limite, tente reduzir o uso de imagens ou emojis. Saiba como gerenciar o conteúdo de notificação por push no [esta seção](../push/create-push.md).

![](assets/push_alert.png)

Quando a notificação por push estiver pronta, conclua a configuração de seu [jornada](../building-journeys/journey-gs.md) ou [campanha](../campaigns/create-campaign.md) para enviá-lo.
