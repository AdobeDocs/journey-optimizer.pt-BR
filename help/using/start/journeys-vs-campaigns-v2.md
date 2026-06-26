---
solution: Journey Optimizer
product: journey optimizer
title: Jornadas versus campanhas - escolha a abordagem correta
description: Compare Jornadas, campanhas de ação e campanhas acionadas por API para escolher a abordagem certa para suas necessidades de marketing no Adobe Journey Optimizer.
feature: Journeys, Campaigns, Get Started, Overview
topic: Content Management
role: User
level: Beginner
hide: true
keywords: jornada, campanha, comparação, escolher, decisão, fluxo de trabalho, tempo real, lote, orquestração, várias etapas, agendado, acionado por API, orientado por evento
source-git-commit: ab31811861ccaab22fc787ce3c687204637fbd46
workflow-type: tm+mt
source-wordcount: '1965'
ht-degree: 2%

---


# Jornadas versus campanhas: escolha a abordagem certa {#journeys-vs-campaigns}

>[!BEGINSHADEBOX]

**Nesta página:** compare as jornadas com campanhas acionadas por ação e API para poder escolher a abordagem certa para cada caso de uso de marketing no Adobe Journey Optimizer. Para campanhas orquestradas, consulte [Introdução às campanhas orquestradas](../orchestrated/gs-orchestrated-campaigns.md).

>[!ENDSHADEBOX]

O [!DNL Adobe Journey Optimizer] oferece duas formas principais de alcançar e envolver seus clientes: **Jornadas** e **Campanhas**. As jornadas foram projetadas para a orquestração em tempo real e em várias etapas, orientada pelo comportamento do cliente, enquanto as campanhas são mais adequadas para transmissões únicas ou programadas para um público definido — ou para ativações de canais de entrada na borda para personalização de baixa latência.

>[!NOTE]
>
>**Campanhas orquestradas** têm características de arquitetura distintas (execução em lote no hub, dados relacionais de várias entidades) que exigem orientação dedicada. Não são incluídos na comparação abaixo para evitar uma simplificação excessiva. [Saiba mais sobre Campanhas orquestradas](../orchestrated/gs-orchestrated-campaigns.md)

## Qual abordagem você deve usar? {#decision-guide}

A resposta geralmente se resume a uma pergunta: *o que precisa acontecer e para quem?*

Se você precisar que **cada cliente se mova no seu próprio ritmo** — recebendo mensagens com base no que ele faz, aguardando e reagindo à próxima ação — use uma **Jornada**. As jornadas acompanham onde cada perfil está e o que fizeram, tornando-as ideais para experiências de várias etapas, como sequências de integração, fluxos de abandono de carrinho ou programas de fidelidade.

Se você deseja **enviar uma mensagem a um grupo de pessoas de acordo com um agendamento** — um informativo, um anúncio de produto, uma promoção sazonal — use uma **Campanha de ação**. Todos no público-alvo recebem a mensagem ao mesmo tempo, sem necessidade de lógica por perfil. As campanhas de ação também oferecem suporte a ativações de canais de entrada (no aplicativo, na Web, em cartões de conteúdo e com base em código) para personalização de borda de baixa latência.

Se um **sistema externo precisar acionar uma mensagem imediatamente** — uma confirmação de pedido da sua plataforma de comércio eletrônico, um alerta de envio do seu sistema logístico, uma redefinição de senha do seu aplicativo — use uma **campanha acionada por API** para uma única mensagem sob demanda ou uma **jornada de eventos unitária** se esse acionador precisar iniciar um fluxo de várias etapas.

Se você precisar de um **fluxo de trabalho em lote complexo com segmentação avançada, dados de várias entidades ou contagens exatas de pré-envio**, consulte [Introdução às campanhas orquestradas](../orchestrated/gs-orchestrated-campaigns.md).

>[!TIP]
>
>**Não tem certeza de onde começar?** A maioria das equipes usa Jornadas para experiências comportamentais orientadas por eventos e campanhas de ação para comunicações programadas. Esses dois abrangem a maioria dos casos de uso.

## Como eles se comparam {#quick-overview}

| Abordagem | Melhor para | Estilo de execução |
|----------|----------|-----------------|
| **Jornadas** | Experiências do cliente em tempo real em várias etapas com lógica condicional | 1:1 orquestração — cada perfil em seu próprio ritmo |
| **Campanhas de ação** | Ativações agendadas ou recorrentes para públicos | Execução em lote — público-alvo processado junto no momento do envio |
| **Campanhas acionadas por API** | Mensagens transacionais ou orientadas por eventos de sistemas externos | Execução sob demanda — acionada pela chamada da API com carga |

## Como cada abordagem funciona {#key-distinctions}

### Jornada: 1:1 orquestração em tempo real

Uma Jornada é uma tela na qual cada perfil percorre seu próprio caminho em seu próprio ritmo. O AJO rastreia onde cada pessoa está no fluxo e reage em tempo real ao seu comportamento, seja uma ação que realiza, um período de inatividade ou uma mudança em seu perfil.

Os principais recursos incluem atividades de espera que criam um tempo personalizado entre as etapas, ramificação condicional que roteia perfis para caminhos diferentes, limite de frequência para controlar a frequência com que um cliente recebe mensagens e modo de teste para validar a lógica antes de entrar em funcionamento. As jornadas também podem dividir perfis em grupos baseados em porcentagem para experimentos A/B entre caminhos.

Uma jornada de abandono de carrinho ilustra a diferença claramente:

```
Customer A: Abandoned cart → Wait 2 hours → No purchase? → Send reminder → Purchased? → End
Customer B: Abandoned cart → Wait 2 hours → Already purchased → End immediately
```

Cada cliente tem uma linha do tempo diferente com base no que realmente faz. [Saiba mais sobre o Jornada](../building-journeys/journey.md)

### Campanhas: entrega em lote ou acionada

Uma campanha executa uma única ação — para todos em um público-alvo de uma só vez ou sob demanda quando chamada por um sistema externo. Não há tela e nenhum estado por perfil: todos os perfis são processados de forma idêntica.

**As campanhas de ação** são entregues a um público agendado (único ou recorrente) e também oferecem suporte à entrega de entrada em várias superfícies — até 10 ações de canal de entrada por campanha, com regras de direcionamento para criar variantes de mensagens com base na associação de público-alvo ou atributos de perfil.

**Campanhas acionadas por API** são acionadas imediatamente quando um sistema externo chama a API, com a personalização de mensagens orientada pelos dados de carga enviados nessa chamada.

```
Monday 9 AM → Send newsletter to 100,000 subscribers → All receive simultaneously
```

[Saiba mais sobre Campanhas](../campaigns/get-started-with-campaigns.md)

## Exemplos de caso de uso {#use-cases}

| Caso de uso | Método recomendado | Por que |
|----------|---------------------|-----|
| Dê as boas-vindas a novos clientes com integração em várias etapas | Jornadas | Entrada em tempo real, vários pontos de contato, caminhos condicionais |
| Abandono do carrinho com sequência de lembretes | Jornadas | Acionador em tempo real, tempos de espera e acompanhamento condicional |
| Reengajamento de usuários inativos com base no comportamento | Jornadas | Acionado pela qualificação de público-alvo, caminho personalizado |
| Venda rápida acionada por um evento comercial | Jornadas (Evento Comercial) | Acionador em tempo real que afeta vários clientes |
| Informativo mensal para assinantes | Campanhas de ação | Mensagem agendada para o público-alvo |
| Anúncio promocional para todos os clientes | Campanhas de ação | Mensagem única, entrega imediata |
| Confirmação de pedido ou alerta de remessa | Campanhas acionadas por API | Acionador do sistema externo, entrega imediata |
| Fluxo de várias etapas acionado por API | Jornadas (evento unitário) | O sistema externo envia evento por meio da API; o jornada coordena as etapas de acompanhamento |
| Fluxo de trabalho de lote complexo com dados de várias entidades | Campanhas orquestradas | Consulte [Introdução às campanhas orquestradas](../orchestrated/gs-orchestrated-campaigns.md) |

## Disponibilidade de recursos {#feature-availability}

### Canais

Todas as três abordagens oferecem suporte ao conjunto completo de canais de saída do AJO: email, push, SMS, LINE e WhatsApp. A tabela abaixo mostra as diferenças para canais de entrada e digitais.

| Canal | Jornadas | Campanhas de ação | Campanhas acionadas por API |
|---------|:--------:|:----------------:|:-----------------------:|
| No aplicativo | ✅ | ✅ | ✅ |
| Web | ✅ | ✅ | ❌ |
| Baseado em código | ✅ | ✅ | ❌ |
| Cartões de conteúdo | ✅ | ✅ | ❌ |
| Correspondência direta | ✅ | ✅ | ❌ |

>[!NOTE]
>
>Para obter a disponibilidade do canal de campanhas orquestradas, consulte [Canais em jornadas e campanhas](../channels/gs-channels.md#channels).

### Recursos avançados

| Recurso | Jornadas | Campanhas de ação | Campanhas acionadas por API |
|-----------|:--------:|:----------------:|:-----------------------:|
| Fluxos de trabalho de várias etapas | ✅ | ❌ | ❌ |
| Acionadores em tempo real | ✅ | ❌ | ✅ |
| Atividades de espera | ✅ | ❌ | ❌ |
| Ramificação condicional | ✅ | ❌ | ❌ |
| Execução programada | ✅ | ✅ | ✅ |
| Acionamento da API | ✅ (somente evento unitário) | ❌ | ✅ |
| Otimização de hora de envio | ✅ | ❌ | ❌ |
| Teste AB | ✅ | ✅ | ❌ |
| Fluxos de trabalho de aprovação | ✅ | ✅ | ✅ |
| Dados de várias entidades | ❌ | ❌ | ❌ |
| Contagens exatas de pré-envio | ❌ | ❌ | ❌ |

>[!NOTE]
>
>Para obter detalhes sobre recursos de campanhas orquestradas, incluindo experimentos de conteúdo, acionamento de API em lote e segmentação de várias entidades, consulte [Introdução a campanhas orquestradas](../orchestrated/gs-orchestrated-campaigns.md).

## Perguntas comuns {#common-questions}

+++ É possível combinar jornadas e campanhas em minha estratégia de marketing?

Sim. Muitas organizações usam todas as abordagens para diferentes cenários:

* **Jornadas** para envolvimento comportamental e em tempo real
* **Campanhas de ação** para comunicações agendadas ou ativações de entrada
* **Campanhas acionadas por API** para mensagens transacionais
* **Campanhas orquestradas** para campanhas em lote complexas e com muitos dados — consulte [Introdução a campanhas orquestradas](../orchestrated/gs-orchestrated-campaigns.md)

Use a ferramenta certa para cada caso de uso, em vez de forçar uma abordagem para tudo.

+++

+++ Posso converter uma campanha em uma jornada ou vice-versa?

Não, você deve recriar a experiência no formato apropriado. No entanto, você pode reutilizar conteúdo, públicos e conceitos lógicos.

+++

+++ Qual abordagem é mais fácil de criar?

As campanhas de ação normalmente são as mais simples (um único ponto de contato fornecido para um público-alvo), seguidas por campanhas acionadas por API e, em seguida, Jornadas, que exigem mais trabalho de design devido à lógica de várias etapas.

+++

+++ Qual dimensionamento é melhor para públicos-alvo grandes?

Todos os três podem ser bem dimensionados; a escolha certa depende do seu padrão:

* As **Jornadas de Leitura de Público** e as **Campanhas de ação** estão otimizadas para públicos de lote grandes.
* **O Jornada** unitário (baseado em eventos) processa perfis individualmente à medida que os eventos ocorrem, portanto, a escala depende do volume e da taxa de transferência do evento.

Para segmentação complexa com grandes conjuntos de dados e dados de várias entidades, consulte [Campanhas orquestradas](../orchestrated/gs-orchestrated-campaigns.md).

+++

+++ Posso usar o mesmo público-alvo em jornadas e campanhas?

Sim. Os públicos-alvo criados em [!DNL Adobe Experience Platform] podem ser usados em Jornadas, campanhas de Ação e campanhas Orquestradas. As campanhas acionadas por API são orientadas por carga útil e não usam públicos pré-criados da mesma maneira.

+++

## Próximas etapas {#next-steps}

Pronto(a) para começar a criar? Explore a documentação detalhada da abordagem escolhida:

* **[Introdução ao Jornada](../building-journeys/journey.md)** - Tipos de Jornada, designer e fluxo de trabalho
* **[Introdução às Campanhas](../campaigns/get-started-with-campaigns.md)** - Campanhas acionadas por ação e API
* **[Introdução a campanhas orquestradas](../orchestrated/gs-orchestrated-campaigns.md)** - Fluxos de trabalho de tela de lote com dados de várias entidades (orientação separada)

>[!MORELIKETHIS]
>
>* [comparação de tipos de Jornada](../building-journeys/journey.md#journey-types-comparison)
>* [Comparação de tipos de campanha](../campaigns/get-started-with-campaigns.md#campaign-types)
>* [Perguntas frequentes sobre o Jornada](../building-journeys/journey-faq.md)
>* [Perguntas frequentes sobre campanhas orquestradas](../orchestrated/orchestrated-campaigns-faq.md)

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** Escolha entre Jornadas, campanhas de Ação e campanhas acionadas por API com base na necessidade ou não de orquestração em tempo real 1:1, entrega em lote agendada ou de entrada ou execução acionada por API sob demanda.

**Intenções:**
* Entenda as principais diferenças entre Jornadas, campanhas de ação e campanhas acionadas por API
* Selecione a abordagem certa para um determinado caso de uso de marketing usando o guia de decisão e as tabelas de comparação
* Entenda quando as campanhas de Ação oferecem suporte a ativações de canal de entrada em relação a difusões de saída
* Saber quando escalar para campanhas orquestradas (composição ad-hoc, dados federados, várias entidades)
* Combinar várias abordagens de maneira eficaz em uma estratégia de marketing

**Glossário:**
* **Jornada**: um fluxo de orquestração em várias etapas e em tempo real no qual cada perfil avança no seu próprio ritmo com base no comportamento e nos eventos. *(específico do produto)*
* **Campanha de ação**: uma campanha que fornece ativações agendadas ou recorrentes para públicos-alvo — ativações de canal de entrada ou transmissão de saída para a borda para personalização de baixa latência. *(específico do produto)*
* **Campanha acionada por API**: uma campanha iniciada por um sistema externo por meio de uma chamada de API, fornecendo uma única mensagem sob demanda com personalização orientada por carga. *(específico do produto)*
* **Campanha orquestrada**: uma campanha em lote do lado do hub que oferece suporte a dados relacionais de várias entidades, composição de público ad hoc e fontes de dados federadas; não coberta pelas tabelas de comparação desta página. *(específico do produto)*
* **jornada de evento unitária**: uma jornada acionada por uma única ação de perfil em tempo real; use quando for necessária a orquestração de várias etapas após um evento enviado por API. *(específico do produto)*
* **Ativação de canal de entrada**: fornecendo experiências personalizadas para a borda (experiência baseada em código, no aplicativo, Cartão de Conteúdo, Web) para renderização de baixa latência, com suporte em campanhas de Ação. *(específico do produto)*

**Medidas de Proteção:**
* Até 10 ações de canal de entrada por campanha de Ação (limite rígido) — aplica-se somente a canais de entrada: experiência baseada em código, no aplicativo, Cartão de conteúdo, Web
* As campanhas orquestradas são excluídas das tabelas de comparação nesta página para evitar simplificação excessiva; consulte a documentação dedicada das campanhas orquestradas para obter detalhes de arquitetura

**Terminologia:**
* Nome canônico: Campanhas de ação — variantes: &quot;campanhas programadas&quot;, &quot;campanhas de transmissão&quot;
* Nome canônico: campanhas acionadas por API — variantes: &quot;campanhas transacionais&quot;, &quot;campanhas orientadas por evento&quot;
* Não confunda: &quot;Campanhas de ação&quot; (entrega agendada/entrada para públicos-alvo) ≠ &quot;Campanhas acionadas por API&quot; (sob demanda, orientadas por carga, sem público-alvo pré-construído) ≠ &quot;Campanhas orquestradas&quot; (lote do lado do hub com dados relacionais)
* Não confunda: &quot;jornada de evento unitária&quot; (acionada pela ação em tempo real de um perfil) ≠ &quot;jornada de evento comercial&quot; (acionada por um evento que não é de perfil e que afeta várias pessoas por meio de uma etapa interna Ler público)
* Sinônimos: &quot;ativação do canal de entrada&quot; = &quot;ação do canal de entrada&quot; (usado alternadamente nesta página para experiências entregues pela borda em campanhas de ação)

**Perguntas frequentes:**
* **P: Quando devo usar uma Jornada em vez de uma Campanha de ação?** — use Jornadas quando os clientes precisarem se mover em seu próprio ritmo com lógica condicional em tempo real em vários pontos de contato; use campanhas de ação para entrega agendada ou de entrada para um público-alvo predefinido.
* **P: As campanhas de Ação podem ser entregues aos canais de entrada?** — Sim. As campanhas de ação oferecem suporte à ativação do canal de entrada (experiência baseada em código, no aplicativo, cartão de conteúdo, Web) na borda para personalização de baixa latência, com até 10 ações de entrada por campanha e regras de direcionamento para variantes de mensagens.
* **P: O que distingue as campanhas Orquestradas das Campanhas de Ação?** — campanhas orquestradas executam execução em lote no hub com dados relacionais de várias entidades, contagens exatas de pré-envio, composição de público-alvo ad-hoc e suporte a dados federados; as campanhas de ação são deliveries de execução única sem estado para públicos da Experience Platform.
* **P: Quando devo usar uma campanha acionada por API vs. uma jornada de eventos Unitária?** — use uma campanha acionada por API quando um sistema externo precisar acionar uma única mensagem imediatamente com dados de payload; use uma jornada de evento unitária quando a orquestração em várias etapas for necessária após o evento enviado pela API.
* **P: Posso combinar Jornadas e campanhas na mesma estratégia de marketing?** — Sim. Use Jornadas para envolvimento comportamental em tempo real, campanhas de ação para transmissões agendadas ou ativações de entrada, campanhas acionadas por API para mensagens transacionais e campanhas orquestradas para fluxos de trabalho em lote complexos.

+++
<!-- ai-accordion-version: 1 | source-hash: 873097f5 -->
