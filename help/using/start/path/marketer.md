---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer — Introdução para profissionais de marketing
description: Como profissional de jornadas, saiba mais sobre como trabalhar com o Journey Optimizer
level: Beginner
feature: Get Started
Role: User
exl-id: 34304142-3ee8-4081-94b9-e914968c75ba
source-git-commit: 6fbb9f3d47f4299b35214be4966aafb8151183a2
workflow-type: tm+mt
source-wordcount: '1122'
ht-degree: 6%

---

# Introdução para profissionais de marketing {#get-started-marketers}

Como **profissional de marketing** ou **profissional de jornadas**, você é responsável por criar ofertas, jornadas e conteúdo. Você pode começar a trabalhar com o [!DNL Adobe Journey Optimizer] assim que o [Administrador do sistema](administrator.md) e o [Engenheiro de dados](data-engineer.md) concederem acesso e prepararem seu ambiente.

## Introdução ao essentials

O Journey Optimizer permite criar experiências personalizadas e conectadas do cliente por email, SMS, push, no aplicativo, Web, cartões de conteúdo e muito mais. Trabalhe com seus [Administradores](administrator.md) para obter acesso e com os [Engenheiros de Dados](data-engineer.md) para configurar públicos e dados.

Siga estas etapas principais para começar a criar experiências:

1. **Criar públicos-alvo**. Crie públicos-alvo por meio de definições de segmento, carregue arquivos CSV ou use a composição de público-alvo. A Journey Optimizer oferece várias maneiras de direcionar os clientes certos. Saiba mais sobre [públicos-alvo](../../audience/about-audiences.md) e [criação de definições de segmento](../../audience/creating-a-segment-definition.md).

1. **Criar conteúdo**. Crie mensagens atraentes em todos os canais, incluindo email, SMS, push, no aplicativo, Web e cartões de conteúdo:
   * Use o **Assistente de IA** para gerar conteúdo de email, linhas de assunto e imagens com base nas diretrizes da sua marca. [Saiba mais sobre a geração de conteúdo de IA](../../content-management/gs-generative.md)
   * **Personalize mensagens** com dados do cliente, conteúdo dinâmico e lógica condicional. [Saiba mais sobre personalização](../../personalization/personalize.md)
   * **Repita em dados contextuais** para exibir listas dinâmicas de eventos, ações personalizadas e pesquisas de conjuntos de dados. [Saiba mais sobre a iteração de dados contextuais](../../personalization/iterate-contextual-data.md)
   * Crie **modelos de conteúdo** e **fragmentos** reutilizáveis para manter a consistência da marca. [Trabalhar com modelos](../../content-management/content-templates.md)
   * Forneça **cartões de conteúdo** persistentes e não intrusivos em aplicativos móveis e sites. Diferentemente das notificações por push, os cartões de conteúdo permanecem visíveis até serem descartados. [Saiba mais sobre cartões de conteúdo](../../content-card/create-content-card.md)
   * Gerenciar ativos com a integração do **Adobe Experience Manager Assets**. [Saiba mais sobre ativos](../../integrations/assets.md)

   ![](../assets/perso_ee2.png)

1. **Adicionar ofertas e decisões**. Forneça a melhor oferta para cada cliente na hora certa usando a decisão baseada em IA. Saiba mais sobre a [Gestão de decisões](../../offers/get-started/starting-offer-decisioning.md) e a [Experience Decisioning](../../experience-decisioning/gs-experience-decisioning.md).

   ![](../assets/offers-e2e-offers-displayed.png)

1. **Testar e validar**. Visualizar e testar o conteúdo antes de enviar:
   * Use **perfis de teste** para visualizar a personalização e verificar a renderização entre dispositivos
   * Testar com **dados de amostra** de arquivos CSV/JSON
   * Visualizar **renderização de email** entre clientes de email populares
   * Execute **testes A/B e experimentos** para otimizar as variações de conteúdo. Use a experimentação de bandit multi-armed para alocar automaticamente mais tráfego a variações vencedoras em tempo real. [Saiba mais sobre experimentação](../../content-management/content-experiment.md)
   * Configure **workflows de aprovação** para campanhas e jornadas (requer licença adicional). [Saiba mais sobre aprovações](../../test-approve/gs-approval.md)

   Saiba como [testar e validar mensagens](../../content-management/preview-test.md).

1. **Criar jornadas do cliente**. Crie experiências personalizadas em tempo real usando a tela de jornada:

   * Acione jornadas com **eventos** (ações do cliente) ou **públicos-alvo** (envios em lote)
   * Adicione **condições** para criar caminhos personalizados com base nos dados do cliente
   * Use **atividades de espera** para criar um tempo perfeito entre mensagens
   * Enviar mensagens em **vários canais** em uma jornada
   * Aplicar **teste A/B** e otimizar os tempos de envio para maximizar o envolvimento
   * Use a **pesquisa de conjunto de dados** para enriquecer jornadas com dados em tempo real do Adobe Experience Platform. [Saiba mais sobre a pesquisa de conjunto de dados](../../building-journeys/dataset-lookup.md)
   * Use **identificadores complementares** para permitir que o mesmo perfil entre em várias instâncias do jornada (por exemplo, pedidos ou reservas diferentes). [Saiba mais sobre identificadores complementares](../../building-journeys/supplemental-identifier.md)

   ![](../assets/journey-design.png)

   Saiba como [projetar e executar jornadas](../../building-journeys/journey-gs.md) e explorar [casos de uso do jornada](../../building-journeys/jo-use-cases.md). Entenda os [critérios de entrada/saída](../../building-journeys/entry-exit-criteria-guide.md) para controlar o fluxo de perfil.

1. **Monitorar e otimizar**. Acompanhe o desempenho e melhore os resultados ao longo do tempo:
   * Monitorar o desempenho da **jornada em tempo real** e identificar gargalos
   * Analisar as taxas de **entrega de mensagens** e as métricas de envolvimento
   * Use os **painéis de relatórios** com a integração do Customer Journey Analytics
   * Rastrear a **conversão** e o impacto nos negócios
   * Gerencie a **frequência e a priorização de mensagens** com regras de gerenciamento de conflitos para evitar comunicação excessiva. [Saiba mais sobre o gerenciamento de conflitos](../../conflict-prioritization/gs-conflict-prioritization.md)

   Saiba como [monitorar o desempenho](../../reports/report-gs-cja.md).

## Práticas recomendadas para o sucesso

### Criação de conteúdo

* **Comece com modelos**: use modelos pré-criados e fragmentos de conteúdo para acelerar a criação e manter a consistência
* **Teste com antecedência, teste com frequência**: sempre visualize o conteúdo entre dispositivos e use perfis de teste para validar a personalização
* **Aproveite a IA com sabedoria**: use o AI Assistant para rascunhos e variações iniciais, mas sempre revise e refine para voz da sua marca
* **Mantenha a simplicidade**: mensagens claras e concisas com chamadas para ação fortes têm melhor desempenho do que layouts complexos

### Jornada design

* **Definir metas claras**: estabelecer métricas de sucesso antes de criar sua jornada
* **Mapear a experiência do cliente**: visualizar toda a jornada antes da implementação
* **Usar atividades de espera estrategicamente**: dê aos clientes tempo para se engajarem antes de enviar acompanhamentos
* **Planejar estratégias de saída**: defina quando e por que os clientes devem sair da jornada
* **Teste no modo de rascunho**: valide a lógica de jornada com simulação antes de ativar

[Conheça as práticas recomendadas do jornada](../../building-journeys/entry-exit-criteria-guide.md#best-practices)

### Direcionamento de público

* **Segmente cuidadosamente**: crie segmentos de público-alvo específicos e acionáveis com base em critérios claros
* **Atualizar regularmente**: certifique-se de que os públicos-alvo permaneçam atualizados, definindo cronogramas de avaliação apropriados
* **Tamanho e precisão de equilíbrio**: públicos-alvo grandes o suficiente para significância estatística, mas específicos o suficiente para relevância
* **Usar atributos de enriquecimento**: use atributos computados e dados de enriquecimento para uma personalização mais profunda

### Gerenciamento de frequência

* **Respeitar as preferências do cliente**: respeitar as opções de não participação e de comunicação
* **Definir limites de frequência**: use conjuntos de regras para evitar a fadiga da mensagem entre canais
* **Coordenar campanhas**: use o gerenciamento de conflitos para garantir que os clientes recebam a mensagem certa na hora certa
* **Monitorar engajamento**: observe sinais de fadiga (taxas de abertura decrescentes, aumento de cancelamentos de assinatura)

[Saiba mais sobre limite de frequência](../../conflict-prioritization/channel-capping.md)

## Explorar casos de uso

Aprenda com exemplos práticos que demonstram os recursos do Journey Optimizer:

**Casos de uso populares:**

* **Série de boas-vindas**: integre novos clientes com jornadas personalizadas de várias etapas. [Exibir caso de uso](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding)
* **Recuperação do carrinho abandonado**: envolva novamente os clientes que deixaram itens em seus carrinhos. [Exibir caso de uso](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart)
* **Campanhas de reengajamento**: conquiste clientes inativos com ofertas direcionadas. [Exibir caso de uso](https://experienceleague.adobe.com/pt-br/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma)
* **Campanhas de aniversário**: envie mensagens de aniversário personalizadas com ofertas especiais
* **Recomendações de produto**: sugerir produtos relevantes com base no histórico de navegação e compra
* **Mensagens orientadas por eventos**: responda às ações do cliente em tempo real

**padrões de Jornada:**

* [Enviar mensagens aos assinantes](../../building-journeys/message-to-subscribers-uc.md): listas de assinaturas de destino com conteúdo personalizado
* [Mensagens multicanais](../../building-journeys/journeys-uc.md): combinar email e push com eventos de reação
* [Emails somente para dias da semana](../../building-journeys/weekday-email-uc.md): agendar comunicações usando condições baseadas em tempo

Procure a [biblioteca de casos de uso do jornada](../../building-journeys/jo-use-cases.md) completa para obter mais padrões e implementações.

## Colaborar com outras funções

Seu trabalho de marketing se conecta com outras equipes:

* **Trabalhe com [Engenheiros de dados](data-engineer.md)**: solicite novos atributos computados, forneça feedback sobre a qualidade do público e coordene sobre os requisitos de dados
* **Trabalhar com [Desenvolvedores](developer.md)**: alinhar em disparadores de eventos, testar implementações móveis e validar o rastreamento
* **Trabalhar com [Administradores](administrator.md)**: solicitar configurações de canal, relatar problemas com permissões e coordenar a habilitação de novos recursos

## Permanecer atualizado

Acompanhe os recursos mais recentes do Journey Optimizer e de marketing:

* **[Notas de versão](../../rn/release-notes.md)**: Revise novos recursos, atualizações de canal e melhorias lançadas a cada mês
* **[Atualizações da documentação](../../rn/documentation-updates.md)**: controle alterações recentes, incluindo novos casos de uso, práticas recomendadas e documentação de recursos
* **Notificações do Produto**: Habilite as notificações no seu [perfil do Adobe Experience Cloud](https://experience.adobe.com/preferences){target="_blank"} para receber alertas sobre:
   * Novos canais e recursos disponíveis para você
   * Próximos lançamentos de recursos e programas beta
   * Práticas recomendadas e oportunidades de treinamento
   * Anúncios importantes que afetam suas campanhas

  Para habilitar notificações, clique no ícone de perfil na parte superior direita do Adobe Experience Cloud, vá para **Preferências > Notificações** e configure suas preferências de notificação do Journey Optimizer.

## Próximas etapas

1. **Comece pequeno**: crie uma jornada de boas-vindas simples ou uma campanha de mensagem única para conhecer a plataforma
2. **Aproveite a IA**: use o Assistente de IA para fazer perguntas e acelerar a criação de conteúdo
3. **Ingressar na comunidade**: conectar-se a outros usuários do Journey Optimizer na [Comunidade do Experience League](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer?profile.language=pt){target="_blank"}
4. **Explorar tutoriais**: Assista aos vídeos passo a passo no [Experience League](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/overview){target="_blank"}
