---
solution: Journey Optimizer
product: journey optimizer
title: Recursos do Journey Optimizer por pacote
description: Entenda quais recursos do Adobe Journey Optimizer estão disponíveis com base na sua licença, pacote e canais ativados.
feature: Get Started
topic: Content Management
role: Admin, User
level: Beginner
keywords: jornada otimizer, pacote, licença, select, prime, ultimate, recursos, modular, canais
hide: true
source-git-commit: 46a5a6dc0a3486633a1a71f8bba8a3cd53aaa618
workflow-type: tm+mt
source-wordcount: '1007'
ht-degree: 5%

---


# O que está disponível no meu pacote [!DNL Adobe Journey Optimizer]? {#ajo-packages}

>[!BEGINSHADEBOX]

**Nesta página:** Descubra quais recursos do Adobe Journey Optimizer seu pacote desbloqueia, se você usa o modelo atual do Campaigns e Jornada ou o licenciamento Select, Prime e Ultimate herdado, para poder confirmar o que está disponível e acessar cada recurso.

>[!ENDSHADEBOX]

Os recursos do [!DNL Adobe Journey Optimizer] variam com base no contrato de licença, canais habilitados e permissões de usuário. Use este guia para entender quais recursos normalmente estão disponíveis em seu pacote e navegue diretamente para a documentação do produto de cada recurso.

A disponibilidade também pode depender da configuração do canal, dos pré-requisitos de implementação e dos complementos adquiridos. Selecione a guia que corresponde ao modelo de licença.

>[!BEGINTABS]

>[!TAB Jornadas e campanhas]

Essa guia se aplica aos clientes licenciados sob o atual modelo de empacotamento modular [!DNL Adobe Journey Optimizer] (Journey Optimizer - Campanhas, Journey Optimizer - Jornada ou Journey Optimizer - Campanhas e Jornadas).

## Pacotes básicos {#current-packages}

| Pacote | O que inclui |
|---------|----------------|
| **Journey Optimizer - Campanhas** | Orquestração de campanha: fluxos de trabalho de público-alvo de uma ou várias etapas para envolvimento em lote. Mensagens transacionais por email, push e SMS incluídas. |
| **Journey Optimizer - Jornada** | Real-time Journey Orchestration: jornadas acionadas por eventos que oferecem suporte ao processamento em lote e por transmissão. Mensagens transacionais por email, push e SMS incluídas. |
| **Journey Optimizer - Campanhas e Jornadas** | Orquestração de campanhas e Journey Orchestration em tempo real combinados. Mensagens transacionais por email, push e SMS incluídas. |

>[!NOTE]
>
>O direito total ao Volume de Dados difere por pacote: **Campanhas** clientes têm direito a 15 KB por perfil endereçável; clientes do **Jornada** e do **Campanhas e Jornada** têm direito a 75 KB por perfil endereçável.

Os complementos a seguir estendem a cobertura de canal para além de qualquer pacote básico. O complemento **Todos os Canais** agrupa Entrega de Saída, Dispositivo Móvel e Web.

| Complemento | Canais desbloqueados |
|--------|----------------|
| **Entrega de saída** | Email, notificações por push, correspondência direta. Inclui Fundamentos Da Capacidade De Entrega. |
| **Móvel** | Mensagens no aplicativo, notificações por push, cartões de conteúdo e canais baseados em código para superfícies móveis |
| **Web** | Canal da Web e canais baseados em código para superfícies da Web |
| **Todos os canais** | Pacotes de entrega de saída + Mobile + Web |
| **Decisão** | Decisão de oferta em tempo real e otimização baseada em IA |

## Matriz de recursos {#capability-matrix-current}

| Recurso | O que você pode fazer | Journey Optimizer - Campanhas | JOURNEY OPTIMIZER - JORNADA | Journey Optimizer - Campanhas e Jornadas | Complemento necessário | Saiba mais |
|-----------|----------------|:-----------------------------:|:----------------------------:|:----------------------------------------:|:---------------:|-----------|
| **Mensagens transacionais** | Enviar mensagens acionadas em tempo real por email, push ou SMS | ✓ | ✓ | ✓ | — | [Saiba mais sobre mensagens transacionais](../building-journeys/journey-gs.md) |
| **Email** | Projetar e enviar mensagens de email personalizadas | ✓ | ✓ | ✓ | Entrega de saída | [Saiba como enviar emails](../email/get-started-email.md) |
| **Notificações por push** | Enviar alertas por push em dispositivos móveis | ✓ | ✓ | ✓ | Entrega de saída | [Saiba como enviar notificações por push](../push/get-started-push.md) |
| **Correspondência direta** | Criar e enviar partes do email físico | ✓ | ✓ | ✓ | Entrega de saída | [Saiba como usar a correspondência direta](../direct-mail/get-started-direct-mail.md) |
| **SMS/MMS** | Enviar mensagens de texto e multimídia | ✓ | ✓ | ✓ | Entrega de saída | [Saiba como enviar mensagens móveis](../mobile/get-started-mobile.md) |
| **Mensagens no aplicativo** | Exibir mensagens dentro do aplicativo móvel | ✓ | ✓ | ✓ | Dispositivo móvel | [Saiba como usar mensagens no aplicativo](../in-app/get-started-in-app.md) |
| **Cartões de conteúdo** | Fornecer mensagens no produto persistentes e não intrusivas | ✓ | ✓ | ✓ | Dispositivo móvel | [Saiba como usar cartões de conteúdo](../content-card/get-started-content-card.md) |
| **Canal da Web** | Personalizar páginas da Web em tempo real | ✓ | ✓ | ✓ | Web | [Saiba como usar o canal da Web](../web/get-started-web.md) |
| **Experiências baseadas em código** | Personalizar qualquer superfície por meio da API ou do SDK | ✓ | ✓ | ✓ | Móvel ou na Web | [Saiba como usar experiências baseadas em código](../code-based/get-started-code-based.md) |
| **WhatsApp** | Enviar mensagens via WhatsApp Business | ✓ | ✓ | ✓ | WhatsApp | [Saiba como usar o WhatsApp](../whatsapp/get-started-whatsapp.md) |
| **Campanhas orquestradas** | Crie fluxos de trabalho de público-alvo de várias etapas para envolvimento em lote. Canais compatíveis: somente email, SMS, push e correspondência direta. | ✓ | — | ✓ | — | [Saiba como usar campanhas orquestradas](../orchestrated/gs-orchestrated-campaigns.md) |
| **jornadas automatizadas** | Criar jornadas do cliente em tempo real acionadas por eventos | — | ✓ | ✓ | — | [Saiba como criar jornadas](../building-journeys/journey-gs.md) |
| **Acionadores em tempo real** | Reagir aos eventos do cliente conforme eles ocorrem | — | ✓ | ✓ | — | [Saiba mais sobre eventos de jornada](../event/about-events.md) |
| **Decisão** | Selecione a melhor oferta para cada cliente em tempo real | Depende da sua licença | Depende da sua licença | Depende da sua licença | Tomada de decisão | [Saiba como usar a decisão](../experience-decisioning/gs-experience-decisioning.md) |
| **Classificação baseada em IA** | Otimizar a seleção de ofertas usando o aprendizado de máquina | Depende da sua licença | Depende da sua licença | Depende da sua licença | Tomada de decisão | [Saiba mais sobre modelos de IA](../offers/ranking/ai-models.md) |

>[!TAB Selecionar / Prime / Ultimate]

Essa guia se aplica aos clientes com contratos de licença existentes que usam a terminologia de empacotamento Select, Prime ou Ultimate.

## Resumos de pacote {#package-summaries}

+++**Selecionar**

Mais adequado para organizações que estão começando a usar mensagens transacionais e em lote:

- Campanhas em lote e mensagens transacionais programadas
- Campanha principal e execução de jornada
- Fundamentos do canal de ação personalizada, email, SMS e push
- Medidas de proteção de orquestração padrão

+++

+++**Prime**

Inclui tudo no Select, além de orquestração em tempo real e canais de entrada:

- Orquestração de jornadas acionada por eventos em tempo real
- Canais de entrada: Web, mensagens no aplicativo, experiências baseadas em código, cartões de conteúdo e correspondência direta
- Segmentação e direcionamento avançados de público

+++

+++**Ultimate**

Inclui tudo no Prime, além de decisões e otimização avançada:

- Decisão e personalização de ofertas em tempo real
- Modelos de classificação e otimização alimentados por IA
- Recursos avançados de relatórios e experimentação

+++

## Matriz de recursos {#capability-matrix-legacy}

| Recurso | O que você pode fazer | Selecionar | Prime | Ultimate | Saiba mais |
|-----------|----------------|:------:|:-----:|:--------:|-----------|
| **Email** | Projetar e enviar mensagens de email personalizadas | Incluído | Incluído | Incluído | [Saiba como enviar emails](../email/get-started-email.md) |
| **SMS/MMS** | Enviar mensagens de texto e multimídia | Incluído | Incluído | Incluído | [Saiba como enviar mensagens móveis](../mobile/get-started-mobile.md) |
| **Notificações por push** | Enviar alertas por push em dispositivos móveis | Incluído | Incluído | Incluído | [Saiba como enviar notificações por push](../push/get-started-push.md) |
| **Campanhas em lote** | Agendar mensagens para um público | Incluído | Incluído | Incluído | [Saiba como criar campanhas](../campaigns/get-started-with-campaigns.md) |
| **jornadas automatizadas** | Criar jornadas do cliente acionadas por eventos | Incluído | Incluído | Incluído | [Saiba como criar jornadas](../building-journeys/journey-gs.md) |
| **Acionadores de jornada em tempo real** | Reaja ao comportamento do cliente conforme ele ocorre | — | Incluído | Incluído | [Saiba mais sobre eventos de jornada](../event/about-events.md) |
| **Mensagens no aplicativo** | Exibir mensagens dentro do aplicativo móvel | — | Incluído | Incluído | [Saiba como usar mensagens no aplicativo](../in-app/get-started-in-app.md) |
| **Canal da Web** | Personalizar páginas da Web em tempo real | — | Incluído | Incluído | [Saiba como usar o canal da Web](../web/get-started-web.md) |
| **Experiências baseadas em código** | Personalizar qualquer superfície por meio da API ou do SDK | — | Incluído | Incluído | [Saiba como usar experiências baseadas em código](../code-based/get-started-code-based.md) |
| **Cartões de conteúdo** | Fornecer mensagens no produto persistentes e não intrusivas | — | Incluído | Incluído | [Saiba como usar cartões de conteúdo](../content-card/get-started-content-card.md) |
| **Correspondência direta** | Criar e enviar partes do email físico | — | Disponível com o Prime e superior | Incluído | [Saiba como usar a correspondência direta](../direct-mail/get-started-direct-mail.md) |
| **Decisão** | Selecione a melhor oferta para cada cliente em tempo real | — | — | Incluído | [Saiba como usar a decisão](../experience-decisioning/gs-experience-decisioning.md) |
| **Classificação baseada em IA** | Otimizar a seleção de oferta e conteúdo usando o aprendizado de máquina | — | — | Incluído | [Saiba mais sobre modelos de IA](../offers/ranking/ai-models.md) |
| **WhatsApp** | Enviar mensagens via WhatsApp Business | Depende da sua licença e da configuração do canal | Depende da sua licença e da configuração do canal | Depende da sua licença e da configuração do canal | [Saiba como usar o WhatsApp](../whatsapp/get-started-whatsapp.md) |

>[!ENDTABS]
