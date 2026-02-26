---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer — Introdução para profissionais de marketing
description: Como profissional de jornadas, saiba mais sobre como trabalhar com o Journey Optimizer
level: Beginner
feature: Get Started
Role: User
exl-id: 34304142-3ee8-4081-94b9-e914968c75ba
source-git-commit: fd10a600cb54b8c35e2d195be7379b0dd120b6a7
workflow-type: tm+mt
source-wordcount: '1591'
ht-degree: 89%

---

# Introdução para profissionais de marketing {#get-started-marketers}

Como **Profissional de marketing** ou **Profissional de negócios**, você cria jornadas do cliente para fornecer experiências pessoais e contextuais aos clientes. Crie e gerencie todos os vários componentes dessas jornadas personalizadas, incluindo mensagens de email e push, ofertas e componentes de decisão para personalizar o conteúdo de mensagens de forma inteligente. O Journey Optimizer fornece uma experiência do usuário unificada, onde é possível implementar casos de uso completos em um único local. Você pode começar a trabalhar com o [!DNL Adobe Journey Optimizer] assim que o(a) [admin de sistema](administrator.md) e o(a) [engenheiro(a) de dados](data-engineer.md) concederem acesso e prepararem seu ambiente.

## Introdução às noções básicas

O Journey Optimizer reúne insights do cliente em tempo real, orquestração omnicanal moderna e decisões inteligentes em um único aplicativo. Crie experiências personalizadas e conectadas do cliente por email, SMS, push, push da Web, no aplicativo, Web, correspondência direta, cartões de conteúdo e muito mais.

O Journey Optimizer oferece duas abordagens eficientes de orquestração:

* **Jornadas**: engajamento individualizado em tempo real no qual cada cliente avança no seu próprio ritmo, acionado por comportamento ou eventos
* **Campanhas orquestradas**: campanhas em lote complexas, com várias etapas e em grande escala, onde os públicos-alvo progridem juntos por meio de fluxos de trabalho. Ideais para campanhas iniciadas pela marca, como promoções sazonais, lançamentos de produtos ou comunicações baseadas em contas

Trabalhe com [admins](administrator.md) para obter acesso e com [engenheiros(as) de dados](data-engineer.md) na configuração de públicos-alvo, dados e esquemas relacionais para segmentação avançada.

Siga estas etapas principais para começar a criar experiências:

1. **Criar públicos-alvo**. Crie públicos-alvo por meio de definições de segmento, carregue arquivos CSV ou use a composição de público-alvo. O Journey Optimizer oferece várias maneiras de direcionar os clientes certos. Saiba mais sobre [públicos-alvo](../../audience/about-audiences.md) e a [criação de definições de segmento](../../audience/creating-a-segment-definition.md).

1. **Criar conteúdo**.  Crie mensagens atraentes em todos os canais, incluindo email, SMS, push, push da Web, no aplicativo, Web, correspondência direta e cartões de conteúdo:
   * Use o **Assistente de IA** para gerar conteúdo de email, linhas de assunto e imagens com base nas diretrizes da sua marca. [Saiba mais sobre a geração de conteúdo de IA](../../content-management/gs-generative.md)
   * **Personalize mensagens** com dados do cliente, conteúdo dinâmico e lógica condicional. [Saiba mais sobre personalização](../../personalization/personalize.md)
   * **Itere sobre dados contextuais** para exibir listas dinâmicas de eventos, ações personalizadas e pesquisas de conjuntos de dados. [Saiba mais sobre a iteração de dados contextuais](../../personalization/iterate-contextual-data.md)
   * Crie **modelos de conteúdo** e **fragmentos** reutilizáveis para manter a consistência da marca. [Trabalhar com modelos](../../content-management/content-templates.md)
   * Forneça **cartões de conteúdo** persistentes e não intrusivos em aplicativos móveis e sites. Diferentemente das notificações por push, os cartões de conteúdo permanecem visíveis até serem descartados. [Saiba mais sobre cartões de conteúdo](../../content-card/create-content-card.md)
   * Gerenciar ativos com a integração do **Adobe Experience Manager Assets**. [Saiba mais sobre ativos](../../integrations/assets.md)

   ![](../assets/perso_ee2.png)

1. **Adicionar ofertas e decisões**. Forneça a melhor oferta para cada cliente na hora certa com a tomada de decisões viabilizada por IA. Use o Decisioning para personalizar push, SMS e outros canais. Saiba mais sobre a [Gestão de decisões](../../offers/get-started/starting-offer-decisioning.md) e a [Escolha de experiências](../../experience-decisioning/gs-experience-decisioning.md).

   ![](../assets/offers-e2e-offers-displayed.png)

1. **Testar e validar**. Visualize e teste o conteúdo antes de enviar:
   * Use **perfis de teste** para visualizar a personalização e verificar a renderização nos dispositivos
   * Teste com **dados de amostra** de arquivos CSV/JSON
   * Visualize a **renderização do email** nos clientes de email populares
   * Execute **testes A/B e experimentos** para otimizar as variações de conteúdo. Use a experimentação de multi-armed bandit para alocar automaticamente mais tráfego a variações vencedoras em tempo real. [Saiba mais sobre experimentação](../../content-management/content-experiment.md)
   * Configure **fluxos de trabalho de aprovação** para campanhas e jornadas (requer licença adicional). [Saiba mais sobre aprovações](../../test-approve/gs-approval.md)

   Saiba mais sobre como [testar e validar mensagens](../../content-management/preview-test.md).

1. **Criar jornadas do cliente**. Crie experiências personalizadas em tempo real usando a tela de jornada. Use o **Journey Agent** no AI Assistant para criar jornadas a partir de prompts de linguagem natural. [Saiba mais sobre o Journey Agent](../ai-features.md#journey-agent)

   * Acione jornadas com **eventos** (ações do cliente) ou **públicos-alvo** (envios em lote)
   * Adicione **condições** para criar caminhos personalizados com base nos dados do cliente
   * Use a **Atividade de ação** unificada para todas as ações de canal (email, push, SMS e muito mais). [Saiba mais sobre a atividade de Ação](../../building-journeys/journey-action.md)
   * Adicione a **Atividade de decisão de conteúdo** para integrar ofertas personalizadas diretamente ao seu fluxo de jornada. [Saiba mais sobre a atividade de decisão de conteúdo](../../building-journeys/content-decision.md)
   * Use **atividades de espera** para criar um intervalo perfeito entre mensagens
   * Enviar mensagens em **vários canais** em uma jornada
   * Use o **envio de onda** para entregar mensagens em lotes controlados (Disponibilidade limitada para jornada)
   * Aplicar o **teste A/B** e otimizar os tempos de envio para maximizar o engajamento
   * Use a **pesquisa de conjunto de dados** para enriquecer jornadas com dados em tempo real da Adobe Experience Platform. [Saiba mais sobre a pesquisa de conjunto de dados](../../building-journeys/dataset-lookup.md)
   * Use **identificadores complementares** para permitir que o mesmo perfil entre em várias instâncias da jornada (por exemplo, pedidos ou reservas diferentes). [Saiba mais sobre identificadores complementares](../../building-journeys/supplemental-identifier.md)

   ![](../assets/journey-design.png)

   Saiba como [projetar e executar jornadas](../../building-journeys/journey-gs.md) e explorar [casos de uso de jornadas](../../building-journeys/jo-use-cases.md). Entenda os [critérios de entrada/saída](../../building-journeys/entry-exit-criteria-guide.md) para controlar o fluxo do perfil.

1. **Iniciar campanhas orquestradas**. Projete campanhas em lote complexas e com várias etapas em grande escala com uma tela visual:

   * Crie **públicos-alvo sob demanda** instantaneamente usando consultas relacionais para conectar dados do cliente com contas, compras, assinaturas e outras entidades
   * Crie uma **segmentação de várias entidades** para direcionamento preciso (por exemplo, &quot;clientes com assinaturas que expiram em 30 dias&quot; ou &quot;contas com compras recentes de alto valor&quot;)
   * Obtenha a **visibilidade de pré-envio** com contagens precisas de público-alvo antes de iniciar
   * Crie **fluxos de trabalho de várias etapas** para promoções sazonais, lançamentos de produtos, ofertas de fidelidade ou account-based marketing
   * Programar campanhas para execução imediata, em horários específicos ou em agendamentos recorrentes (diariamente, semanalmente, mensalmente)
   * Processar públicos-alvo no **modo de lote**, onde todos os perfis avançam juntos pelo fluxo de trabalho
   * Use o **envio de onda** para entregar mensagens em lotes controlados para melhorar a capacidade de entrega e o controle de carga

   Saiba como [começar a usar campanhas orquestradas](../../orchestrated/gs-orchestrated-campaigns.md) e entenda quando [usar campanhas ou jornadas](../../orchestrated/orchestrated-campaigns-faq.md).

1. **Monitorar e otimizar**. Acompanhe o desempenho e melhore os resultados ao longo do tempo:
   * Monitore o desempenho da **jornada em tempo real** e identifique gargalos
   * Analise as taxas de **entrega de mensagens** e as métricas de engajamento
   * Use os **painéis de relatórios** com a integração do Customer Journey Analytics
   * Rastreie a **conversão** e o impacto nos negócios
   * Gerencie a **frequência e a priorização de mensagens** com regras de gerenciamento de conflitos para evitar comunicação excessiva
   * Use **horas de silêncio** (exclusões baseadas em tempo) para evitar o envio durante períodos específicos. [Saiba mais sobre o gerenciamento de conflitos](../../conflict-prioritization/gs-conflict-prioritization.md) e [horas de silêncio](../../conflict-prioritization/quiet-hours.md)

   Saiba como [monitorar o desempenho](../../reports/report-gs-cja.md).

## Práticas recomendadas para obter sucesso

### Criação de conteúdo

* **Comece com modelos**: use modelos pré-criados e fragmentos de conteúdo para acelerar a criação e manter a consistência
* **Teste com antecedência, teste com frequência**: sempre visualize o conteúdo nos dispositivos e use perfis de teste para validar a personalização
* **Aproveite a IA com sabedoria**: use o Assistente de IA para criar rascunhos e variações iniciais, mas sempre revise e refine de acordo com a voz da marca
* **Mantenha a simplicidade**: mensagens claras e concisas com chamadas para ação fortes têm melhor desempenho do que layouts complexos

### Design da jornada

* **Defina metas claras**: estabeleça métricas de sucesso antes de criar a jornada
* **Mapeie a experiência do cliente**: visualize toda a jornada antes da implementação
* **Use atividades de espera estrategicamente**: dê aos clientes tempo para engajar antes de enviar novas mensagens
* **Planejar estratégias de saída**: defina quando e por que os clientes devem sair da jornada
* **Teste no modo de rascunho**: valide a lógica da jornada com uma execução de teste antes de ativar

[Saiba mais sobre as práticas recomendadas para jornadas](../../building-journeys/entry-exit-criteria-guide.md#best-practices)

### Orquestração de campanha

* **Escolha a abordagem correta**: [compare os tipos de jornada](../../building-journeys/journey.md#journey-types) para experiências acionadas por comportamento em tempo real ou os [tipos de campanha](../../campaigns/get-started-with-campaigns.md#campaign-types) para campanhas em lote agendadas
* **Defina objetivos claros da campanha**: estabeleça metas antes de criar fluxos de trabalho de várias etapas
* **Inicie com públicos-alvo piloto**: valide as contagens e a lógica de segmentação antes de dimensionar
* **Aproveite os dados relacionais**: use a segmentação de várias entidades e conecte os dados do cliente a contas, compras e assinaturas para um direcionamento preciso
* **Mantenha a segmentação simples**: otimize o desempenho e a transparência com regras claras e sustentáveis
* **Use uma nomenclatura consistente**: facilite o gerenciamento de campanhas com convenções de nomenclatura claras

### Direcionamento de público-alvo

* **Segmente com cuidado**: crie segmentos de público-alvo específicos e acionáveis com base em critérios claros
* **Atualize regularmente**: certifique-se de que os públicos-alvo permaneçam atualizados, definindo cronogramas de avaliação apropriados
* **Equilibre tamanho e precisão**: direcione públicos-alvo grandes o suficiente para possuir significância estatística, mas com a especificidade necessária para ter relevância
* **Use atributos de enriquecimento**: use atributos computados e dados de enriquecimento para uma personalização mais profunda

### Gerenciamento de frequência

* **Respeite as preferências do cliente**: respeite as recusas e as preferências de comunicação
* **Defina limites de frequência**: use conjuntos de regras para evitar a fadiga com mensagens nos canais
* **Coordenação de campanhas**: use o gerenciamento de conflitos para garantir que os clientes recebam a mensagem certa na hora certa
* **Monitore o engajamento**: observe sinais de fadiga (taxas de abertura em queda, aumento de cancelamentos de assinatura)

[Saiba mais sobre o limite de frequência](../../conflict-prioritization/channel-capping.md)

## Explore casos de uso

Aprenda com exemplos práticos que demonstram os recursos do Journey Optimizer:

**Casos de uso de jornadas** (tempo real, um para um):

* **Série de boas-vindas**: integre novos clientes com jornadas personalizadas de várias etapas. [Exibir caso de uso](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding)
* **Recuperação do carrinho abandonado**: engaje novamente os clientes que deixaram itens no carrinho. [Exibir caso de uso](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart)
* **Mensagens orientadas por eventos**: responda às ações do cliente em tempo real
* **Campanhas de aniversário**: envie mensagens de aniversário personalizadas acionadas por datas de perfil
* **Recomendações de produto**: sugira produtos relevantes com base no histórico de navegação e compras

**Casos de uso de campanha orquestrada** (em lote, um para muitos):

* **Promoções sazonais**: lance campanhas coordenadas pelos segmentos de clientes (por exemplo: vendas de fim de ano, volta às aulas)
* **Lançamentos de produtos**: anuncie novos produtos a públicos-alvo direcionados com mensagens sequenciadas
* **Ofertas do programa de fidelidade**: recompense clientes de alto valor com ofertas por níveis baseadas no histórico de compras
* **Account-based marketing**: direcione contas com características específicas e contatos relacionados
* **Renovações de assinatura**: alcance clientes com assinaturas que vencem em breve usando consultas de várias entidades
* **Campanhas de reengajamento**: conquiste clientes inativos com ofertas direcionadas no modo de lote. [Exibir caso de uso](https://experienceleague.adobe.com/pt-br/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma)

**Padrões da jornada:**

* [Enviar mensagens para assinantes](../../building-journeys/message-to-subscribers-uc.md): direcione listas de assinatura com conteúdo personalizado
* [Mensagens multicanais](../../building-journeys/journeys-uc.md): combine email e push com eventos de reação
* [Emails somente para dias da semana](../../building-journeys/weekday-email-uc.md): agende comunicações usando condições baseadas em tempo

Navegue pela [biblioteca de casos de uso de jornadas](../../building-journeys/jo-use-cases.md) completa e saiba mais sobre [campanhas orquestradas](../../orchestrated/gs-orchestrated-campaigns.md).

## Colaborar entre funções

Seu trabalho de marketing se conecta com outras equipes:

>[!BEGINTABS]

>[!TAB Trabalhar com Engenheiros de dados]

Colabore com os [Engenheiros de dados](data-engineer.md) nas configurações de dados e público-alvo:

* Solicite novos atributos computados para personalização e segmentação
* Coordene esquemas relacionais para campanhas orquestradas
* Forneça feedback sobre a qualidade do público-alvo e a precisão dos dados
* Alinhe os requisitos de dados de várias entidades para segmentação avançada

>[!TAB Trabalhar com desenvolvedores]

Colabore com [desenvolvedores](developer.md) no rastreamento e na implementação de eventos:

* Alinhe quais interações do usuário devem acionar eventos de jornada
* Teste implementações para dispositivos móveis e para a web antes do lançamento
* Valide o rastreamento do desempenho do conteúdo e do engajamento do usuário
* Solucione problemas com a entrega ou personalização de mensagens

>[!TAB Trabalhar com admins]

Colabore com [Admins](administrator.md) no acesso e nas configurações:

* Solicite configurações de canal para campanhas e jornadas
* Confirme o acesso à licença para campanhas orquestradas e outros recursos
* Relatar problemas com permissões ou acesso
* Coordene a habilitação de novos recursos e os ambientes de teste

>[!ENDTABS]

## Próximas etapas

1. **Comece aos poucos**: crie uma jornada de boas-vindas simples ou uma campanha de mensagem única para conhecer a plataforma
2. **Aproveite a IA**: use o Assistente de IA para fazer perguntas e acelerar a criação de conteúdo
3. **Ingresse na comunidade**: conecte-se a outros usuários do Journey Optimizer na [Comunidade da Experience League](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"}
4. **Explore tutoriais**: assista aos vídeos passo a passo na [Experience League](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=pt-BR){target="_blank"}
