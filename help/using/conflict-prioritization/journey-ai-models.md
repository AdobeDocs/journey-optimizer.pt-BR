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
source-git-commit: fe6e8221201ee813251a46c6603d85f0803873c0
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 4%

---

# Usar modelos de IA para classificar jornadas {#journey-ai-models}

>[!AVAILABILITY]
>
>Este recurso está atualmente com a Disponibilidade Limitada. Entre em contato com o representante da Adobe para obter acesso.

O [!DNL Adobe Journey Optimizer] ajuda você a controlar quais jornadas um perfil pode inserir quando se qualificar para mais do que o sistema permite. Para fazer isso, você pode usar [conjuntos de regras](rule-sets.md) para definir limites na entrada de jornada ou simultaneidade. Quando um perfil é qualificado para mais jornadas do que o limite permite, a prioridade atribuída a cada jornada determina quais jornadas são selecionadas.

Em vez de usar fórmulas de prioridade ou classificação, você pode usar **modelos de IA** para classificar jornadas dinamicamente com base em pontuações de modelo treinadas. Você pode criar modelos de IA na seção **[!UICONTROL Classificação de orquestração]** da interface e usá-los em conjuntos de regras para aplicá-los a jornadas.

Para obter uma visão geral dos tipos de modelo de IA disponíveis em [!DNL Journey Optimizer], consulte [Introdução aos modelos de IA](../experience-decisioning/ranking/ai-models.md#ai-model-types) na seção Decisão.

## Criar um modelo de IA {#create-ai-model}

>[!CAUTION]
>
>Para criar, editar ou excluir modelos de IA, você deve ter a permissão **Gerenciar estratégias de classificação**. [Saiba mais](../administration/high-low-permissions.md#manage-ranking-strategies)

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

1. A seção **[!UICONTROL Métrica de otimização]** fornece informações sobre o evento de conversão usado pelo modelo de IA. [!DNL Journey Optimizer] classificações com base no **índice de conversão** (Índice de conversão = Número total de eventos de conversão / Número total de eventos de impressão). A taxa de conversão é calculada usando:

   * **Eventos de impressão** (itens exibidos)
   * **Eventos de conversão** (itens que resultam em cliques ou conversões)

   Esses eventos são capturados automaticamente usando o Web SDK ou o SDK móvel. Saiba mais na visão geral do [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=pt-BR).

1. Selecione os conjuntos de dados nos quais os eventos de conversão e impressão são coletados. Saiba como criar esses conjuntos de dados [nesta seção](../experience-decisioning/data-collection/create-dataset.md).

   ![Seleção de conjunto de dados para eventos de conversão e impressão](../experience-decisioning/assets/ai-model-datasets.png){width="85%"}

   >[!CAUTION]
   >
   >Somente os conjuntos de dados criados a partir de esquemas associados ao grupo de campos **[!UICONTROL Evento de experiência - Interações de apresentação]** (anteriormente conhecido como mixin) são exibidos na lista suspensa.

1. &#x200B;<!--If you are creating a **[!UICONTROL Personalized optimization]** AI model, -->Selecione os segmentos a serem usados para treinar o modelo de IA.

   >[!NOTE]
   >
   >Você pode selecionar até 5 públicos-alvo.

1. Salve e ative o modelo de IA.

O modelo de IA agora está disponível ao configurar um conjunto de regras.

## Atribuir o modelo de IA a um conjunto de regras {#assign-ai-model-to-ruleset}

Para usar um modelo de IA para classificar suas jornadas, é necessário usá-lo em uma fórmula e atribuí-la a um conjunto de regras.

1. Crie uma fórmula de classificação usando o modelo de IA criado. [Saiba como](journey-ranking-formulas.md#create-journey-ranking-formula)

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
