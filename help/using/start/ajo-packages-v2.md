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
source-git-commit: d0e43b37ab759fde2794e2bf981e233875ba620a
workflow-type: tm+mt
source-wordcount: '937'
ht-degree: 2%

---


# Pacotes e recursos do Adobe Journey Optimizer {#ajo-packages-v2}

[!DNL Adobe Journey Optimizer] usa um modelo de empacotamento modular. Comece com a oferta base que corresponde ao caso de uso principal e, em seguida, adicione os canais e recursos avançados necessários.

>[!NOTE]
>
>A disponibilidade do pacote e os recursos incluídos podem variar de acordo com o contrato, os complementos selecionados e a disponibilidade regional. Entre em contato com seu representante da Adobe para obter detalhes específicos sobre sua organização.

## Etapa 1 — escolha a oferta base {#base-offers}

Há três ofertas básicas disponíveis. Escolha aquele que corresponde a como você envolve principalmente os clientes.

| Oferta base | Melhor para | Comportamento principal |
|-----------|---------|--------------|
| **Journey Optimizer - Campanhas** | Lote, alcance planejado pelo profissional de marketing | Orquestração agendada com base no público-alvo. Fluxos de trabalho de campanha de etapa única ou múltipla usando o Armazenamento de dados relacional. |
| **Journey Optimizer - Jornada** | Engajamento do cliente em tempo real | Orquestração de 1:1 orientada por evento. Oferece suporte ao processamento de jornada em lote e por transmissão. |
| **Journey Optimizer - Campanhas e Jornadas** | Clientes que precisam de ambos | Combina a orquestração de campanhas com base no público e a orquestração de jornadas em tempo real. |

### Campanhas versus Jornadas — qual é a diferença? {#campaigns-vs-journeys}

| | Journey Optimizer - Campanhas | JOURNEY OPTIMIZER - JORNADA | Journey Optimizer - Campanhas e Jornadas |
|--|:-----------------------------:|:----------------------------:|:----------------------------------------:|
| Orquestração em lote baseada no público-alvo | ✓ | Limitado a casos de uso do jornada | ✓ |
| Orquestração orientada por eventos em tempo real | — | ✓ | ✓ |
| Mensagens transacionais (email, push, SMS) | ✓ | ✓ | ✓ |
| Complementos de canal disponíveis | ✓ | ✓ | ✓ |
| Complemento de decisão disponível | ✓ | ✓ | ✓ |

>[!NOTE]
>
>O direito total do Volume de Dados é diferente: **Campanhas** clientes recebem 15 KB por perfil endereçável; **Jornadas** e **Campanhas e Jornadas** clientes recebem 75 KB por perfil endereçável.

## Etapa 2 — Adicionar os canais necessários {#channel-addons}

Os canais não são agrupados na oferta base. Selecione o complemento de canal ou o pacote complementar que se adapta à sua estratégia de engajamento.

>[!BEGINTABS]

>[!TAB Entrega de saída]

Alcance públicos por meio de canais de mensagens de saída.

**Inclui:** email, notificações por push, correspondência direta

**Casos de uso típicos:** emails promocionais, alertas transacionais por push, campanhas por email físico

**Superfícies com suporte:** caixa de entrada, tela de bloqueio de dispositivo móvel/bandeja de notificação, endereço postal

Inclui fundamentos de capacidade de entrega para suporte ao aquecimento de IP em novas instâncias. [Saiba mais sobre a capacidade de entrega](../reports/deliverability.md)

>[!TAB Móvel]

Envolva os usuários do aplicativo com experiências móveis persistentes e na sessão.

**Inclui:** mensagens no aplicativo, notificações por push, cartões de conteúdo, canais baseados em código para superfícies móveis

**Casos de uso típicos:** fluxos de integração, anúncios de recursos, chamadas de atenção para fidelidade, ofertas no aplicativo em tempo real

**Superfícies com suporte:** telas de aplicativos móveis, bandeja de notificação, slots de conteúdo persistentes, superfícies de aplicativos personalizadas via SDK

>[!TAB Web]

Personalizar experiências da Web sem implantar código.

**Inclui:** canal da Web (editor visual e não visual), canais baseados em código para superfícies da Web

**Casos de uso típicos:** banners de página inicial, personalização de página de aterrissagem, testes A/B, personalização da Web headless via API

**Superfícies com suporte:** páginas do navegador, aplicativos de página única (SPA), pontos de extremidade da Web headless

>[!TAB Todos os canais]

O complemento **Todos os Canais** agrupa Entrega de saída + Dispositivo móvel + Web em uma única compra.

Mais adequado para organizações que precisam de cobertura omnicanal completa em superfícies de saída, de aplicativos móveis e da Web.

>[!ENDTABS]

O **WhatsApp** está disponível como um complemento separado para clientes que precisam enviar mensagens por meio do WhatsApp Business. [Saiba como usar o WhatsApp](../whatsapp/get-started-whatsapp.md)

## Etapa 3 — Adicionar recursos avançados {#advanced-addons}

### Tomada de decisão {#decisioning-addon}

O complemento **Decisioning** permite definir, gerenciar e fornecer a melhor oferta, ação ou experiência para cada perfil em tempo real, em qualquer canal.

**O que ele desbloqueia:**
- Seleção de oferta em tempo real usando regras de qualificação, lógica de classificação e restrições
- Modelos de classificação alimentados por IA para otimizar o desempenho da oferta automaticamente
- Políticas de decisão que podem ser usadas em jornadas, campanhas e experiências baseadas em código

**Disponível em:** todas as três ofertas básicas, sujeitas ao seu contrato de licença. [Saiba como usar a decisão](../experience-decisioning/gs-experience-decisioning.md) | [Saiba mais sobre modelos de IA](../offers/ranking/ai-models.md)

## Principais características da comparação {#comparison-matrix}

| Recurso | Journey Optimizer - Campanhas | JOURNEY OPTIMIZER - JORNADA | Journey Optimizer - Campanhas e Jornadas | Complemento necessário |
|-----------|:-----------------------------:|:----------------------------:|:----------------------------------------:|:---------------:|
| Mensagens transacionais (email, push, SMS) | ✓ | ✓ | ✓ | — |
| Campanhas em lote | ✓ | — | ✓ | — |
| Campanhas orquestradas _(somente email, SMS, push, correspondência direta)_ | ✓ | — | ✓ | — |
| Jornadas automatizadas | — | ✓ | ✓ | — |
| Acionadores de eventos em tempo real | — | ✓ | ✓ | — |
| Email | ✓ | ✓ | ✓ | Entrega de saída |
| Notificações por push | ✓ | ✓ | ✓ | Entrega de saída |
| Correspondência direta | ✓ | ✓ | ✓ | Entrega de saída |
| SMS/MMS | ✓ | ✓ | ✓ | Entrega de saída |
| Mensagens no aplicativo | ✓ | ✓ | ✓ | Dispositivo móvel |
| Cartões de conteúdo | ✓ | ✓ | ✓ | Dispositivo móvel |
| Canal da web | ✓ | ✓ | ✓ | Web |
| Experiências baseadas em código | ✓ | ✓ | ✓ | Móvel ou na Web |
| WhatsApp | ✓ | ✓ | ✓ | WhatsApp |
| Tomada de decisão | Depende da licença | Depende da licença | Depende da licença | Tomada de decisão |
| Classificação baseada em IA | Depende da licença | Depende da licença | Depende da licença | Tomada de decisão |

## Perguntas frequentes {#faq}

+++**Todas as ofertas básicas incluem todos os canais?**

Não. O [!DNL Adobe Journey Optimizer] usa um modelo modular: a oferta base determina a capacidade de orquestração (Campanhas, Jornadas ou ambas) e os complementos de canal determinam quais superfícies de mensagens você pode utilizar. Você escolhe a combinação que se adapta ao seu caso de uso e orçamento.

+++

+++**Qual é a diferença entre Campanhas e Jornadas?**

**As campanhas** são baseadas no público-alvo e planejadas pelo profissional de marketing — você define um público-alvo, cria uma mensagem e a agenda ou aciona como um envio em lote. Eles são melhores para alcance promocional, boletins informativos e fluxos de trabalho de público-alvo de várias etapas.

As **Jornadas** são orientadas por eventos e em tempo real. Elas reagem ao comportamento individual do cliente à medida que ele ocorre e organizam 1:1 experiências nos pontos de contato. Eles são melhores para fluxos de integração, sequências pós-compra e mensagens acionadas em tempo real.

O **Campaigns &amp; Jornada** oferece ambos os recursos em uma única licença.

+++

+++**Quais canais são suportados nas campanhas Orquestradas?**

As campanhas orquestradas (fluxos de trabalho de público em várias etapas usando o recurso de Orquestração de Campanhas) oferecem suporte somente a **email, SMS, notificações por push e correspondência direta**. Os canais de cartão de conteúdo, da Web, no aplicativo e com base em código não são compatíveis com fluxos de trabalho de campanha orquestradas.

+++

+++**A Decisão está incluída em todas as configurações?**

Não. A decisão é um complemento de recurso avançado distinto e não está incluído em nenhuma oferta base por padrão. Entre em contato com seu representante da Adobe para adicionar a Decisão à sua configuração.

+++

+++**Já ouvi falar de Select, Prime ou Ultimate. Esses ainda são o modelo de empacotamento atual?**

O [!DNL Adobe Journey Optimizer] agora é oferecido por meio de um modelo de empacotamento modular criado com base em ofertas básicas (Campanhas, Jornadas, Campanhas e Jornadas) e complementos. Se você for um cliente existente usando a terminologia Select, Prime ou Ultimate e tiver dúvidas sobre seus direitos atuais, entre em contato com o representante da Adobe.

+++
