---
title: Etapas principais para criar uma oferta
description: Descubra as principais etapas necessárias para criar uma oferta.
feature: Ofertas
topic: Integrações
role: User
level: Intermediate
source-git-commit: 5631a1937b854c3e14d1816df9e8d30690588303
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 12%

---

# Etapas principais para criar e gerenciar ofertas {#key-steps}

As principais etapas para criar, configurar e gerenciar ofertas, bem como usá-las em uma decisão, são apresentadas abaixo.

![](../../assets/offer-create-manage-process.png)

Para obter um exemplo completo mostrando como configurar ofertas, use-as em uma decisão e aproveite essa decisão em um email, confira [esta página](../offers-e2e.md).

## Criar componentes

Antes de começar a criar ofertas, você deve definir vários componentes que usará em suas ofertas.

1. **Crie disposições**, que são contêineres que serão usados para mostrar suas ofertas. Você pode, por exemplo, criar uma disposição que será dedicada apenas a ofertas no formato de imagem e situada na parte superior das mensagens.

1. **Crie** regras de decisão que especificarão as condições em que as ofertas serão apresentadas.

1. **Crie** tags que serão associadas às ofertas, permitindo que você as organize e pesquise facilmente na biblioteca.

1. Se você quiser definir regras que determinam qual oferta deve ser apresentada primeiro para uma determinada disposição (em vez de considerar as pontuações de prioridade das ofertas), poderá **criar uma fórmula de classificação**.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-placement.svg" width="60px"><p><a href="../offer-library/creating-placements.md">Criar inserções</a></p></td>
<td><img src="../../assets/do-not-localize/icon-rules.svg" width="60px"><p><a href="../offer-library/creating-decision-rules.md">Criar regras de decisão</a></p></td>
<td><img src="../../assets/do-not-localize/icon-tags.svg" width="60px"><p><a href="../offer-library/creating-tags.md">Criar tags</a></p></td>
<td><img src="../../assets/do-not-localize/icon-ranking.svg" width="60px"><p><a href="../offer-library/create-ranking-formulas.md">Criar fórmulas de classificação</a></p></td>
</table>

## Criar e gerenciar ofertas

1. **Crie ofertas** e configure seu conteúdo e propriedades.

1. **Crie ofertas** de fallback, que são as últimas ofertas de recurso a serem exibidas se os clientes não estiverem qualificados para nenhuma das ofertas selecionadas.

1. **Crie uma** coleção para incluir as ofertas personalizadas que você criou e usá-las em uma decisão.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-offer.svg" width="60px"><p><a href="../offer-library/creating-personalized-offers.md">Criar ofertas</a></p></td>
<td><img src="../../assets/do-not-localize/icon-fallback.svg" width="60px"><p><a href="../offer-library/creating-fallback-offers.md">Criar ofertas substitutas</a></p></td>
<td><img src="../../assets/do-not-localize/icon-collection.svg" width="60px"><p><a href="../offer-library/creating-collections.md">Criar coleções</a></p></td></tr>
</table>

## Criar e configurar decisões

1. **Crie uma** decisão que combinará disposições com as ofertas personalizadas e as ofertas de fallback. Essa combinação será usada pelo mecanismo do Offer Decisioning para encontrar a melhor oferta para um perfil específico.

1. **Configure a decisão**. Para fazer isso, selecione as disposições e, para cada disposição, selecione uma coleção e um fallback.

1. Se necessário, você pode **atribuir uma fórmula de classificação** a uma disposição ao configurar a decisão.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md">Criar decisões</a></p></td>
<td><img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md#add-offers">Configurar decisões</a></p></td>
<td><img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px"><p><a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">Atribuir classificação</a></p></td>
</tr>
</table>
