---
solution: Journey Optimizer
product: journey optimizer
title: Relatório de jornada
description: Saiba como usar os dados do relatório de jornada
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
badge: label="Disponibilidade limitada" type="Informative"
source-git-commit: b93d2288156713ac7479eef491f6104df1955a18
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 1%

---

# Monitorar suas ações personalizadas {#reporting}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_custom_actions_monitor"
>title="Monitorar suas ações personalizadas"
>abstract="A página de relatórios **[!UICONTROL Ação personalizada]** permite rastrear o desempenho e a confiabilidade das chamadas de API feitas pelo seu jornada para sistemas de terceiros."

>[!AVAILABILITY]
>
>No momento, os relatórios de ações personalizados estão disponíveis apenas para um conjunto de organizações (disponibilidade limitada).

A página de relatórios **[!UICONTROL Ação personalizada]** permite monitorar a confiabilidade e o desempenho das chamadas de API feitas de suas jornadas para sistemas de terceiros. Esses relatórios ajudam a identificar rapidamente problemas de integração, gargalos de latência ou limites de limitação/limitação que podem afetar a entrega.

A página Relatórios de ação personalizados funciona como outros Relatórios de tempo integral no Journey Optimizer. Para obter detalhes sobre as funcionalidades do painel, consulte [esta documentação](../reports/report-cja-manage.md).

Para acessar a página de relatórios **[!UICONTROL Ação personalizada]**, clique em ![](assets/do-not-localize/Smock_Monitoring_18_N.svg) na sua página inicial **[!UICONTROL Ações]**.

![](assets/monitor-1.png)

➡️ [Saiba mais sobre como configurar suas Ações personalizadas](../action/about-custom-action-configuration.md)

## KPIs {#kpis}

![](assets/monitor-2.png)

Os KPIs (Indicadores-chave de desempenho) de **[!UICONTROL Ação personalizada]** atuam como um painel centralizado, fornecendo uma exibição consolidada da integridade operacional e da confiabilidade das suas chamadas de ação personalizadas. Essas métricas permitem avaliar o desempenho, identificar gargalos e garantir integrações estáveis com sistemas externos.

+++ Saiba mais sobre KPIs de ação personalizados

* **[!UICONTROL Chamadas com êxito]**: número total de chamadas HTTP que retornaram uma resposta válida sem erro.

* **[!UICONTROL 4xx/5xx errors]**: número de chamadas com falha devido a erros do lado do cliente (4xx) ou do lado do servidor (5xx), destacando problemas de configuração ou falhas de ponto de extremidade.

* **[!UICONTROL Limites de tempo]**: número de chamadas que falharam porque excederam o tempo máximo de resposta. Isso ajuda a exibir problemas de latência ou desempenho com pontos de extremidade externos.

* **[!UICONTROL Chamadas limitadas]**: Número de chamadas bloqueadas devido a limites de limitação, garantindo que os sistemas downstream não sejam sobrecarregados.

* **[!UICONTROL Média de RPS]**: número de solicitações por segundo processadas pela ação personalizada durante o intervalo de tempo selecionado.

+++

## Chamadas de hora extra {#calls}

![](assets/monitor-3.png)

O gráfico de **[!UICONTROL Horas extras das chamadas]** mostra a tendência do KPI de chamadas HTTP durante o período selecionado para o relatório. A granularidade da série temporal depende do intervalo de tempo selecionado. Por exemplo:

* Para um relatório de 7 dias, cada ponto de dados mostrará os KPIs para um dia.
* Se você selecionar um intervalo de tempo de 1 dia, o gráfico mostrará os KPIs por hora.
* Se você selecionar um intervalo de tempo de 1 hora, o gráfico mostrará os KPIs por minuto.

➡️[Consulte a seção KPIs para obter uma descrição das métricas de chamada HTTP](#kpis)

## Detalhamento de chamadas {#breakdown}

![](assets/monitor-4.png)

A tabela **[!UICONTROL Detalhamento de chamadas]** fornece um detalhamento hierárquico das métricas de chamadas HTTP, desde as métricas gerais por ponto de extremidade no nível superior até as métricas por Ação personalizada usando cada ponto de extremidade até as jornadas que dependem delas no nível inferior.

➡️[Consulte a seção KPIs para obter uma descrição das métricas de chamada HTTP](#kpis)


