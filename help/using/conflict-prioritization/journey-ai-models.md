---
title: Jornada modelos de IA de arbitragem
description: Saiba como criar e usar modelos de IA para classificar jornadas para arbitragem, de modo que a melhor jornada seja selecionada por perfil com base em pontuações orientadas por IA.
feature: Journeys, Decisioning
role: User
level: Intermediate
version: Journey Orchestration
badge: label="Disponibilidade limitada" type="Informative"
hide: true
hidefromtoc: true
exl-id: 3e7c3069-b022-4709-936d-acaad56b5882
source-git-commit: afc09bbcb76d53404574bb53c0a896109cd7f1da
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 3%

---

# Usar modelos de IA para classificar jornadas {#journey-ai-models}

>[!AVAILABILITY]
>
>Este recurso está atualmente com a Disponibilidade Limitada. Entre em contato com o representante da Adobe para obter acesso.

O [!DNL Adobe Journey Optimizer] ajuda você a controlar quais jornadas um perfil pode inserir quando se qualificar para mais do que o sistema permite. Para fazer isso, você pode usar [conjuntos de regras](rule-sets.md) para definir limites na entrada de jornada ou simultaneidade. Quando um perfil é qualificado para mais jornadas do que o limite permite, a prioridade atribuída a cada jornada determina quais jornadas são selecionadas.

Em vez de usar a prioridade, você também pode usar **modelos de IA** nas fórmulas de classificação para classificar jornadas dinamicamente com base em pontuações de modelo treinadas.

## Criar um modelo de IA {#create-ai-model}

<!--Do you need specific permissions to create AI models?
>[!CAUTION]
>
>To create, edit, or delete AI models, you must have the **Manage Ranking Strategies** permission. [Learn more](../administration/high-low-permissions.md#manage-ranking-strategies)-->

Para criar um modelo de IA para classificação de jornada, siga as etapas abaixo.

1. Crie um conjunto de dados em que os eventos de conversão serão coletados. [Saiba como](../experience-decisioning/data-collection/create-dataset.md)

1. Acesse a seção **[!UICONTROL Classificação de orquestração]** e selecione a guia **[!UICONTROL Modelos de IA]**. A lista de modelos de IA criados anteriormente é exibida.

1. Clique em **[!UICONTROL Criar modelo de IA]**.

1. Especifique um nome exclusivo e, se necessário, uma descrição para o modelo de IA.

   ![Painel de detalhes do modelo de IA com campos de nome e descrição](assets/journey-model-details.png){width="80%"}

   >[!NOTE]
   >
   >O objeto de classificação é a entidade à qual a fórmula de classificação será aplicada. Por padrão, o objeto de classificação está definido como **[!UICONTROL Jornada]**.

<!--
1. Select the type of AI model you want to create:

    * **[!UICONTROL Auto-optimization]** optimizes based on past performance. [Learn more](../experience-decisioning/ranking/auto-optimization-model.md)
    * **[!UICONTROL Personalized optimization]** optimizes and personalizes based on audiences and performance. [Learn more](../experience-decisioning/ranking/personalized-optimization-model.md)-->

1. Na **[!UICONTROL Métrica de otimização]**, todas as métricas da [!DNL Customer Journey Analytics] [visualização de dados](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/data-views){target="_blank"} padrão são exibidas na lista. Selecione a métrica em que deseja otimizar seu modelo.

   ![Painel de detalhes do modelo de IA com campos de nome e descrição](assets/journey-model-metrics.png){width="80%"}

   [!DNL Journey Optimizer] classificações com base no **índice de conversão** (Índice de conversão = Número total de eventos de conversão / Número total de eventos de impressão). A taxa de conversão é calculada usando:

   * **Eventos de impressão** (itens exibidos)
   * **Eventos de conversão** (itens que resultam em cliques ou conversões)

   Esses eventos são capturados automaticamente usando o Web SDK ou o SDK móvel. Saiba mais na visão geral do [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=pt-BR).

1. Selecione os conjuntos de dados nos quais os eventos de conversão e impressão são coletados. Saiba como criar esses conjuntos de dados [nesta seção](../experience-decisioning/data-collection/create-dataset.md).

   ![Seleção de conjunto de dados para eventos de conversão e impressão](../experience-decisioning/assets/ai-model-datasets.png){width="85%"}

   >[!CAUTION]
   >
   >Somente os conjuntos de dados criados a partir de esquemas associados ao grupo de campos **[!UICONTROL Evento de experiência - Interações de apresentação]** (anteriormente conhecido como mixin) são exibidos na lista suspensa.

1. <!--If you are creating a **[!UICONTROL Personalized optimization]** AI model, -->Selecione os segmentos a serem usados para treinar o modelo de IA.

   >[!NOTE]
   >
   >Você pode selecionar até 50 públicos-alvo.

1. Salve e ative o modelo de IA.

O modelo de IA agora está disponível para seleção ao criar uma fórmula de classificação.

## Selecionar um modelo de IA para uma fórmula de classificação {#select-ai-model-for-ranking-formula}

Agora você pode definir o modelo de IA como uma referência para criar uma fórmula de classificação. Siga as etapas abaixo.

1. Crie uma fórmula de classificação. [Saiba como](journey-ranking-formulas.md#create-journey-ranking-formula)

1. Use o botão **[!UICONTROL Selecionar modelo de IA]** para selecionar o modelo de IA que deseja usar.

   ![Jornada painel de detalhes da fórmula de classificação com seleção de modelo de IA](assets/journey-formula-ai-model.png){width="80%"}

1. Em pelo menos uma das seções de **[!UICONTROL Critério]**, defina uma condição e selecione **[!UICONTROL Pontuação do modelo de IA]** como o método de classificação. Por exemplo, se a jornada tiver uma tag &quot;Promo&quot;, a pontuação da classificação será a pontuação do modelo de IA.

   ![Fórmula de classificação: a marca promocional usa a pontuação do modelo de IA](assets/journey-formula-ex-2.png){width="60%"}

1. Clique em **[!UICONTROL Criar]** para concluir a fórmula de classificação.

## Atribuir o modelo de IA a um conjunto de regras {#assign-ai-model-to-ruleset}

Para usar um modelo de IA para classificar suas jornadas, é necessário atribuir a fórmula que faz referência a esse modelo de IA a um conjunto de regras.

1. No menu **[!UICONTROL Regras de negócio]**, crie um conjunto de regras que você deseja usar para arbitragem de jornada. [Saiba como](rule-sets.md#Create)

1. Selecione o domínio **[!UICONTROL Jornada]**.

1. Nas propriedades do conjunto de regras, defina o **[!UICONTROL Método de classificação]** como **[!UICONTROL Fórmula]** (em vez de **[!UICONTROL Prioridade]**).

1. Selecione na lista suspensa a fórmula que usa o modelo de IA criado.

1. Crie as regras de limite de jornada que deseja adicionar ao conjunto de regras. [Saiba como](journey-capping.md#create-rule)

1. Salve o conjunto de regras.

Agora, a fórmula que usa o modelo de IA é atribuída ao conjunto de regras. Você pode aplicar esse conjunto de regras às suas jornadas.

## Aplicar o conjunto de regras a uma jornada {#assign-rule-set-to-journey}

Para atribuir o conjunto de regras a uma jornada, siga as etapas abaixo.

1. Crie ou abra a jornada à qual deseja atribuir o conjunto de regras. [Saiba como criar uma jornada](../building-journeys/journey-gs.md)

1. Nas propriedades da jornada, selecione o conjunto de regras na lista suspensa. [Saiba como](journey-capping.md#apply-capping).

   >[!NOTE]
   >
   >Somente um conjunto de regras pode ser aplicado a uma jornada de cada vez.

1. Salve a jornada.

Todas as jornadas que usam esse conjunto de regras serão classificadas com a fórmula selecionada usando o modelo de IA quando o limite for aplicado.
