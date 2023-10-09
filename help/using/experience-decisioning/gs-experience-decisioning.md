---
title: Introdução ao Offer Decisioning
description: Saiba mais sobre o Experience Decisioning
feature: Offers
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 18%

---

# Introdução ao Offer Decisioning {#get-started-experience-decisioning}

>[!BEGINSHADEBOX]

O que há neste guia de documentação:

* **[Introdução ao Offer Decisioning](gs-experience-decisioning.md)**
* Gerencie seus itens de decisão
   * [Configurar o catálogo de itens](catalogs.md)
   * [Criar itens de decisão](items.md)
   * [Gerenciar coleções de itens](collections.md)
* Configurar a seleção de itens
   * [Criar regras de decisão](rules.md)
   * [Criar métodos de classificação](ranking.md)
* [Criar estratégias de seleção](selection-strategies.md)
* [Criar políticas de decisão](create-decision.md)

>[!ENDSHADEBOX]

## O que é o Experience Decisioning {#about}

>[!AVAILABILITY]
>
>O recurso de decisão de experiência está disponível atualmente como um beta apenas para usuários selecionados. Para participar do programa beta, entre em contato com o Atendimento ao cliente da Adobe.

O Experience Decisioning simplifica a personalização oferecendo um catálogo centralizado de ofertas de marketing conhecidas como &quot;itens de decisão&quot; e um mecanismo de decisão sofisticado. Esse mecanismo usa regras e critérios de classificação para selecionar e apresentar os itens de decisão mais relevantes para cada indivíduo.

Esses itens de decisão são perfeitamente integrados em uma grande variedade de superfícies de entrada por meio do novo canal de experiência baseado em código, agora acessível nas campanhas do Journey Optimizer.

**Limitações:**

* As políticas de decisão estão disponíveis para uso somente em campanhas de experiência baseadas em código.
* Por enquanto, o limite de frequência não está disponível no Experience Decisioning.

## Principais etapas do Experience Decisioning {#steps}

As principais etapas para trabalhar com o Experience Decisioning são as seguintes:

1. **Configurar atributos personalizados**: personalize o catálogo dos itens de decisão de acordo com suas necessidades específicas, configurando atributos personalizados no esquema do catálogo.

1. **Criar itens de decisão** para mostrar ao público-alvo direcionado.

1. **Organizar com coleções**: use coleções para categorizar itens de decisão com base em regras baseadas em atributos. Incorpore coleções nas estratégias de seleção para determinar qual coleção de itens de decisão deve ser considerada.

1. **Criar regras de decisão**: as regras de decisão são usadas em itens de decisão e/ou estratégias de seleção para determinar para quem um item de decisão pode ser mostrado.

1. **Implementar métodos de classificação**: crie métodos de classificação e aplique-os nas estratégias de decisão para determinar a ordem de prioridade para selecionar itens de decisão.

1. **Criar estratégias de seleção**: crie estratégias de seleção que aproveitam coleções, regras de decisão e métodos de classificação para identificar os itens de decisão adequados para exibição em perfis.

1. **Incorpore uma política de decisão à sua campanha baseada em código**: as políticas de decisão combinam várias estratégias de seleção para determinar os itens de decisão qualificados a serem exibidos para o público-alvo desejado.
