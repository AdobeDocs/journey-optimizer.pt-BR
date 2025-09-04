---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade Bifurcação
description: Saiba como usar a atividade Bifurcação em uma campanha orquestrada
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 86%

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

A atividade **[!UICONTROL Bifurcação]** é um componente de **[!UICONTROL Controle do fluxo]** que permite criar várias transições de saída, permitindo que várias atividades sejam executadas em paralelo.

## Configuração da atividade de bifurcação{#fork-configuration}

Siga estas etapas para configurar a atividade **[!UICONTROL Bifurcação]**:

![](../assets/workflow-fork.png)

1. Adicione uma atividade **[!UICONTROL Fork]** à sua campanha Orquestrada.

1. Defina um **[!UICONTROL Rótulo]**.

1. Atribua um rótulo a cada transição de saída. Por padrão, duas transições são fornecidas.

1. Para remover uma transição, clique no ícone ![](../assets/do-not-localize/Smock_Delete_18_N.svg).

1. Se necessário, clique em **[!UICONTROL Adicionar transição]** para adicionar outra transição de saída.
