---
product: experience platform
solution: Experience Platform
title: Introdução a modelos de IA
description: Saiba mais sobre os modelos de IA que permitem classificar ofertas
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
source-git-commit: 12bc2373ac5c391764df3880c5c87666a19e99b2
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 4%

---

# Introdução a modelos de IA {#ai-models}

[!DNL Journey Optimizer] O permite usar um sistema de modelo treinado que classifica ofertas para exibição em um determinado perfil.

Este recurso permite que você crie diferentes **Modelos de IA** com base em suas metas comerciais. Usando essas diferentes estratégias baseadas em objetivos em uma decisão, o sistema de modelo treinado ajudará você a entender como os diferentes modelos de IA estão afetando suas metas.

Por exemplo, você pode selecionar um modelo de IA para o canal de email e outro para o canal de push. Para cada canal, o sistema de modelo treinado aproveitará vários pontos de dados para determinar qual oferta deve ser apresentada primeiro para uma determinada disposição, em vez de considerar as pontuações de prioridade das ofertas ou uma [fórmula de classificação](create-ranking-formulas.md).

## Tipos de modelo de IA {#ai-model-types}

Dois tipos de modelos de IA estão disponíveis em [!DNL Journey Optimizer]:

* **Modelos de otimização automática** têm como objetivo fornecer ofertas que maximizem o retorno (KPIs) definido por clientes comerciais. Esses KPIs podem estar na forma de taxas de conversão, receita etc. Neste ponto, a Otimização automática se concentra na otimização de cliques de oferta com a conversão de oferta como nossa meta. A otimização automática não é personalizada e otimiza com base no desempenho &quot;global&quot; das ofertas. [Saiba mais](auto-optimization-model.md)

* **Modelos de personalização** permite definir objetivos de negócios e utilizar dados de clientes para treinar modelos orientados a negócios para fornecer ofertas personalizadas e maximizar KPIs. [Saiba mais](personalized-optimization-model.md)

   >[!CAUTION]
   >
   >O uso de modelos de Otimização personalizada está disponível no momento somente para usuários selecionados.

## Criação de um modelo de IA {#create-ai-model}

As principais etapas para criar e usar modelos de IA são as seguintes:

1. Crie um conjunto de dados no qual os eventos de conversão e impressão serão coletados. [Saiba mais](create-dataset.md)
1. Crie um modelo de IA que aproveitará eventos do conjunto de dados para classificar ofertas. [Saiba mais](create-ranking-strategies.md)
1. Configure seu schema de ofertas para capturar automaticamente eventos. [Saiba mais](schema-requirement.md)
1. Atribua o modelo de IA a uma disposição em uma decisão de classificar ofertas elegíveis. [Saiba mais](../offer-activities/configure-offer-selection.md)
