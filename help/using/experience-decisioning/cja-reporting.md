---
title: Relatório sobre a decisão
description: Saiba como criar relatórios sobre a Decisão.
feature: Experience Decisioning
topic: Integrations
role: User
level: Experienced
badge: label="Disponibilidade limitada"
exl-id: 7c45cd8a-8e86-4646-ba0a-db393e92d9da
source-git-commit: 841a114610bfee743f5ebb349e3eef6312de0f7b
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 3%

---


# Relatório sobre a decisão {#decisioning-report}

## Relatórios de campanhas baseadas em código {#campaigns}

Quando a experiência baseada em código estiver disponível, você poderá acessar relatórios dedicados para monitorar os Indicadores principais de desempenho (KPIs) como um painel abrangente, fornecendo uma análise das métricas essenciais associadas à sua campanha.

Isso abrange detalhes relacionados ao desempenho dos itens de decisão e como os usuários interagiram com eles. [Saiba como trabalhar com relatórios de experiência baseados em código](../reports/campaign-global-report-cja-code.md)

![](../reports/assets/cja-decisioning-item-performance.png)

## Relatórios no Customer Journey Analytics {#cja}

Se estiver trabalhando com o Customer Journey Analytics, você pode criar painéis de relatórios personalizados para suas campanhas baseadas em código usando o Decisioning.

As principais etapas estão listadas abaixo. Informações detalhadas sobre como trabalhar com o Customer Journey Analytics estão disponíveis na [documentação sobre o Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing){target="_blank"}.

1. Crie e configure uma **conexão** no Customer Journey Analytics. Isso permite que você se conecte ao conjunto de dados para o qual deseja relatórios. [Saiba como criar uma conexão](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection){target="_blank"}

1. Crie uma **visualização de dados** e associe-a à conexão criada anteriormente. Na guia **[!UICONTROL Componentes]**, escolha os campos de esquema relevantes que deseja exibir nos relatórios. Para a Decisão, inclua os campos **propositioninteraction** e **propositiondisplay**. [Saiba como criar e configurar visualizações de dados](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}

1. Combine componentes de dados, tabelas e visualizações em **projetos do espaço de trabalho** para criar e compartilhar relatórios para sua campanha baseada em código.[Saiba como criar projetos do espaço de trabalho](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects){target="_blank"}
