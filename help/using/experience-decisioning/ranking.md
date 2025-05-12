---
title: Métodos de classificação
description: Saiba como trabalhar com métodos de classificação
feature: Decisioning, Ranking
topic: Integrations
role: User
level: Intermediate
exl-id: c1d69bc9-4486-4037-b218-f4f704b2ba9c
source-git-commit: 4995bf642231248ece0211a7ecf2f38ccd846d36
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 5%

---

# Métodos de classificação {#rankings}

Os métodos de classificação permitem classificar itens para exibição em um determinado perfil. Depois que um método de classificação é criado, será possível atribuí-lo a uma estratégia de seleção para definir quais itens devem ser selecionados primeiro.

Dois tipos de métodos de classificação estão disponíveis:

* **As fórmulas** permitem definir regras que determinarão qual item deve ser apresentado primeiro, em vez de considerar as pontuações de prioridade do item.

* Os **modelos de IA** permitem usar sistemas de modelo treinados que aproveitarão vários pontos de dados para determinar qual item deve ser apresentado primeiro.

## Criar métodos de classificação {#create}

Para criar um método de classificação, siga estas etapas:

1. Navegue até o menu **[!UICONTROL Configuração de estratégia]** e selecione o menu **[!UICONTROL Fórmulas]** ou **[!UICONTROL Modelos de IA]**, dependendo do tipo de classificação que deseja usar.

1. Clique no botão **[!UICONTROL Criar fórmula]** ou **[!UICONTROL Criar modelo de IA]** no canto superior direito da tela.

   ![](assets/ranking-create.png)

1. Configure a fórmula ou o modelo de IA para atender às suas necessidades e salve.

   Informações detalhadas sobre como criar fórmulas de classificação e modelos de IA estão disponíveis na documentação da gestão de decisões:

   <!--* [Ranking formulas](exd-ranking-formulas.md)-->
   * [Fórmulas de classificação](../offers/ranking/create-ranking-formulas.md)
   * [Modelos de IA](../offers/ranking/ai-models.md)

   >[!NOTE]
   >
   >A profundidade do aninhamento em uma fórmula de classificação é limitada a 30 níveis. Isso é medido pela contagem dos parênteses de fechamento `)` na cadeia de caracteres do PQL. Uma sequência de regras pode ter até 8 KB para caracteres codificados em UTF-8. É equivalente a 8.000 caracteres ASCII (1 byte cada) ou 2.000-4.000 caracteres não ASCII (2-4 bytes cada). [Saiba mais sobre as medidas de proteção e limitações da decisão](gs-experience-decisioning.md#guardrails)

Uma política de decisão suporta até 10 estratégias de seleção e itens de decisão combinados. [Saiba mais sobre as medidas de proteção e limitações da decisão](gs-experience-decisioning.md#guardrails)

+++ Otimização de modelos nas métricas [!DNL Customer Journey Analytics] personalizadas

>[!NOTE]
>
>Este recurso só está disponível para [!DNL Customer Journey Analytics] clientes com direitos de administrador.
>
>Antes de começar, verifique se você integrou o Journey Optimizer ao Customer Journey Analytics para exportar conjuntos de dados do Journey Optimizer para suas visualizações de dados padrão. [Saiba como aproveitar [!DNL Journey Optmizer] os dados em [!DNL Customer Journey Analytics]](../reports/cja-ajo.md)

Os modelos de otimização personalizados são um tipo de modelo de IA que permite definir metas comerciais e utilizar dados do cliente para treinar modelos orientados para negócios a fim de fornecer ofertas personalizadas e maximizar KPIs. Informações detalhadas sobre como criar um modelo de IA personalizado estão disponíveis na [documentação da gestão de decisões](../offers/ranking/personalized-optimization-model.md).

Por padrão, os modelos de otimização personalizados usam **cliques de oferta** como métrica de otimização. Se você estiver trabalhando com o [!DNL Customer Journey Analytics], o [!DNL Decisioning] permitirá que você aproveite suas próprias métricas personalizadas para otimizar seu modelo.

Para fazer isso, acesse a tela de criação do modelo de IA personalizado e expanda o menu suspenso **[!UICONTROL Evento de conversão]**. Todas as métricas da sua [!DNL Customer Journey Analytics] [visualização de dados](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/data-views){target="_blank"} padrão são exibidas na lista. Selecione a métrica em que deseja otimizar o modelo e conclua a criação do modelo de IA como de costume.

![](assets/ai-ranking-custom-metrics.png)

>[!NOTE]
>
>Por padrão, as métricas em [!DNL Customer Journey Analytics] usam um modelo de atribuição &quot;Último contato&quot;, que atribui 100% do crédito ao ponto de contato que ocorre mais recentemente antes da conversão.
>
>Embora seja possível modificar o modelo de atribuição, nem todos os modelos de atribuição são ideais para a otimização do modelo de IA. Recomendamos selecionar cuidadosamente um modelo de atribuição que se alinhe às suas metas de otimização para garantir a precisão e o desempenho do modelo.
>
>Para obter mais detalhes sobre modelos de atribuição disponíveis e orientação sobre seu uso, consulte a [[!DNL Customer Journey Analytics] documentação](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/component-settings/attribution){target="_blank"}

+++

## Aproveitar atributos de itens de decisão em fórmulas {#items}

As fórmulas de classificação são expressas em **sintaxe PQL** e podem aproveitar vários atributos, como atributos de perfil, [dados de contexto](context-data.md) e atributos relacionados aos seus itens de decisão.

>[!NOTE]
>
>Para obter mais informações sobre como usar a sintaxe do PQL, consulte a [documentação dedicada](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=pt-BR)

Para aproveitar os atributos relacionados aos seus itens de decisão em fórmulas, siga a sintaxe abaixo no código da fórmula de classificação. Expanda cada seção para obter mais informações:

+++Aproveitar atributos padrão de itens de decisão

![](assets/formula-attribute.png)

+++

+++Aproveitar atributos personalizados de itens de decisão

![](assets/formula-attribute-custom.png)

+++
