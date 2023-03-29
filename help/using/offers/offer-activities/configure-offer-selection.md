---
title: Configurar seleção de ofertas em decisões
description: Saiba como gerenciar a seleção de ofertas em decisões
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 8c7135d7-bf5a-4671-afdf-afec60907a56
source-git-commit: 4f3d22c9ce3a5b77969a2a04dafbc28b53f95507
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 6%

---

# Configurar seleção de ofertas em decisões {#offers-selection-in-decisions}

Se várias ofertas estiverem qualificadas para uma determinada disposição, você poderá escolher o método que selecionará a melhor oferta para cada perfil ao configurar uma decisão. Você pode classificar ofertas por:
* Prioridade da oferta
* Fórmula de classificação
* [Classificação de IA](#use-ranking-strategy)

![](../assets/offer-rank-by.png)

## Prioridade da oferta {#offer-priority}

Por padrão, quando várias ofertas estão qualificadas para uma determinada disposição em uma decisão, as ofertas com o maior **priority** serão entregues aos clientes primeiro.

![](../assets/offer-priority.png)

As pontuações de prioridade das ofertas são atribuídas ao criar uma oferta. Saiba como criar uma oferta personalizada no [esta seção](../offer-library/creating-personalized-offers.md).

## Fórmula de classificação {#assign-ranking-formula}

Além da prioridade da oferta, o Journey Optimizer permite criar **fórmulas de classificação**. Essas são fórmulas que determinam qual oferta deve ser apresentada primeiro para uma determinada disposição, em vez de considerar as pontuações de prioridade das ofertas.

Por exemplo, você pode aumentar a prioridade de todas as ofertas em que a data final seja daqui a menos de 24 horas, ou impulsionar ofertas da categoria &quot;em execução&quot; se o ponto de interesse do perfil estiver &quot;em execução&quot;.

Saiba como criar uma fórmula de classificação no [esta seção](../ranking/create-ranking-formulas.md).

Depois que uma fórmula é criada, você pode atribuí-la a uma disposição em uma decisão. Para fazer isso, siga as etapas abaixo:

1. Crie uma decisão ou edite uma existente. Consulte [Criar decisões](../offer-activities/create-offer-activities.md).

1. Adicione as disposições que conterão suas ofertas. Consulte [Criar disposições](../offer-library/creating-placements.md).

1. Para cada disposição, adicione uma coleção. Consulte [Criar coleções](../offer-library/creating-collections.md).

1. Selecionar **[!UICONTROL Fórmula]** como método de classificação, clique em **[!UICONTROL Adicionar classificação]**.

   ![](../assets/offer-activity-ranking.png)

1. Selecione a fórmula desejada e clique em **[!UICONTROL Selecionar]**.

   ![](../assets/ranking-selection.png)

A fórmula de classificação agora está associada à disposição.

Se várias ofertas estiverem qualificadas para serem apresentadas nesta disposição, a decisão usará a fórmula selecionada para calcular qual oferta entregar primeiro.

## Classificação de IA {#use-ranking-strategy}

<!--If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service,-->

Você também pode usar um sistema de modelo treinado que classifica automaticamente as ofertas para exibição em um determinado perfil selecionando uma estratégia de classificação. Saiba como criar uma estratégia de classificação no [esta seção](../ranking/create-ranking-strategies.md).

Depois que uma estratégia de classificação for criada, você poderá atribuí-la a uma disposição em uma decisão. Para fazer isso, siga as etapas abaixo:

1. Crie uma decisão ou edite uma existente. Consulte [Criar decisões](../offer-activities/create-offer-activities.md).

1. Adicione as disposições que conterão suas ofertas. Consulte [Criar disposições](../offer-library/creating-placements.md).

1. Para cada disposição, adicione uma coleção. Consulte [Criar coleções](../offer-library/creating-collections.md).

1. Escolha classificar ofertas por **[!UICONTROL Classificação AI]** na lista suspensa e clique em **[!UICONTROL Adicionar classificação]**.

   ![](../assets/ranking-selection-ai-ranking.png)

1. Selecione a estratégia de classificação criada. Todos os detalhes da estratégia de classificação são exibidos.

   ![](../assets/ranking-selection-ai-ranking-selected.png)

1. Clique em **[!UICONTROL Selecionar]**. A estratégia de classificação agora está associada ao posicionamento.

Se várias ofertas forem elegíveis, o sistema de modelo treinado determinará qual oferta deve ser apresentada primeiro para uma determinada disposição.

