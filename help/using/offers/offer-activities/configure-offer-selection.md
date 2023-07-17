---
title: Configurar seleção de ofertas em decisões
description: Saiba como gerenciar a seleção de ofertas em decisões
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 8c7135d7-bf5a-4671-afdf-afec60907a56
source-git-commit: f2174848c70610fc543ea9ddf766f0f7e579053a
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 6%

---

# Configurar seleção de ofertas em decisões {#offers-selection-in-decisions}

Se várias ofertas estiverem qualificadas para uma determinada inserção, você poderá escolher o método que selecionará a melhor oferta para cada perfil ao configurar uma decisão. Você pode classificar ofertas por:
* Prioridade da oferta
* Fórmula de classificação
* [Classificação de IA](#use-ranking-strategy)

![](../assets/offer-rank-by.png)

## Prioridade da oferta {#offer-priority}

Por padrão, quando várias ofertas são qualificadas para uma determinada inserção em uma decisão, as ofertas com a maior **prioridade** será entregue aos clientes primeiro.

![](../assets/offer-priority.png)

As pontuações de prioridade de ofertas são atribuídas ao criar uma oferta. Saiba como criar uma oferta personalizada no [nesta seção](../offer-library/creating-personalized-offers.md).

## Fórmula de classificação {#assign-ranking-formula}

Além da prioridade de oferta, o Journey Optimizer permite criar **fórmulas de classificação**. Essas fórmulas determinam qual oferta deve ser apresentada primeiro para determinada inserção, em vez de considerar as pontuações de prioridade das ofertas.

Por exemplo, você pode aumentar a prioridade de todas as ofertas em que a data de término for inferior a 24 horas a partir de agora ou impulsionar ofertas da categoria &quot;em execução&quot; se o ponto de interesse do perfil for &quot;em execução&quot;.

Saiba como criar uma fórmula de classificação no [nesta seção](../ranking/create-ranking-formulas.md).

Depois que uma fórmula é criada, é possível atribuí-la a uma inserção em uma decisão. Para fazer isso, siga as etapas abaixo:

1. Crie uma decisão ou edite uma existente. Consulte [Criar decisões](../offer-activities/create-offer-activities.md).

1. Adicione os posicionamentos que conterão suas ofertas. Consulte [Criar posicionamentos](../offer-library/creating-placements.md).

1. Para cada posicionamento, adicione uma coleção. Consulte [Criar coleções](../offer-library/creating-collections.md).

1. Selecionar **[!UICONTROL Fórmula]** como o método de classificação e, em seguida, clique em **[!UICONTROL Adicionar classificação]**.

   ![](../assets/offer-activity-ranking.png)

1. Selecione a fórmula desejada e clique em **[!UICONTROL Selecionar]**.

   ![](../assets/ranking-selection.png)

A fórmula de classificação agora está associada ao posicionamento.

Se várias ofertas forem elegíveis para serem apresentadas neste posicionamento, a decisão usará a fórmula selecionada para calcular qual oferta entregar primeiro.

## Classificação de IA {#use-ranking-strategy}

<!--If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service,-->

Você também pode usar um sistema de modelo treinado que classifica automaticamente as ofertas para exibição em determinado perfil ao selecionar um modelo de IA. Saiba como criar um modelo de IA no [nesta seção](../ranking/create-ranking-strategies.md).

Depois que um modelo de IA é criado, é possível atribuí-lo a uma inserção em uma decisão. Para fazer isso, siga as etapas abaixo:

1. Crie uma decisão ou edite uma existente. Consulte [Criar decisões](../offer-activities/create-offer-activities.md).

1. Adicione os posicionamentos que conterão suas ofertas. Consulte [Criar posicionamentos](../offer-library/creating-placements.md).

1. Para cada posicionamento, adicione uma coleção. Consulte [Criar coleções](../offer-library/creating-collections.md).

1. Optar por classificar ofertas por **[!UICONTROL Classificação de IA]** na lista suspensa e clique em **[!UICONTROL Adicionar classificação]**.

   ![](../assets/ranking-selection-ai-ranking.png)

1. Selecione o modelo de IA criado. Todos os detalhes do modelo são exibidos.

   ![](../assets/ranking-selection-ai-ranking-selected.png)

1. Clique em **[!UICONTROL Selecionar]**. O modelo de IA agora está associado à inserção.

Se várias ofertas forem qualificadas, o sistema de modelo treinado determinará qual oferta deve ser apresentada primeiro para uma determinada inserção.

