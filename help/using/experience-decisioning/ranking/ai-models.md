---
solution: Journey Optimizer
product: Journey Optimizer
title: Introdução a modelos de IA
description: Saiba mais sobre os modelos de IA que permitem classificar ofertas
feature: Ranking, Decisioning
topic: Artificial Intelligence
role: User
level: Intermediate
exl-id: 07679823-2288-4528-b09a-12fd76a69482
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/sWJEr5Pm1wl83Q-2HVb-7mqy7hasQ1ffqRDmJsOFomw
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 338
ht-degree: 22%

---

# Introdução a modelos de IA {#ai-models}

O [!DNL Journey Optimizer] permite usar um sistema de modelo treinado que classifica as ofertas para exibição em determinado perfil.

Este recurso permite criar **modelos de IA** diferentes com base em suas metas comerciais. Ao usar essas diferentes estratégias baseadas em metas em uma decisão, o sistema de modelo treinado ajudará você a entender como os diferentes modelos de IA estão afetando suas metas.

<!--
For example, you can select an AI model for the email channel and another one for the push channel. For each channel, the trained model system will leverage multiple data points to determine which offer should be presented first for a given decision policy?, rather than taking into account the offers' priority scores or a [ranking formula](create-ranking-formulas.md).

>[!IMPORTANT]
>
>For now, ranking models are not supported in Journey Optimizer authored channels.
-->

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

1. Monitore o status e o desempenho do treinamento do modelo de IA. [Saiba mais](ai-model-observability.md)
