---
solution: Journey Optimizer
product: journey optimizer
title: Relatório de campanha
description: Saiba como usar os dados de experimentação no relatório de campanha
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 69742163-7378-49ab-929e-86213d6e65e3
TQID: https://experienceleague.adobe.com/m11Vxa3bSvaOHe1kFs5tU9oQS08lzcL0DSPyrABbXBI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a9f73820-6899-47c2-a597-3fec28ab756aid: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2: id: d145add9-d5b9-481b-aa8a-e15e6bb7f813id: a7289281-9ae4-47b1-b8cf-4028b98af776id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 339
ht-degree: 9%

---

# Relatório de campanha de experimentação {#campaign-global-report-cja-experimentation}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="Métricas de sucesso"
>abstract="O valor total da métrica sucesso, anteriormente selecionado ao criar seus experimentos, dividido pelo número de perfis."

## Experimentação {#experimentation}

A guia **[!UICONTROL Experimentação]** fornece informações importantes sobre o desempenho de cada variante e identifica a mais bem-sucedida.

Observe que a definição do melhor desempenho pode levar algum tempo. Se o experimento não for bem-sucedido, ele será definido como **Inconclusivo**.

![](assets/cja-experimentation-1.png)

### KPIs de experimentação {#experimentation-kpis}

![](assets/cja-experimentation-kpis.png)

Os KPIs (Indicadores-chave de desempenho) da **[!UICONTROL Experimentação]** funcionam como um painel abrangente, fornecendo uma análise das métricas essenciais associadas à sua experimentação.

+++ Saiba mais sobre métricas de KPIs de experimentação

* **[!UICONTROL Aumento]**: medida da melhora da porcentagem na taxa de conversão de um determinado tratamento em relação à linha de base.

* **[!UICONTROL Confiança]**: evidência de que um determinado tratamento é igual ao tratamento de linha de base. [Saiba mais](../content-management/experiment-calculations.md#adobes-statistical-methodology-any-time-valid-confidence-sequences)

+++

### Variante por métrica de sucesso {#variant-inbound}

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