---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade Fork
description: Saiba como usar a atividade Bifurcação em uma campanha orquestrada
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
source-git-commit: 2935e611bb9682256a324485b28e7dd2552e1dd2
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 59%

---

# Bifurcação {#fork}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork"
>title="Atividade Bifurcação"
>abstract="A atividade **Bifurcação** permite criar transições de saída para iniciar várias atividades ao mesmo tempo."


>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork_transitions"
>title="Transições da atividade bifurcação"
>abstract="Por padrão, duas transições são criadas com uma atividade **Bifurcação**. Clique em **Adicionar transição** para definir uma transição de saída adicional e insira seu rótulo."

+++ Sumário

| Bem-vindo às campanhas orquestradas | Iniciar sua primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](gs-orchestrated-campaigns.md)<br/><br/>[Etapas de configuração](configuration-steps.md)<br/><br/>[Etapas principais para a criação de campanhas orquestradas](gs-campaign-creation.md) | [Criar uma campanha orquestrada](create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](orchestrate-activities.md)<br/><br/>[Enviar mensagens com campanhas orquestradas](send-messages.md)<br/><br/>[Iniciar e monitorar a campanha](start-monitor-campaigns.md)<br/><br/>[Relatórios](reporting-campaigns.md) | [Trabalhar com o Query Modeler](orchestrated-query-modeler.md)<br/><br/>[Criar sua primeira consulta](build-query.md)<br/><br/>[Editar expressões](edit-expressions.md) | [Introdução às atividades](activities/about-activities.md)<br/><br/>Atividades:<br/>[And-join](activities/and-join.md) - [Criar público](activities/build-audience.md) - [Alterar dimensão](activities/change-dimension.md) - [Combinar](activities/combine.md) - [Eliminação de Duplicação](activities/deduplication.md) - [Enriquecimento](activities/enrichment.md) - [Bifurcação](activities/fork.md) - [Reconciliação](activities/reconciliation.md) - [Divisão](activities/split.md) - [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/><br/>

A atividade **Bifurcação** é uma atividade de **Controle de fluxo**. Ela permite criar transições de saída para iniciar várias atividades ao mesmo tempo.

## Configurar a atividade de bifurcação{#fork-configuration}

Siga estas etapas para configurar a atividade de **Bifurcação**:

![](../assets/workflow-fork.png)

1. Adicione uma atividade **Fork** à sua campanha orquestrada.
1. Clique em **Adicionar transição** para adicionar uma nova transição de saída. Por padrão, são definidas duas transições.
1. Adicione um rótulo a cada transição.

## Exemplo{#fork-example}

No exemplo a seguir, estaremos usando duas atividades de **Bifurcação**:

* Uma antes das duas consultas, para executá-las ao mesmo tempo.
* Uma após a interseção, para enviar um email e um SMS simultaneamente à população direcionada.

![](../assets/workflow-fork-example.png)
