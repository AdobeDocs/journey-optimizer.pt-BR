---
solution: Journey Optimizer
product: journey optimizer
title: Sobre públicos-alvo da Adobe Experience Platform
description: Saiba como trabalhar com públicos-alvo da Adobe Experience Platform
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: d3aecaefb0b356eb1d25b151e8d210620b51ea5f
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 92%

---

# Introdução aos públicos-alvo da Adobe Experience Platform {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="Público-alvo"
>abstract="Ao aproveitar os dados do perfil do cliente em tempo real, a Adobe Experience Platform permite criar facilmente definições de segmento para criar públicos-alvo que capturam as preferências e os comportamentos exclusivos dos clientes."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_audience"
>title="Selecione o público-alvo da campanha"
>abstract="Esta lista exibe todos os públicos-alvo disponíveis na Adobe Experience Platform. Selecione o público-alvo a ser direcionado pela campanha. A mensagem configurada na campanha será enviada a todas as pessoas pertencentes ao público-alvo selecionado. [Saiba mais sobre públicos-alvo](../audience/about-audiences.md)"

O [!DNL Journey Optimizer] permite criar e aproveitar públicos-alvo da Adobe Experience Platform usando dados do Perfil do cliente em tempo real diretamente do menu **[!UICONTROL Públicos-alvo]** e usá-los em suas jornadas ou campanhas. Saiba mais na [Documentação do Serviço de segmentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=pt-BR).

## Utilização de públicos-alvo no [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Você pode selecionar em campanhas e jornadas qualquer público da Adobe Experience Platform gerado usando [definições de segmento](../audience/creating-a-segment-definition.md).

>[!NOTE]
>
>Além disso, também é possível direcionar públicos-alvo da Adobe Experience Platform criados com o [composições de público](../audience/get-started-audience-orchestration.md) ou [carregado de um arquivo CSV](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience){target="_blank"}. No momento, esses recursos estão disponíveis como um beta privado.

É possível aproveitar os públicos-alvo no **[!DNL Journey Optimizer]** de maneiras diferentes:

* Escolha um público para uma **campanha**, na qual a mensagem é enviada a todos os indivíduos que pertencem ao público-alvo selecionado. [Saiba como definir o público-alvo de uma campanha](../campaigns/create-campaign.md#define-the-audience-audience).

* Use uma atividade de orquestração **Ler público-alvo** em uma jornada para fazer com que todas as pessoas físicas no público entrem na jornada e recebam as mensagens incluídas na jornada.

  Digamos que você tenha um público-alvo de “cliente prata”. Com essa atividade, você pode fazer com que todos os clientes prata entrem em uma jornada e enviar-lhes uma série de mensagens personalizadas. [Saiba como configurar uma atividade Ler público-alvo](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

* Use a atividade de evento **Qualificação de público-alvo** em uma jornada para fazer com que as pessoas físicas entrem ou avancem na jornada com base nas entradas e saídas de público do Adobe Experience Platform.

  Por exemplo, é possível fazer com que todos os novos clientes prata entrem em uma jornada e enviar-lhes mensagens. Para obter mais informações sobre como usar essa atividade, consulte [Saiba como configurar uma atividade de qualificação de público-alvo](../building-journeys/audience-qualification-events.md).

* Use a atividade **Condição** em uma jornada para criar condições com base na associação de público-alvo. [Saiba como usar públicos-alvo em condições](../building-journeys/condition-activity.md#using-a-segment).

## Métodos de avaliação de público-alvo{#evaluation-method-in-journey-optimizer}

No Adobe Journey Optimizer, os públicos-alvo são gerados a partir das definições de segmento usando um dos dois métodos de avaliação:

* **Segmentação por transmissão**: a lista de perfis do público-alvo é mantida atualizada em tempo real à medida que novos dados fluem para o sistema.

  A segmentação por transmissão é um processo contínuo de seleção de dados que atualiza os públicos-alvo em resposta à atividade do usuário. Depois que uma definição de segmento é criada e o público-alvo resultante é salvo, a definição de segmento é aplicada aos dados recebidos no Journey Optimizer. Isso significa que as pessoas físicas são adicionadas ou removidas do público à medida que os dados do perfil são alterados, garantindo que o público seja sempre relevante.

* **Segmentação em lote**: a lista de perfis do público-alvo é avaliada a cada 24 horas.

  A segmentação em lote é uma alternativa à segmentação por transmissão que processa todos os dados de perfil de uma só vez através das definições de segmento. Isso cria um instantâneo do público-alvo que pode ser salvo e exportado para uso. No entanto, diferentemente da segmentação por transmissão, a segmentação em lote não atualiza continuamente a lista de públicos-alvo em tempo real, e os novos dados que chegam após o processamento do lote não serão refletidos no público-alvo até o próximo processamento do lote.

A determinação entre a segmentação em lote e a segmentação por transmissão é feita pelo sistema para cada público-alvo, com base na complexidade e no custo da avaliação da regra de definição de segmento. É possível visualizar o método de avaliação para cada público-alvo na coluna **[!UICONTROL Método de avaliação]** da lista de públicos-alvo.

![](assets/evaluation-method.png)

>[!NOTE]
>
>Se a coluna **[!UICONTROL Método de avaliação]** não for exibida, será necessário adicioná-la usando o botão de configuração na parte superior direita da lista.

Depois de definir um público-alvo pela primeira vez, perfis serão adicionados ele quando se qualificarem.

O preenchimento retroativo de dados anteriores no público-alvo pode levar até 24 horas. Depois que o público-alvo é preenchido retroativamente, ele será mantido atualizado continuamente e está sempre pronto para o direcionamento.
