---
title: Sobre segmentos da Adobe Experience Platform
description: Saiba como configurar um segmento do Adobe Experience Platform
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 3c8c059e5e3953807b9fc2d8d0eded0d00e49003
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 2%

---

# Introdução a segmentos do Adobe Experience Platform {#about-segments}

[!DNL Journey Optimizer]  permite criar segmentos do Adobe Experience Platform usando dados de Perfil do cliente em tempo real diretamente do **[!UICONTROL Segments]** e aproveite-as em suas jornadas.

Observe que os segmentos também podem ser criados a partir do próprio serviço de Segmentação. Saiba mais na [Documentação do Serviço de segmentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

Você pode aproveitar os segmentos em jornadas de diferentes maneiras:

* Use um **Ler segmento** atividade de orquestração para fazer com que todos os indivíduos pertencentes ao segmento especificado entrem na jornada. As mensagens incluídas na jornada são enviadas aos indivíduos pertencentes ao segmento. Digamos que você tenha um segmento de &quot;cliente prateado&quot;. Com essa atividade, é possível fazer com que todos os clientes prateados insiram uma jornada e enviem uma série de mensagens personalizadas.

   Para obter mais informações sobre como usar o **[!UICONTROL Read segment]** atividade , consulte [esta seção](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Use o **Qualificação do segmento** atividade de evento para fazer indivíduos entrarem ou avançarem em uma jornada com base nas entradas e saídas do segmento do Adobe Experience Platform. Por exemplo, você pode fazer com que todos os novos clientes de prata insiram uma jornada e enviem mensagens para eles. Para obter mais informações sobre como usar essa atividade, consulte [esta seção](../building-journeys/segment-qualification-events.md).

* Criar **condições complexas** em suas jornadas usando o editor de expressão simples ou avançado. Saiba mais [nesta seção](../building-journeys/condition-activity.md#using-a-segment).

## Método de avaliação no Adobe Journey Optimizer {#evaluation-method-in-journey-optimizer}

No Adobe Journey Optimizer, os públicos-alvo são gerados a partir das definições de segmento usando um destes métodos de avaliação:

* Segmentação de fluxo - a lista de públicos-alvo do segmento é mantida atualizada em tempo real, enquanto novos dados fluem para o sistema.
* Segmentação em lote - a lista de públicos-alvo do segmento é atualizada de hora em hora, com base nos dados que chegaram na última hora.

A determinação entre a segmentação de lote e a segmentação de fluxo é feita pelo sistema para cada definição de segmento, com base na complexidade e no custo da avaliação da regra de segmento.

Você pode visualizar o método de avaliação para cada segmento na **[!UICONTROL Evaluation method]** da lista de segmentos.

Após ter definido um segmento pela primeira vez, os perfis são adicionados ao público-alvo quando se qualificam.

O preenchimento retroativo do público-alvo a partir de dados anteriores pode demorar até 24 horas. Após o preenchimento retroativo do público-alvo, ele é continuamente atualizado e está sempre pronto para o direcionamento.
