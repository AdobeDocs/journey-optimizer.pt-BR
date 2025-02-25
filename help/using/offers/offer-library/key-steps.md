---
title: Etapas principais para criar uma oferta
description: Descubra as principais etapas necessárias para criar uma oferta
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: e375fd3a-b10d-45f4-a95b-ceb48116e841
source-git-commit: 4847415fa33ebf1c21622ebf4faecafd4decc8d3
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 5%

---

# Etapas principais para criar e gerenciar ofertas {#key-steps-to-manage-offers}

As principais etapas para criar, configurar e gerenciar ofertas, bem como usá-las em uma decisão, são apresentadas abaixo.

![](../assets/offer-create-manage-process.png)

Para obter um exemplo completo mostrando como configurar ofertas, usá-las em uma decisão e aproveitar esta decisão em um email, confira [esta página](../offers-e2e.md).

## Criar componentes {#create-components}

Antes de começar a criar ofertas, você deve definir vários componentes que usará em suas ofertas.

1. [Crie inserções](creating-placements.md), que são contêineres que serão usados para exibir suas ofertas. Por exemplo, é possível criar uma disposição que será dedicada às ofertas somente no formato de imagem e situada na parte superior das mensagens.

1. [Crie regras de decisão](creating-decision-rules.md) que especificarão as condições em que as ofertas serão apresentadas.

1. [Criar qualificadores de coleção](creating-tags.md) (anteriormente conhecidos como &quot;marcas&quot;) que você associará às ofertas, permitindo que você os organize e pesquise facilmente na biblioteca.

1. Se quiser definir regras que determinem qual oferta deve ser apresentada primeiro para determinado posicionamento (em vez de considerar as pontuações de prioridade das ofertas), você pode [criar uma fórmula de classificação](../ranking/create-ranking-formulas.md).

<!--
<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-placement.svg" width="60px">
<div>
<a href="../offer-library/creating-placements.md">Create placements</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-rules.svg" width="60px">
<div>
<a href="../offer-library/creating-decision-rules.md">Create decision rules</a>
</div>
<p>
<td>
<img src="../../assets/do-not-localize/icon-tags.svg" width="60px">
<div>
<a href="../offer-library/creating-tags.md">Create collection qualifiers</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-ranking.svg" width="60px">
<div>
<a href="../ranking/create-ranking-formulas.md">Create ranking formulas</a>
</div>
<p>
</td>
</tr>
</table>
-->

## Criar e gerenciar ofertas {#create-and-manage-offers}

1. [Crie ofertas](creating-personalized-offers.md) e configure o conteúdo e as propriedades.

1. [Criar ofertas substitutas](creating-fallback-offers.md), que são as últimas ofertas de recurso a serem exibidas se os clientes não estiverem qualificados para nenhuma das ofertas selecionadas.

1. [Crie uma coleção](creating-collections.md) para incluir as ofertas personalizadas que você criou e use-as em uma decisão.

<!--
<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-offer.svg" width="60px">
<div>
<a href="../offer-library/creating-personalized-offers.md">Create offers</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-fallback.svg" width="60px">
<div>
<a href="../offer-library/creating-fallback-offers.md">Create fallback offers</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-collection.svg" width="60px">
<div>
<a href="../offer-library/creating-collections.md">Create collections</a>
</div>
<p>
</td>
</tr>
</table>
-->

## Criar e configurar decisões {#create-and-configure-decisions}

1. [Crie uma decisão](../offer-activities/create-offer-activities.md) que combinará disposições com as ofertas personalizadas e as ofertas substitutas. Essa combinação será usada pelo mecanismo de decisão para encontrar a melhor oferta para um perfil específico.

1. [Configurar a decisão](../offer-activities/create-offer-activities.md#add-decision-scopes). Para fazer isso, selecione os posicionamentos e, para cada posicionamento, selecione uma coleção e um fallback.

1. Se necessário, você pode [atribuir uma fórmula de classificação](../offer-activities/configure-offer-selection.md#assign-ranking-formula) ou [classificação de IA](../offer-activities/configure-offer-selection.md#use-ranking-strategy) a um posicionamento ao configurar a decisão.

<!--
<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-decision.svg" width="60px">
<div>
<a href="../offer-activities/create-offer-activities.md">Create decisions</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px">
<div>
<a href="../offer-activities/create-offer-activities.md#add-offers">Configure decisions</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px">
<div>
<a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">Assign ranking</a>
</div>
<p>
</td>
</tr>
</table>
-->