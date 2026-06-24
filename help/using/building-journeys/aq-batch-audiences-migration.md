---
solution: Journey Optimizer
product: journey optimizer
title: Migrar públicos em lote de jornadas de qualificação de público-alvo
description: Saiba como migrar jornadas que usam públicos-alvo em lote em um nó de Qualificação de público-alvo antes da data de imposição.
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
keywords: qualificação de público, público em lote, descontinuação, migração, público de leitura, público de transmissão
exl-id: f3c2a7d1-b58e-4a92-c3d5-0e871f2a9b4c
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: ad78185d-8f79-40ad-9bad-cbde74af74eeid: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
source-git-commit: 4a5cbd65b7046e8f1b82147cdc2cd61a3991c258
workflow-type: tm+mt
source-wordcount: 867
ht-degree: 0%

---


# Migrar públicos em lote de jornadas de qualificação de público-alvo {#aq-batch-migration}

A partir de agosto de 2026, a Journey Optimizer bloqueará a publicação de jornadas que usam um público-alvo em lote em um nó de qualificação de público-alvo. Identifique seu caso de uso abaixo e siga o caminho de migração recomendado.

>[!CAUTION]
>
>**Data de aplicação: agosto de 2026.** Jornadas novas, de rascunho e duplicadas usando um público-alvo em lote em um nó de Qualificação de público-alvo não podem ser publicadas após essa data. Um aviso de validação já foi exibido na tela de jornada desde a versão de junho de 2026.

## Por que essa mudança {#why}

O nó **[Qualificação de público-alvo](audience-qualification-events.md)** foi projetado para reagir em tempo quase real conforme perfis individuais entram ou saem de um público-alvo — os eventos de qualificação chegam continuamente, um por um. Ele é destinado a **[públicos-alvo de streaming](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer)**.

Quando um público-alvo em lote é usado com um nó de Qualificação de público-alvo, todos os eventos de qualificação chegam simultaneamente durante a janela de assimilação. Isso pode acionar dezenas de milhares ou milhões de entradas de jornada no mesmo instante, causando tensão grave no sistema e comportamento imprevisível em sistemas downstream. Esse não é o design pretendido do nó de qualificação de público-alvo.

A atividade **[Ler público-alvo](read-audience.md)** é a ferramenta certa para casos de uso baseados em lote: ela é criada para lidar com o processamento em massa agendado de maneira controlada e previsível.

## Como suas jornadas são afetadas {#impact}

Uma jornada em tempo real que usa um público-alvo em lote em um nó de Qualificação de público-alvo continua a ser executada após agosto de 2026. No entanto, se você interromper, duplicar ou republicar a jornada, ela será bloqueada até que a configuração seja atualizada.


| Status da jornada | Impacto após agosto de 2026 |
| --- | --- |
| **jornada ao vivo** | Não afetado. As jornadas ativas existentes continuam em execução. Sem parada automática. |
| **Novas jornadas** | Bloqueado da publicação até que o público-alvo do lote seja substituído. |
| **jornadas de rascunho** | Bloqueado da publicação até que o público-alvo do lote seja substituído. |
| **jornadas duplicadas** | Bloqueado da publicação até que o público-alvo do lote seja substituído. |


## Guia de migração {#migration-paths}

Se você estiver usando um público-alvo em lote em um nó de Qualificação de público-alvo, identifique o caso de uso abaixo e siga o caminho de migração recomendado.

### Caso de uso 1 — Público-alvo criado em eventos de rastreamento de mensagens do AJO {#use-case-1}

**Aparência:** seu público-alvo de Qualificação de Público-alvo usa condições baseadas em envios, aberturas ou cliques de email dos conjuntos de dados de rastreamento interno da Journey Optimizer — por exemplo, *&quot;perfil recebeu um email&quot;* ou *&quot;perfil abriu um email.&quot;*

>[!NOTE]
>
>Desde novembro de 2024, a segmentação por transmissão não oferece mais suporte a eventos de envio e abertura de conjuntos de dados de rastreamento do Journey Optimizer. Os públicos-alvo com base nesses eventos agora são avaliados em modo de lote. [Saiba mais sobre os métodos de avaliação de público](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer)

**Alternativas recomendadas:**

* **Reagindo a aberturas ou cliques na mesma jornada** — Use o nó **[Evento de reação](reaction-events.md)**. Ela foi criada com propósitos específicos para responder a aberturas e cliques de uma mensagem enviada dentro da mesma jornada, sem exigir um público-alvo separado. [Veja um exemplo completo usando eventos de Reação](journeys-uc.md#send-multi-channel-messages)

* **Direcionamento de cliques entre jornadas** — Crie um [público-alvo de streaming](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer) a partir de eventos de clique e use o nó de Qualificação de público-alvo com esse público de streaming.

* **Supressão baseada em rejeição** — Use a [lista de supressão](../configuration/manage-suppression-list.md) nativa do Journey Optimizer em vez de modelar o comportamento de rejeição como uma condição de público-alvo.

* **Qualquer lógica de envio/abertura restante** — Alterne para uma jornada de **[Leitura de Público](read-audience.md)** em uma execução agendada para processar com segurança o público em lotes.


### Caso de uso 2 — Jornada aguardando novos dados de segmentação em lote {#use-case-2}

**Aparência:** você agenda a execução de uma jornada após um trabalho diário de segmentação e usa um nó de Qualificação de público-alvo para garantir que a jornada seja acionada somente depois que os dados de público-alvo mais recentes estiverem disponíveis.

**Alternativa recomendada:**

Use uma jornada **[Read Audience](read-audience.md)** com a opção **[!UICONTROL Trigger after batch audience evaluation]** habilitada. Esse recurso integrado mantém a execução da jornada até que o trabalho de segmentação seja concluído e, em seguida, inicia imediatamente quando dados novos estão disponíveis, sem exigir um nó de qualificação de público-alvo. [Saiba como configurar esta opção](read-audience.md#schedule)


### Caso de uso 3 — Ativação de público-alvo em lote periódico de grande porte {#use-case-3}

**Aparência:** você ativa ou atualiza periodicamente um grande público-alvo (possivelmente milhões de perfis), e a jornada de Qualificação de Público-alvo é acionada para todos os perfis recém-qualificados de uma só vez.

**Alternativa recomendada:**

Use uma jornada **[Read Audience](read-audience.md)**. Ele foi criado para processar grandes públicos-alvo em massa, lidar com perfis em lotes controlados e fornecer uma execução de jornada mais previsível e confiável em escala. [Veja um exemplo completo](message-to-subscribers-uc.md)

## E se nenhuma das alternativas funcionar no seu caso de uso? {#exceptions}

Se o caso de uso não puder ser resolvido usando qualquer um dos caminhos de migração acima, entre em contato com o representante da Adobe. Os casos que não puderem ser tratados com as alternativas existentes serão analisados individualmente.

## Recursos relacionados {#related}

* [Eventos de qualificação de público-alvo](audience-qualification-events.md) — guia de configuração completo e medidas de proteção
* [Ler atividade de público-alvo](read-audience.md) — como configurar a entrada de público-alvo em lote agendada
* [Eventos de reação](reaction-events.md) — como reagir a aberturas e cliques na mesma jornada
* [Métodos de avaliação de público-alvo](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer) — segmentação em lote, streaming e borda explicada
* [Sobre públicos-alvo](../audience/about-audiences.md) — tipos de público-alvo e como eles são criados no Journey Optimizer
* [Gerenciar a lista de supressão](../configuration/manage-suppression-list.md) — como acessar e configurar a supressão de rejeição
* [Jornada medidas de proteção e limitações](limitations.md)
* [Critérios de entrada e saída do Jornada](entry-exit-criteria-guide.md) — entenda os padrões de entrada em lote em tempo real com exemplos reais
* [Enviar mensagens multicanais](journeys-uc.md#send-multi-channel-messages) — caso de uso completo combinando Ler público-alvo, eventos de reação, email e push
* [Enviar uma mensagem aos assinantes](message-to-subscribers-uc.md) — caso de uso completo para ativação de público-alvo em massa com o Público-alvo de Leitura
