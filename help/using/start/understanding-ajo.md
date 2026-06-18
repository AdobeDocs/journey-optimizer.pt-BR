---
solution: Journey Optimizer
product: journey optimizer
title: Noções básicas sobre o Journey Optimizer
description: Saiba como o Adobe Journey Optimizer funciona com o Adobe Experience Platform para fornecer experiências personalizadas ao cliente
feature: Get Started
topic: Content Management
role: Admin, Developer, User
level: Beginner
keywords: jornada otimizer, como funciona, arquitetura, plataforma de experiência, áreas funcionais
exl-id: 9df179a0-a5f6-4dbd-a9db-a103731b1854
TQID: https://experienceleague.adobe.com/E2ksPVFZBggv1RgEri7jx30G2oSanpmNs77vH9Yuq78
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
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: cbcb1cb0abbb8d4c6ea173c4deff071d0081da4e
workflow-type: tm+mt
source-wordcount: 984
ht-degree: 3%

---

# Noções básicas sobre o Journey Optimizer {#understanding-ajo}

>[!BEGINSHADEBOX]

**Nesta página:** veja como o Adobe Journey Optimizer funciona com o Adobe Experience Platform para que você possa entender o ciclo de dados para experiência, as áreas funcionais e a arquitetura por trás de jornadas personalizadas.

>[!ENDSHADEBOX]

Esta página explica como o Adobe Experience Platform e o Journey Optimizer trabalham juntos, abordando o ciclo contínuo de dados para experiência, as principais áreas funcionais, os detalhes da arquitetura e os pontos de integração.

O Adobe Journey Optimizer e o Adobe Experience Platform trabalham juntos para permitir a personalização orientada por dados em escala. Esta página explica como esses sistemas operam e como suas principais áreas funcionais se combinam para fornecer experiências excepcionais ao cliente. [Saiba mais sobre os principais recursos](get-started.md) | [Explorar a terminologia principal](terminology.md)

## Como o Journey Optimizer funciona {#how-it-works}

Sem uma base de dados unificada, as marcas são forçadas a confiar em várias ferramentas específicas de canal — dificultando a manutenção de uma visualização consistente de cada cliente ou a ação em seu comportamento em tempo real. A Journey Optimizer resolve isso criando uma base no Adobe Experience Platform para conectar os dados do cliente, a criação de conteúdo e a orquestração de jornadas em um único sistema contínuo. O resultado são experiências de marca significativas que impulsionam a fidelidade do cliente e o valor vitalício.

O Adobe Journey Optimizer funciona como um fluxo contínuo em que os dados são coletados, analisados e aplicados para criar jornadas personalizadas do cliente.

![Diagrama mostrando o Adobe Experience Platform como a camada de dados fundamental, com o Journey Optimizer integrado ao Real-Time CDP, Customer Journey Analytics e Adobe Mix Modeler, todos compartilhando os serviços principais, como Perfil do Cliente em Tempo Real, governança de dados e resolução de identidade.](assets/ajo-aep-architecture-diagram.png)

### Adobe Experience Platform: a base {#aep-foundation}

O Adobe Experience Platform serve como backbone, permitindo que as marcas centralizem os dados dos clientes e os ativem para experiências personalizadas:

* **Plataforma de dados** - Hub central para coletar, gerenciar e estruturar dados do cliente para garantir a consistência entre os sistemas. [Saiba mais sobre esquemas e conjuntos de dados](../data/get-started-schemas.md)
* **Assimilação de dados (Fontes)** - Importe dados de plataformas CRM, sites, aplicativos móveis e armazenamento na nuvem usando conectores pré-criados. [Explorar fontes de dados](get-started-sources.md)
* **Perfil do cliente em tempo real** - Cria perfis unificados ao mesclar dados de várias fontes (interações de email, compras na loja, comportamento da web). [Saiba mais sobre perfis](../audience/get-started-profiles.md)
* **Camada de governança** - Controla o acesso aos dados, a conformidade com a privacidade e a segurança enquanto segue as regulamentações. [Exibir documentação de privacidade](../privacy/get-started-privacy.md)

### Adobe Journey Optimizer: o mecanismo de orquestração {#ajo-orchestration}

O Adobe Journey Optimizer aplica os dados e insights do Adobe Experience Platform para fornecer experiências inteligentes e personalizadas aos clientes:

* **Noções básicas do cliente** - Os Perfis de clientes em tempo real permitem a segmentação em públicos para mensagens direcionadas. [Criar públicos-alvo](../audience/about-audiences.md)
* **Conteúdo e ofertas** - um designer visual integrado, modelos reutilizáveis e uma biblioteca de ativos centralizada permitem que as equipes criem e personalizem mensagens para qualquer canal, sem sair da plataforma. A personalização dinâmica adapta o conteúdo com base nos atributos, comportamento e contexto do cliente. A lógica de decisão em tempo real seleciona a melhor oferta para cada indivíduo. [Criar conteúdo](../../rp_landing_pages/content-management-landing-page.md) | [Gerenciar ativos](../integrations/assets.md) | [Gerenciar ofertas](../offers/get-started/starting-offer-decisioning.md)
* **Gerenciamento de Jornadas e Campanhas** - Automatiza sequências de interações (jornadas) ou agenda mensagens direcionadas únicas (campanhas). [Criar jornadas](../building-journeys/journey-gs.md) | [Criar campanhas](../campaigns/get-started-with-campaigns.md)
* **Entrega (Conexões)** - Entrega mensagens por canais como email, SMS, notificações por push e correspondência direta; exporta dados para sistemas externos. [Configurar canais](../configuration/get-started-configuration.md)
* **Avaliação e análise** - Acompanha o engajamento do cliente e o desempenho da campanha com relatórios para melhoria contínua. [Exibir relatórios](../reports/campaign-global-report-cja.md)

### O ciclo de otimização contínuo {#optimization-cycle}

Esse ecossistema opera como um ciclo de otimização contínuo. Os dados impulsionam a compreensão do cliente, que informa o conteúdo personalizado e as decisões. Eles são orquestrados em jornadas, distribuídos em canais, medidos para eficiência e refinados ao longo do tempo.

![Diagrama que ilustra o ciclo de otimização contínua no Journey Optimizer: a assimilação de dados alimenta perfis de clientes, que informam as decisões de conteúdo e oferta, orquestrados em jornadas, entregues em canais, medidos para desempenho e refinados ao longo do tempo.](../assets/do-not-localize/get-started-flow.png)

## Principais áreas funcionais {#functional-areas}

O Journey Optimizer inclui sete áreas funcionais principais que funcionam em conjunto perfeitamente:

| Área funcional | Finalidade | Principais atividades |
|-----------------|---------|----------------|
| **Gerenciamento de dados** | Organize os dados do cliente | Defina esquemas, crie conjuntos de dados e importe dados de vários sistemas. [Saiba mais](../data/get-started-schemas.md) |
| **Gerenciamento de Clientes** | Entenda quem são seus clientes | Crie perfis unificados, resolva identidades e crie públicos. [Saiba mais](../audience/get-started-profiles.md) |
| **Gerenciamento de conteúdo** | Criar mensagens personalizadas | Projete emails, gerencie ativos, crie modelos e fragmentos e personalize conteúdo. [Saiba mais](../../rp_landing_pages/content-management-landing-page.md) |
| **Gestão de decisões** | Selecione a melhor oferta em tempo real | Gerencie a biblioteca de ofertas, defina regras, aplique restrições e estabeleça a lógica de classificação. [Saiba mais](../offers/get-started/starting-offer-decisioning.md) |
| **Gerenciamento de Jornadas** | Projetar experiências automatizadas do cliente | Crie jornadas com o designer visual, defina acionadores, adicione condições e aguarde etapas. [Saiba mais](../building-journeys/journey-gs.md) |
| **Conexões** | Conectar fontes de dados e canais | Configure conectores de origem, configure canais e conecte a plataformas externas. [Saiba mais](../configuration/get-started-configuration.md) |
| **Administração e Privacidade** | Configuração e conformidade do controle | Gerencie usuários, configure sandboxes, configure canais e lide com solicitações de privacidade. [Saiba mais](../administration/permissions.md) |

### Como essas áreas funcionam juntas {#working-together}

Estas áreas funcionais operam em um ciclo contínuo:

1. **Assimilação de dados** - Fluxos de dados na Adobe Experience Platform, estruturados pela Gestão de Dados
2. **Noções básicas do cliente** - Os perfis de clientes em tempo real unificam os dados; o gerenciamento de clientes cria públicos
3. **Estratégia de conteúdo e oferta** - O gerenciamento de conteúdo cria mensagens; o gerenciamento de decisões define a lógica de oferta
4. **Orquestração** - O Gerenciamento de Jornadas mapeia interações entre canais usando dados, conteúdo e decisões do cliente
5. **Entrega** - As conexões facilitam a entrega de mensagens via canais ou o compartilhamento de dados com sistemas externos
6. **Medição** - Os dados de desempenho alimentam os insights para refinar públicos, conteúdo, decisões e jornadas
7. **Governança** - Os controles de administração e privacidade garantem a conformidade em todo o

## Detalhes da arquitetura {#architecture-details}

O Journey Optimizer é um dos quatro aplicativos criados nativamente no Adobe Experience Platform, junto com o Real-Time CDP, Customer Journey Analytics e Adobe Mix Modeler. Ele compartilha os principais serviços da AEP — perfil do cliente em tempo real, gráfico de identidade, governança de dados e serviços de consulta — para acessar uma base de dados unificada do cliente sem exigir integrações separadas. O Journey Optimizer pode operar como um aplicativo independente ou interoperar com outros aplicativos nativos da AEP.

Para aprofundar a arquitetura técnica, incluindo padrões de integração, pré-requisitos e fluxos de dados do sistema, consulte os [Adobe Journey Optimizer Blueprints](https://experienceleague.adobe.com/pt-br/docs/blueprints-learn/architecture/architecture-diagrams/customer-journeys/journey-optimizer/journey-optimizer-overview){target="_blank"}. Para considerações de implementação, [revise as medidas de proteção e as limitações](guardrails.md).

## Privacidade e segurança {#privacy-security}

As práticas de privacidade e segurança de [!DNL Adobe CX Enterprise] se aplicam ao Adobe Journey Optimizer. Essas medidas garantem a conformidade com as regulamentações de privacidade, como o GDPR, permitindo que você forneça experiências personalizadas, mantendo a confiança do cliente. [Saiba mais sobre privacidade no Journey Optimizer](../privacy/get-started-privacy.md)
