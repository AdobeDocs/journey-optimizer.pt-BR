---
title: Sobre segmentos do Adobe Experience Platform
description: Saiba como configurar um segmento do Adobe Experience Platform
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: 40dd6e3714aea3dc95183e1decbf1b8f83dad50a
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 1%

---

# Sobre segmentos do Adobe Experience Platform {#about-segments}

[!DNL Journey Optimizer]  O permite criar segmentos do Adobe Experience Platform usando dados de Perfil do cliente em tempo real diretamente do  **[!UICONTROL Segments]** menu e aproveitá-los em suas jornadas.

Observe que os segmentos também podem ser criados a partir do próprio serviço de Segmentação. Saiba mais na [documentação do Serviço de segmentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

Você pode aproveitar os segmentos em jornadas de diferentes maneiras:

* Use uma atividade de orquestração **Read segment** para que todos os indivíduos pertencentes ao segmento especificado entrem na jornada. As mensagens incluídas na jornada são enviadas aos indivíduos pertencentes ao segmento. Digamos que você tenha um segmento de &quot;cliente prateado&quot;. Com essa atividade, é possível fazer com que todos os clientes prateados insiram uma jornada e enviem uma série de mensagens personalizadas.

   Para obter mais informações sobre como usar a atividade **[!UICONTROL Read segment]**, consulte [esta seção](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Use a atividade de evento **Segment qualification** para fazer com que os indivíduos insiram ou avancem em uma jornada com base nas entradas e saídas do segmento Adobe Experience Platform. Por exemplo, você pode fazer com que todos os novos clientes de prata insiram uma jornada e enviem mensagens para eles. Para obter mais informações sobre como usar essa atividade, consulte [esta seção](../building-journeys/segment-qualification-events.md).

* Crie **condições complexas** em suas jornadas usando o editor de expressão simples ou avançado. Saiba mais [nesta seção](../building-journeys/condition-activity.md#using-a-segment).

## Método de avaliação no Adobe Journey Optimizer {#evaluation-method-in-journey-optimizer}

No Adobe Journey Optimizer, os públicos-alvo são gerados a partir das definições de segmento usando um destes métodos de avaliação:

* Segmentação de fluxo - a lista de públicos-alvo do segmento é mantida atualizada em tempo real, enquanto novos dados fluem para o sistema.
* Segmentação em lote - a lista de públicos-alvo do segmento é atualizada de hora em hora, com base nos dados que chegaram na última hora.

A determinação entre a segmentação de lote e a segmentação de fluxo é feita pelo sistema para cada definição de segmento, com base na complexidade e no custo da avaliação da regra de segmento.

Você pode exibir o método de avaliação para cada segmento na coluna **[!UICONTROL Evaluation method]** da lista de segmentos.

Após ter definido um segmento pela primeira vez, os perfis são adicionados ao público-alvo quando se qualificam.

O preenchimento retroativo do público-alvo a partir de dados anteriores pode demorar até 24 horas. Após o preenchimento retroativo do público-alvo, ele é continuamente atualizado e está sempre pronto para o direcionamento.
