---
solution: Journey Optimizer
product: journey optimizer
title: Trabalhar com atividades de campanha orquestradas
description: Saiba como organizar atividades de campanha
exl-id: 02f986b2-8200-4e0e-8918-44e528a6a3ec
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/OUKBJeSTaPJKav-NNCCxKZ8esY-62JkdRMmcwoJpZJ0
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29c
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: e232ccfded6b522d99a93d8368cb8085231ccac7
workflow-type: tm+mt
source-wordcount: 530
ht-degree: 44%

---

# Sobre atividades de campanha orquestradas {#orchestrated-campaign-activities}

As atividades da campanha orquestrada são agrupadas em três categorias. Dependendo do contexto, as atividades disponíveis podem ser diferentes.

Todas as atividades estão detalhadas nas seções abaixo:

* [Atividades de direcionamento](#targeting)
* [Atividades do canal](#channel)
* [Atividades de controle do fluxo](#flow-control)

![Lista de atividades disponíveis na tela](../assets/orchestrated-activities.png){width="80%" align="left"}

>[!NOTE]
>
>Dependendo do modelo de licenciamento, das permissões e da implementação, as atividades disponíveis podem ser diferentes.

## Medidas de proteção e limitações {#activity-guardrails}

* **Limite de atividades do canal** - Uma campanha Orquestrada oferece suporte a no máximo 10 atividades de canal em publicação (Email, SMS, Push ou Correspondência direta). O direcionamento e as atividades de controle de fluxo não contam para esse limite.

* **Limite de atividades da tela** - O número de atividades na tela é limitado a 500. Para manutenção e desempenho, mantenha os workflows abaixo de 100 atividades na prática.

Consulte [Medidas de proteção e limitações](../guardrails.md) para todas as medidas de proteção e limitações de campanhas orquestradas.

## Atividades de direcionamento {#targeting}

Estas atividades são especificamente para direcionamento. Elas permitem criar uma ou mais direções definindo um público-alvo e dividindo ou combinando esses públicos-alvo usando operações de interseção, união ou exclusão.

![Lista de atividades de direcionamento](../assets/targeting-activities.png){width="40%" align="left"}

As atividades de direcionamento disponíveis são:

* [Criar público-alvo](build-audience.md): defina a sua população-alvo. Você pode selecionar um público-alvo existente ou usar o criador de regras para definir sua própria consulta.
* [Alterar dimensão](change-dimension.md): altere a targeting dimension enquanto você estiver criando sua campanha Orquestrada.
* [Combinar](combine.md): aplique uma segmentação à sua população de entrada. Você pode usar uma união, uma interseção ou uma exclusão.
* [Desduplicação](deduplication.md): exclua duplicatas no(s) resultado(s) das atividades de entrada.
* [Enriquecimento](enrichment.md): definir dados adicionais para processar em sua campanha Orquestrada. Com essa atividade, você pode aproveitar a transição de entrada e configurar a atividade para concluir a transição de saída com dados adicionais.
* [Reconciliação](reconciliation.md): defina o vínculo entre os dados do Journey Optimizer e os dados de uma tabela de trabalho, como, por exemplo, dados carregados de um arquivo externo.
* [Divisão](split.md): segmente a população de entrada em vários subconjuntos.

## Atividades do canal {#channel}

O Adobe Journey Optimizer permite automatizar e executar campanhas de marketing em diversos canais. Você pode combinar [atividades de canal](channels.md) na tela para criar uma campanha Orquestrada entre canais que pode acionar ações com base no comportamento do cliente.

Saiba como [criar uma ação de canal em uma campanha orquestrada](channels.md).

## Atividades de controle do fluxo {#flow-control}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_end"
>title="Atividade de término"
>abstract="A atividade **End** marca o fim de uma ramificação na tela. Opcionalmente, use **Sinal externo** para iniciar uma campanha orquestrada downstream e transmitir parâmetros quando a ramificação for concluída. [Saiba mais](../trigger-orchestrated-campaign.md#signal-end)"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_signal"
>title="Sinal externo"
>abstract="Selecione a campanha orquestrada downstream para começar quando esta ramificação terminar e mapeie os nomes e valores dos parâmetros para enviar no sinal. A campanha downstream deve ser definida como **Acionada por um sinal** e publicada antes que esta campanha atinja a atividade End. [Saiba mais](../trigger-orchestrated-campaign.md#signal-end)"

As atividades a seguir são específicas para organizar e executar campanhas orquestradas. Sua principal tarefa é coordenar as outras atividades.

![Lista de atividades de controle do fluxo](../assets/flow-control-activities.png){width="20%" align="left"}

As atividades de controle de fluxo disponíveis são:

* [And-join](and-join.md): sincroniza várias ramificações de execução de uma campanha Orquestrada.
* [Bifurcação](fork.md): crie transições de saída para iniciar várias atividades ao mesmo tempo.
* [Aguardar](wait.md): pausar momentaneamente a execução de uma parte de uma campanha Orquestrada.
  <!--* [Test](test.md): Enable transitions based on specified conditions.-->

* **[!UICONTROL Fim]**: marca o fim de uma ramificação na tela. Opcionalmente, é possível usá-lo para enviar um sinal para outra campanha Orquestrada que começa em um sinal. [Saiba mais](../trigger-orchestrated-campaign.md#signal-end)
