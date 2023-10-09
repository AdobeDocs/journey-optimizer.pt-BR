---
title: Regras de decisão
description: Saiba como trabalhar com regras de decisão
feature: Offers
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
source-git-commit: 4b23f9fa2d6d7d12988f3c590d6e835637c05bea
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 17%

---

# Regras de decisão {#rules}

>[!BEGINSHADEBOX]

O que há neste guia de documentação:

* [Introdução ao Offer Decisioning](gs-experience-decisioning.md)
* Gerencie seus itens de decisão
   * [Configurar o catálogo de itens](catalogs.md)
   * [Criar itens de decisão](items.md)
   * [Gerenciar coleções de itens](collections.md)
* Configurar a seleção de itens
   * **[Criar regras de decisão](rules.md)**
   * [Criar métodos de classificação](ranking.md)
* [Criar estratégias de seleção](selection-strategies.md)
* [Criar políticas de decisão](create-decision.md)

>[!ENDSHADEBOX]

As regras de decisão permitem definir o público-alvo dos itens de decisão aplicando restrições, diretamente no nível do item de decisão ou em uma estratégia de seleção específica. Isso permite que você controle com precisão quais itens devem ser apresentados a quem.

Por exemplo, vamos considerar um cenário onde você tem itens de decisão com produtos relacionados a Yoga projetados para mulheres. Com as regras de decisão, você pode especificar que esses itens só devem ser exibidos para perfis cujo gênero é &quot;Feminino&quot; e que indicaram um &quot;Ponto de interesse&quot; em &quot;Yoga&quot;.

>[!NOTE]
>
>Além das regras de decisão em nível de estratégia de seleção e item, você também pode definir o público-alvo desejado no nível da campanha. [Saiba mais](../campaigns/create-campaign.md#audience)


A lista de regras de decisão está acessível no **[!UICONTROL Configuração]** / **[!UICONTROL Regras de decisões]** menu.

<!--![](assets/decision-rules-list.png)-->

>[!IMPORTANT]
>
>Journey Optimizer Por enquanto, as regras de decisão são gerenciadas usando o **Gerenciamento de decisão** menu. Como resultado, a **[!UICONTROL Regras de decisão]** A lista no Experience Decisioning inclui regras criadas com base na Journey Optimizer **[!UICONTROL Gerenciamento de decisão]** ou **[!UICONTROL Experience Decisioning]** menus.

Para criar uma regra, siga estas etapas:

1. Navegue até **[!UICONTROL Configuração]** / **[!UICONTROL Regras de decisão]**.
1. A interface do usuário de Gestão de decisões da Journey Optimizer é exibida na área central. Siga as etapas detalhadas na seção [Documentação da gestão de decisões](../offers/offer-library/creating-decision-rules.md) para criar a regra com base nas suas necessidades.

1. Uma vez criada, a regra aparece na lista e está disponível para uso em itens de decisão e estratégias de seleção para controlar a apresentação de itens de decisão para perfis.
