---
solution: Journey Optimizer
product: Journey Optimizer
title: Definir regras de limites de mensagens e jornada
description: Definir regras de limites de mensagens e jornada
redpen-status: CREATED_||_2025-08-11_20-28-34
exl-id: 630e252a-aab2-4a27-ad46-d4dbfbc3f3a4
source-git-commit: 9e23162373564e7866af115ee2cd706527336e4a
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 38%

---

# Definir regras de limites de mensagens e jornada{#section-overview}

As regras de limitação fazem parte do [gerenciamento de conflitos e priorização](../using/conflict-prioritization/gs-conflict-prioritization.md). Elas ajudam a garantir que os clientes recebam a quantidade certa de comunicação sem se sentirem sobrecarregados. Antes de aplicar regras, use a [ferramenta de detecção de conflitos](../using/conflict-prioritization/conflicts.md) para identificar jornadas e campanhas sobrepostas. Quando várias comunicações se qualificam para o mesmo perfil, as [pontuações de prioridade](../using/conflict-prioritization/priority-scores.md) determinam qual mensagem é entregue primeiro.

Você pode definir limites na frequência com que as mensagens são enviadas (limite de frequência), quantas jornadas um perfil pode inserir (limite de jornada) e quando as mensagens são bloqueadas (horas de silêncio). As regras são agrupadas em **conjuntos de regras** e aplicadas a campanhas ou jornadas. Para obter controle programático de sistemas externos, consulte a [API de Limite](../using/configuration/capping.md).

## Definir regras de limite de mensagens e jornadas

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

Trabalhar com conjuntos de regras

Saiba como criar, gerenciar e ativar conjuntos de regras para controlar a frequência das mensagens e as regras de entrada de jornadas no Adobe Journey Optimizer.

[Explore os conjuntos de regras](../using/conflict-prioritization/rule-sets.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

Limite e arbitragem de jornadas

Descubra como definir limites de simultaneidade e entradas da jornada, priorizar jornadas e monitorar exclusões para evitar excesso de comunicação.

[Saiba mais sobre o limite de jornadas](../using/conflict-prioritization/journey-capping.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

Limite de frequência por canal

Entenda como criar e aplicar regras de limite da frequência específicas de cada canal para otimizar a entrega de mensagens e evitar uma comunicação excessiva.

[Definir limite de frequência](../using/conflict-prioritization/channel-capping.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg)

Definir Período de Silêncio

Defina exclusões com base no tempo para emails, SMS, push e WhatsApp para que nenhuma mensagem seja enviada durante períodos específicos, respeitando as preferências e a conformidade do cliente.

[Definir períodos de silêncio](../using/conflict-prioritization/quiet-hours.md)
:::

::::

## Recursos adicionais

- **[Introdução ao gerenciamento de conflitos e priorização](../using/conflict-prioritization/gs-conflict-prioritization.md)** - Visão geral da detecção de conflitos, pontuações de prioridade e conjuntos de regras.
- **[Identificar possíveis conflitos](../using/conflict-prioritization/conflicts.md)** - Detectar jornadas e campanhas sobrepostas antes de aplicar regras de limitação.
- **[Atribuir pontuações de prioridade](../using/conflict-prioritization/priority-scores.md)** - Controla qual jornada ou campanha tem prioridade quando um perfil se qualifica para várias comunicações.
