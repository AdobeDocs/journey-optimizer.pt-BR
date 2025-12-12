---
solution: Journey Optimizer
product: journey optimizer
title: Funções e responsabilidades
description: Saiba mais sobre as diferentes funções envolvidas no Adobe Journey Optimizer e suas responsabilidades
feature: Get Started
role: Admin, Developer, User
level: Beginner
exl-id: 71ab7369-fd84-46eb-95d2-941bd887d565
redpen-status: PASS_||_2025-04-28_15-13-07
source-git-commit: d3765f66beff13aaf77cd585c5da5f93c44fa1df
workflow-type: tm+mt
source-wordcount: '1724'
ht-degree: 13%

---


# Funções e responsabilidades

O Adobe Journey Optimizer permite que as marcas forneçam experiências conectadas, contextuais e personalizadas por toda a jornada do cliente. Criada com um foco completo em escala, velocidade e flexibilidade, a Journey Optimizer combina três principais impulsionadores de valor em um aplicativo unificado:

* **Insights e engajamento do cliente em tempo real** viabilizados pelo perfil do cliente em tempo real da Adobe
* **Orquestração omnicanal moderna** por meio de telas unificadas para jornadas em tempo real e campanhas em lote, além de um designer de mensagens moderno
* **Decisão e personalização inteligentes** por meio da gestão de decisões e dos recursos de IA/ML

O Journey Optimizer oferece duas abordagens de orquestração para atender a diferentes necessidades de marketing:

* **Jornadas**: ideal para o envolvimento individualizado em tempo real, no qual cada cliente avança no seu ritmo e é acionado por comportamento ou eventos
* **Campanhas orquestradas**: ideal para campanhas em lote e de um para muitos, em que os públicos-alvo avançam juntos por meio de fluxos de trabalho de várias etapas de acordo com um cronograma; ideal para promoções sazonais, lançamentos de produtos e comunicações baseadas em conta

Essa experiência unificada permite implementar casos de uso inteiros em um único local, desde definir públicos e criar jornadas até criar conteúdo personalizado e analisar resultados. Esta documentação explica as principais funções para o uso eficaz do Journey Optimizer, suas responsabilidades e como começar.

**Observação importante:** o Adobe Journey Optimizer define funções distintas com responsabilidades específicas. Uma única pessoa pode realizar várias funções ou todas as funções, dependendo da estrutura da organização.

## Guias de início rápido com base em funções

Para simplificar a implementação, o Adobe Journey Optimizer organiza tarefas em funções específicas com base na experiência. Cada função se concentra em tarefas essenciais necessárias para fornecer uma experiência fluida ao cliente.

| Função | Responsabilidades principais | Habilidades principais | Tarefas típicas |
|-------------------|----------------------------------|--------------------------------|-----------------------------------------------|
| **Admin** | Configuração do ambiente e gerenciamento de acesso | Configuração do sistema, gerenciamento de usuários, segurança | Configurar sandboxes, gerenciar permissões de usuário, canais e predefinições de mensagem |
| **Engenheiro de dados** | Dados e fontes de dados do perfil do cliente | Modelagem de dados, esquemas XDM, conectores de origem | Modelar dados de perfil e de negócios em esquemas, configurar conectores de origem, monitorar assimilação de dados |
| **Desenvolvedor** | Implementação técnica e integrações | SDK para dispositivos móveis/Web, APIs, arquitetura orientada por eventos | Integrar SDKs, implementar eventos, criar endpoints de ação personalizados |
| **Profissional de marketing** | Jornada experiências personalizadas e de design | Orquestração de jornadas, criação de conteúdo, direcionamento de público | Projete jornadas do cliente, crie e personalize mensagens, gerencie ofertas e componentes de decisão e defina públicos |

Cada função aborda uma fase específica da implementação do Adobe Journey Optimizer e garante um processo de implantação estruturado e eficiente.

## Ordem de implementação e Dependências de funções

Uma implementação bem-sucedida do Journey Optimizer normalmente segue essa sequência, o que reflete nas dependências entre as funções:

1. **Admin**: configura o ambiente\
   O administrador estabelece a base configurando sandboxes, definindo controles de acesso e preparando configurações de canal. Isso deve acontecer primeiro para permitir que outras equipes trabalhem.
   * Configurar sandboxes de desenvolvimento, preparo e produção
   * Configurar atribuições, permissões e OLAC (object-level access control, controle de acesso em nível de objeto)
   * Definir as configurações de canal (email, SMS, push, no aplicativo, Web, cartões de conteúdo)
   * Delegar subdomínios e configurar pools de IP
   * Configurar listas de supressão e políticas de consentimento

2. **Engenheiro de dados**: cria a base de dados\
   Os engenheiros de dados criam a infraestrutura de dados que viabiliza a personalização, definindo como os dados do cliente fluem para e pelo sistema.
   * Criar namespaces de identidade para identificação do cliente
   * Criar esquemas XDM (perfil, eventos de experiência, relacional)
   * Configurar conjuntos de dados e ativá-los para o Perfil do cliente em tempo real
   * Configurar a assimilação de dados (em lote e transmissão)
   * Criar atributos computados para cálculos complexos
   * Configurar eventos e fontes de dados para o jornada

3. **Desenvolvedor**: implementa integrações técnicas\
   Os desenvolvedores conectam aplicativos ao Journey Optimizer integrando SDKs, enviando eventos e criando endpoints de API. Essas implementações permitem que as jornadas acionem e executem.
   * Integrar o Mobile SDK (iOS/Android) à configuração de notificação por push
   * Implementar o Web SDK para experiências na Web
   * Enviar eventos de aplicativos para acionar jornadas
   * Criar endpoints de ação personalizados para integrações de sistema externas
   * Testar implementações usando o Adobe Experience Platform Assurance

4. **Profissional de marketing**: projeta e executa experiências de clientes\
   Os profissionais de marketing aproveitam todo o trabalho fundamental para criar jornadas, criar conteúdo e otimizar as experiências do cliente em todos os canais.
   * Crie públicos-alvo usando segmentação, upload de CSV ou composição de público-alvo
   * Projetar conteúdo personalizado com o Assistente de IA e modelos
   * Criar jornadas multicanal com acionadores de evento e público-alvo
   * Testar com fluxos de trabalho de aprovação antes do lançamento
   * Monitore o desempenho e otimize com base em insights de relatórios

**Observação:** embora esta sequência seja típica, algumas atividades podem ocorrer em paralelo. Por exemplo, os desenvolvedores podem trabalhar em integrações de aplicativos, enquanto os engenheiros de dados configuram esquemas.

## Introdução por função

Cada função começa com tarefas específicas condizentes com o foco de cada uma delas. A conclusão destas etapas iniciais garante uma integração e um alinhamento ininterruptos em relação ao processo geral de implementação:

### Para profissionais de marketing {#for-marketers}

Como profissional de marketing ou profissional de negócios, você cria jornadas para clientes a fim de fornecer experiências pessoais e contextuais em todos os pontos de contato. Você trabalhará em uma interface unificada para implementar casos de uso completos do início ao fim.

**Principais recursos que você usará:**

* **Journey Orchestration**: crie um engajamento do cliente individualizado em tempo real, no qual cada pessoa se move no seu próprio ritmo e acionado por comportamento ou eventos entre canais
* **Orquestração de campanhas**: projete e automatize campanhas em lote complexas e com várias etapas em escala usando uma tela visual. Perfeito para campanhas iniciadas pela marca, como promoções sazonais, lançamentos de produtos e comunicações baseadas em conta. Aproveite a segmentação de várias entidades para criar públicos-alvo precisos conectando dados do cliente a entidades relacionadas (contas, compras, reservas)
* **Modern Message Designer**: crie e personalize mensagens de email e dispositivos móveis com uma interface de arrastar e soltar. Edite modelos prontos para uso para acelerar o tempo de comercialização
* **Gerenciamento de decisão**: crie e gerencie ofertas, regras de elegibilidade e outros componentes em uma biblioteca centralizada que possa ser incorporada a emails e pontos de contato do cliente
* **Gerenciamento de ativos**: acesse o Adobe Experience Manager Assets Essentials totalmente incorporado ao Journey Optimizer para obter acesso e entrega simplificados de ativos
* **Definição de público-alvo**: crie públicos-alvo sob demanda com refinamento instantâneo usando consultas relacionais, com visibilidade de pré-envio para contagens precisas de público-alvo
* **Serviços de IA/ML**: aproveite a otimização de tempo de envio e as pontuações de engajamento preditivo para direcionar clientes de alto valor e minimizar o risco de churn

**Comece com:** use modelos de casos de uso e assistentes para criar e implantar facilmente novas jornadas de clientes.

[Introdução como profissional de marketing →](path/marketer.md)

### Para engenheiros de dados {#for-data-engineers}

Como arquiteto ou engenheiro de dados, você configura e mantém os dados de perfil do cliente e outras fontes de dados que potencializam as experiências orquestradas pela Journey Optimizer.

**Principais responsabilidades:**

* **Dados de perfil do cliente**: modele dados de perfil do cliente e dados de negócios para esquemas para criar uma visualização unificada de 360 graus do cliente
* **Modelagem de Dados Relacionais**: Para campanhas Orquestradas, crie esquemas relacionais para habilitar a segmentação de várias entidades, conectando dados do cliente a entidades relacionadas, como contas, compras, assinaturas e reservas, para proporcionar uma criação flexível de público-alvo
* **Source Connectors**: configure conectores de origem para assimilar dados da Web, do CRM, de dados offline e de outras fontes na Adobe Experience Platform
* **Resolução de identidade**: configure namespaces de identidade para atualizar perfis continuamente e mover clientes para dentro e para fora de segmentos e jornadas em tempo real
* **Fontes de Dados**: configure as fontes de dados para ouvir sinais externos em tempo real na jornada do cliente
* **Gerenciamento de perfil**: habilitar conjuntos de dados para o Perfil do cliente em tempo real para potencializar experiências personalizadas
* **Qualidade dos dados**: monitore a assimilação de dados para garantir que tudo flua sem problemas para o Journey Optimizer

**Comece com:** Modele seu primeiro esquema de perfil de cliente e configure um conector de origem para começar a assimilar dados.

[Introdução como engenheiro de dados →](path/data-engineer.md)

### Para administradores {#for-administrators}

Como administrador, você configura o ambiente do Journey Optimizer para permitir que suas equipes trabalhem com eficiência e segurança.

**Principais responsabilidades:**

* **Sandboxes**: criar e gerenciar sandboxes para particionar dados e jornadas para diferentes grupos de usuários (desenvolvimento, teste, produção)
* **Gerenciamento de Usuários**: Configurar grupos de usuários e permissões para controlar o acesso a diferentes funcionalidades
* **Configuração de Canal**: configure canais de entrega e predefinições de mensagem para garantir uma identidade visual consistente entre as mensagens e os ativos entregues por meio do Journey Optimizer
* **Segurança e governança**: aplique o OLAC (controle de acesso em nível de objeto), configure políticas de consentimento e implemente políticas de governança de dados
* **Capacidade de entrega**: delegar subdomínios, criar pools de IP e gerenciar listas de supressão e listas de permissões
* **Configuração da Jornada**: definir os elementos e as configurações da jornada para suas equipes

**Comece com:** Configure sandboxes e permissões de usuário e, em seguida, defina as primeiras configurações de canal e predefinições de mensagem.

[Introdução como administrador →](path/administrator.md)

### Para desenvolvedores {#for-developers}

Implemente integrações técnicas que conectam o Journey Optimizer aos seus aplicativos.

**Principais responsabilidades:**

* Integrar o Adobe Experience Platform Mobile SDK (iOS/Android)
* Implementar o Web SDK para experiências na Web e notificações por push da Web
* Configurar credenciais e certificados de notificação por push
* Enviar eventos de aplicativos para acionar jornadas
* Criar endpoints de API que o Journey Optimizer chama por meio de ações personalizadas
* Implementar experiências baseadas em código para superfícies da Web, móveis e outras
* Implementações de teste e depuração com o Adobe Experience Platform Assurance
* Trabalhar com APIs do Journey Optimizer para acesso programático

**Comece com:** integre o Mobile ou o Web SDK e implemente seu primeiro evento para acionar uma jornada.

[Introdução como desenvolvedor →](path/developer.md)

## Cross-Role Collaboration

As implementações bem-sucedidas do Journey Optimizer exigem colaboração em todas as funções. Cada função trabalha com outras pessoas para fornecer experiências contínuas ao cliente:

>[!BEGINTABS]

>[!TAB Administradores]

**Os administradores** habilitam todas as equipes gerenciando o acesso e as configurações. Eles trabalham com:

* **Engenheiros de dados**: concedam permissões para gerenciamento de dados, aprovem o acesso à sandbox e coordenem políticas de governança
* **Desenvolvedores**: fornecer credenciais de API, configurar ambientes de teste, aprovar configurações de canal
* **Profissionais de marketing**: atribuir permissões para jornadas/campanhas, configurar canais e suportar ambientes de teste

>[!TAB Engenheiros de dados]

**Os engenheiros de dados** fornecem a base de dados para todos. Eles trabalham com:

* **Administradores**: solicitem permissões para gerenciamento de dados, coordenem políticas de governança e retenção
* **Desenvolvedores**: fornecer esquemas XDM e estruturas de evento, definir formatos de carga do evento, testar assimilação de dados
* **Profissionais de marketing**: criar atributos computados para personalização, compilar públicos, configurar esquemas relacionais

>[!TAB Desenvolvedores]

**Desenvolvedores** implementam integrações técnicas que alimentam o jornada. Eles trabalham com:

* **Engenheiros de dados**: obtenha esquemas XDM e estruturas de evento, alinhe-se aos requisitos de coleta de dados e teste a entrega de eventos
* **Administradores**: fornecer especificações de API, solicitar permissões e credenciais e coordenar a estratégia de teste
* **Profissionais de marketing**: entender acionadores de eventos, implementar rastreamento, oferecer suporte a testes de jornada e solucionar problemas

>[!TAB Profissionais de marketing]

**Os profissionais de marketing** criam experiências para os clientes e fornecem comentários. Eles trabalham com:

* **Engenheiros de dados**: solicitem atributos computados, coordenem os requisitos de público-alvo e forneçam feedback sobre a qualidade dos dados
* **Desenvolvedores**: alinhar em disparadores de eventos, implementações de teste, rastreamento de validação
* **Administradores**: solicitar configurações de canal, confirmar acesso a recursos e coordenar a habilitação

>[!ENDTABS]

**Prática recomendada:** realize reuniões multifuncionais regulares para se alinhar às prioridades, compartilhar progresso e endereçar bloqueadores entre equipes.

## Vídeo tutorial {#video}

Para saber mais sobre os principais recursos e personas do Journey Optimizer, assista ao vídeo de introdução. O vídeo aborda a interface do usuário e destaca os principais recursos com base em fluxos de trabalho específicos de cada função.

>[!VIDEO](https://video.tv.adobe.com/v/3424995?quality=12)

## Recursos adicionais

Para lições e atualizações mais detalhadas, confira os seguintes recursos:

>[!BEGINTABS]

>[!TAB Aprendizagem e Documentação]

* [Vídeos tutoriais](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/overview){target="_blank"} - Tutoriais em vídeo passo a passo para todas as funções
* [Biblioteca de Casos de Uso do Jornada](../building-journeys/jo-use-cases.md) - Exemplos práticos e padrões de implementação
* [IA e recursos inteligentes](ai-features.md) - Saiba mais sobre o Assistente de IA, otimização de tempo de envio e geração de conteúdo
* [Guia da Interface do Usuário](user-interface.md) - Navegue pela Journey Optimizer com eficiência

>[!TAB Permanecer atualizado]

* [Notas de versão](../rn/release-notes.md) - Recursos, melhorias e correções mais recentes
* [Atualizações da documentação](../rn/documentation-updates.md) - Rastreie alterações recentes na documentação
* [Notificações de Produto](../rn/releases.md#staying-informed) - Saiba como assinar emails e alertas no produto para atualizações do Journey Optimizer

>[!TAB Comunidade e suporte]

* [Comunidade do Experience League](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"} - Conecte-se com outros usuários e especialistas
* [Fórum de produtos](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"} - Faça perguntas e compartilhe conhecimento

>[!ENDTABS]
