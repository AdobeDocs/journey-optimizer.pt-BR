---
solution: Journey Optimizer
product: journey optimizer
title: Verificação e envio da notificação por push
description: Saiba como verificar e enviar sua notificação por push no Journey Optimizer
feature: Push
topic: Content Management
role: User
level: Beginner
exl-id: aad4e08a-3369-454d-9e32-974347a3b393
source-git-commit: 27447578dad6bd2612989d79cd0dc8ddbe78d629
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 5%

---

# Verificação e envio da notificação por push {#send-push}

## Pré-visualizar sua notificação por push {#preview-push}

Depois que o conteúdo da mensagem for definido, você poderá usar perfis de teste para visualizar seu conteúdo. Se você inseriu conteúdo personalizado, é possível verificar como esse conteúdo é exibido na mensagem, usando os dados do perfil de teste.

Para fazer isso, clique em **[!UICONTROL Simular conteúdo]** em seguida, adicione um perfil de teste. Em seguida, é possível selecionar o tipo de dispositivo para visualizar o conteúdo: **[!UICONTROL iOS]** ou **[!UICONTROL Android]**.

![](assets/push_preview_3.png)

Informações detalhadas sobre como selecionar perfis de teste e pré-visualizar seu conteúdo estão disponíveis na [Gestão de conteúdo](../content-management/preview-test.md) seção.

## Validar sua notificação por push {#push-validate}

Você deve verificar os alertas na seção superior do editor. Alguns deles são avisos simples, mas outros podem impedir que você envie a mensagem. Dois tipos de alertas podem ocorrer: avisos e erros.

* **Avisos** consulte recomendações e práticas recomendadas.

* **Erros** impedir que você teste ou ative a jornada, desde que não sejam resolvidos, como:

   * **[!UICONTROL A versão push da mensagem está vazia]**: esse erro é exibido quando o corpo ou o título da notificação por push está ausente. Saiba como definir o conteúdo de notificação por push no [nesta seção](create-push.md).

   * **[!UICONTROL A superfície não existe]**: não será possível usar a mensagem se a superfície selecionada for excluída após a criação da mensagem. Se este erro ocorrer, selecione outra superfície na mensagem **[!UICONTROL Propriedades]**. Saiba mais sobre superfícies de canal em [nesta seção](../configuration/channel-surfaces.md).

   * **[!UICONTROL A carga do Push iOS/Android excedeu o limite de 4 KB]**: o tamanho da notificação por push não pode exceder 4 KB. Para respeitar esse limite, tente reduzir o uso de imagens ou emojis. Saiba como gerenciar o conteúdo de notificação por push no [nesta seção](../push/create-push.md).

  ![](assets/push_alert.png)


>[!NOTE]
>
> Para melhorar a capacidade de delivery, você sempre deve usar os números de telefone nos formatos compatíveis com o provedor. Por exemplo, o Twilio e o Sinch suportam apenas números de telefone no formato E.164.

## Enviar a notificação por push{#push-send}

Quando a mensagem de push estiver pronta, conclua a configuração de [jornada](../building-journeys/journey-gs.md) ou [campaign](../campaigns/create-campaign.md) para enviá-lo.

**Tópicos relacionados**

* [Configurar canal por push](push-configuration.md)
* [Relatório de notificação por push](../reports/journey-global-report.md#push-global)
* [Criar uma notificação por push](create-push.md)
* [Adicionar uma mensagem em uma jornada](../building-journeys/journeys-message.md)
* [Adicionar uma mensagem em uma campanha](../campaigns/create-campaign.md)

