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
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: c132d929-fa62-4271-803e-b823be07b914
  - id: ed0d8d0e-04b9-4326-be72-a0fbca265377
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
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

