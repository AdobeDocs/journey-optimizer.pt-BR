---
solution: Journey Optimizer
product: journey optimizer
title: Funções e responsabilidades do AJO
description: Saiba mais sobre as diferentes funções envolvidas no Adobe Journey Optimizer e suas responsabilidades
feature: Get Started
role: Admin, Data Engineer, Developer, User
level: Beginner
exl-id: 71ab7369-fd84-46eb-95d2-941bd887d565
redpen-status: PASS_||_2025-04-28_15-13-07
source-git-commit: d2cdafef6f2d69ea85d9d042c859a8b1e7654d7d
workflow-type: ht
source-wordcount: '634'
ht-degree: 100%

---


# Funções e responsabilidades do AJO

O Adobe Journey Optimizer (AJO) permite que as marcas forneçam jornadas conectadas e contextualizadas ao cliente por todo o seu ciclo de vida. Ele permite que as equipes personalizem interações em escala e alinhem as expectativas do cliente às metas de negócios. Esta documentação explica as principais funções para o uso eficaz do Journey Optimizer, suas responsabilidades e como começar.

**Observação importante:** o Adobe Journey Optimizer define funções distintas com responsabilidades específicas. Uma única pessoa pode realizar várias funções ou todas as funções, dependendo da estrutura da organização.

## Guias de início rápido com base em funções

Para simplificar a implementação, o AJO organiza tarefas em funções específicas com base na experiência. Cada função se concentra em tarefas essenciais necessárias para fornecer uma experiência fluida ao cliente.

| Função | Responsabilidades principais | Habilidades principais | Tarefas típicas |
|-------------------|----------------------------------|--------------------------------|-----------------------------------------------|
| **Admin** | Configuração do sistema e gerenciamento de permissões | Configuração do sistema, gerenciamento de usuários, segurança | Configurar sandboxes, gerenciar usuários e definir canais |
| **Engenheiro de dados** | Configurar estrutura de dados e fluxos | Modelagem de dados, design de esquema, integração de API | Configurar esquemas, gerenciar conjuntos de dados, configurar fontes de dados |
| **Desenvolvedor** | Integrações e personalizações técnicas | Desenvolvimento para dispositivos móveis, implementação de API, codificação | Integrar aplicativos móveis, implementar APIs e criar ações personalizadas |
| **Profissional de marketing** | Projetar e executar jornadas do cliente | Estratégia de marketing, criação de conteúdo, design de jornada | Criar campanhas, projetar jornadas e analisar relatórios |

Cada função aborda uma fase específica da implementação do AJO e garante um processo de implantação estruturado e eficiente.

## Ordem de implementação e Dependências de funções

Uma implementação bem-sucedida do Journey Optimizer normalmente segue essa sequência, o que reflete nas dependências entre as funções:

1. **Admin**: configura o ambiente\
   O administrador estabelece a base técnica para o sistema e garante o acesso e a configuração adequados a todos os usuários.
   * Configurar sandboxes e permissões
   * Configurar o acesso do usuário
   * Configurar canais de mensagens e configurações técnicas

2. **Engenheiro de dados**: cria a base de dados\
   Os engenheiros de dados definem a estrutura e o fluxo de dados, que são essenciais para experiências personalizadas.
   * Projetar e implementar esquemas
   * Configurar namespaces de identidade
   * Configurar ingestão de dados
   * Criar perfis de teste

3. **Desenvolvedor**: lida com integrações técnicas\
   Os desenvolvedores habilitam a interação do AJO com aplicativos móveis, sites e sistemas externos ao implementar integrações técnicas. As notificações por push, por exemplo, dependem de configurações determinadas por desenvolvedores.
   * Integrar aplicativos móveis para notificações por push
   * Implementar SDKs da web
   * Desenvolver integrações personalizadas com APIs
   * Criar ações personalizadas para sistemas de terceiros

4. **Profissional de marketing**: cria e inicia jornadas\
   Os profissionais de marketing usam a base estabelecida por outras funções para projetar e implantar experiências do cliente. Eles se concentram na segmentação de público-alvo, no conteúdo personalizado e na otimização de jornadas.
   * Projetar segmentos de público-alvo
   * Criar conteúdo personalizado
   * Criar e testar jornadas
   * Analisar o desempenho e otimizar

**Observação:** embora esta sequência seja típica, algumas atividades podem ocorrer em paralelo. Por exemplo, os desenvolvedores podem trabalhar em integrações de aplicativos, enquanto os engenheiros de dados configuram esquemas.

## Introdução por função

Cada função começa com tarefas específicas condizentes com o foco de cada uma delas. A conclusão destas etapas iniciais garante uma integração e um alinhamento ininterruptos em relação ao processo geral de implementação:

1. **Para profissionais de marketing**: concentre-se na criação de jornadas, no design de mensagens e na execução de campanhas.\
   Exemplo: comece criando uma campanha de email de boas-vindas para novos clientes.

2. **Para engenheiros de dados**: estabeleça a base dos dados, configure esquemas e integre fontes de dados.\
   Exemplo: configure um esquema para rastrear o histórico de compras do cliente a fim de fornecer recomendações personalizadas.

3. **Para administradores**: crie ambientes, gerencie permissões e configure canais de mensagens.\
   Exemplo: configure ambientes de sandbox para testar diferentes estratégias de mensagens.

4. **Para desenvolvedores**: integre aplicativos móveis, implemente APIs e crie integrações personalizadas.\
   Exemplo: use a API do AJO para acionar notificações por push com base nas ações dos clientes no aplicativo móvel.

Clique na sua função abaixo para acessar orientações específicas de acordo com as suas responsabilidades:

* [Introdução para profissionais de marketing](path/marketer.md)
* [Introdução para engenheiros de dados](path/data-engineer.md)
* [Introdução para administradores](path/administrator.md)

## Vídeo tutorial {#video}

Para saber mais sobre os principais recursos e personas do Journey Optimizer, assista ao vídeo de introdução. O vídeo aborda a interface do usuário e destaca os principais recursos com base em fluxos de trabalho específicos de cada função.

>[!VIDEO](https://video.tv.adobe.com/v/3430320?quality=12&captions=por_br)

## Recursos adicionais

Para lições e atualizações mais detalhadas, confira os seguintes recursos:
* [Notas de versão](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/whats-new/release-notes)
* [Vídeos tutoriais](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/overview)