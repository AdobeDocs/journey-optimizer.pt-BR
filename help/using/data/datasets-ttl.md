---
solution: Journey Optimizer
product: journey optimizer
title: Sobre a nova proteção de Tempo de vida (TTL)
description: Nova proteção de TTL (Time-to-live) no Adobe Journey Optimizer
feature: Data Model, Datasets, Data Management
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: plataforma, data lake, criar, lake, conjuntos de dados, perfil
source-git-commit: f16ce53f61d64d23f530d007e0124a84e2cc3405
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 5%

---


# Atualizações de segmentação de transmissão e tempo de vida útil (TTL) {#ttl-guardrail}

## Grade de proteção de tempo de vida (TTL) {#ttl}

A partir de 1º de novembro de 2024, uma garantia de TTL (time-to-live) será implantada para conjuntos de dados gerados pelo sistema da Journey Optimizer em **novas sandboxes e novas organizações** da seguinte maneira:

* 90 dias para dados na loja de perfis
* 13 meses para dados no data lake

Esta alteração será implantada em **sandboxes de cliente existentes** posteriormente em uma fase posterior.

**Perguntas frequentes**

+++ Essa alteração se aplicará somente às sandboxes de produção ou também se aplicará às sandboxes de desenvolvimento?

Essa alteração será aplicada a todos os tipos de sandbox.

+++


+++ Para o TTL de 90 dias no armazenamento de perfis, os próprios perfis são afetados?

Os dados do conjunto de dados gerados pelo sistema no perfil são descartados após 90 dias, não os próprios perfis.

+++

+++ Se os dados de um conjunto de dados gerado pelo sistema forem enviados para o Customer Journey Analytics (CJA), os dados no CJA também serão afetados pelo TTL?

Os dados no CJA são mantidos em sincronia com o Experience Platform. Portanto, uma remoção de dados devido a um TTL em dados de conjunto de dados gerados pelo sistema também afetará os dados no CJA.

+++

## Atualizações de segmentação de transmissão {#segmentation-update}

Além disso, em 1º de novembro, a segmentação por transmissão não oferecerá mais suporte ao uso de eventos de envio e feedback de conjuntos de dados de rastreamento e feedback. Informações sobre por que esta prática foi desencorajada no passado podem ser encontradas [aqui](../audience/about-audiences.md#streaming-segmentation-events-guardrails).


**Perguntas frequentes**

+++ Essas alterações afetarão o uso de cliques ou outros eventos de rastreamento?

Essa alteração afeta apenas o uso de eventos de envio e abertos; os cliques e outros eventos de rastreamento ainda podem ser usados em um segmento de transmissão.

+++

+++ A segmentação em lote será afetada por essa alteração?

Essa alteração afeta apenas a segmentação por transmissão; eventos de envio e abertos ainda podem ser usados em um segmento em lote. Se forem usados em um segmento de transmissão, serão avaliados em lote.

+++

+++ Essa alteração afetará a coleta de dados de rastreamento?

Essa alteração não afeta a coleta de dados de rastreamento. Eventos de envio e abertura continuarão a ser coletados.

+++


+++ Os eventos de reação são afetados por essa alteração?

Os eventos de reação nas Jornadas não são afetados por essa alteração.

+++


+++ Essa alteração se aplicará somente às sandboxes de produção ou também se aplicará às sandboxes de desenvolvimento?

Essa alteração será aplicada a todos os tipos de sandbox.

+++