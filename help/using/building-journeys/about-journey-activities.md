---
title: Sobre as atividades do jornada
description: Saiba mais sobre as atividades do jornada
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 25%

---

# Sobre as atividades do jornada {#about-journey-activities}

![](../assets/do-not-localize/badge.png)

Combine diferentes atividades de evento, orquestração e ação para criar cenários de canais em várias etapas.

## Atividades de eventos {#event-activities}

Os eventos configurados pelo usuário técnico (consulte [this page](../event/about-events.md)) são exibidos na primeira categoria da paleta, no lado esquerdo da tela. As seguintes atividades de eventos estão disponíveis:

* [Eventos gerais](../building-journeys/general-events.md)
* [Reação](../building-journeys/reaction-events.md)
* [Qualificação do segmento](../building-journeys/segment-qualification-events.md)

![](../assets/journey43.png)

Inicie a jornada arrastando e soltando uma atividade de evento. Você também pode clicar duas vezes nela.

![](../assets/journey44.png)

## Atividades de orquestração {#orchestration-activities}

Na paleta, no lado esquerdo da tela, as seguintes atividades de orquestração estão disponíveis:

* [Condição](../building-journeys/condition-activity.md)
* [End](../building-journeys/end-activity.md)
* [Aguardar](../building-journeys/wait-activity.md)
* [Ler segmento](../building-journeys/read-segment.md)

![](../assets/journey49.png)

## Atividades de ação {#action-activities}

Na paleta, no lado esquerdo da tela, abaixo de **[!UICONTROL Events]** e **[!UICONTROL Orchestration]**, você encontrará a categoria **[!UICONTROL Actions]**. As seguintes atividades de ação estão disponíveis:

* [Mensagem](../building-journeys/journeys-message.md)
* [Ações personalizadas](../building-journeys/using-custom-actions.md)
* [Salto](../building-journeys/jump.md)

![](../assets/journey58.png)

Essas atividades representam os diferentes canais de comunicação disponíveis. É possível combiná-los para criar um cenário entre canais.

Se você configurou ações personalizadas, elas serão exibidas aqui (consulte [esta página](../building-journeys/using-custom-actions.md)).

## Práticas recomendadas {#best-practices}

A maioria das atividades permite definir um **[!UICONTROL Label]**. Isso adiciona um sufixo ao nome que aparecerá sob sua atividade na tela. Isso é útil se você usar a mesma atividade várias vezes na jornada e quiser identificá-las mais facilmente. Também facilitará a depuração em caso de erros e facilitará a leitura dos relatórios. Você também pode adicionar um **[!UICONTROL Description]** opcional.

![](../assets/journey59bis.png)

A jornada de uma pessoa para quando ocorre um erro em uma ação ou condição. O único modo de fazê-la continuar é marcando a caixa **[!UICONTROL Add an alternative path in case of a timeout or an error]**. Consulte [esta seção](../building-journeys/using-the-journey-designer.md#paths).

![](../assets/journey42.png)
