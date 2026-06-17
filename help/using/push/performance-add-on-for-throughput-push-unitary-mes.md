---
solution: Journey Optimizer
product: journey optimizer
title: Complemento de desempenho para taxa de transferência - (push) Unitário - Entrega de mensagem
description: Saiba como configurar e usar o complemento de desempenho para entrega de mensagens - (Push) Unitário no Adobe Journey Optimizer.
feature: Push
topic: Content Management
role: User
level: Intermediate
exl-id: 2d0677ad-41c8-4299-a7c8-0e4f8a1716f7
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: c96d2aa5-76a2-443d-8d23-5de95577c909
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b6b77c26-2a48-4a62-9ceb-5ae67f4dfde5
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 4aebdb06094628cfe7393c7f7b41e5fe0ee9df13
workflow-type: tm+mt
source-wordcount: 252
ht-degree: 3%

---


# Complemento de desempenho para taxa de transferência - (push) Unitário - Entrega de mensagem {#performance-add-on-for-throughput-push-unitary-mes}

>[!AVAILABILITY]
>
>Este recurso está disponível no **AJO26.7** (27/07/2026).

## Visão geral {#overview}

O Adobe Journey Optimizer apresenta o **Complemento de desempenho para Taxa de transferência - (Push) Unitário - Entrega de mensagem**, permitindo que as organizações forneçam experiências do cliente mais relevantes e personalizadas em canais de push.

Esta página explica como configurar e usar esse recurso em suas campanhas e jornadas.

## Pré-requisitos {#prerequisites}

Antes de começar:

* Você tem acesso ao Adobe Journey Optimizer com as permissões de **Push** necessárias.
* Uma superfície de canal de push está configurada. Consulte [Configurar canal Push](../configuration/channel-surfaces.md).

## Como funciona {#how-it-works}

Complemento de desempenho para taxa de transferência - (Push) Unitário - A entrega de mensagens integra-se diretamente com o mecanismo de execução do AJO. Quando um perfil atinge uma ação de push em uma jornada ou campanha, o recurso aplica os parâmetros configurados no momento do envio.

Principais recursos:

* **Personalização em nível de perfil** — as configurações são adaptadas por destinatário usando atributos de perfil e contexto.
* **suporte a campanhas e Jornadas** — funciona em jornadas orquestradas e campanhas únicas.
* **Métricas em tempo real** — os resultados aparecem nos [Relatórios de push](../reports/push-report.md).

## Configurar o complemento de desempenho para a taxa de transferência {#configure}

1. No menu esquerdo do AJO, navegue até **Canais** > **Configurações de push**.
1. Selecione ou crie uma configuração de canal.
1. Na seção **Complemento de Desempenho para**, habilite o recurso.
1. Defina os parâmetros necessários.
1. Clique em **Save**.

>[!NOTE]
>
>As alterações de configuração se aplicam a novas execuções de jornada. As jornadas em andamento não são afetadas.

## Tópicos relacionados {#related-topics}

* [Introdução ao Push](get-started-push.md)
* [Criar uma notificação por push](create-push.md)
* [Notas de versão do AJO26.7](../rn/release-notes.md)
