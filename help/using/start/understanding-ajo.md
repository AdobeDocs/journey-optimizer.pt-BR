---
solution: Journey Optimizer
product: journey optimizer
title: Noções básicas sobre o Journey Optimizer
description: Saiba como o Adobe Journey Optimizer funciona com o Adobe Experience Platform para fornecer experiências personalizadas ao cliente
feature: Get Started
role: Admin, Developer, User
level: Beginner
source-git-commit: a956684ab52f9045b5e1f84cc0b8d0071689873b
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 1%

---

# Noções básicas sobre o Journey Optimizer {#understanding-ajo}

O Adobe Journey Optimizer (AJO) e o Adobe Experience Platform (AEP) trabalham juntos para permitir a personalização orientada por dados em escala. Esta página explica como esses sistemas operam e como suas principais áreas funcionais se combinam para fornecer experiências excepcionais ao cliente.

## Como o Journey Optimizer funciona {#how-it-works}

O Adobe Journey Optimizer funciona como um fluxo contínuo em que os dados são coletados, analisados e aplicados para criar jornadas personalizadas do cliente.

![](assets/ajo-aep-architecture-diagram.png)

### Adobe Experience Platform: a base {#aep-foundation}

O Adobe Experience Platform serve como backbone, permitindo que as marcas centralizem os dados dos clientes e os ativem para experiências personalizadas:

* **Plataforma de dados** - Hub central para coletar, gerenciar e estruturar dados do cliente para garantir a consistência entre os sistemas
* **Assimilação de dados (Fontes)** - Importe dados de plataformas CRM, sites, aplicativos móveis e armazenamento na nuvem usando conectores pré-criados
* **Perfil do cliente em tempo real** - Cria perfis unificados ao mesclar dados de várias fontes (interações de email, compras na loja, comportamento da web)
* **Camada de governança** - Controla o acesso aos dados, a conformidade com a privacidade e a segurança enquanto segue as regulamentações

### Adobe Journey Optimizer: o mecanismo de orquestração {#ajo-orchestration}

O Adobe Journey Optimizer aplica os dados e insights do AEP para fornecer experiências inteligentes e personalizadas aos clientes:

* **Noções básicas do cliente** - Os perfis de clientes em tempo real habilitam a segmentação em públicos para mensagens direcionadas
* **Conteúdo e ofertas** - Ferramentas para criar, gerenciar e personalizar conteúdo; lógica em tempo real para selecionar a melhor oferta para cada indivíduo
* **Gerenciamento de Jornadas e Campanhas** - Automatiza sequências de interações (jornadas) ou agenda mensagens direcionadas únicas (campanhas)
* **Entrega (Conexões)** - Entrega mensagens por canais como email, SMS, notificações por push e correspondência direta; exporta dados para sistemas externos
* **Avaliação e análise** - Acompanha o engajamento do cliente e o desempenho da campanha com relatórios para melhoria contínua

### O ciclo de otimização contínua {#optimization-cycle}

Esse ecossistema opera como um ciclo de otimização contínuo. Os dados impulsionam a compreensão do cliente, que informa o conteúdo personalizado e as decisões. Eles são orquestrados em jornadas, distribuídos em canais, medidos para eficiência e refinados ao longo do tempo.

![](../assets/do-not-localize/get-started-flow.png)

## Áreas Funcionais Principais {#functional-areas}

O Journey Optimizer inclui sete áreas funcionais principais que funcionam em conjunto perfeitamente:

| Área funcional | Finalidade | Principais atividades |
|-----------------|---------|----------------|
| **Gerenciamento de dados** | Organize os dados do cliente | Definir esquemas, criar conjuntos de dados, importar dados de vários sistemas |
| **Gerenciamento de Clientes** | Entenda quem são seus clientes | Criar perfis unificados, resolver identidades, criar públicos |
| **Gerenciamento de conteúdo** | Criar mensagens personalizadas | Projetar emails, gerenciar ativos, criar modelos e fragmentos, personalizar conteúdo |
| **Gestão de decisões** | Selecione a melhor oferta em tempo real | Gerenciar biblioteca de ofertas, definir regras, aplicar restrições, estabelecer lógica de classificação |
| **Gerenciamento de Jornadas** | Projetar experiências automatizadas do cliente | Crie jornadas com o visual designer, defina acionadores, adicione condições e etapas de espera |
| **Conexões** | Conectar fontes de dados e canais | Configurar conectores de origem, configurar canais, conectar a plataformas externas |
| **Administração e Privacidade** | Configuração e conformidade do controle | Gerenciar usuários, configurar sandboxes, configurar canais, lidar com solicitações de privacidade |

### Como Essas Áreas Trabalham Juntas {#working-together}

Estas áreas funcionais operam em um ciclo contínuo:

1. **Assimilação de dados** - Fluxos de dados na AEP, estruturados pela Gestão de Dados
2. **Noções básicas do cliente** - Os perfis de clientes em tempo real unificam os dados; o gerenciamento de clientes cria públicos
3. **Estratégia de conteúdo e oferta** - O gerenciamento de conteúdo cria mensagens; o gerenciamento de decisões define a lógica de oferta
4. **Orquestração** - O Gerenciamento de Jornadas mapeia interações entre canais usando dados, conteúdo e decisões do cliente
5. **Entrega** - As conexões facilitam a entrega de mensagens via canais ou o compartilhamento de dados com sistemas externos
6. **Medição** - Os dados de desempenho alimentam os insights para refinar públicos, conteúdo, decisões e jornadas
7. **Governança** - Os controles de administração e privacidade garantem a conformidade em todo o

## Detalhes da arquitetura {#architecture-details}

Para equipes técnicas, este é o diagrama detalhado de arquitetura que mostra como o Journey Optimizer se integra ao Adobe Experience Platform:

![Arquitetura do Adobe Journey Optimizer](assets/ajo-architecture.png)

Quatro aplicativos são criados nativamente no Experience Platform: Adobe Real-Time Customer Data Platform, Journey Optimizer, Customer Journey Analytics e Adobe Mix Modeler. O Journey Optimizer funciona perfeitamente com esses aplicativos, mas também pode funcionar de forma independente.

### Pontos de integração {#integration-points}

O Journey Optimizer integra-se ao Adobe Experience Platform em vários níveis:

* **Camada de dados** - Compartilha o mesmo Perfil do cliente em tempo real, Gráfico de identidade e conjuntos de dados
* **Camada de serviço** - Aproveita os serviços de governança, privacidade e consulta da AEP
* **Camada de aplicativos** - Oferece orquestração de jornadas, gestão de decisões e gestão de conteúdo sobre o AEP

Saiba mais sobre [blueprints do Adobe Journey Optimizer](https://experienceleague.adobe.com/pt-br/docs/blueprints-learn/architecture/customer-journeys/journey-optimizer/journey-optimizer-overview){target="_blank"}.

## Privacidade e segurança {#privacy-security}

As práticas de privacidade e segurança da Adobe Experience Cloud se aplicam ao Adobe Journey Optimizer. Essas medidas garantem a conformidade com as regulamentações de privacidade, como o GDPR, permitindo que você forneça experiências personalizadas, mantendo a confiança do cliente.

[Saiba mais sobre privacidade no Journey Optimizer](../privacy/get-started-privacy.md)

>[!MORELIKETHIS]
>
>* [Introdução ao Journey Optimizer](get-started.md)
>* [Terminologia de chave](terminology.md)
>* [Guia da interface do usuário](user-interface.md)
>* [Medidas de proteção e limitações](guardrails.md)

