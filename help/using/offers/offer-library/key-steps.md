---
title: Etapas principais para criar uma oferta
description: Descubra as principais etapas necessárias para criar uma oferta
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: e375fd3a-b10d-45f4-a95b-ceb48116e841
source-git-commit: 9cd9d37576b5befbdb62e00a9e07475b8bc9295a
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 14%

---

# Etapas principais para criar e gerenciar ofertas {#key-steps-to-manage-offers}

As principais etapas para criar, configurar e gerenciar ofertas, bem como usá-las em uma decisão, são apresentadas abaixo.

![](../assets/offer-create-manage-process.png)

Para obter um exemplo completo mostrando como configurar ofertas, usá-las em uma decisão e aproveitar essa decisão em um email, confira [esta página](../offers-e2e.md).

## Criar componentes {#create-components}

Antes de começar a criar ofertas, você deve definir vários componentes que usará em suas ofertas.

1. **Criar posicionamentos**, que são contêineres que serão usados para exibir suas ofertas. Por exemplo, é possível criar uma disposição que será dedicada às ofertas somente no formato de imagem e situada na parte superior das mensagens.

1. **Criar regras de decisão** que especificará as condições em que as ofertas serão apresentadas.

1. **Criar qualificadores de coleção** (anteriormente conhecido como &quot;tags&quot;) que você associará às ofertas, permitindo que organize e pesquise facilmente na biblioteca.

1. Se quiser definir regras que determinarão qual oferta deve ser apresentada primeiro para uma determinada inserção (em vez de considerar as pontuações de prioridade das ofertas), você poderá **criar uma fórmula de classificação**.

<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-placement.svg" width="60px">
<div>
<a href="../offer-library/creating-placements.md">Criar posicionamentos</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-rules.svg" width="60px">
<div>
<a href="../offer-library/creating-decision-rules.md">Criar regras de decisão</a>
</div>
<p>
<td>
<img src="../../assets/do-not-localize/icon-tags.svg" width="60px">
<div>
<a href="../offer-library/creating-tags.md">Criar tags</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-ranking.svg" width="60px">
<div>
<a href="../ranking/create-ranking-formulas.md">Criar fórmulas de classificação</a>
</div>
<p>
</td>
</tr>
</table>

## Criar e gerenciar ofertas {#create-and-manage-offers}

1. **Criar ofertas** e configure o conteúdo e as propriedades.

1. **Criar ofertas substitutas**, que são as ofertas de último recurso a serem exibidas se os clientes não estiverem qualificados para nenhuma das ofertas selecionadas.

1. **Criar uma coleção** para incluir as ofertas personalizadas que você criou e usá-las em uma decisão.

<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-offer.svg" width="60px">
<div>
<a href="../offer-library/creating-personalized-offers.md">Criar ofertas</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-fallback.svg" width="60px">
<div>
<a href="../offer-library/creating-fallback-offers.md">Criar ofertas de fallback</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-collection.svg" width="60px">
<div>
<a href="../offer-library/creating-collections.md">Criar coleções</a>
</div>
<p>
</td>
</tr>
</table>

## Criar e configurar decisões {#create-and-configure-decisions}

1. **Criar uma decisão** que combinará disposições com as ofertas personalizadas e as ofertas substitutas. Essa combinação será usada pelo mecanismo de decisão para encontrar a melhor oferta para um perfil específico.

1. **Configurar a decisão**. Para fazer isso, selecione os posicionamentos e, para cada posicionamento, selecione uma coleção e um fallback.

1. Se necessário, você pode **atribuir uma fórmula de classificação** para um posicionamento ao configurar a decisão.

<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-decision.svg" width="60px">
<div>
<a href="../offer-activities/create-offer-activities.md">Criar decisões</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px">
<div>
<a href="../offer-activities/create-offer-activities.md#add-offers">Configurar decisões</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px">
<div>
<a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">Atribuir classificação</a>
</div>
<p>
</td>
</tr>
</table>
