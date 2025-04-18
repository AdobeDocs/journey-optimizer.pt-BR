---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade Fork
description: Saiba como usar a atividade Bifurcação em uma campanha orquestrada
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
source-git-commit: bdc584c1aae0c735d81dfc95e11f96f755bea26a
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 83%

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
