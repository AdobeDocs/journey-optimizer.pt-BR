---
solution: Journey Optimizer
product: journey optimizer
title: Terminologia principal
description: Termos e conceitos essenciais no Adobe Journey Optimizer
feature: Get Started
role: Admin, Developer, User
level: Beginner
exl-id: 14e72376-87ad-4fae-bf8c-f347109d7903
TQID: https://experienceleague.adobe.com/-aDvt4RUXyf0EnPfFTJkG1CvWgte-1Fr6YaWvgcNNu4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fdac7813-bd56-47ae-9f6d-fa94ad1c5dee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: 0047bf4386b33c99fded37750e24ed9fbf4188f6
workflow-type: tm+mt
source-wordcount: 1569
ht-degree: 7%

---

# Terminologia principal {#key-terminology}

Este guia de referência define os termos essenciais que você encontrará ao usar o Adobe Journey Optimizer. A compreensão desses conceitos ajuda você a navegar na plataforma com confiança e a colaborar efetivamente com a sua equipe.

Para pares de termos com sonoridade semelhante que são frequentemente confundidos — como **Decisão vs. Gerenciamento de Decisão** ou **Cartões de Conteúdo vs. Mensagens no Aplicativo** — consulte [Quando os termos são semelhantes](#disambiguation) na parte inferior desta página.

>[!NOTE]
>
>O Adobe Journey Optimizer foi criado em **Adobe Experience Platform**. Muitos conceitos fundamentais que você encontrará — como perfis de clientes em tempo real, sandboxes, esquemas e conjuntos de dados — são conceitos do Adobe Experience Platform, não específicos do Journey Optimizer. Para obter as definições desses termos, consulte o [glossário do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/glossary.html?lang=pt-BR){target="_blank"}.

## Termos de Jornada e campanha {#journey-campaign-terms}

| Termo | Definição |
|------|------------|
| **Jornada** | Uma série de etapas conectadas que orientam os clientes pelas experiências com sua marca ao longo do tempo. Cada etapa ocorre com base nas ações do cliente ou nos acionadores de tempo, permitindo interações sequenciais e personalizadas. [Saiba mais](../building-journeys/journey.md) |
| **Campaign** | Uma ação de marketing coordenada que entrega conteúdo a um público específico em um ou mais canais. Diferentemente das jornadas, as campanhas executam ações simultaneamente. O Journey Optimizer oferece suporte a três tipos de campanha: **Campanhas de ação** (envios em lote agendados), **campanhas acionadas por API** (mensagens em tempo real orientadas por eventos via API) e **Campanhas orquestradas** (fluxos de trabalho complexos de várias etapas com uma tela visual). [Saiba mais](../campaigns/get-started-with-campaigns.md) |
| **Evento** | Uma ação ou ocorrência que aciona ou avança uma jornada. Os eventos podem ser ações do cliente (fazer uma compra, abandonar um carrinho) ou eventos do sistema (data/hora, alteração de dados). [Saiba mais](../event/about-events.md) |
| **Canal** | O método usado para se comunicar com os clientes: email, SMS, notificações por push, mensagens no aplicativo, Web ou correspondência direta. Cada canal requer uma configuração específica. [Saiba mais](../configuration/get-started-configuration.md) |

## Termos de cliente e público-alvo {#customer-audience-terms}

| Termo | Definição |
|------|------------|
| **Público-alvo** | Um grupo de clientes que compartilham características ou comportamentos comuns, como &quot;clientes que compraram nos últimos 30 dias&quot; ou &quot;membros de programa de fidelidade&quot;. Os públicos-alvo são usados para direcionar segmentos específicos de clientes. [Saiba mais](../audience/about-audiences.md) |
| **Qualificação de público-alvo** | O processo automático que ocorre quando um cliente entra ou sai de um público-alvo. O Journey Optimizer pode acionar ações quando alguém entrar ou sair de um público-alvo, garantindo comunicações oportunas e relevantes. [Saiba mais](../building-journeys/audience-qualification-events.md) |
| **Público-alvo envolvente** | O número de perfis de clientes que você pode contatar ativamente por meio do Adobe Journey Optimizer com base no contrato de licença. Normalmente, refere-se aos perfis envolvidos nos últimos 12 meses. |
| **Perfil de Teste** | Perfis fictícios usados para testar e visualizar mensagens antes de enviá-las para clientes reais. Os perfis de teste ajudam a verificar a personalização, o conteúdo e a lógica da jornada. [Saiba mais](../audience/creating-test-profiles.md) |

## Termos de conteúdo e personalização {#content-terms}

| Termo | Definição |
|------|------------|
| **Personalização** | O processo de personalizar o conteúdo para clientes individuais usando os dados de perfil, as preferências e os comportamentos. Por exemplo, inserir o nome de um cliente ou mostrar recomendações de produto com base no histórico de navegação. [Saiba mais](../personalization/personalize.md) |
| **Modelo de conteúdo** | Um design de mensagem reutilizável que pode ser usado em várias campanhas e jornadas para manter a consistência da marca e acelerar a criação de conteúdo. [Saiba mais](../content-management/content-templates.md) |
| **Fragmento** | Um bloco de conteúdo reutilizável (como cabeçalho, rodapé ou banner promocional) que pode ser usado em várias mensagens para garantir consistência e permitir atualizações centralizadas. [Saiba mais](../content-management/fragments.md) |
| **Página de aterrissagem** | Uma página da Web independente em que os clientes podem aceitar ou recusar comunicações, assinar serviços ou fornecer informações por meio de formulários online. [Saiba mais](../landing-pages/get-started-lp.md) |
| **Experimento de conteúdo** | Uma estrutura de testes A/B que divide um público-alvo em grupos aleatórios e fornece diferentes variantes de mensagem (conteúdo, linha de assunto ou oferta) para cada grupo e, em seguida, identifica a variante com melhor desempenho com base em uma métrica de sucesso definida. [Saiba mais](../content-management/get-started-experiment.md) |
| **Experimentação** | A capacidade mais ampla do Journey Optimizer para testar e otimizar decisões: experimentos de conteúdo testam variantes de mensagens em campanhas e jornadas, enquanto testes de experimentação de decisão oferecem estratégias de seleção. Ambos usam análise estatística para identificar abordagens vencedoras. [Saiba mais](../content-management/get-started-experiment.md) |

## Termos de decisão e oferta {#decision-terms}

| Termo | Definição |
|------|------------|
| **Decisão** | A estrutura de decisão da geração atual no Journey Optimizer, recomendada para novas implementações. Oferece gerenciamento de catálogo de itens baseado em esquema, regras flexíveis de coleção, componentes de decisão reutilizáveis e recursos de experimentação. Disponível para Experiência baseada em código, Push, SMS e Email. [Saiba mais](../experience-decisioning/gs-experience-decisioning.md) |
| **Gestão de decisões** | O recurso herdado do Offer Decisioning no Journey Optimizer. Usa uma biblioteca central de ofertas de marketing e um mecanismo de decisão baseado em regras que aplica restrições aos perfis do cliente em tempo real. Ainda há suporte para implementações existentes, mas as novas implementações devem usar a Decisão em vez disso. Oferece suporte a email, no aplicativo, push, SMS e correspondência direta. [Saiba mais](../offers/get-started/starting-offer-decisioning.md) |
| **Oferta** | Uma mensagem de marketing, desconto ou promoção que pode ser apresentada aos clientes. As ofertas incluem regras de qualificação que determinam quais clientes podem recebê-las. [Saiba mais](../offers/offer-library/creating-personalized-offers.md) |
| **Política de decisão** | Um conjunto de regras e estratégias que determinam qual oferta mostrar a qual cliente em que momento, com base em restrições como elegibilidade, prioridade e regras de limite. [Saiba mais](../experience-decisioning/create-decision.md) |

## Dados e termos de configuração {#data-config-terms}

| Termo | Definição |
|------|------------|
| **Configuração de canal** | As configurações que definem como as mensagens são entregues para um canal específico, incluindo detalhes do remetente, subdomínio, pool de IP e tipo de mensagem (marketing ou transacional). Anteriormente conhecido como &quot;superfície&quot; ou &quot;predefinição&quot; na documentação mais antiga. [Saiba mais](../configuration/channel-surfaces.md) |
| **Lista de supressão** | Uma lista de endereços de email e domínios excluídos automaticamente da entrega de mensagens devido a devoluções permanentes, reclamações de spam ou adições manuais. O envio para endereços suprimidos está bloqueado para proteger a capacidade de entrega e a reputação do remetente. [Saiba mais](../reports/suppression-list.md) |

## Termos de conflito e priorização {#conflict-terms}

| Termo | Definição |
|------|------------|
| **Conjunto de regras** | Um grupo nomeado de regras de negócios aplicadas a jornadas e campanhas para controlar o comportamento de mensagens. Um conjunto de regras pode combinar limite de frequência, limites de entrada de jornada e horas de silêncio em uma única política reutilizável. [Saiba mais](../conflict-prioritization/rule-sets.md) |
| **Limite de frequência** | Uma regra em um conjunto de regras que limita quantas mensagens um perfil pode receber em um determinado período, por canal ou tipo de comunicação (Vendas, Promocional etc.). Os perfis que excedem o limite são excluídos automaticamente do delivery. [Saiba mais](../conflict-prioritization/channel-capping.md) |

## Quando os termos são semelhantes: guia de desambiguação {#disambiguation}

O Adobe Journey Optimizer cresceu ao longo de vários anos, o que significa que algumas áreas de recursos compartilham nomes semelhantes. Use as tabelas abaixo para identificar rapidamente qual recurso atende às suas necessidades.

### Gestão de decisões vs. gerenciamento de decisões {#decisioning-vs-dm}

Ambos os recursos selecionam e fornecem ofertas, mas atendem a diferentes estágios do ciclo de vida do produto.

| | Tomada de decisão | Gestão de decisões |
|---|---|---|
| **Status** | Atual — recomendado para todas as novas implementações | **Herdados** — ainda são suportados, mas não são mais recomendados para novas implementações |
| **Catálogo de itens** | Metadados flexíveis com base em esquema | Biblioteca de ofertas centralizada |
| **Canais com suporte** | Experiência baseada em código, push, SMS, email | Email, No aplicativo, Push, SMS, Correspondência direta |
| **Diferencial de chave** | Componentes de decisão reutilizáveis, experimentação, roteiro de canais mais amplo | Mecanismo de restrições comprovado; migrar para o Decisioning para novos projetos |
| **Introdução** | [Decisão](../experience-decisioning/gs-experience-decisioning.md) | [Gestão de decisões](../offers/get-started/starting-offer-decisioning.md) |

Se você estiver usando o Gerenciamento de decisão e quiser alternar, consulte o [guia de migração](../experience-decisioning/migrate-to-decisioning.md).

### Tipos de campanha {#campaign-types-disambiguation}

O Journey Optimizer oferece três tipos de campanha que são ativados de forma diferente e atendem a casos de uso distintos.

| | Campanhas de ação (campanhas programadas) | Campanhas acionadas por API | Campanhas orquestradas |
|---|---|---|---|
| **Ativação** | Manual ou programado | Chamada de API externa | Tela de fluxo de trabalho visual |
| **Recomendado para** | Envios em lote únicos ou recorrentes (boletins informativos, promoções) | Mensagens orientadas por eventos em tempo real (confirmações de pedidos, redefinições de senha) | Programas complexos, com vários canais e em várias etapas |
| **origem do Personalization** | Atributos do perfil | Atributos de perfil + contexto de carga da API | Atributos do perfil + dados relacionais |
| **Introdução** | [Campanhas de ação](../campaigns/create-campaign.md) | [Campanhas acionadas por API](../campaigns/api-triggered-campaigns.md) | [Campanhas orquestradas](../orchestrated/gs-orchestrated-campaigns.md) |

Para obter uma visão geral completa de todos os tipos de campanha e quando usar cada um, consulte [Introdução às campanhas](../campaigns/get-started-with-campaigns.md).

### Limite de frequência vs. arbitragem de jornada {#capping-vs-arbitration}

Ambos são mecanismos definidos por regras no conjunto de ferramentas de Conflitos e priorização, mas abordam problemas diferentes.

| | Limite de frequência | Arbitragem de jornada |
|---|---|---|
| **Problema resolvido** | Um perfil recebe muitas mensagens ao longo do tempo | Um perfil se qualifica para várias jornadas simultaneamente |
| **Escopo** | Por canal e tipo de comunicação (Vendas, Promocional etc.) | Inscrição na jornada — número de jornadas simultâneas ou qual jornada ganha |
| **Mecanismo** | Limita o número de mensagens por período; exclui automaticamente perfis excessivamente solicitados | Usa pontuações de prioridade e regras de limite para decidir em qual jornada um perfil entra |
| **Configurado em** | Conjuntos de regras → Limite de frequência | Conjuntos de regras → Limite de Jornada e arbitragem |
| **Saiba mais** | [Definir limite de frequência por canal](../conflict-prioritization/channel-capping.md) | [Gerenciar limite e arbitragem de jornada](../conflict-prioritization/journey-capping.md) |

### Cartões de conteúdo vs. mensagens no aplicativo {#content-cards-vs-in-app}

Ambos os canais fornecem mensagens em um aplicativo móvel ou da Web, mas têm modelos de renderização e comportamentos de persistência diferentes.

| | Cartões de conteúdo | Mensagens no aplicativo |
|---|---|---|
| **Modelo de exibição** | Cartões persistentes incorporados à interface do usuário do aplicativo (feed, caixa de entrada ou superfície personalizada) | Sobreposições transitórias, banners ou modais mostrados na parte superior do aplicativo |
| **Persistência** | Permanece visível até ser explicitamente descartado ou expirar | Desaparece depois que o usuário interage ou o fecha |
| **Acionador** | O SDK é renderizado na carga, as regras controlam a exibição e a demissão | Um evento em tempo real na jornada ou campanha aciona o delivery |
| **Recomendado para** | Promoções contínuas, status de fidelidade, alertas persistentes | Dicas de integração, ofertas por tempo limitado, notificações transitórias |
| **Introdução** | [Cartões de conteúdo](../content-card/create-content-card.md) | [Mensagens no aplicativo](../in-app/get-started-in-app.md) |

>[!NOTE]
>
>**Adobe Journey Optimizer vs Journey Optimizer B2B edition:** São dois produtos separados na mesma família de marcas. O Adobe Journey Optimizer (esta documentação) é direcionado para jornadas de clientes B2C. O Journey Optimizer B2B edition foi desenvolvido especificamente para marketing baseado em conta, trabalhando com grupos de compra e públicos-alvo de conta. Se você estiver procurando a documentação do B2B edition, visite o [guia do Journey Optimizer B2B edition](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-b2b/user/guide-overview){target="_blank"}.

## Tópicos relacionados {#related-topics}

* [Noções básicas sobre como o Journey Optimizer funciona](understanding-ajo.md) — veja como as jornadas, campanhas, perfis e canais se encaixam na arquitetura do produto.
* [Introdução aos recursos de decisão](../experience-decisioning/gs-decision.md) — compare a Decisão e a Gestão de decisões lado a lado e escolha a abordagem certa para sua implementação.
* [Introdução ao jornada](../building-journeys/journey.md) — saiba como criar experiências sequenciais acionadas por eventos para o cliente passo a passo.
* [Introdução às campanhas](../campaigns/get-started-with-campaigns.md) — Entenda os três tipos de campanha (Ação, Acionado por API, Orquestrado) e quando usar cada um.
* [Gerenciamento de conflitos e priorização](../conflict-prioritization/gs-conflict-prioritization.md) — Saiba como usar conjuntos de regras, limite de frequência, pontuações de prioridade e horas de silêncio para evitar mensagens excessivas.
* [Introdução aos canais de comunicação](../channels/gs-channels.md) — Procure todos os canais disponíveis, seus pré-requisitos e como configurá-los.
