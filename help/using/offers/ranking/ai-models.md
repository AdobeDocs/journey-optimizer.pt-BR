---
product: experience platform
solution: Experience Platform
title: Introdução a modelos de IA
description: Saiba mais sobre os modelos de IA que permitem classificar ofertas
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
source-git-commit: 12b01cb9de84399e5ede987866609acc10b64c5f
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 3%

---

# Introdução a modelos de IA {#ai-models}

[!DNL Journey Optimizer] O permite usar um sistema de modelo treinado que classifica ofertas para exibição em um determinado perfil.

Este recurso permite que você crie diferentes **Modelos de IA** com base em suas metas comerciais. Usando essas diferentes estratégias baseadas em objetivos em uma decisão, o sistema de modelo treinado ajudará você a entender como os diferentes modelos de IA estão afetando suas metas.

Por exemplo, você pode selecionar um modelo de IA para o canal de email e outro para o canal de push. Para cada canal, o sistema de modelo treinado aproveitará vários pontos de dados para determinar qual oferta deve ser apresentada primeiro para uma determinada disposição, em vez de considerar as pontuações de prioridade das ofertas ou uma [fórmula de classificação](create-ranking-formulas.md).

## Tipos de modelo de IA {#ai-model-types}

Por enquanto, [!DNL Journey Optimizer]** fornece um modelo de IA, **Otimização automática**, que otimiza as ofertas com base no desempenho da oferta anterior. Informações detalhadas sobre esse tipo de modelo de IA estão disponíveis em [esta seção](auto-optimization-model.md).

## Criação de um modelo de IA {#create-ai-model}

As principais etapas para criar e usar modelos de IA são as seguintes:

1. Crie um conjunto de dados no qual os eventos de conversão e impressão serão coletados. [Saiba mais](create-dataset.md)
1. Crie um modelo de IA que aproveitará eventos do conjunto de dados para classificar ofertas. [Saiba mais](create-ranking-strategies.md)
1. Configure seu schema de ofertas para capturar automaticamente eventos. [Saiba mais](schema-requirement.md)
1. Atribua o modelo de IA a uma disposição em uma decisão de classificar ofertas elegíveis. [Saiba mais](../offer-activities/configure-offer-selection.md)
