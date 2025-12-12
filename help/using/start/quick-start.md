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
source-git-commit: 5ff7987c00afda3263cb97654967c5b698f726c2
workflow-type: tm+mt
source-wordcount: '1177'
ht-degree: 20%

---


# Funções e responsabilidades

O Adobe Journey Optimizer permite que as marcas forneçam jornadas conectadas e contextualizadas ao cliente por todo o seu ciclo de vida. Ele permite que as equipes personalizem interações em escala e alinhem as expectativas do cliente às metas de negócios. Esta documentação explica as principais funções para o uso eficaz do Journey Optimizer, suas responsabilidades e como começar.

**Observação importante:** o Adobe Journey Optimizer define funções distintas com responsabilidades específicas. Uma única pessoa pode realizar várias funções ou todas as funções, dependendo da estrutura da organização.

## Guias de início rápido com base em funções

Para simplificar a implementação, o Adobe Journey Optimizer organiza tarefas em funções específicas com base na experiência. Cada função se concentra em tarefas essenciais necessárias para fornecer uma experiência fluida ao cliente.

| Função | Responsabilidades principais | Habilidades principais | Tarefas típicas |
|-------------------|----------------------------------|--------------------------------|-----------------------------------------------|
| **Admin** | Configuração do ambiente e gerenciamento de acesso | Configuração do sistema, gerenciamento de usuários, segurança | Configurar sandboxes, gerenciar permissões e definir configurações de canal |
| **Engenheiro de dados** | Base e arquitetura de dados | Modelagem de dados, esquemas XDM, qualidade dos dados | Crie esquemas e conjuntos de dados, configure a assimilação de dados e gerencie o ciclo de vida dos dados |
| **Desenvolvedor** | Implementação técnica e integrações | SDK para dispositivos móveis/Web, APIs, arquitetura orientada por eventos | Integrar SDKs, implementar eventos, criar endpoints de ação personalizados |
| **Profissional de marketing** | Design e execução da experiência do cliente | Jornada design, criação de conteúdo, análise de dados | Criar jornadas, criar conteúdo personalizado, otimizar campanhas |

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

Concentre-se em criar experiências personalizadas do cliente em todos os canais.

**Principais recursos que você usará:**

* Crie públicos e segmentos com vários métodos (definições de segmento, upload de CSV, composição de público)
* Projetar conteúdo com o AI Assistant para geração de texto e imagem
* Criar jornadas de clientes multicanal com o designer de arrastar e soltar
* Aproveite a otimização de tempo de envio e o gerenciamento de conflitos para maximizar o engajamento
* Testar o conteúdo e usar fluxos de trabalho de aprovação antes da publicação
* Monitore o desempenho com painéis de relatórios integrados

**Comece com:** crie uma jornada de boas-vindas simples ou uma campanha de recuperação de carrinho abandonada usando modelos pré-criados.

[Introdução como profissional de marketing →](path/marketer.md)

### Para engenheiros de dados {#for-data-engineers}

Estabeleça a base de dados que viabiliza experiências personalizadas.

**Principais responsabilidades:**

* Criar namespaces de identidade e configurar a resolução de identidade
* Criar esquemas XDM para dados de perfil e evento (padrão e relacional)
* Configurar conjuntos de dados e ativá-los para o Perfil do cliente em tempo real
* Configurar conectores de origem para assimilação de dados em lote e por transmissão
* Criar atributos computados para simplificar a segmentação
* Configurar eventos e fontes de dados para execução de jornada
* Gerencie a qualidade, a governança e o ciclo de vida dos dados

**Comece com:** Configure namespaces de identidade e crie seu primeiro esquema de perfil com os grupos de campos necessários.

[Introdução como engenheiro de dados →](path/data-engineer.md)

### Para administradores {#for-administrators}

Configure e gerencie o ambiente do Journey Optimizer para sua organização.

**Principais responsabilidades:**

* Criar e gerenciar sandboxes para desenvolvimento, teste e produção
* Configure funções e permissões usando funções prontas para uso ou personalizadas
* Aplicar OLAC (controle de acesso no nível do objeto) para proteger recursos
* Definir configurações de canal para email, SMS, push, no aplicativo, Web e cartões de conteúdo
* Delegar subdomínios e criar pools de IP para capacidade de entrega de email
* Gerenciar listas de supressão e listas de permissões
* Configurar políticas de consentimento e governança de dados (com o Healthcare/Privacy Shield)

**Comece com:** Configure sandboxes, configure funções e permissões básicas e, em seguida, trabalhe com sua equipe em configurações de canal.

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

As implementações bem-sucedidas do Journey Optimizer exigem colaboração em todas as funções:

* **Administradores** habilitam outras funções definindo sandboxes, permissões e configurações de canal
* **Os engenheiros de dados** fornecem a base de dados sobre a qual os desenvolvedores e profissionais de marketing se baseiam
* **Desenvolvedores** implementam as integrações técnicas que os profissionais de marketing usam para acionar jornadas
* **Os profissionais de marketing** fornecem feedback a todas as equipes sobre qualidade de dados, solicitações de recursos e experiência do usuário

**Prática recomendada:** realize reuniões multifuncionais regulares para se alinhar às prioridades, compartilhar progresso e endereçar bloqueadores entre equipes.

## Vídeo tutorial {#video}

Para saber mais sobre os principais recursos e personas do Journey Optimizer, assista ao vídeo de introdução. O vídeo aborda a interface do usuário e destaca os principais recursos com base em fluxos de trabalho específicos de cada função.

>[!VIDEO](https://video.tv.adobe.com/v/3430320?captions=por_br&quality=12)

## Recursos adicionais

Para lições e atualizações mais detalhadas, confira os seguintes recursos:

**Aprendizagem e Documentação:**

* [Vídeos tutoriais](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/overview){target="_blank"} - Tutoriais em vídeo passo a passo para todas as funções
* [Biblioteca de Casos de Uso do Jornada](../building-journeys/jo-use-cases.md) - Exemplos práticos e padrões de implementação
* [IA e recursos inteligentes](ai-features.md) - Saiba mais sobre o Assistente de IA, otimização de tempo de envio e geração de conteúdo
* [Guia da Interface do Usuário](user-interface.md) - Navegue pela Journey Optimizer com eficiência

**Permanecer atualizado:**

* [Notas de versão](../rn/release-notes.md) - Recursos, melhorias e correções mais recentes
* [Atualizações da documentação](../rn/documentation-updates.md) - Rastreie alterações recentes na documentação
* **Notificações de Produto** - Habilite alertas no [perfil do Adobe Experience Cloud](https://experience.adobe.com/preferences){target="_blank"} para receber notificações sobre novas versões, janelas de manutenção e anúncios importantes. Clique no ícone de perfil > Preferências > Notificações para configurar.

**Comunidade e suporte:**

* [Comunidade do Experience League](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer?profile.language=pt){target="_blank"} - Conecte-se com outros usuários e especialistas
* [Fórum de produtos](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer?profile.language=pt){target="_blank"} - Faça perguntas e compartilhe conhecimento
