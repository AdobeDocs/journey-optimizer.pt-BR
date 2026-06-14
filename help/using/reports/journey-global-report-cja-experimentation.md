---
solution: Journey Optimizer
product: journey optimizer
title: Jornada relatório de experimento
description: Saiba como usar os dados de experimentação no relatório de Jornadas
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: a2b4ef74-96a9-4907-ba70-7aee69e45f20
TQID: https://experienceleague.adobe.com/oN7VFQvhQlwNa2U5CmcAYkGbKb0Vnxc7yA5rCLDjQw4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a9f73820-6899-47c2-a597-3fec28ab756a
  - id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2:
  - id: d145add9-d5b9-481b-aa8a-e15e6bb7f813
  - id: a7289281-9ae4-47b1-b8cf-4028b98af776
  - id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 7f28f19b11ead867b0851943fdd997dcc3af170b
workflow-type: tm+mt
source-wordcount: 407
ht-degree: 2%

---

# Relatório de jornada de experimentação {#campaign-global-report-cja-experimentation}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como ler as métricas de experimentação no relatório de jornada, incluindo KPIs de experimento, aumento e confiança, e desempenho da variante por métrica de sucesso para seus experimentos de conteúdo e caminho.

>[!ENDSHADEBOX]

Seu relatório de Jornada fornece uma visão completa do desempenho de seu experimento, juntamente com as métricas principais necessárias para entender seu impacto.

No Journey Optimizer, a experimentação do jornada é dividida em dois tipos:

* [Experimentos de conteúdo](../content-management/content-experiment.md)

  Observe que as tabelas e os KPIs detalhados para o experimento de conteúdo são iguais aos de um experimento de caminho. Consulte a [documentação abaixo](#experimentation) se você configurou um experimento de Conteúdo.

* [Experimentos de caminho](../building-journeys/optimize.md)

## Experimento de caminho {#experimentation}

### KPIs de experimentação {#experimentation-kpis}

![](assets/journey-report-experiment-1.png)

O **Resumo da experimentação** fornece informações importantes sobre o desempenho do seu experimento e identifica o mais bem-sucedido. Observe que a definição do melhor desempenho pode levar algum tempo. Se o experimento não for bem-sucedido, ele será definido como **Inconclusivo**.

Os **Indicadores-chave de desempenho (KPIs) de experimentação** funcionam como um painel abrangente, fornecendo uma análise das métricas essenciais associadas à sua experimentação.

+++ Saiba mais sobre métricas de KPIs de experimentação

* **[!UICONTROL Aumento]**: medida da melhora da porcentagem na taxa de conversão de um determinado tratamento em relação à linha de base.

* **[!UICONTROL Confiança]**: evidência de que um determinado tratamento é igual ao tratamento de linha de base. [Saiba mais](../content-management/experiment-calculations.md#adobes-statistical-methodology-any-time-valid-confidence-sequences)

+++



### Variante por métricas de sucesso {#variant-inbound}

![](assets/cja-experimentation-variants.png)

A tabela **Variante por métricas de sucesso** mostra o desempenho de cada variante com base na métrica de sucesso selecionada ao configurar o experimento.
Para aprofundar esses resultados e como interpretá-los, consulte [esta página](../content-management/get-started-experiment.md#interpret-results).

+++ Saiba mais sobre a Variante por métrica de sucesso

* **[!UICONTROL Pessoas]**: número de perfis de usuário qualificados como perfis de destino para suas mensagens.

* **[!UICONTROL Cliques de entrada]**: valor total da métrica de Sucesso, selecionada anteriormente ao criar seus Experimentos.

* **[!UICONTROL Taxa de conversão]**: valor total da métrica de Sucesso, selecionada anteriormente ao criar seus Experimentos, dividido pelo número de perfis.

* **[!UICONTROL Aumento]**: medida da melhora da porcentagem na taxa de conversão de um determinado tratamento em relação à linha de base.

* **[!UICONTROL Limite inferior de confiança]**: valor estimado mais baixo da diferença da taxa de conversão entre o tratamento e a linha de base, dentro do intervalo de confiança escolhido.

* **[!UICONTROL Confiança]**: evidência de que um determinado tratamento é igual ao tratamento de linha de base. [Saiba mais](../content-management/experiment-calculations.md#adobes-statistical-methodology-any-time-valid-confidence-sequences)

* **[!UICONTROL Limite superior de confiança]**: valor estimado mais alto da diferença da taxa de conversão entre o tratamento e a linha de base, dentro do intervalo de confiança escolhido.

+++

### Taxa de conversão para a métrica de Sucesso {#conversion-rate}

![](assets/cja-experimentation-conversion.png)

O gráfico **[!UICONTROL Intervalo de confiança]** mostra o intervalo de melhorias possíveis, comparando a linha de base com o tratamento de melhor desempenho para a métrica de sucesso escolhida. [Saiba mais](../content-management/experiment-calculations.md#adobes-statistical-methodology-any-time-valid-confidence-sequences).
