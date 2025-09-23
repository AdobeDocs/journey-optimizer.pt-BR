---
solution: Journey Optimizer
product: journey optimizer
title: Métricas do Journey Optimizer Experimentation Accelerator
description: Melhore sua capacidade de conduzir experimentos com eficiência e gerar insights
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: conteúdo, experimento, vários, público-alvo, tratamento
hide: true
hidefromtoc: true
exl-id: 74868625-f4ea-44f9-ae2a-8e5fdd22a081
source-git-commit: 70fce6fae4db58c72496945c50155dbd0b4986b4
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 2%

---

# Métricas {#experiment-accelerator-metrics}

>[!BEGINSHADEBOX]

* [Introdução à Journey Optimizer Experimentation Accelerator](experiment-accelerator.md)
* [Uso de dados na IA com o Journey Optimizer Experimentation Accelerator](experiment-accelerator-security.md)
* [Práticas recomendadas do Journey Optimizer Experimentation Accelerator](experiment-accelerator-best-practices.md)
* [Monitorar experimentos](experiment-accelerator-monitor.md)
* **[Métricas de experimentação](experiment-accelerator-metrics.md)**

>[!ENDSHADEBOX]

A página **[!UICONTROL Métricas]** exibe as métricas de sucesso dos experimentos do Journey Optimizer e do Target em um único local, permitindo o monitoramento do desempenho, a comparação e insights mais profundos.

## Painel {#dashboard}

Ao acessar a guia **[!UICONTROL Métricas]**, todas as métricas de sucesso disponíveis do Journey Optimizer e do Adobe Target são listadas em uma exibição consolidada para ajudá-lo a acompanhar o desempenho nas iniciativas, comparar resultados e identificar rapidamente as áreas que exigem atenção.

Acesse filtros clicando em ![](assets/do-not-localize/Smock_Filter_18_N.svg), que oferece opções específicas de contexto, como filtragem por **[!UICONTROL Source]** ou **[!UICONTROL Usado em experimentos ativos]**.

Como alternativa, localize rapidamente qualquer métrica digitando seu nome na barra de pesquisa.

![](assets/experiment-monitor-metrics.png)

## Detalhes da métrica {#metric-details}

### Incremental ao longo do tempo

![](assets/experiment-monitor-metrics-2.png)

O gráfico **[!UICONTROL Incremental ao longo do tempo]** fornece um detalhamento visual de como a métrica selecionada está em tendência ao longo de um intervalo de tempo escolhido. Use o menu suspenso para alternar entre exibições diárias ou semanais a fim de ajustar o nível de granularidade.

Os seguintes valores de resumo estão disponíveis para referência rápida:

* **[!UICONTROL Total]**: o valor cumulativo da métrica selecionada durante o período do relatório.

* **[!UICONTROL Média]**: o valor típico da métrica calculada através do intervalo de tempo selecionado. Ao equilibrar as flutuações diárias ou semanais, ele fornece um quadro mais claro do desempenho normal e pode ser usado como uma linha de base para comparação.

* **[!UICONTROL Taxa de conversão]**: porcentagem de perfis que concluíram a ação desejada (por exemplo, compra, inscrição) após verem o tratamento.

Cada valor inclui uma alteração de porcentagem em relação ao período anterior, tornando fácil ver se o desempenho está melhorando, diminuindo ou permanecendo estável.

### Efeito do experimento

Esta seção exibe todos os experimentos ativos dentro do período selecionado (Últimos 90 dias, Últimos 30 dias ou Últimos 7 dias) e destaca sua contribuição para a métrica.

As seguintes métricas estão disponíveis:

* **[!UICONTROL Aumento]**: medida da melhora da porcentagem na taxa de conversão de um determinado tratamento em relação à linha de base.

* **[!UICONTROL Confiança]**: evidência de que um determinado tratamento é igual ao tratamento de linha de base. [Saiba mais](../content-management/experiment-calculations.md#understand-confidence)

* **[!UICONTROL Contribuição]**: a proporção da alteração geral na métrica que pode ser atribuída a um experimento ou tratamento específico, permitindo a identificação das iniciativas que exercem o maior impacto relativo.
