---
title: Métodos de classificação
description: Saiba como trabalhar com métodos de classificação
feature: Experience Decisioning, Ranking
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: c1d69bc9-4486-4037-b218-f4f704b2ba9c
source-git-commit: f92e3882d3b5e515e672a4af8e787813d4d939ce
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 21%

---

# Métodos de classificação {#rankings}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_formulas"
>title="Criar fórmulas de classificação"
>abstract="As fórmulas permitem definir regras que determinarão qual item deve ser apresentado primeiro, em vez de considerar as pontuações de prioridade do item. Depois que um método de classificação é criado, é possível atribuí-lo a uma estratégia de decisão para definir quais itens devem ser selecionados primeiro."

>[!BEGINSHADEBOX]

O que há neste guia de documentação:

* [Introdução ao Offer Decisioning](gs-experience-decisioning.md)
* Gerencie seus itens de decisão
   * [Configurar o catálogo de itens](catalogs.md)
   * [Criar itens de decisão](items.md)
   * [Gerenciar coleções de itens](collections.md)
* Configurar a seleção de itens
   * [Criar regras de decisão](rules.md)
   * **[Criar métodos de classificação](ranking.md)**
* [Criar estratégias de seleção](selection-strategies.md)
* [Criar políticas de decisão](create-decision.md)

>[!ENDSHADEBOX]

Os métodos de classificação permitem classificar itens para exibição em um determinado perfil. Depois que um método de classificação é criado, é possível atribuí-lo a uma estratégia de decisão para definir quais itens devem ser selecionados primeiro.

Os métodos de classificação podem ser acessados no **[!UICONTROL Configuração]** / **[!UICONTROL Métodos de classificação]** menu. Dois tipos de métodos de classificação estão disponíveis:

* **Fórmulas** O permite definir regras que determinarão qual item deve ser apresentado primeiro, em vez de considerar as pontuações de prioridade do item.

* **Modelos de IA** O permite usar sistemas de modelo treinados que aproveitarão vários pontos de dados para determinar qual item deve ser apresentado primeiro.

![](assets/ranking-create.png)

Informações detalhadas sobre cada tipo de método de classificação e como criá-lo estão disponíveis na documentação da gestão de decisões acessível aqui:

* [Fórmulas de classificação](../offers/ranking/create-ranking-formulas.md)
* [Modelos de IA](../offers/ranking/ai-models.md)
