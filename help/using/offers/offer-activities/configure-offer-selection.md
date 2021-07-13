---
title: Configurar seleção de ofertas em decisões
description: Saiba como gerenciar a seleção de ofertas em decisões.
feature: Ofertas
topic: Integrações
role: User
level: Intermediate
source-git-commit: 807157d4d6fc1dba018bbe796c8bd213504589dc
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 7%

---

# Configurar seleção de ofertas em decisões {#offers-selection-in-activities}

Se várias ofertas estiverem qualificadas para uma determinada disposição, você poderá escolher o método que selecionará a melhor oferta para cada perfil ao configurar uma decisão (anteriormente conhecida como atividade de oferta). Você pode classificar ofertas por:
* Prioridade da oferta
* Fórmula de classificação

## Prioridade da oferta {#about-offers-priority}

Por padrão, quando várias ofertas estão qualificadas para uma determinada disposição em uma decisão (anteriormente conhecida como atividade de oferta), as ofertas com a maior **prioridade** serão entregues primeiro aos clientes.

![](../../assets/offer-priority.png)

As pontuações de prioridade das ofertas são atribuídas ao criar uma oferta. Saiba como criar uma oferta personalizada em [esta seção](../offer-library/creating-personalized-offers.md)).

## Fórmula de classificação {#assign-ranking-formula}

Além da prioridade da oferta, o Journey Optimizer permite criar **fórmulas de classificação**. Essas são fórmulas que determinam qual oferta deve ser apresentada primeiro para uma determinada disposição, em vez de considerar as pontuações de prioridade das ofertas.

Por exemplo, você pode aumentar a prioridade de todas as ofertas em que a data final seja daqui a menos de 24 horas, ou impulsionar ofertas da categoria &quot;em execução&quot; se o ponto de interesse do perfil estiver &quot;em execução&quot;.

Saiba como criar uma fórmula de classificação em [nesta seção](../offer-library/create-ranking-formulas.md).

Depois que uma fórmula de classificação é criada, é possível atribuí-la a uma disposição em uma decisão (anteriormente conhecida como atividade de oferta). Para fazer isso, siga as etapas abaixo:

1. Crie uma decisão ou edite uma existente. Consulte [Criar decisões](../offer-activities/create-offer-activities.md).

1. Adicione as disposições que conterão suas ofertas. Consulte [Criar disposições](../offer-library/creating-placements.md).

1. Para cada disposição, adicione uma coleção. Consulte [Criar coleções](../offer-library/creating-collections.md).

1. Escolha classificar as ofertas por **[!UICONTROL Ranking]** na lista suspensa e clique em **[!UICONTROL Add ranking]**.

   ![](../../assets/offer-activity-ranking.png)

1. Selecione a fórmula de classificação desejada e clique em **[!UICONTROL Select]**.

   ![](../../assets/ranking-selection.png)

A fórmula de classificação agora está associada à disposição.

Se várias ofertas estiverem qualificadas para serem apresentadas nesta disposição, a decisão usará a fórmula de classificação para calcular qual oferta entregar primeiro.
