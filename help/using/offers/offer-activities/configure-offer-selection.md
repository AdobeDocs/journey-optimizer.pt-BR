---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Configurar seleção de ofertas em decisões
description: Saiba como gerenciar a seleção de ofertas em decisões
badge: label="Legado" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 8c7135d7-bf5a-4671-afdf-afec60907a56
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/cuderynmp3lamdVZiG5A5Lo9ZSBym46mw0hhiVp88uU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 467
ht-degree: 10%

---

# Configurar seleção de ofertas em decisões {#offers-selection-in-decisions}

>[!TIP]
>
>O serviço de Decisão, o novo recurso de tomada de decisão do [!DNL Adobe Journey Optimizer], agora está disponível por meio da experiência baseada em código e dos canais de email. [Saiba mais](../../experience-decisioning/gs-experience-decisioning.md)

Se várias ofertas estiverem qualificadas para uma determinada inserção, você poderá escolher o método que selecionará a melhor oferta para cada perfil ao configurar uma decisão. Você pode classificar ofertas por:

* Prioridades de ofertas
* Fórmula de classificação
* [Classificação de IA](#use-ranking-strategy)

![](../assets/offer-rank-by.png)

## Prioridades de ofertas {#offer-priority}

Por padrão, quando várias ofertas estão qualificadas para um determinado posicionamento em uma decisão, as ofertas com a **prioridade** mais alta serão entregues aos clientes primeiro.

![](../assets/offer-priority.png)

As pontuações de prioridade de ofertas são atribuídas ao criar uma oferta. Saiba como criar uma oferta personalizada em [esta seção](../offer-library/creating-personalized-offers.md).

## Fórmula de classificação {#assign-ranking-formula}

Além da prioridade de oferta, o Journey Optimizer permite criar **fórmulas de classificação**. Essas fórmulas determinam qual oferta deve ser apresentada primeiro para determinada inserção, em vez de considerar as pontuações de prioridade das ofertas.

Por exemplo, você pode aumentar a prioridade de todas as ofertas em que a data de término for inferior a 24 horas a partir de agora ou impulsionar ofertas da categoria &quot;em execução&quot; se o ponto de interesse do perfil for &quot;em execução&quot;.

Saiba como criar uma fórmula de classificação em [esta seção](../ranking/create-ranking-formulas.md).

Depois que uma fórmula é criada, é possível atribuí-la a uma inserção em uma decisão. Para fazer isso, siga as etapas abaixo:

1. Crie uma decisão ou edite uma existente. Consulte [Criar decisões](../offer-activities/create-offer-activities.md).

1. Adicione os posicionamentos que conterão suas ofertas. Consulte [Criar inserções](../offer-library/creating-placements.md).

1. Para cada posicionamento, adicione uma coleção. Consulte [Criar coleções](../offer-library/creating-collections.md).

1. Selecione **[!UICONTROL Fórmula]** como o método de classificação e clique em **[!UICONTROL Adicionar classificação]**.

   ![](../assets/offer-activity-ranking.png)

1. Selecione a fórmula desejada e clique em **[!UICONTROL Selecionar]**.

   ![](../assets/ranking-selection.png)

A fórmula de classificação agora está associada ao posicionamento.

Se várias ofertas forem elegíveis para serem apresentadas neste posicionamento, a decisão usará a fórmula selecionada para calcular qual oferta entregar primeiro.

## Classificação de IA {#use-ranking-strategy}

<!--If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service,-->

Você também pode usar um sistema de modelo treinado que classifica automaticamente as ofertas para exibição em determinado perfil ao selecionar um modelo de IA. Saiba como criar um modelo de IA em [esta seção](../ranking/create-ranking-strategies.md).

Depois que um modelo de IA é criado, é possível atribuí-lo a uma inserção em uma decisão. Para fazer isso, siga as etapas abaixo:

1. Crie uma decisão ou edite uma existente. Consulte [Criar decisões](../offer-activities/create-offer-activities.md).

1. Adicione os posicionamentos que conterão suas ofertas. Consulte [Criar inserções](../offer-library/creating-placements.md).

1. Para cada posicionamento, adicione uma coleção. Consulte [Criar coleções](../offer-library/creating-collections.md).

1. Escolha classificar as ofertas por **[!UICONTROL Classificação de IA]** na lista suspensa e clique em **[!UICONTROL Adicionar classificação]**.

   ![](../assets/ranking-selection-ai-ranking.png)

1. Selecione o modelo de IA criado. Todos os detalhes do modelo são exibidos.

   ![](../assets/ranking-selection-ai-ranking-selected.png)

1. Clique em **[!UICONTROL Selecionar]**. O modelo de IA agora está associado à inserção.

Se várias ofertas forem qualificadas, o sistema de modelo treinado determinará qual oferta deve ser apresentada primeiro para uma determinada inserção.

