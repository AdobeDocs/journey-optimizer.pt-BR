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
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 3%

---

# Relatório global da campanha {#objective-report}

O relatório global da campanha pode ser acessado diretamente do seu Campaign com o **[!UICONTROL Exibir relatório]** botão.

A campanha **[!UICONTROL Relatório global]** O é dividido em widgets diferentes detalhando o sucesso e os erros da campanha. Cada widget pode ser redimensionado e excluído, se necessário. Para obter mais informações, consulte esta [seção](../reports/global-report.md#modify-dashboard).

Para obter uma lista detalhada de cada métrica disponível no Adobe Journey Optimizer, consulte [esta página](global-report.md#list-of-components-global.md)

## Guia Campanha {#campaign-global-objectives}

### Entrega {#delivery-global-objectives}

![](assets/campaign_report_global_1.png)

A variável **[!UICONTROL Estatísticas da campanha]** o widget detalha as principais informações relacionadas à sua campanha:

* **[!UICONTROL Perfis inseridos]**: Número de perfis que iniciaram a jornada.

* **[!UICONTROL Ações entregues]**: Número total de vezes que uma ação na jornada foi entregue.

* **[!UICONTROL Ações com falha em %]**: Número total de vezes que uma ação falhou na jornada em comparação ao número total de vezes que uma ação foi entregue.

### Relatório de objetivos {#objective-global}

>[!AVAILABILITY]
>
>A variável **Relatório de objetivos** No momento, o recurso está disponível apenas para algumas organizações (disponibilidade limitada). Para obter mais informações, entre em contato com o seu representante da Adobe.

![](assets/performance_report.gif)

A variável **[!UICONTROL Objetivos]** permite ajustar melhor os relatórios dos deliveries ao direcionar uma métrica específica.

A variável **[!UICONTROL Objetivos]** listadas estão vinculadas a **[!UICONTROL Conjuntos de dados]** que definem uma conexão com um sistema para recuperar informações adicionais. Uma lista de componentes integrados **[!UICONTROL Objetivos]** está disponível, mas você pode adicionar a sua própria adicionando novas **[!UICONTROL Conjunto de dados]**. Para obter o procedimento detalhado, consulte este [seção](../campaigns/reporting-configuration.md).

Após selecionar os objetivos que deseja direcionar, os dois **[!UICONTROL Visão geral do desempenho]** e **[!UICONTROL Objetivo da campanha]** Os widgets fornecerão um resumo detalhado do desempenho do seu delivery.

Com o **[!UICONTROL Objetivo da campanha]** , você também pode optar por comparar seu objetivo principal com outra métrica.

### Relatório de experimentação {#experimentation-global-objectives}

![](assets/experimentation_report_3.png)

A variável **[!UICONTROL Experimentação]** A guia fornece informações importantes sobre o desempenho de cada variante e identifica a mais bem-sucedida.

Observe que a definição do melhor desempenho pode levar algum tempo. Ela será representada por esse ícone ![](assets/experimentation_report_1.png).

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o relatório Experimentação.

A variável **[!UICONTROL Resultado do experimento]** o widget detalha o desempenho de cada variante. Você pode alterar sua linha de base selecionando um dos tratamentos nas **[!UICONTROL Linha de base]** o menu suspenso. O melhor tratamento será representado com um ícone de estrela.

A tabela apresenta as seguintes métricas:

* **[!UICONTROL Aumento sobre a linha de base]**: Medida da melhora da porcentagem na taxa de conversão de um determinado tratamento em relação à linha de base.

* **[!UICONTROL Confiança]**: Evidência de que um determinado tratamento é igual ao tratamento inicial. [Saiba mais](../campaigns/experiment-calculations.md#understand-confidence)

* **[!UICONTROL Cliques de saída únicos]**: Contagem total de cliques nos canais de saída.

* **[!UICONTROL Perfis]**: Número de perfis direcionados para este tratamento.

* **[!UICONTROL Cliques/perfis de saída únicos]**: Valor total da métrica de Sucesso, selecionada anteriormente ao criar seus Experimentos, dividido pelo número de perfis.

A variável **[!UICONTROL Intervalo de confiança]** O gráfico mede a incerteza em torno da melhoria. Ela detalha a diferença percentual de desempenho entre a linha de base e o tratamento com melhor desempenho. [Saiba mais](../campaigns/experiment-calculations.md#confidence-intervals).
+++

Para aprofundar esses resultados e como interpretá-los, consulte [esta página](../campaigns/get-started-experiment.md#interpret-results).
