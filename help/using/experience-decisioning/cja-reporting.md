---
title: Relatório de decisões
description: Saiba como criar relatórios sobre a Decisão.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 7c45cd8a-8e86-4646-ba0a-db393e92d9da
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/jbakmb7S9cFitmpa7ypVe8YrYvbZh0E0VogYi3KpNbo
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 270
ht-degree: 4%

---

# Relatório de decisões {#decisioning-report}

## Relatórios de decisão {#campaigns}

Quando as jornadas ou campanhas com estratégias de seleção estiverem ativas, você poderá acessar relatórios dedicados para monitorar os Indicadores-chave de desempenho (KPIs) da decisão.

<!--
Once code-based experiences are live, you can access dedicated reports to monitor Key Performance Indicators (KPIs) as an all-encompassing dashboard, delivering an analysis of essential metrics associated with your campaign.

This encompasses details related to the decision items performances and how users interacted with them. [Learn how to work with Code-based experience reports](../reports/campaign-global-report-cja-code.md)
-->

![](../reports/assets/cja-decisioning-kpis.png)

Você também pode acessar detalhes relacionados ao desempenho dos itens de decisão e como os usuários interagiram com eles, fornecendo uma análise das métricas essenciais associadas à sua campanha.

![](../reports/assets/cja-decisioning-item-performance.png)

Saiba como trabalhar com relatórios de experiência baseados em código na Decisão do [nesta seção](../reports/campaign-global-report-cja-code.md#decisioning-reporting).

## Relatórios no Customer Journey Analytics {#cja}

Se estiver trabalhando com o Customer Journey Analytics, você pode criar painéis de relatórios personalizados para suas campanhas baseadas em código usando a Decisão.

As principais etapas estão listadas abaixo. Informações detalhadas sobre como trabalhar com o Customer Journey Analytics estão disponíveis na [documentação do Customer Journey Analytics](https://experienceleague.adobe.com/pt-br/docs/analytics-platform/using/cja-landing){target="_blank"}.

1. Crie e configure uma **conexão** no Customer Journey Analytics. Isso permite que você se conecte ao conjunto de dados para o qual deseja relatórios. [Saiba como criar uma conexão](https://experienceleague.adobe.com/pt-br/docs/analytics-platform/using/cja-connections/create-connection){target="_blank"}

1. Crie uma **visualização de dados** e associe-a à conexão criada anteriormente. Na guia **[!UICONTROL Componentes]**, escolha os campos de esquema relevantes que deseja exibir nos relatórios. Para a Decisão, inclua os campos **propositioninteraction** e **propositiondisplay**. [Saiba como criar e configurar visualizações de dados](https://experienceleague.adobe.com/pt-br/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}

1. Combine componentes de dados, tabelas e visualizações em **projetos do espaço de trabalho** para criar e compartilhar relatórios para sua campanha baseada em código. [Saiba como criar projetos do espaço de trabalho](https://experienceleague.adobe.com/pt-br/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects){target="_blank"}
