---
solution: Journey Optimizer
product: journey optimizer
title: Introdução às atividades de jornada
description: Introdução às atividades de jornada
feature: Journeys, Activities, Overview
topic: Journeys
role: User
level: Beginner, Intermediate
keywords: jornada, atividades, introdução, eventos, ação
exl-id: 239b3d72-3be0-4a82-84e6-f219e33ddca4
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 17%

---

# Introdução às atividades de jornada {#about-journey-activities}

Combine diferentes atividades de evento, orquestração e ação para criar cenários de canais em várias etapas.

## Atividades de eventos {#event-activities}

Eventos são o que aciona uma jornada personalizada, como uma compra online. Uma vez que alguém entra em uma jornada, ele se move como um indivíduo, e não há dois indivíduos se movendo ao longo da mesma taxa ou ao longo do mesmo caminho. Ao iniciar a jornada com um evento, a jornada é acionada ao receber o evento. Cada pessoa na jornada segue, individualmente, as próximas etapas definidas na jornada.

Eventos configurados pelo usuário técnico (consulte [esta página](../event/about-events.md)) são exibidos na primeira categoria da paleta, no lado esquerdo da tela. As seguintes atividades de eventos estão disponíveis:

* [Eventos gerais](../building-journeys/general-events.md)
* [Reação](../building-journeys/reaction-events.md)
* [Qualificação do público-alvo](../building-journeys/audience-qualification-events.md)

![](assets/journey43.png)

Inicie a jornada arrastando e soltando uma atividade de evento. Você também pode clicar duas vezes nela.

![](assets/journey44.png)

## Atividades de orquestração {#orchestration-activities}

As atividades de orquestração são condições diferentes que ajudam a determinar a próxima etapa da jornada. Pode ser se a pessoa tiver um caso de suporte aberto ou não, a previsão do tempo em seu local atual, se ela concluiu uma compra ou não, ou atingiu 10.000 pontos de fidelidade.

Na paleta, no lado esquerdo da tela, as seguintes atividades de orquestração estão disponíveis:

* [Condição](../building-journeys/condition-activity.md)
* [Aguardar](../building-journeys/wait-activity.md)
* [Ler público-alvo](../building-journeys/read-audience.md)

![](assets/journey49.png)

## Atividades de ação {#action-activities}

As ações são o que você deseja que aconteça como resultado de algum tipo de acionador, como enviar uma mensagem. É a parte da jornada que o cliente experimenta.

Na paleta, no lado esquerdo da tela, abaixo de **[!UICONTROL Eventos]** e **[!UICONTROL Orquestração]**, você pode encontrar o **[!UICONTROL Ações]** categoria. As seguintes atividades de ação estão disponíveis:

* [Email, SMS, Push](../building-journeys/journeys-message.md)
* [Ações personalizadas](../building-journeys/using-custom-actions.md)
* [Salto](../building-journeys/jump.md)

![](assets/journey58.png)

Essas atividades representam os diferentes canais de comunicação disponíveis. É possível combiná-los para criar um cenário entre canais.

Se você tiver configurado ações personalizadas, elas também aparecerão aqui. [Saiba mais](../building-journeys/using-custom-actions.md)).

## Práticas recomendadas {#best-practices}

### Adicionar um rótulo

A maioria das atividades permite definir um **[!UICONTROL Rótulo]**. Isso adiciona um sufixo ao nome que aparecerá na atividade na tela. Isso é útil se você usar a mesma atividade várias vezes na jornada e quiser identificá-la mais facilmente. Também facilitará a depuração em caso de erros e facilitará a leitura dos relatórios. Você também pode adicionar um **[!UICONTROL Descrição]**.

![](assets/journey-action-label.png)

>[!NOTE]
>
>Para algumas atividades, a ID também está visível no painel. Essa ID pode ser usada nos relatórios como uma chave mais estável do que o rótulo, que pode mudar.

### Gerenciar os parâmetros avançados {#advanced-parameters}

A maioria das atividades do exibe vários parâmetros avançados e/ou técnicos que você não pode modificar.

![](assets/journey-advanced-parameters.png)

Para melhorar a compreensão, é possível ocultar esses parâmetros usando o **[!UICONTROL Ocultar campos somente leitura]** botão.

![](assets/journey-hide-read-only-fields.png)

Em alguns contextos específicos, é possível substituir os valores desses parâmetros para uso específico. Para forçar um valor, clique no ícone **[!UICONTROL Habilitar substituição de parâmetro]** à direita do campo. [Saiba mais](../configuration/primary-email-addresses.md#journey-parameters)

![](assets/journey-enable-parameter-override.png)

### Adicionar um caminho alternativo

A jornada de uma pessoa para quando ocorre um erro em uma ação ou condição. A única maneira de fazê-lo continuar é marcando a caixa **[!UICONTROL Adicionar um caminho alternativo em caso de tempo limite ou erro]**. Consulte [esta seção](../building-journeys/using-the-journey-designer.md#paths).

![](assets/journey42.png)
