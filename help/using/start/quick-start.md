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
source-git-commit: fd10a600cb54b8c35e2d195be7379b0dd120b6a7
workflow-type: tm+mt
source-wordcount: '1831'
ht-degree: 88%

---


# Funções e responsabilidades

O Adobe Journey Optimizer (AJO) permite que as marcas forneçam experiências conectadas, contextualizadas e personalizadas durante toda a jornada do cliente. Criado com foco de ponta a ponta em escala, velocidade e flexibilidade, o Journey Optimizer combina três impulsionadores de valor principais em um aplicativo unificado:

* **Insights do cliente e engajamento em tempo real** viabilizados pelo perfil do cliente em tempo real da Adobe
* **Orquestração omnicanal moderna** por meio de telas unificadas para jornadas em tempo real e campanhas em lote, além de um designer de mensagens moderno
* **Tomada de decisão e personalização inteligentes** por meio da gestão de decisões e dos recursos de IA e aprendizado de máquina

O Journey Optimizer oferece duas abordagens de orquestração para atender a diferentes necessidades de marketing:

* **Jornadas**: a melhor opção para engajamento um a um em tempo real, no qual cada cliente avança no seu ritmo e é acionado por comportamento ou eventos
* **Campanhas orquestradas**: a melhor opção para campanhas em lote de um para muitos, em que os públicos-alvo avançam juntos por fluxos de trabalho de várias etapas de acordo com um cronograma. Ideal para promoções sazonais, lançamentos de produtos e comunicações baseadas em conta

Essa experiência unificada permite implementar casos de uso completos em um único local, desde a definição de públicos-alvo e a criação de jornadas até a criação de conteúdo personalizado e a análise de resultados. Esta documentação explica as principais funções para o uso eficaz do Journey Optimizer, suas responsabilidades e como começar.

**Observação importante:** o Adobe Journey Optimizer define funções distintas com responsabilidades específicas. Uma única pessoa pode realizar várias funções ou todas as funções, dependendo da estrutura da organização.

## Guias de início rápido com base em funções

Para simplificar a implementação, o Adobe Journey Optimizer organiza tarefas em funções específicas com base na experiência. Cada função se concentra em tarefas essenciais necessárias para fornecer uma experiência fluida ao cliente.

| Função | Responsabilidades principais | Habilidades principais | Tarefas típicas |
|-------------------|----------------------------------|--------------------------------|-----------------------------------------------|
| **Admin** | Configuração do ambiente e gerenciamento de acesso | Configuração do sistema, gerenciamento de usuários, segurança | Configure sandboxes, gerencie permissões de usuário, configure canais e predefinições de mensagem |
| **Engenheiro de dados** | Dados e fontes de dados do perfil do cliente | Modelagem de dados, esquemas XDM, conectores de origem | Modele dados de perfil e de negócios em esquemas, configure conectores de origem, monitore a ingestão de dados |
| **Desenvolvedor** | Implementação técnica e integrações | SDK para dispositivos móveis/web, APIs, arquitetura orientada por eventos | Integre SDKs, implemente eventos, crie pontos de acesso de ações personalizadas |
| **Profissional de marketing** | Design de jornadas e experiências personalizadas | Orquestração de jornadas, criação de conteúdo, direcionamento de público-alvo | Projete jornadas do cliente, crie e personalize mensagens, gerencie ofertas e componentes de decisão e defina públicos-alvo |

Cada função aborda uma fase específica da implementação do Adobe Journey Optimizer e garante um processo de implantação estruturado e eficiente.

## Ordem de implementação e Dependências de funções

Uma implementação bem-sucedida do Journey Optimizer normalmente segue essa sequência, o que reflete nas dependências entre as funções:

1. **Admin**: configura o ambiente\
   O admin estabelece a base configurando sandboxes, definindo controles de acesso e preparando as configurações de canal. Isso deve acontecer primeiro para permitir que outras equipes trabalhem.
   * Configure sandboxes de desenvolvimento, preparo e produção
   * Configure funções, permissões e o controle de acesso no nível do objeto (OLAC)
   * Definir as configurações de canal (email, SMS, push, push da Web, no aplicativo, Web, correspondência direta, cartões de conteúdo)
   * Delegue subdomínios e configure pools de IP
   * Configure listas de supressão e políticas de consentimento

2. **Engenheiro de dados**: cria a base de dados\
   Os engenheiros de dados criam a infraestrutura de dados que viabiliza a personalização, definindo como os dados do cliente fluem para e pelo sistema.
   * Crie namespaces de identidade para identificação do cliente
   * Crie esquemas XDM (perfil, eventos de experiência, relacionais)
   * Configure conjuntos de dados e habilite-os para o Perfil do cliente em tempo real
   * Configure a ingestão de dados (em lote e transmissão)
   * Crie atributos computados para cálculos complexos
   * Configure eventos e fontes de dados para jornadas

3. **Desenvolvedor**: lida com integrações técnicas\
   Os desenvolvedores conectam aplicativos ao Journey Optimizer integrando SDKs, enviando eventos e criando pontos de acesso de API. Essas implementações habilitam as jornadas a acionar e executar.
   * Integre o SDK para dispositivos móveis (iOS/Android) à configuração de notificações por push
   * Implementar o SDK da web para experiências na web e notificações por push da web
   * Envie eventos de aplicativos para acionar jornadas
   * Criar pontos de acesso de ações personalizadas para integrações de sistema externas
   * Monitorar a integridade e o desempenho da ação personalizada
   * Testar implementações com o Adobe Experience Platform Assurance

4. **Profissional de marketing**: projeta e executa as experiências do cliente\
   Os profissionais de marketing aproveitam todo o trabalho de base para criar jornadas, conteúdo e otimizar as experiências do cliente em todos os canais.
   * Crie públicos-alvo usando a segmentação, upload de CSV ou a composição de público-alvo
   * Projetar conteúdo personalizado com o Assistente de IA e modelos
   * Crie jornadas multicanal com acionadores de evento e público-alvo
   * Teste com fluxos de trabalho de aprovação antes do lançamento
   * Monitore o desempenho e otimize com base em insights de relatórios

**Observação:** embora esta sequência seja típica, algumas atividades podem ocorrer em paralelo. Por exemplo, os desenvolvedores podem trabalhar em integrações de aplicativos, enquanto os engenheiros de dados configuram esquemas.

## Introdução por função

Cada função começa com tarefas específicas condizentes com o foco de cada uma delas. A conclusão destas etapas iniciais garante uma integração e um alinhamento ininterruptos em relação ao processo geral de implementação:

### Para profissionais de marketing {#for-marketers}

Como Profissional de marketing ou Profissional de negócios, você cria jornadas do cliente para fornecer experiências pessoais e contextuais em todos os pontos de contato. Você trabalhará em uma interface unificada para implementar casos de uso completos do início ao fim.

**Principais recursos que você usará:**

* **Journey Orchestration**: crie um engajamento do cliente individualizado em tempo real, no qual cada pessoa se move no seu próprio ritmo e acionado por comportamento ou eventos entre canais. Use a atividade de ação unificada para todas as ações de canal, a atividade de decisão de conteúdo para integrar ofertas em jornadas e o Journey Agent para criar jornadas a partir de prompts de linguagem natural
* **Orquestração de campanhas**: projete e automatize em grande escala campanhas em lote complexas e com várias etapas com uma tela visual. Perfeito para campanhas iniciadas pela marca, como promoções sazonais, lançamentos de produtos e comunicações baseadas em conta. Aproveite a segmentação de várias entidades para criar públicos-alvo precisos conectando dados do cliente a entidades relacionadas (contas, compras, reservas). Usar envio de onda para entregar mensagens em lotes controlados
* **Designer de mensagens moderno**: crie e personalize mensagens de email e dispositivos móveis com uma interface de arrastar e soltar. Edite modelos prontos para uso para acelerar o tempo de lançamento no mercado
* **Gerenciamento de decisão**: crie e gerencie ofertas, regras de elegibilidade e outros componentes em uma biblioteca centralizada que possa ser incorporada a emails e pontos de contato do cliente. Usar o Decisioning para personalização por push e SMS
* **Gerenciamento de ativos**: acesse o Adobe Experience Manager Assets Essentials totalmente incorporado ao Journey Optimizer para um acesso simplificado aos ativos e à entrega
* **Definição de público-alvo**: crie públicos-alvo sob demanda com refinamento instantâneo usando consultas relacionais, com visibilidade de pré-envio para contagens precisas de público-alvo
* **Serviços de IA e aprendizado de máquina**: aproveite a otimização de tempo de envio e as pontuações de engajamento preditivo para direcionar clientes de alto valor e minimizar o risco de churn
* **Controle de Entrega**: use o horário silencioso (exclusões com base no tempo) e o gerenciamento de conflitos para respeitar as preferências do cliente e evitar comunicação excessiva

**Comece com:** use modelos de casos de uso e assistentes para criar e implantar facilmente novas jornadas de clientes. Use o Journey Agent para criar jornadas a partir de prompts de idioma natural.

[Introdução para Profissionais de marketing →](path/marketer.md)

### Para Engenheiros de dados {#for-data-engineers}

Como Arquiteto(a) ou Engenheiro(a) de dados, você configura e mantém os dados do perfil do cliente e outras fontes de dados que viabilizam as experiências orquestradas pelo Journey Optimizer.

**Principais responsabilidades:**

* **Dados do perfil do cliente**: modele dados do perfil do cliente e dados de negócios em esquemas para criar uma visualização unificada de 360 graus do cliente
* **Modelagem de dados relacionais**: em campanhas orquestradas, crie esquemas relacionais para habilitar a segmentação de várias entidades, conectando dados do cliente a entidades relacionadas, como contas, compras, assinaturas e reservas, para proporcionar uma criação flexível de público-alvo
* **Conectores de origem**: configure conectores de origem para ingerir dados da web, do CRM, de dados offline e de outras fontes na Adobe Experience Platform
* **Resolução de identidade**: configure namespaces de identidade para atualizar perfis continuamente e mover clientes para dentro e para fora de segmentos e jornadas em tempo real
* **Fontes de dados**: configure as fontes de dados para ouvir sinais externos em tempo real na jornada do cliente
* **Gerenciamento de perfil**: habilite conjuntos de dados no Perfil do cliente em tempo real para viabilizar experiências personalizadas
* **Qualidade dos dados**: monitore a ingestão de dados e garanta o fluxo adequado de todos eles para o Journey Optimizer

**Para começar:** modele seu primeiro esquema de perfil do cliente e configure um conector de origem para começar a ingerir dados.

[Introdução para Engenheiros de dados →](path/data-engineer.md)

### Para admins {#for-administrators}

Como admin, você configura o ambiente do Journey Optimizer para permitir que suas equipes trabalhem com eficiência e segurança.

**Principais responsabilidades:**

* **Sandboxes**: crie e gerencie sandboxes e particione dados e jornadas para diferentes grupos de usuários (desenvolvimento, teste, produção)
* **Gerenciamento de usuários**: configure grupos de usuários e permissões para controlar o acesso a diferentes funcionalidades
* **Configuração de canal**: configure canais de entrega e predefinições de mensagem para garantir uma identidade visual consistente nas mensagens e nos ativos entregues por meio do Journey Optimizer
* **Segurança e governança**: aplique o controle de acesso no nível do objeto (OLAC), configure políticas de consentimento e implemente políticas de governança de dados
* **Capacidade de entrega**: delegar subdomínios, migrar subdomínios para delegação personalizada quando necessário, criar pools de IP e gerenciar listas de supressão e listas de permissões
* **Configuração da jornada**: defina os elementos e as configurações da jornada para as equipes
* **Configuração do canal**: configurar notificações por push da Web, correspondência direta e exportação de mensagens (email/SMS) quando necessário

**Comece com:** configure sandboxes e permissões de usuário e, em seguida, defina as primeiras configurações de canal e predefinições de mensagem.

[Introdução para admins →](path/administrator.md)

### Para desenvolvedores {#for-developers}

Implemente integrações técnicas que conectam o Journey Optimizer aos seus aplicativos.

**Principais responsabilidades:**

* Integrar o SDK para dispositivos móveis da Adobe Experience Platform (iOS/Android)
* Implementar o SDK da web para experiências na web e notificações por push da web
* Configurar credenciais e certificados de notificação por push
* Envie eventos de aplicativos para acionar jornadas
* Criar pontos de acesso de API que o Journey Optimizer chama por meio de ações personalizadas
* Implementar experiências baseadas em código para superfícies da web, móveis e outras
* Implementações de teste e depuração com o Adobe Experience Platform Assurance
* Trabalhar com APIs do Journey Optimizer para acesso programático

**Para começar:** integre o SDK para dispositivos móveis ou o SDK da web e implemente o primeiro evento para acionar uma jornada.

[Introdução para desenvolvedores→](path/developer.md)

## Colaboração entre funções

As implementações bem-sucedidas do Journey Optimizer exigem colaboração entre todas as funções. As funções trabalham umas com as outras para fornecer experiências fluidas ao cliente:

>[!BEGINTABS]

>[!TAB Admins]

**Admins** habilitam todas as equipes gerenciando o acesso e as configurações. Eles trabalham com:

* **Engenheiros de dados**: concedem permissões para gerenciamento de dados, aprovam o acesso à sandbox e coordenam políticas de governança
* **Desenvolvedores**: fornecem credenciais de API, configuram ambientes de teste e aprovam configurações de canal
* **Profissionais de marketing**: atribuem permissões para jornadas/campanhas, configuram canais e dão suporte a ambientes de teste

>[!TAB Engenheiros de dados]

Os **Engenheiros de dados** fornecem a base de dados para todos. Eles trabalham com:

* **Admins**: solicitam permissões para gerenciamento de dados, coordenam políticas de governança e retenção
* **Desenvolvedores**: fornecem esquemas XDM e estruturas de evento, definem formatos de conteúdo de eventos e testam a ingestão de dados
* **Profissionais de marketing**: criam atributos computados para personalização e públicos-alvo e configuram esquemas relacionais

>[!TAB Desenvolvedores]

**Desenvolvedores** implementam integrações técnicas que viabilizam jornadas. Eles trabalham com:

* **Engenheiros de dados**: obtêm esquemas XDM e estruturas de evento, alinham os requisitos de coleta de dados e testam a entrega de eventos
* **Admins**: fornecem especificações de API, solicitam permissões e credenciais e coordenam a estratégia de teste
* **Profissionais de marketing**: compreendem acionadores de eventos, implementam o rastreamento, oferecem suporte a testes de jornada e solucionam problemas

>[!TAB Profissionais de marketing]

Os **profissionais de marketing** criam as experiências do cliente e fornecem comentários. Eles trabalham com:

* **Engenheiros de dados**: solicitam atributos computados, coordenam os requisitos de público-alvo e fornecem feedback sobre a qualidade dos dados
* **Desenvolvedores**: alinham acionadores de eventos, implementações de teste e o rastreamento de validação
* **Admins**: solicitam configurações de canal, confirmam o acesso a recursos e coordenam a habilitação

>[!ENDTABS]

**Prática recomendada:** realize reuniões multifuncionais regulares para alinhar as prioridades, compartilhar o progresso e solucionar bloqueios entre as equipes.

## Vídeo tutorial {#video}

Para saber mais sobre os principais recursos e personas do Journey Optimizer, assista ao vídeo de introdução. O vídeo aborda a interface do usuário e destaca os principais recursos com base em fluxos de trabalho específicos de cada função.

>[!VIDEO](https://video.tv.adobe.com/v/3424995?quality=12)

## Recursos adicionais

Para lições e atualizações mais detalhadas, confira os seguintes recursos:

>[!BEGINTABS]

>[!TAB Aprendizagem e documentação]

* [Vídeos tutoriais](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=pt-BR){target="_blank"} - Tutoriais em vídeo passo a passo para todas as funções
* [Biblioteca de casos de uso de jornadas](../building-journeys/jo-use-cases.md) - Exemplos práticos e padrões de implementação
* [IA e recursos inteligentes](ai-features.md) - Saiba mais sobre o Assistente de IA, a otimização de tempo de envio e a geração de conteúdo
* [Guia da Interface](user-interface.md) - Navegue pelo Journey Optimizer com eficiência

>[!TAB Permaneça atualizado(a)]

* [Notas de versão](../rn/release-notes.md) - Recursos, melhorias e correções mais recentes
* [Atualizações da documentação](../rn/documentation-updates.md) - Rastreie alterações recentes na documentação
* [Notificações do produto](../rn/releases.md#staying-informed) - Saiba como assinar alertas de email e no produto para atualizações do Journey Optimizer

>[!TAB Comunidade e suporte]

* [Comunidade da Experience League](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer?profile.language=pt){target="_blank"} - Conecte-se com outros usuários e especialistas
* [Fórum do produto](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer?profile.language=pt){target="_blank"} - Faça perguntas e compartilhe conhecimento

>[!ENDTABS]
