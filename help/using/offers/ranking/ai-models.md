---
product: experience platform
solution: Experience Platform
title: Introdução a modelos de IA
description: Saiba mais sobre os modelos de IA que permitem classificar ofertas
feature: Ranking, Decision Management
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
source-git-commit: 12f6c41252809bcc85bc076902f9a831a6c6e7d9
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 14%

---

# Introdução a modelos de IA {#ai-models}

[!DNL Journey Optimizer] O permite usar um sistema de modelo treinado que classifica as ofertas para exibição em determinado perfil.

Esse recurso permite criar **Modelos de IA** com base em suas metas comerciais. Ao usar essas diferentes estratégias baseadas em metas em uma decisão, o sistema de modelo treinado ajudará você a entender como os diferentes modelos de IA estão afetando suas metas.

Por exemplo, você pode selecionar um modelo de IA para o canal de email e outro para o canal de push. Para cada canal, o sistema de modelo treinado aproveitará vários pontos de dados para determinar qual oferta deve ser apresentada primeiro para um determinado posicionamento, em vez de considerar as pontuações de prioridade das ofertas ou uma [fórmula de classificação](create-ranking-formulas.md).

>[!IMPORTANT]
>
>Por enquanto, os modelos de classificação não são compatíveis com os canais criados pela Journey Optimizer.

## Tipos de modelo de IA {#ai-model-types}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_ai_model_type"
>title="Escolha o tipo de modelo"
>abstract="Selecione o tipo de modelo de IA que deseja criar: a **Otimização automática** otimiza ofertas com base no desempenho de ofertas anteriores, enquanto a **Otimização personalizada** otimiza e personaliza ofertas com base em públicos-alvo e desempenho da oferta."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/offer-decisioning/rankings/ai-models/create-ranking-strategies#create-ranking-strategy" text="Criar um modelo de IA"

Dois tipos de modelos de IA estão disponíveis em [!DNL Journey Optimizer]:

* **Modelos de otimização automática** O objetivo é fornecer ofertas que maximizam o retorno (KPIs) definido pelos clientes empresariais. Esses KPIs podem estar na forma de taxas de conversão, receita etc. Nesse ponto, a Otimização automática se concentra na otimização de cliques na oferta com a conversão de oferta como destino. A otimização automática não é personalizada e é otimizada com base no desempenho &quot;global&quot; das ofertas. [Saiba mais](auto-optimization-model.md)

* **Modelos de otimização personalizados** O permite definir metas de negócios e utilizar dados do cliente para treinar modelos orientados a negócios para fornecer ofertas personalizadas e maximizar KPIs. [Saiba mais](personalized-optimization-model.md)

## Criação de um modelo de IA {#create-ai-model}

As principais etapas para criar e usar modelos de IA são as seguintes:

1. Crie um conjunto de dados em que os eventos de conversão e impressão serão coletados. [Saiba mais](../data-collection/create-dataset.md)

1. Crie um modelo de IA que aproveitará os eventos do conjunto de dados para classificar ofertas. [Saiba mais](create-ranking-strategies.md)

1. Configure seu schema de ofertas para capturar eventos automaticamente. [Saiba mais](../data-collection/schema-requirement.md)

   >[!IMPORTANT]
   >
   >Os modelos de classificação exigem que os eventos de feedback sejam enviados como eventos de experiência para serem coletados. [Saiba mais sobre a coleção de dados da Gestão de decisões](../data-collection/data-collection.md)

1. Atribua o modelo de IA a um posicionamento em uma decisão para classificar ofertas elegíveis. [Saiba mais](../offer-activities/configure-offer-selection.md)
