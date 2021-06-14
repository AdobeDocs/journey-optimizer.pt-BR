---
title: Sobre segmentos do Adobe Experience Platform
description: Saiba como configurar um segmento do Adobe Experience Platform
feature: Jornadas
topic: Gerenciamento de conteúdo
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 3%

---

# Sobre segmentos do Adobe Experience Platform {#about-segments}

![](../assets/do-not-localize/badge.png)

O Journey Optimizer permite criar segmentos do Adobe Experience Platform usando dados de Perfil do cliente em tempo real diretamente do menu **[!UICONTROL Segments]** e aproveitá-los em suas jornadas.

Observe que os segmentos também podem ser criados a partir do próprio serviço de Segmentação. Saiba mais na [documentação do Serviço de segmentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

Você pode aproveitar os segmentos em jornadas de diferentes maneiras:

* Use uma atividade de orquestração **Read segment** para que todos os indivíduos pertencentes ao segmento especificado entrem na jornada. As mensagens incluídas na jornada são enviadas aos indivíduos pertencentes ao segmento. Digamos que você tenha um segmento de &quot;cliente prateado&quot;. Com essa atividade, é possível fazer com que todos os clientes prateados insiram uma jornada e enviem uma série de mensagens personalizadas.

   Para obter mais informações sobre como usar a atividade **[!UICONTROL Read segment]**, consulte [esta seção](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Use a atividade de evento **Segment qualification** para fazer com que os indivíduos insiram ou avancem em uma jornada com base nas entradas e saídas do segmento Adobe Experience Platform. Por exemplo, você pode fazer com que todos os novos clientes de prata insiram uma jornada e enviem mensagens para eles. Para obter mais informações sobre como usar essa atividade, consulte [esta seção](../building-journeys/segment-qualification-events.md).

* Crie **condições complexas** em suas jornadas usando o editor de expressão simples ou avançado. Saiba mais [nesta seção](../building-journeys/condition-activity.md#using-a-segment).
