---
solution: Journey Optimizer
product: journey optimizer
title: Relatório de campanha
description: Saiba como usar os dados do canal personalizado no relatório de Campanha
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: ac64dd4ca2ed5fd1b9d816e19c6726a3ac82d193
workflow-type: tm+mt
source-wordcount: '544'
ht-degree: 0%

---

# Relatório de campanha de canal personalizado {#campaign-global-report-cja-custom-channel}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como ler o relatório Campanha de canal personalizado no Adobe Journey Optimizer para revisar KPIs, resultados, latência e detalhamento de resultados para suas chamadas de canal personalizadas.

>[!ENDSHADEBOX]

>[!BEGINSHADEBOX]

Você pode acessar o relatório de campanha Canal personalizado clicando no botão **[!UICONTROL Relatórios]** da campanha e selecionando **[!UICONTROL Exibir relatório de todos os tempos]**. [Saiba mais](report-gs-cja.md)

![](assets/report-access.png)

>[!ENDSHADEBOX]

## KPIs {#kpis-custom}

![](assets/kpis-custom.png)

A seção **[!UICONTROL KPIs]** fornece uma exibição consolidada da integridade operacional e da confiabilidade das suas chamadas de canal personalizadas.

+++ Saiba mais sobre métricas de KPIs

* **[!UICONTROL Chamadas com êxito]**: número total de chamadas HTTP que retornaram uma resposta válida sem erro.

* **[!UICONTROL 4xx errors]**: número de chamadas com falha devido a erros do lado do cliente, realçando problemas de configuração ou falhas de ponto de extremidade.

* **[!UICONTROL 5xx errors]**: número de chamadas com falha devido a erros do lado do servidor, realçando problemas de configuração ou falhas de ponto de extremidade.

* **[!UICONTROL Chamadas de tempo limite]**: número de chamadas que falharam porque excederam o tempo máximo de resposta. Isso ajuda a exibir problemas de latência ou desempenho com pontos de extremidade externos.

* **[!UICONTROL Falhas de pré-chamada]**: Número de envios de canais personalizados que falharam antes da chamada HTTP ter sido feita ao ponto de extremidade externo. Essas falhas ocorrem na própria camada de infraestrutura do [!DNL Journey Optimizer], não no sistema externo, e incluem falhas de autenticação, erros de geração de solicitação e erros de análise HTTP.

* **[!UICONTROL Latência média]**: tempo médio de resposta de ponta a ponta (em milissegundos) para todas as chamadas HTTP, incluindo chamadas bem-sucedidas, erros e tempos limite.

+++

## Resultados do canal personalizado {#outcomes-custom}

![](assets/outcomes-custom.png)

O gráfico **[!UICONTROL Resultados]** mostra a tendência do KPI de chamadas HTTP ao longo do período selecionado, com uma granularidade que depende do intervalo de tempo selecionado (por dia para um relatório de 7 dias, por hora para um intervalo de 1 dia ou por minuto para um intervalo de 1 hora), enquanto a tabela **[!UICONTROL Detalhamento dos resultados]** fornece um detalhamento hierárquico dessas métricas de chamadas HTTP, desde as métricas gerais por ponto de extremidade no nível superior até as métricas por canal personalizado usando esse ponto de extremidade, passando pelas campanhas e jornadas que dependem delas no nível inferior.

+++ Saiba mais sobre Métricas de detalhamento de resultados

* **[!UICONTROL Canal personalizado bem-sucedido]**: número total de chamadas HTTP que retornaram uma resposta válida sem erro.

* **[!UICONTROL 4xx errors]**: número de chamadas com falha devido a erros do lado do cliente, realçando problemas de configuração ou falhas de ponto de extremidade.

* **[!UICONTROL 5xx errors]**: número de chamadas com falha devido a erros do lado do servidor, realçando problemas de configuração ou falhas de ponto de extremidade.

* **[!UICONTROL Chamadas de tempo limite]**: número de chamadas que falharam porque excederam o tempo máximo de resposta. Isso ajuda a exibir problemas de latência ou desempenho com pontos de extremidade externos.

* **[!UICONTROL Falhas de pré-chamada]**: Número de envios de canais personalizados que falharam antes da chamada HTTP ter sido feita ao ponto de extremidade externo. Essas falhas ocorrem na própria camada de infraestrutura do [!DNL Journey Optimizer], não no sistema externo, e incluem falhas de autenticação, erros de geração de solicitação e erros de análise HTTP.

* **[!UICONTROL Chamadas]**: Número total de chamadas HTTP, incluindo chamadas bem-sucedidas, erros e tempos limite.

+++

## Latência {#latency-custom}

![](assets/latency-custom.png)

O gráfico e as tabelas de **[!UICONTROL Latência]** visualizam a tendência das métricas de latência. Essas exibições permitem rastrear padrões de desempenho, identificar períodos de latência de pico e monitorar o impacto de otimizações ou alterações do sistema ao longo do tempo.

+++ Saiba mais sobre Métricas de latência

* **[!UICONTROL Latência média]**: tempo médio de resposta de ponta a ponta (em milissegundos) para todas as chamadas HTTP, incluindo chamadas bem-sucedidas, erros e tempos limite.

* **[!UICONTROL Latência média de êxito]**: tempo médio de resposta de ponta a ponta (em milissegundos) para chamadas HTTP que retornaram uma resposta válida sem erros.

+++
