---
solution: Journey Optimizer
product: journey optimizer
title: Pacotes e recursos do Journey Optimizer
description: Entenda como o Adobe Journey Optimizer é fornecido e quais recursos estão disponíveis com base em sua oferta básica, complementos de canal e complementos de recursos avançados.
feature: Get Started
topic: Content Management
role: Admin, User
level: Beginner
keywords: Otimizador de jornadas, pacote, licença, campanhas, jornadas, canais, decisão, saída, móvel, web, modular
hide: true
source-git-commit: a3301bfc25f76ba0f74622fd1f169585c2d96ebd
workflow-type: tm+mt
source-wordcount: '1046'
ht-degree: 4%

---


# Pacotes e recursos do Adobe Journey Optimizer {#ajo-packages}

[!DNL Adobe Journey Optimizer] usa um modelo de empacotamento modular. Comece com a oferta base que corresponde ao caso de uso de orquestração principal e, em seguida, adicione o canal e os recursos avançados necessários.

>[!NOTE]
>
>A disponibilidade dos recursos pode variar com base no contrato de licença, nos complementos selecionados, na disponibilidade regional, na configuração do canal e nos pré-requisitos de implementação. Entre em contato com seu representante da Adobe para obter detalhes específicos sobre sua organização.

## Etapa 1 — escolha a oferta base {#base-offers}

Há três ofertas básicas disponíveis. Escolha a que melhor corresponde a como você envolve principalmente os clientes.

| Oferta base | Melhor para | O que inclui |
|-----------|---------|-----------------|
| **Journey Optimizer - Campanhas** | Lote, alcance planejado pelo profissional de marketing | Orquestração de campanha programada e baseada em público para envolvimento em lote e alcance planejado pelo profissional de marketing. |
| **Journey Optimizer - Jornada** | Engajamento do cliente em tempo real | Orquestração de jornadas orientada por eventos de 1:1 para engajamento do cliente em tempo real. |
| **Journey Optimizer - Campanhas e Jornadas** | Clientes que precisam de ambos | Inclui a orquestração de campanhas com base no público e a orquestração de jornadas em tempo real em uma oferta. |

### Campanhas versus Jornadas — qual é a diferença? {#campaigns-vs-journeys}

| Recurso | Journey Optimizer - Campanhas | JOURNEY OPTIMIZER - JORNADA | Journey Optimizer - Campanhas e Jornadas |
|--|:-----------------------------:|:----------------------------:|:----------------------------------------:|
| Orquestração em lote baseada no público-alvo | ✓ | — | ✓ |
| Orquestração orientada por eventos em tempo real | — | ✓ | ✓ |
| Complementos de canal disponíveis | ✓ | ✓ | ✓ |
| Complemento de decisão disponível | ✓ | ✓ | ✓ |

### Quando devo escolher Campanhas? {#when-to-choose-campaigns}

Escolha **Journey Optimizer - Campanhas** se seus principais casos de uso forem:

- campanhas programadas
- alcance com base no público
- workflows de marketing em lote
- programas de envolvimento planejados pelo profissional de marketing

### Quando devo escolher Jornadas? {#when-to-choose-journeys}

Escolha **Journey Optimizer - Jornada** se os principais casos de uso forem:

- comunicação acionada por evento
- fluxos de acompanhamento pós-evento
- integração e jornadas do ciclo de vida
- envolvimento 1:1 em tempo real

### Quando devo escolher Campanhas e Jornadas? {#when-to-choose-both}

Escolha **Journey Optimizer - Campanhas e Jornadas** se precisar de ambos:

- orquestração em lote com base no público e
- orquestração orientada por eventos em tempo real

## Etapa 2 — Adicionar os canais necessários {#channel-addons}

As ofertas básicas definem seu recurso de orquestração. A disponibilidade do canal depende dos complementos licenciados.

>[!BEGINTABS]

>[!TAB Entrega de saída]

Alcance públicos por meio de canais de mensagens de saída.

**Os recursos típicos incluem:**
- email
- Correspondência direta
- notificações por push

**Casos de uso típicos:**
- campanhas de email promocionais
- mensagens de saída acionadas
- campanhas de correspondência direta

**Superfícies típicas:**
- Caixa de entrada
- superfícies de notificação de dispositivos móveis
- workflows de delivery postal

[Saiba como enviar emails](../email/get-started-email.md) | [Saiba como enviar notificações por push](../push/get-started-push.md) | [Saiba como usar a correspondência direta](../direct-mail/get-started-direct-mail.md) | [Saiba mais sobre a capacidade de entrega](../reports/deliverability.md)

>[!TAB Móvel]

Envolva os usuários do aplicativo com experiências móveis.

**Os recursos típicos incluem:**
- mensagens no aplicativo
- notificações por push
- Cartões de conteúdo
- experiências móveis baseadas em código

**Casos de uso típicos:**
- fluxos de integração
- anúncios de recursos
- chamadas de atenção de fidelidade
- envolvimento contextual no aplicativo

**Superfícies típicas:**
- telas de aplicativos móveis
- superfícies de notificação
- inserções de conteúdo persistentes
- superfícies do aplicativo personalizado via SDK

[Saiba como usar mensagens no aplicativo](../in-app/get-started-in-app.md) | [Saiba como usar cartões de conteúdo](../content-card/get-started-content-card.md) | [Saiba como usar experiências baseadas em código](../code-based/get-started-code-based.md)

>[!TAB Web]

Personalize experiências da Web em superfícies baseadas em navegador.

**Os recursos típicos incluem:**
- experiências de canal da web
- personalização visual e não visual da web
- experiências da web baseadas em código

**Casos de uso típicos:**
- banners de página inicial
- personalização da landing page
- ofertas contextuais
- experimentação e personalização baseadas em navegador

**Superfícies típicas:**
- páginas do navegador
- aplicativos de página única (SPA)
- superfícies da web personalizadas

[Saiba como usar o canal da Web](../web/get-started-web.md) | [Saiba como usar experiências baseadas em código](../code-based/get-started-code-based.md)

>[!TAB Todos os canais]

O complemento **Todos os Canais** reúne recursos de canal de saída, móvel e Web.

Essa opção é mais adequada para organizações que precisam de ampla cobertura omnicanal em experiências de saída, de aplicativos e da Web.

>[!ENDTABS]

### Disponibilidade de canal adicional {#additional-channels}

Alguns canais e recursos específicos do canal podem ser licenciados separadamente, dependendo da sua configuração e contrato.

Por exemplo:

- O [WhatsApp](../whatsapp/get-started-whatsapp.md) pode estar disponível como um complemento separado
- outros canais podem depender da sua configuração licenciada e da configuração suportada

## Etapa 3 — Adicionar recursos avançados {#advanced-capabilities}

### Tomada de decisão {#decisioning}

O complemento **Decisioning** permite definir, gerenciar e fornecer a melhor oferta, ação ou experiência para cada perfil em tempo real.

**Os recursos típicos incluem:**
- seleção de oferta com base nas regras de elegibilidade e restrições
- lógica de classificação para escolher a oferta mais relevante
- Modelos de classificação alimentados por IA quando licenciados
- decisões em campanhas, jornadas e experiências com código compatíveis

[Saiba como usar a decisão](../experience-decisioning/gs-experience-decisioning.md) | [Saiba mais sobre modelos de IA](../offers/ranking/ai-models.md)

## Comparação rápida de recursos {#compare-capabilities}

### Recursos de orquestração {#orchestration-capabilities}

| Recurso | Journey Optimizer - Campanhas | JOURNEY OPTIMIZER - JORNADA | Journey Optimizer - Campanhas e Jornadas | Saiba mais |
|-----------|:-----------------------------:|:----------------------------:|:----------------------------------------:|-----------|
| Campanhas em lote | Incluído | — | Incluído | [Introdução às campanhas](../campaigns/get-started-with-campaigns.md) |
| Campanhas orquestradas | Incluído | — | Incluído | [Introdução a campanhas orquestradas](../orchestrated/gs-orchestrated-campaigns.md) |
| Jornadas automatizadas | — | Incluído | Incluído | [Introdução ao jornada](../building-journeys/journey-gs.md) |
| Acionadores de eventos em tempo real | — | Incluído | Incluído | [Sobre eventos de jornada](../event/about-events.md) |

### Recursos avançados e de canal {#channel-and-advanced-capabilities}

| Recurso | Disponibilidade | Saiba mais |
|-----------|-------------|-----------|
| Email | Disponível com o complemento de canal licenciado | [Introdução ao email](../email/get-started-email.md) |
| Correspondência direta | Disponível com o complemento de canal licenciado | [Introdução à correspondência direta](../direct-mail/get-started-direct-mail.md) |
| Notificações por push | Disponível com o complemento de canal licenciado | [Introdução às notificações por push](../push/get-started-push.md) |
| SMS/MMS | Disponível com base na sua configuração licenciada | [Introdução a mensagens móveis](../mobile/get-started-mobile.md) |
| Mensagens no aplicativo | Disponível com dispositivos móveis | [Introdução a mensagens no aplicativo](../in-app/get-started-in-app.md) |
| Cartões de conteúdo | Disponível com dispositivos móveis | [Introdução aos cartões de conteúdo](../content-card/get-started-content-card.md) |
| Canal da web | Disponível com a Web | [Introdução ao canal Web](../web/get-started-web.md) |
| Experiências baseadas em código | Disponível com Mobile ou Web, dependendo da superfície | [Introdução a experiências baseadas em código](../code-based/get-started-code-based.md) |
| WhatsApp | Pode estar disponível como um complemento separado | [Começar a usar o WhatsApp](../whatsapp/get-started-whatsapp.md) |
| Tomada de decisão | Disponível com o complemento Decisioning | [Introdução à decisão](../experience-decisioning/gs-experience-decisioning.md) |
| Classificação baseada em IA | Disponível com o complemento Decisioning | [Saiba mais sobre modelos de IA](../offers/ranking/ai-models.md) |

## Perguntas frequentes {#faq}

+++**Todas as ofertas básicas incluem todos os canais?**

Não. As ofertas básicas definem seu recurso de orquestração. O acesso ao canal depende dos complementos e da configuração licenciada da sua organização.

+++

+++**Qual é a diferença entre Campanhas e Jornadas?**

**Campanhas** são baseadas em público e planejadas pelo profissional de marketing. Eles são melhores para alcance agendado, programas promocionais e workflows de campanhas em lote.

As **Jornadas** são orientadas por eventos e em tempo real. Eles são melhores para um compromisso de :1 que reage ao comportamento do cliente quando ele ocorre.

**Campanhas e Jornadas** incluem ambos os modelos de orquestração.

+++

+++**Quais canais são suportados em campanhas orquestradas?**

As campanhas orquestradas oferecem suporte a um subconjunto de canais usados para fluxos de trabalho de orquestração de campanhas. A disponibilidade do canal depende da sua configuração licenciada. [Saiba mais sobre campanhas orquestradas](../orchestrated/gs-orchestrated-campaigns.md)

+++

+++**A Decisão está incluída em todas as configurações?**

Não. A decisão é um complemento de recurso avançado separado. [Saiba como usar a decisão](../experience-decisioning/gs-experience-decisioning.md)

+++

+++**Já ouvi falar de Select, Prime ou Ultimate. Esses ainda são o modelo de empacotamento atual?**

O [!DNL Adobe Journey Optimizer] agora é oferecido por meio de um modelo de empacotamento modular construído com base em ofertas e complementos. Se você for um cliente do que usa a terminologia de pacotes herdados, entre em contato com o representante da Adobe para confirmar seus direitos atuais.

+++
