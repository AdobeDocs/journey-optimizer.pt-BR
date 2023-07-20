---
solution: Journey Optimizer
product: journey optimizer
title: Sobre públicos da Adobe Experience Platform
description: Saiba como trabalhar com públicos da Adobe Experience Platform
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 5%

---

# Introdução aos públicos da Adobe Experience Platform {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="Público-alvo"
>abstract="Ao aproveitar os dados do perfil do cliente em tempo real, a Adobe Experience Platform permite gerar definições de segmentos com facilidade para criar públicos-alvo que capturam os comportamentos e preferências individuais de seus clientes."

[!DNL Journey Optimizer] O permite criar e aproveitar públicos-alvo da Adobe Experience Platform usando dados do Perfil do cliente em tempo real diretamente da **[!UICONTROL Públicos-alvo]** e use-as em suas jornadas ou campanhas.

Saiba mais na [Documentação do Serviço de segmentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

## Usar públicos-alvo no [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Você pode aproveitar públicos-alvo na **[!DNL Journey Optimizer]** de maneiras diferentes:

* Escolha um público-alvo para um **campaign**, em que a mensagem é enviada a todos os indivíduos que pertencem ao público selecionado. [Saiba como definir o público de uma campanha](../campaigns/create-campaign.md#define-the-audience-audience).

* Use um **Ler público** atividade de orquestração em uma jornada para fazer com que todos os indivíduos no público-alvo entrem na jornada e recebam as mensagens incluídas na jornada.

  Digamos que você tenha um público-alvo de &quot;cliente prata&quot;. Com essa atividade, você pode fazer com que todos os clientes Silver insiram uma jornada e enviem uma série de mensagens personalizadas. [Saiba como configurar uma atividade Ler público](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

* Use o **Qualificação de público** atividade de evento em uma jornada para fazer com que os indivíduos entrem ou avancem na jornada com base nas entradas e saídas do público-alvo do Adobe Experience Platform.

  Por exemplo, você pode fazer com que todos os novos clientes Silver insiram uma jornada e enviem mensagens. Para obter mais informações sobre como usar essa atividade, consulte [Saiba como configurar uma atividade de qualificação de público-alvo](../building-journeys/audience-qualification-events.md).

* Use o **Condição** atividade em uma jornada para criar condições com base na associação de público-alvo. [Saiba como usar públicos-alvo em condições](../building-journeys/condition-activity.md#using-a-segment).

## Métodos de avaliação de público{#evaluation-method-in-journey-optimizer}

No Adobe Journey Optimizer, os públicos-alvo são gerados a partir das definições de segmento usando um dos dois métodos de avaliação:

* **Segmentação de transmissão**: a lista de perfis do público-alvo é mantida atualizada em tempo real à medida que novos dados fluem para o sistema.

  A segmentação de transmissão é um processo contínuo de seleção de dados que atualiza seus públicos-alvo em resposta à atividade do usuário. Depois que uma definição de segmento é criada e o público-alvo resultante é salvo, a definição de segmento é aplicada aos dados recebidos na Journey Optimizer. Isso significa que as pessoas físicas são adicionadas ou removidas do público-alvo à medida que os dados do perfil são alterados, garantindo que o público-alvo seja sempre relevante.

* **Segmentação em lote**: a lista de perfis do público-alvo é avaliada a cada 24 horas.

  A segmentação em lote é uma alternativa à segmentação por transmissão que processa todos os dados de perfil de uma só vez pelas definições de segmento. Isso cria um instantâneo do público-alvo que pode ser salvo e exportado para uso. No entanto, diferentemente da segmentação por transmissão, a segmentação em lote não atualiza continuamente a lista de públicos-alvo em tempo real, e os novos dados que chegam após o processo em lote não serão refletidos no público-alvo até o próximo processo em lote.&quot;

A determinação entre a segmentação em lote e a segmentação por transmissão é feita pelo sistema para cada público, com base na complexidade e no custo da avaliação da regra de definição de segmento. É possível visualizar o método de avaliação para cada público-alvo na **[!UICONTROL Método de avaliação]** da lista de públicos-alvo.

![](assets/evaluation-method.png)

>[!NOTE]
>
>Se a variável **[!UICONTROL Método de avaliação]** não for exibida, é necessário adicioná-la usando o botão de configuração na parte superior direita da lista.

Depois de definir um público-alvo pela primeira vez, os perfis são adicionados ao público-alvo quando se qualificam.

O preenchimento retroativo de dados anteriores no público pode levar até 24 horas. Depois que o público-alvo é preenchido retroativamente, ele é mantido atualizado continuamente e está sempre pronto para o direcionamento.
