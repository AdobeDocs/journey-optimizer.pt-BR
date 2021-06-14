---
title: Configurar seleção de ofertas em decisões
description: Saiba como gerenciar a seleção de ofertas em decisões.
feature: Ofertas
topic: Integrações
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 7%

---

# Configurar seleção de ofertas em decisões {#offers-selection-in-activities}

## Sobre a prioridade Ofertas {#about-offers-priority}

Por padrão, quando várias ofertas estão qualificadas para uma determinada disposição em uma decisão (anteriormente conhecida como atividade de oferta), as ofertas com a maior **prioridade** serão entregues primeiro aos clientes. As pontuações de prioridade das ofertas são atribuídas ao criar uma oferta (consulte [Criar uma oferta personalizada](../offer-library/creating-personalized-offers.md)).

![](../../assets/offer-priority.png)

Além disso, o Journey Optimizer permite criar **fórmulas de classificação**. Essas são fórmulas que determinam qual oferta deve ser apresentada primeiro para uma determinada disposição, em vez de considerar as pontuações de prioridade das ofertas. Por exemplo, você pode aumentar a prioridade de todas as ofertas em que a data final seja daqui a menos de 24 horas, ou impulsionar ofertas da categoria &quot;em execução&quot; se o ponto de interesse do perfil estiver &quot;em execução&quot;.

Para obter mais informações sobre como criar uma fórmula de classificação, consulte [esta seção](../offer-library/create-ranking-formulas.md).

## Atribuir uma fórmula de classificação a uma disposição {#assign-ranking-formula}

Depois que uma fórmula de classificação é criada, você pode atribuí-la a uma disposição em uma decisão. Para fazer isso, siga as etapas abaixo:

* Crie uma decisão ou edite uma existente, em seguida, crie as disposições que conterão suas ofertas (consulte [Criar decisões](../offer-activities/create-offer-activities.md)).

* Para cada disposição, selecione **[!UICONTROL Ranking]** na lista suspensa e clique em **[!UICONTROL Add ranking]**.

   ![](../../assets/offer-activity-ranking.png)

* Selecione a fórmula de classificação desejada e clique em **[!UICONTROL Select]**.

   ![](../../assets/ranking-selection.png)

A fórmula de classificação agora está associada à disposição. Se várias ofertas forem elegíveis para serem apresentadas nesta disposição, a decisão usará a fórmula de classificação para calcular qual oferta entregar primeiro.
