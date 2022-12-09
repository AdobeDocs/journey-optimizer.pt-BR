---
solution: Journey Optimizer
product: journey optimizer
title: Introdução às atividades de jornada
description: Introdução às atividades de jornada
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 239b3d72-3be0-4a82-84e6-f219e33ddca4
source-git-commit: ca423c25d39162838368b2242c1aff99388df768
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Introdução às atividades de jornada {#about-journey-activities}

Combine diferentes atividades de evento, orquestração e ação para criar cenários de canais em várias etapas.

## Atividades de eventos {#event-activities}

Eventos são o que aciona uma jornada personalizada, como uma compra online. Uma vez que alguém entra em uma jornada, ele se move como um indivíduo, e nenhum outro indivíduo se move ao mesmo ritmo ou ao longo do mesmo caminho. Quando você inicia a jornada com um evento, a jornada é acionada quando o evento é recebido. Cada pessoa na jornada segue, individualmente, as próximas etapas definidas na jornada.

Eventos configurados pelo usuário técnico (consulte [esta página](../event/about-events.md)) são exibidas na primeira categoria da paleta, no lado esquerdo da tela. As seguintes atividades de eventos estão disponíveis:

* [Eventos gerais](../building-journeys/general-events.md)
* [Reação](../building-journeys/reaction-events.md)
* [Qualificação do segmento](../building-journeys/segment-qualification-events.md)

![](assets/journey43.png)

Inicie sua jornada arrastando e soltando uma atividade de evento. Você também pode clicar duas vezes nela.

![](assets/journey44.png)

## Atividades de orquestração {#orchestration-activities}

As atividades de orquestração são condições diferentes que ajudam a determinar a próxima etapa da jornada. Pode ser que a pessoa tenha ou não um caso de apoio aberto, as previsões meteorológicas no seu local atual, se tiver concluído uma compra ou não, ou tenha atingido 10.000 pontos de fidelidade.

Na paleta, no lado esquerdo da tela, as seguintes atividades de orquestração estão disponíveis:

* [Condição](../building-journeys/condition-activity.md)
* [Aguardar](../building-journeys/wait-activity.md)
* [Ler segmento](../building-journeys/read-segment.md)

![](assets/journey49.png)

## Atividades de ação {#action-activities}

As ações são o que você deseja que ocorra como resultado de algum tipo de acionador, como enviar uma mensagem. É a jornada que o cliente experimenta.

Na paleta, no lado esquerdo da tela, abaixo **[!UICONTROL Events]** e **[!UICONTROL Orchestration]**, você pode encontrar o **[!UICONTROL Actions]** categoria . As seguintes atividades de ação estão disponíveis:

* [Email, SMS, Push](../building-journeys/journeys-message.md)
* [Ações personalizadas](../building-journeys/using-custom-actions.md)
* [Salto](../building-journeys/jump.md)

![](assets/journey58.png)

Essas atividades representam os diferentes canais de comunicação disponíveis. É possível combiná-los para criar um cenário entre canais.

Se você configurou ações personalizadas, elas também são exibidas aqui. [Saiba mais](../building-journeys/using-custom-actions.md)).

## Práticas recomendadas {#best-practices}

A maioria das atividades permite definir um **[!UICONTROL Label]**. Isso adiciona um sufixo ao nome que aparecerá sob sua atividade na tela. Isso é útil se você usar a mesma atividade várias vezes em sua jornada e quiser identificá-las mais facilmente. Também facilitará a depuração em caso de erros e facilitará a leitura dos relatórios. Você também pode adicionar uma **[!UICONTROL Description]**.

![](assets/journey59bis.png)

Quando ocorre um erro em uma ação ou condição, a jornada de um indivíduo para. A única maneira de fazê-lo continuar é marcando a caixa **[!UICONTROL Add an alternative path in case of a timeout or an error]**. Consulte [esta seção](../building-journeys/using-the-journey-designer.md#paths).

![](assets/journey42.png)
