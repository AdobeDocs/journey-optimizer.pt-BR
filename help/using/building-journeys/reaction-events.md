---
title: Eventos de reações
description: Saiba mais sobre eventos de reação
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
source-git-commit: 7588a675319324e43bbc61a71b1fdfaab9cce93a
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 2%

---

# Eventos de reação {#reaction-events}

Entre as diferentes atividades de evento disponíveis na paleta, você encontrará as **[!UICONTROL Reactions]** evento. Essa atividade permite reagir a dados de rastreamento relacionados a uma mensagem enviada na mesma jornada. Capturamos essas informações em tempo real no momento em que são compartilhadas com a Adobe Experience Platform. Para notificações por push, você pode reagir a mensagens clicadas, enviadas ou com falha. Para mensagens SMS, você pode reagir a mensagens enviadas ou com falha. Para emails, você pode reagir a mensagens clicadas, enviadas, abertas ou com falha.

Você também pode usar esse mecanismo para executar uma ação quando não houver reação às suas mensagens. Para fazer isso, crie um segundo caminho paralelo à atividade de reação e adicione uma atividade de espera. Se não houver reação durante o período definido na atividade de espera, o segundo caminho será escolhido. Você pode optar por enviar, por exemplo, uma mensagem de acompanhamento.

Observe que você só pode usar uma atividade de reação na tela se houver uma **Mensagem** antes.

Consulte [Sobre as atividades de ação](../building-journeys/about-journey-activities.md#action-activities).

![](../assets/journey45.png)

Estas são as diferentes etapas para configurar os eventos de reação:

1. Adicione um **[!UICONTROL Label]** à reação. Esta etapa é opcional.
1. Na lista suspensa, selecione a atividade de ação à qual deseja reagir. Você pode selecionar qualquer atividade de ação posicionada nas etapas anteriores do caminho.
1. Dependendo da ação selecionada, escolha o que deseja reagir.
1. Você pode definir um tempo limite de evento (entre 40 segundos e 30 dias) e um caminho de tempo limite. Isso criará um segundo caminho para indivíduos que não reagiram dentro da duração definida. Ao testar uma jornada que usa um evento de reação, o modo de teste **[!UICONTROL Wait time]** o valor padrão e mínimo é de 40 segundos. Consulte [esta seção](../building-journeys/testing-the-journey.md).

>[!NOTE]
>
>
>Os eventos de reação não podem rastrear mensagens que ocorrem em uma jornada diferente.
>
>Os eventos de reação rastreiam cliques em links do tipo &quot;rastreados&quot;. Os links de unsubscription e mirror pages não são considerados.

>[!IMPORTANT]
>
>Clientes de email como o Gmail permitem bloqueio de imagem. As aberturas de emails são rastreadas usando uma imagem de 0 pixel incluída no email. Se as imagens estiverem bloqueadas, as aberturas de email não serão consideradas.
