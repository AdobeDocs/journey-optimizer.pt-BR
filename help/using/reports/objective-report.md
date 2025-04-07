---
solution: Journey Optimizer
product: journey optimizer
title: Relatório global da campanha
description: Saiba como usar os dados do relatório global do Campaign
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: ec1af88c-7b0a-4eaf-97e1-0d9676268fed
badge: label="Beta" type="Informative"
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 4%

---

# Relatório global da campanha {#objective-report}

O relatório global da campanha pode ser acessado diretamente do Campaign com o botão **[!UICONTROL Exibir relatório]**.

O **[!UICONTROL Relatório global]** da campanha está dividido em widgets diferentes detalhando o sucesso e os erros da campanha. Cada widget pode ser redimensionado e excluído, se necessário. Para obter mais informações, consulte esta [seção](../reports/global-report.md#modify-dashboard).

Para obter uma lista detalhada de cada métrica disponível no Adobe Journey Optimizer, consulte [esta página](global-report.md#list-of-components-global.md)

## Guia Campanha {#campaign-global-objectives}

### Entrega {#delivery-global-objectives}

![](assets/campaign_report_global_1.png)

O widget **[!UICONTROL Estatísticas]** da campanha detalha as principais informações relativas à sua campanha:

* **[!UICONTROL Perfis inseridos]**: número de perfis que iniciaram a jornada.

* **[!UICONTROL Ações entregues]**: número total de vezes que uma ação na jornada foi entregue.

* **[!UICONTROL Ações com falha em %]**: Número total de vezes que uma ação falhou na jornada em comparação ao número total de vezes que uma ação foi entregue.

### Relatório de objetivos {#objective-global}

>[!AVAILABILITY]
>
>O recurso **Relatório de objetivos** está disponível no momento apenas para um conjunto de organizações (Disponibilidade limitada). Para obter mais informações, entre em contato com o(a) representante da Adobe.

![](assets/performance_report.gif)

A guia **[!UICONTROL Objetivos]** permite ajustar melhor os relatórios dos deliveries ao direcionar uma métrica específica.

Os **[!UICONTROL Objetivos]** listados estão vinculados aos **[!UICONTROL Conjuntos de Dados]** que definem uma conexão com um sistema para recuperar informações adicionais. Uma lista interna de **[!UICONTROL Objetivos]** está disponível, mas você pode adicionar a sua própria lista adicionando um novo **[!UICONTROL Conjunto de Dados]**. Para obter o procedimento detalhado, consulte esta [seção](../reports/reporting-configuration.md).

Depois de selecionar os Objetivos que deseja direcionar, os dois widgets **[!UICONTROL Visão geral do desempenho]** e **[!UICONTROL Objetivo da campanha]** fornecerão um resumo detalhado do desempenho da sua entrega.

Com o widget **[!UICONTROL Objetivo da campanha]**, você também pode optar por comparar seu objetivo principal com outra métrica.

### Relatório de experimentação {#experimentation-global-objectives}

![](assets/experimentation_report_3.png)

A guia **[!UICONTROL Experimentação]** fornece informações importantes sobre o desempenho de cada variante e identifica a mais bem-sucedida.

Observe que a definição do melhor desempenho pode levar algum tempo, ela será representada por este ícone ![](assets/experimentation_report_1.png).

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório Experimentação.

O widget **[!UICONTROL Resultado do experimento]** detalha o desempenho de cada variante. Você pode alterar sua linha de base selecionando um dos tratamentos na **[!UICONTROL Linha de base]** do menu suspenso. O melhor tratamento será representado com um ícone de estrela.

A tabela apresenta as seguintes métricas:

* **[!UICONTROL Aumento em relação à linha de base]**: Medida da melhora da porcentagem na taxa de conversão de um determinado tratamento em relação à linha de base.

* **[!UICONTROL Confiança]**: evidência de que um determinado tratamento é igual ao tratamento de linha de base. [Saiba mais](../content-management/experiment-calculations.md#understand-confidence)

* **[!UICONTROL Cliques de saída exclusivos]**: contagem total de cliques nos canais de saída.

* **[!UICONTROL Perfis]**: número de perfis direcionados para este tratamento.

* **[!UICONTROL Cliques/perfis de saída exclusivos]**: valor total da métrica de Sucesso, selecionada anteriormente ao criar seus Experimentos, dividido pelo número de perfis.

O gráfico **[!UICONTROL Intervalo de confiança]** mede a incerteza em torno da melhoria. Ela detalha a diferença percentual de desempenho entre a linha de base e o tratamento com melhor desempenho. [Saiba mais](../content-management/experiment-calculations.md#confidence-intervals).
+++

Para aprofundar esses resultados e como interpretá-los, consulte [esta página](../content-management/get-started-experiment.md#interpret-results).
