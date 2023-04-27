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

[!DNL Journey Optimizer]  permite criar segmentos do Adobe Experience Platform usando dados de Perfil do cliente em tempo real diretamente do **[!UICONTROL Segmentos]** e usá-las em suas jornadas ou campanhas.

Além disso, os segmentos também podem ser criados no próprio serviço de Segmentação. Saiba mais na [Documentação do Serviço de segmentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

## Use segmentos em [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Você pode aproveitar os segmentos em **[!DNL Journey Optimizer]** de diferentes maneiras:

* Escolha um segmento como o **público-alvo de uma campanha**, em que a mensagem é enviada para todos os indivíduos pertencentes ao segmento selecionado. [Saiba como definir o público-alvo de uma campanha](../campaigns/create-campaign.md#define-the-audience-audience).

* Use um **Ler segmento** atividade de orquestração em uma jornada para fazer com que todos os indivíduos no segmento entrem na jornada e recebam as mensagens incluídas na jornada.

   Digamos que você tenha um segmento de &quot;cliente prateado&quot;. Com essa atividade, é possível fazer com que todos os clientes prateados insiram uma jornada e enviem uma série de mensagens personalizadas. [Saiba como configurar uma atividade Read segment](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Use o **Qualificação do segmento** atividade de evento em uma jornada para fazer com que os indivíduos entrem ou avancem na jornada com base nas entradas e saídas do segmento Adobe Experience Platform.

   Por exemplo, você pode fazer com que todos os novos clientes de prata insiram uma jornada e enviem mensagens para eles. Para obter mais informações sobre como usar essa atividade, consulte [Saiba como configurar uma atividade de qualificação de segmento](../building-journeys/segment-qualification-events.md).

* Use o **Condição** em uma jornada para criar condições com base na associação de segmentos. [Saiba como usar segmentos em condições](../building-journeys/condition-activity.md#using-a-segment).

## Métodos de avaliação do público-alvo{#evaluation-method-in-journey-optimizer}

No Adobe Journey Optimizer, os públicos-alvo são gerados a partir das definições de segmento usando um dos dois métodos de avaliação:

* **Segmentação de streaming**: A lista de públicos-alvo do segmento é mantida atualizada em tempo real à medida que novos dados fluem para o sistema.

   A segmentação de transmissão é um processo contínuo de seleção de dados que atualiza os segmentos em resposta à atividade do usuário. Depois que um segmento é criado e salvo, a definição do segmento é aplicada em relação aos dados recebidos no Journey Optimizer. Isso significa que os indivíduos são adicionados ou removidos do segmento à medida que seus dados de perfil são alterados, garantindo que o público-alvo seja sempre relevante.

* **Segmentação em lote**: A lista de públicos-alvo do segmento é avaliada a cada 24 horas.

   A segmentação em lote é uma alternativa à segmentação de fluxo que processa todos os dados de perfil de uma só vez por meio das definições de segmento. Isso cria um instantâneo do público-alvo que pode ser salvo e exportado para uso. No entanto, diferentemente da segmentação de streaming, a segmentação em lote não atualiza continuamente a lista de públicos-alvo em tempo real, e os novos dados que entram após o processo em lote não serão refletidos no segmento até o próximo processo em lote.&quot;

A determinação entre a segmentação de lote e a segmentação de fluxo é feita pelo sistema para cada definição de segmento, com base na complexidade e no custo da avaliação da regra de segmento. Você pode visualizar o método de avaliação para cada segmento na **[!UICONTROL Método de avaliação]** da lista de segmentos.

![](assets/evaluation-method.png)

>[!NOTE]
>
>Se a variável **[!UICONTROL Método de avaliação]** não for exibida, é necessário adicioná-la usando o botão de configuração na parte superior direita da lista.

Após ter definido um segmento pela primeira vez, os perfis são adicionados ao público-alvo quando se qualificam.

O preenchimento retroativo do público-alvo a partir de dados anteriores pode demorar até 24 horas. Após o preenchimento retroativo do público-alvo, ele é continuamente atualizado e está sempre pronto para o direcionamento.
