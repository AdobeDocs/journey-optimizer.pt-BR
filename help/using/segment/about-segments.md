---
solution: Journey Optimizer
product: journey optimizer
title: Sobre segmentos da Adobe Experience Platform
description: Saiba como configurar um segmento do Adobe Experience Platform
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 6c255d66fb89ba756add062d8a4315dd622fd8e7
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 8%

---

# Introdução a segmentos do Adobe Experience Platform {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="Segmento"
>abstract="Ao aproveitar os dados do perfil do cliente em tempo real, a Adobe Experience Platform permite criar segmentos direcionados com facilidade, que capturam os comportamentos e preferências exclusivos de seus clientes."

[!DNL Journey Optimizer]  O permite criar segmentos do Adobe Experience Platform usando dados do Perfil do cliente em tempo real diretamente da **[!UICONTROL Segmentos]** e use-as em suas jornadas ou campanhas.

Além disso, os segmentos também podem ser criados a partir do próprio serviço de Segmentação. Saiba mais na [Documentação do Serviço de segmentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

## Usar segmentos no [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Você pode aproveitar segmentos em **[!DNL Journey Optimizer]** de maneiras diferentes:

* Escolha um segmento como **público-alvo de uma campanha**, em que a mensagem é enviada a todos os indivíduos que pertencem ao segmento selecionado. [Saiba como definir o público de uma campanha](../campaigns/create-campaign.md#define-the-audience-audience).

* Use um **Ler segmento** atividade de orquestração em uma jornada para fazer com que todos os indivíduos no segmento entrem na jornada e recebam as mensagens incluídas na jornada.

   Digamos que você tenha um segmento de &quot;cliente prata&quot;. Com essa atividade, você pode fazer com que todos os clientes Silver insiram uma jornada e enviem uma série de mensagens personalizadas. [Saiba como configurar uma atividade de segmento de leitura](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Use o **Qualificação do segmento** atividade de evento em uma jornada para fazer com que os indivíduos entrem ou avancem na jornada com base nas entradas e saídas do segmento Adobe Experience Platform.

   Por exemplo, você pode fazer com que todos os novos clientes Silver insiram uma jornada e enviem mensagens. Para obter mais informações sobre como usar essa atividade, consulte [Saiba como configurar uma atividade de qualificação de segmento](../building-journeys/segment-qualification-events.md).

* Use o **Condição** atividade em uma jornada para criar condições com base na associação do segmento. [Saiba como usar segmentos em condições](../building-journeys/condition-activity.md#using-a-segment).

## Métodos de avaliação de público{#evaluation-method-in-journey-optimizer}

No Adobe Journey Optimizer, os públicos-alvo são gerados a partir das definições de segmento usando um dos dois métodos de avaliação:

* **Segmentação de transmissão**: a lista de públicos-alvo do segmento é mantida atualizada em tempo real à medida que novos dados fluem para o sistema.

   A segmentação de transmissão é um processo contínuo de seleção de dados que atualiza os segmentos em resposta à atividade do usuário. Depois que um segmento é criado e salvo, a definição do segmento é aplicada aos dados recebidos na Journey Optimizer. Isso significa que os indivíduos são adicionados ou removidos do segmento à medida que os dados do perfil mudam, garantindo que o público-alvo seja sempre relevante.

* **Segmentação em lote**: a lista de públicos-alvo do segmento é avaliada a cada 24 horas.

   A segmentação em lote é uma alternativa à segmentação por transmissão que processa todos os dados de perfil de uma só vez pelas definições de segmento. Isso cria um instantâneo do público-alvo que pode ser salvo e exportado para uso. No entanto, diferentemente da segmentação por transmissão, a segmentação em lote não atualiza continuamente a lista de públicos-alvo em tempo real, e os novos dados que chegam após o processo em lote não serão refletidos no segmento até o próximo processo em lote.&quot;

A determinação entre a segmentação em lote e a segmentação por transmissão é feita pelo sistema para cada definição de segmento, com base na complexidade e no custo da avaliação da regra de segmento. É possível exibir o método de avaliação para cada segmento na **[!UICONTROL Método de avaliação]** coluna da lista de segmentos.

![](assets/evaluation-method.png)

>[!NOTE]
>
>Se a variável **[!UICONTROL Método de avaliação]** não for exibida, é necessário adicioná-la usando o botão de configuração na parte superior direita da lista.

Depois de definir um segmento pela primeira vez, os perfis são adicionados ao público-alvo quando se qualificam.

O preenchimento retroativo de dados anteriores no público pode levar até 24 horas. Depois que o público-alvo é preenchido retroativamente, ele é mantido atualizado continuamente e está sempre pronto para o direcionamento.
