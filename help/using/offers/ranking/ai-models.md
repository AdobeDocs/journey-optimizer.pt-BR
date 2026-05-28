---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Introdução a modelos de IA
description: Saiba mais sobre os modelos de IA que permitem classificar ofertas
badge: label="Legado" type="Informative"
feature: Ranking, Decision Management
topic: Artificial Intelligence
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/Ya5F8s8gr9dM-surRM-0K4VaM9GSs8jIZNVZ9b7pdIM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 440
ht-degree: 27%

---

# Introdução a modelos de IA {#ai-models}

>[!TIP]
>
>O serviço de Decisão, o novo recurso de tomada de decisão do [!DNL Adobe Journey Optimizer], agora está disponível por meio da experiência baseada em código e dos canais de email. [Saiba mais](../../experience-decisioning/gs-experience-decisioning.md)

O [!DNL Journey Optimizer] permite usar um sistema de modelo treinado que classifica as ofertas para exibição em determinado perfil.

Este recurso permite criar **modelos de IA** diferentes com base em suas metas comerciais. Ao usar essas diferentes estratégias baseadas em metas em uma decisão, o sistema de modelo treinado ajudará você a entender como os diferentes modelos de IA estão afetando suas metas.

Por exemplo, você pode selecionar um modelo de IA para o canal de email e outro para o canal de push. Para cada canal, o sistema de modelo treinado utilizará vários pontos de dados para determinar qual oferta deve ser apresentada primeiro para um determinado posicionamento, em vez de considerar as pontuações de prioridade das ofertas ou uma [fórmula de classificação](create-ranking-formulas.md).

>[!IMPORTANT]
>
>Atualmente, os modelos de IA não são compatíveis com os canais criados no Journey Optimizer.

➡️ [Conheça este recurso no vídeo](#video)

## Tipos de modelo de IA {#ai-model-types}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_ai_model_type"
>title="Escolha o tipo de modelo"
>abstract="Selecione o tipo de modelo de IA que deseja criar: a **Otimização automática** otimiza ofertas com base no desempenho de ofertas anteriores, enquanto a **Otimização personalizada** otimiza e personaliza ofertas com base em públicos-alvo e desempenho da oferta."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/decisioning/offer-decisioning/rankings/ai-models/create-ranking-strategies#create-ranking-strategy" text="Criar um modelo de IA"

Dois tipos de modelos de IA estão disponíveis em [!DNL Journey Optimizer]:

* **Os modelos de otimização automática** têm como objetivo fornecer ofertas que maximizam o retorno (KPIs) definido pelos clientes empresariais. Esses KPIs podem estar na forma de taxas de conversão, receita etc. Nesse ponto, a Otimização automática se concentra na otimização de cliques na oferta com a conversão de oferta como destino. A otimização automática não é personalizada e é otimizada com base no desempenho &quot;global&quot; das ofertas. [Saiba mais](auto-optimization-model.md)

* **Os modelos de otimização personalizados** permitem definir metas comerciais e utilizar dados do cliente para treinar modelos orientados para negócios a fim de fornecer ofertas personalizadas e maximizar KPIs. [Saiba mais](personalized-optimization-model.md)

## Criação de um modelo de IA {#create-ai-model}

As principais etapas para criar e usar modelos de IA são as seguintes:

1. Crie um conjunto de dados em que os eventos de conversão e impressão serão coletados. [Saiba mais](../data-collection/create-dataset.md)

1. Crie um modelo de IA que aproveitará os eventos do conjunto de dados para classificar ofertas. [Saiba mais](create-ranking-strategies.md)

1. Configure seu schema de ofertas para capturar eventos automaticamente. [Saiba mais](../data-collection/schema-requirement.md)

   >[!IMPORTANT]
   >
   >Os modelos de IA exigem que os eventos de feedback sejam enviados como eventos de experiência para serem coletados. [Saiba mais sobre a coleção de dados de Gestão de decisão](../data-collection/data-collection.md)

1. Atribua o modelo de IA a um posicionamento em uma decisão para classificar ofertas elegíveis. [Saiba mais](../offer-activities/configure-offer-selection.md)

## Vídeo tutorial {#video}

Saiba como criar um modelo de IA para o Offer decisioning e como aplicá-lo a uma decisão.

>[!VIDEO](https://video.tv.adobe.com/v/3445649?captions=por_br&quality=12)
