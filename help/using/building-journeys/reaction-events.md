---
solution: Journey Optimizer
product: journey optimizer
title: Eventos de reações
description: Saiba como usar eventos de reação para responder aos dados de rastreamento de mensagens, como aberturas e cliques em suas jornadas, e configurar caminhos de tempo limite para não respondedores.
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: jornada, eventos, reação, rastreamento, plataforma
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/6myO49j2-TgkX0-diC8JDePxvMBPjZGnMYdxO466cP4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: d08afb72-92f6-4856-88e3-11ec34313c2f
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
  - id: e57d1da4-32c2-4cc6-945c-9feb219156ff
  - id: ebd64fe4-362a-4a1c-9476-b2573ed12a95
  - id: fa683eda-48de-4558-af32-2673edcd44fe
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 506
ht-degree: 15%

---

# Eventos de reação {#reaction-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_reaction"
>title="Eventos de reação"
>abstract="Essa atividade permite reagir a dados de rastreamento relacionados a uma mensagem enviada na mesma jornada. Capturamos essas informações em tempo real no momento em que são compartilhadas com a [!DNL Adobe Experience Platform]."

## Visão geral {#overview}

Entre as diferentes atividades de evento disponíveis na paleta, você encontrará o evento **[!UICONTROL Reações]** interno. Essa atividade permite reagir a dados de rastreamento relacionados a uma mensagem enviada na mesma jornada. Capturamos essas informações em tempo real no momento em que são compartilhadas com a [!DNL Adobe Experience Platform].

Você pode reagir a mensagens clicadas ou abertas. Por exemplo, você pode enviar outra mensagem se um indivíduo tiver aberto o email anterior ou clicado nele, ou enviar uma mensagem de acompanhamento diferente se ele não interagiu com a sua comunicação.

Consulte [Atividades de ação](../building-journeys/about-journey-activities.md#action-activities).

Você pode usar a atividade **[!UICONTROL Reação]** para executar uma ação quando não houver reação às suas mensagens. Para fazer isso, crie um segundo caminho paralelo à atividade **[!UICONTROL Reaction]** e adicione uma atividade **[!UICONTROL Wait]**. Se não houver reação durante o período definido na atividade **[!UICONTROL Wait]**, o segundo caminho será escolhido. Você pode optar por enviar, por exemplo, uma mensagem de acompanhamento.

## Como configurar eventos de reação {#configure}

![Reagir à configuração do evento com a seleção de canal e as opções de tipo de evento](assets/journey45.png)

Siga estas etapas para configurar os eventos de reação:

1. Coloque uma atividade **[!UICONTROL Reação]** **imediatamente** após uma [atividade de ação de canal](journey-action.md) na tela de jornada.
1. Adicione um **[!UICONTROL Rótulo]** à reação. Esta etapa é opcional.
1. Na lista suspensa, selecione a atividade de ação à qual deseja reagir. Você pode selecionar qualquer atividade de ação posicionada nas etapas anteriores do caminho.
1. Dependendo da ação selecionada, escolha a que deseja reagir.
1. Você pode definir um tempo limite de evento (entre 40 segundos e 90 dias) e um caminho de tempo limite. Isso cria um segundo caminho para indivíduos que não reagiram dentro da duração definida. Ao testar uma jornada que usa um evento de reação, o padrão do modo de teste **[!UICONTROL Tempo de espera]** e o valor mínimo é de 40 segundos. Consulte [esta seção](../building-journeys/testing-the-journey.md).

## Medidas de proteção e limitações {#guardrails-limitations}

* Uma atividade **[!UICONTROL Reação]** deve ser colocada **imediatamente** após uma [atividade de ação de canal](journey-action.md) na tela de jornada.
* Você não pode usar uma atividade **[!UICONTROL Reação]** se não houver uma atividade de ação de canal antes dela.
* Não há suporte para a colocação de uma atividade **[!UICONTROL Wait]** ou qualquer outra atividade entre a ação de canal e a atividade **[!UICONTROL Reaction]** e pode fazer com que a Reação não funcione conforme esperado.
* Os eventos de reação só podem rastrear mensagens enviadas na mesma jornada. Eles não podem rastrear mensagens que ocorrem em uma jornada diferente.
* Os eventos de reação rastreiam cliques em links do tipo &quot;rastreado&quot;. Links de unsubscription e mirror pages não são considerados.
* As aberturas de email são rastreadas usando uma imagem de 0 pixel incluída no email. Se os clientes de email (como o Gmail) bloquearem imagens, as aberturas de email não serão consideradas.
