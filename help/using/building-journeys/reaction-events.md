---
solution: Journey Optimizer
product: journey optimizer
title: Eventos de reações
description: Saiba mais sobre eventos de reação
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: jornada, eventos, reação, rastreamento, plataforma
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 21%

---

# Eventos de reação {#reaction-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_reaction"
>title="Eventos de reação"
>abstract="Essa atividade permite reagir a dados de rastreamento relacionados a uma mensagem enviada na mesma jornada. Capturamos essas informações em tempo real no momento em que são compartilhadas com a Adobe Experience Platform."

Entre as diferentes atividades de evento disponíveis na paleta, você encontrará o incorporado **[!UICONTROL Reações]** evento. Essa atividade permite reagir a dados de rastreamento relacionados a uma mensagem enviada na mesma jornada. Capturamos essas informações em tempo real no momento em que são compartilhadas com a Adobe Experience Platform.

Você pode reagir a mensagens clicadas ou abertas.

Você também pode usar esse mecanismo para executar uma ação quando não houver reação às suas mensagens. Para fazer isso, crie um segundo caminho paralelo à atividade de reação e adicione uma atividade de espera. Se não houver reação durante o período definido na atividade de espera, o segundo caminho será escolhido. Você pode optar por enviar, por exemplo, uma mensagem de acompanhamento.

Observe que você só poderá usar uma atividade de reação na tela se houver uma atividade de ação de canal antes (Email e push).

Consulte [Sobre as atividades de ação](../building-journeys/about-journey-activities.md#action-activities).

![](assets/journey45.png)

Estas são as diferentes etapas para configurar os eventos de reação:

1. Adicionar um **[!UICONTROL Rótulo]** à reação. Esta etapa é opcional.
1. Na lista suspensa, selecione a atividade de ação à qual deseja reagir. Você pode selecionar qualquer atividade de ação posicionada nas etapas anteriores do caminho.
1. Dependendo da ação selecionada, escolha a que deseja reagir.
1. Você pode definir um tempo limite de evento (entre 40 segundos e 30 dias) e um caminho de tempo limite. Isso criará um segundo caminho para indivíduos que não reagiram dentro da duração definida. Ao testar uma jornada que usa um evento de reação, o modo de teste **[!UICONTROL Tempo de espera]** padrão e o valor mínimo é de 40 segundos. Consulte [esta seção](../building-journeys/testing-the-journey.md).

>[!NOTE]
>
>
>Os eventos de reação não podem rastrear mensagens que ocorrem em uma jornada diferente.
>
>Os eventos de reação rastreiam cliques em links do tipo &quot;rastreado&quot;. Links de unsubscription e mirror pages não são considerados.

>[!IMPORTANT]
>
>Clientes de email, como o Gmail, permitem o bloqueio de imagens. As aberturas de emails são rastreadas usando uma imagem de 0 pixel incluída no email. Se as imagens forem bloqueadas, as aberturas de email não serão consideradas.
