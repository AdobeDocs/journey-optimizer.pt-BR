---
product: experience platform
solution: Experience Platform
title: Introdução a modelos de IA
description: Saiba mais sobre os modelos de IA que permitem classificar ofertas
feature: Ranking, Decision Management
role: User
level: Intermediate
source-git-commit: 58f4fdf8ec3cdb609efebf5b8713f6b770ef5414
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 18%

---

# Introdução a modelos de IA {#ai-models}

O [!DNL Journey Optimizer] permite usar um sistema de modelo treinado que classifica as ofertas para exibição em determinado perfil.

Este recurso permite criar **modelos de IA** diferentes com base em suas metas comerciais. Ao usar essas diferentes estratégias baseadas em metas em uma decisão, o sistema de modelo treinado ajudará você a entender como os diferentes modelos de IA estão afetando suas metas.

<!--For example, you can select an AI model for the email channel and another one for the push channel. For each channel, the trained model system will leverage multiple data points to determine which offer should be presented first for a given decision policy?, rather than taking into account the offers' priority scores or a [ranking formula](create-ranking-formulas.md).

>[!IMPORTANT]
>
>For now, ranking models are not supported in Journey Optimizer authored channels.-->

## Tipos de modelo de IA {#ai-model-types}

>[!CONTEXTUALHELP]
>id="ajo_exd_ai_model_type"
>title="Escolha o tipo de modelo"
>abstract="Selecione o tipo de modelo de IA que deseja criar: a **Otimização automática** otimiza ofertas com base no desempenho de ofertas anteriores, enquanto a **Otimização personalizada** otimiza e personaliza ofertas com base em públicos-alvo e desempenho da oferta."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/decisioning/offer-decisioning/rankings/ai-models/create-ranking-strategies#create-ranking-strategy" text="Criar um modelo de IA"

Dois tipos de modelos de IA estão disponíveis em [!DNL Journey Optimizer]:

* **Os modelos de otimização automática** têm como objetivo fornecer ofertas que maximizam o retorno (KPIs) definido pelos clientes empresariais. Esses KPIs podem estar na forma de taxas de conversão, receita etc. Nesse ponto, a Otimização automática se concentra na otimização de cliques na oferta com a conversão de oferta como destino. A otimização automática não é personalizada e é otimizada com base no desempenho &quot;global&quot; das ofertas. [Saiba mais](auto-optimization-model.md)

* **Os modelos de otimização personalizados** permitem definir metas comerciais e utilizar dados do cliente para treinar modelos orientados para negócios a fim de fornecer ofertas personalizadas e maximizar KPIs. [Saiba mais](personalized-optimization-model.md)

## Criar um modelo de IA {#create-ai-model}

As principais etapas para criar e usar modelos de IA são as seguintes:

1. Crie um conjunto de dados em que os eventos de conversão e impressão serão coletados. [Saiba mais](../data-collection/create-dataset.md)

1. Crie um modelo de IA que aproveitará os eventos do conjunto de dados para classificar ofertas. [Saiba mais](create-ai-models.md)

1. Configure seu schema de ofertas para capturar eventos automaticamente. [Saiba mais](../data-collection/schema-requirement.md)

   >[!IMPORTANT]
   >
   >Os modelos de classificação exigem que os eventos de feedback sejam enviados como eventos de experiência para serem coletados. [Saiba mais sobre a coleta de dados de decisão](../data-collection/data-collection.md)

1. Atribua o modelo de IA a uma estratégia de seleção para classificar ofertas elegíveis. [Saiba mais](../selection-strategies.md#select-ranking-method)
