---
solution: Journey Optimizer
product: journey optimizer
title: Recursos inteligentes e de IA
description: Saiba como a IA e o aprendizado de máquina aprimoram os recursos do Adobe Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: 26f9228bacee5865cbc368cf2e3db02370d43a4b
workflow-type: tm+mt
source-wordcount: '1567'
ht-degree: 3%

---

# Recursos inteligentes e de IA {#ai-features}

A Adobe Journey Optimizer aproveita o poder da inteligência artificial e do aprendizado de máquina para ajudá-lo a criar, otimizar e fornecer experiências excepcionais para o cliente. Desde a geração de conteúdo personalizado até a previsão de tempos de envio ideais, os recursos de IA simplificam o fluxo de trabalho e maximizam o impacto.

## Assistente de IA {#ai-assistant}

O Assistente de IA é seu guia conversacional do Adobe Journey Optimizer. Use-o para obter respostas instantâneas sobre os recursos do produto, insights operacionais sobre suas jornadas e ajuda para navegar na plataforma.

### Acessar o Assistente de IA

Clique no ícone do Assistente de IA na barra superior para abrir o painel do assistente no lado direito da tela.

![](assets/do-not-localize/ai-assistant-open.png)

>[!IMPORTANT]
>
>Você deve concordar com as [Diretrizes de usuário da IA gerativa da Adobe Experience Cloud](https://experienceleague.adobe.com/pt-br/docs/experience-platform/ai-assistant/home){target="_blank"} antes de usar o Assistente de IA.

### O que o assistente de IA pode fazer

**Conhecimento do Produto** - Faça perguntas sobre os recursos e conceitos do Adobe Journey Optimizer:

* &quot;Como configurar uma campanha no Adobe Journey Optimizer?&quot;
* &quot;Como criar uma ação personalizada para usar no jornada?&quot;
* &quot;Quantas atividades ativas posso ter em uma sandbox?&quot;

**Insights Operacionais (Beta)** - Obtenha informações em tempo real sobre suas jornadas:

* &quot;Quantas jornadas ao vivo eu tenho?&quot;
* &quot;Dê-me uma lista de todas as jornadas agendadas&quot;
* &quot;Quantas jornadas foram criadas nos últimos sete dias?&quot;

>[!NOTE]
>
>Os insights operacionais estão disponíveis atualmente apenas para **Jornada** e refletem dados da sua sandbox atual.

### Como usar o assistente de IA

1. Insira a sua pergunta no campo de texto na parte inferior do painel
2. Pressione Enter para enviar sua consulta
3. Revisar a resposta gerada pela IA
4. Clique em **Mostrar fontes** para acessar a documentação relacionada
5. Use miniaturas para cima/para baixo para classificar a qualidade da resposta

![](assets/do-not-localize/ai-assistant-answer.png){width="40%" align="left"}

[Saiba mais sobre o Assistente de IA no Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/ai-assistant/home){target="_blank"}

## Agentes avançados de IA para otimização de Jornada {#ai-agents}

Com base nos recursos conversacionais do Assistente de IA, o Adobe Journey Optimizer oferece agentes de IA especializados que fornecem análise detalhada e recomendações acionáveis para otimização e experimentação de jornadas.

### Agente de análise de Jornada {#journey-agent}

O [Agente de Análise de Jornada](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent-analyze){target="_blank"} ajuda a otimizar o desempenho da jornada por meio da análise de linguagem natural:

**Principais Recursos:**

* **Análise de Fallout de Jornada** - Identifique onde e por que os clientes abandonam durante as jornadas e detecte padrões de separação
* **Detecção de sobreposição de público-alvo** - Analise a sobreposição de público-alvo em várias jornadas para evitar a fadiga devido ao excesso de direcionamento
* **Detecção de Conflito de Agendamento** - Identifique conflitos de tempo entre jornadas agendadas direcionadas para o mesmo público
* **Insights Operacionais** - Obtenha insights baseados em prompts como &quot;mostrar todas as jornadas ativas&quot; ou &quot;quais públicos são usados em mais de X jornadas&quot;

**Prompts de Exemplo:**

* &quot;Executar uma análise de fallout para a jornada \[Nome da Jornada\]&quot;
* &quot;Há algum conflito de agendamento para a jornada \[Nome da Jornada\]?&quot;
* &quot;Mostrar conflitos de sobreposição de público-alvo para a jornada \[Nome da Jornada\]&quot;
* &quot;Quais públicos-alvo são usados em mais de cinco jornadas?&quot;

**Permissões necessárias:**

* **Exibir Jornadas** - Exibir insights sobre jornadas diretamente no Assistente de IA
* **Gerenciar Jornadas** - Criar novas jornadas diretamente no Assistente de IA
* **Exibir segmentos** - Exibir insights sobre públicos
* **Gerenciar segmentos** - Crie novos públicos diretamente no Assistente de IA

### Agente de experimentação {#experimentation-agent}

O [Agente de experimentação](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-experiment){target="_blank"} moderniza a forma como você executa e gerencia experimentos digitais em sites, emails, mensagens por push e aplicativos:

**Principais Recursos:**

* **Análise de desempenho** - Uma visão clara do que aconteceu em experimentos
* **Geração de Insights** - Explicação do motivo da ocorrência de resultados
* **Descoberta de Oportunidades** - Orientação sobre as próximas ações a serem executadas
* **Análise de conteúdo** - Examine elementos de mensagens para entender por que certos tratamentos tiveram desempenho melhor que outros
* **Geração de recomendação** - Sugira novos tratamentos ou ajustes com base em insights

**Prompts de Exemplo:**

* &quot;Quais experimentos estão sendo executados para \[Nome da campanha\]?&quot;
* &quot;Para meu \[Nome do experimento\], qual tratamento está liderando?&quot;
* &quot;O que aprendemos com o \[Nome do experimento\]?&quot;
* &quot;O que você recomenda que eu faça depois deste experimento?&quot;
* &quot;Quais padrões comuns estão emergindo dos testes recentes?&quot;

**Permissões necessárias:**

* **Exibir experimentos** - Exibir insights sobre experimentos no Assistente de IA
* **Gerenciar metadados de experimento** - Criar novos experimentos no Assistente de IA

**Observação:** disponível com licença do Journey Optimizer Experimentation Accelerator.

### Agentes de IA adicionais

**Audience Agent** - Para exploração e gerenciamento de público-alvo conversacional em toda a Adobe Experience Platform, incluindo detecção de duplicidade e rastreamento de tamanho. [Saiba mais sobre o Audience Agent](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/audience){target="_blank"}

**Agent Orchestrator** - Coordena vários agentes especializados para solucionar desafios de marketing complexos de várias etapas. O orquestrador determina automaticamente quais agentes envolver e sequencia seu trabalho com eficiência. [Saiba mais sobre o Agent Orchestrator](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator){target="_blank"}

**Obtendo Acesso:**

Os Agentes de IA estão disponíveis para clientes com acesso ao Assistente de IA. Entre em contato com o representante da Adobe para obter detalhes específicos sobre licenciamento e ativação.

## Geração de conteúdo alimentado por IA {#content-generation}

Use a IA generativa para criar e personalizar o conteúdo em vários canais, acelerando o processo de criação de conteúdo e mantendo a consistência da marca.

### Canais suportados

O Assistente de IA para geração de conteúdo está disponível para:

* **Email** - Gerar linhas de assunto, corpo de texto e imagens
* **Notificações por push** - Criar mensagens de notificação envolventes
* **SMS** - Escrever mensagens de texto concisas e convincentes
* **Web** - Gerar conteúdo e experiências da página da Web

### Recursos principais

* **Geração de texto** - Crie uma cópia atraente com base na voz e nos objetivos de sua marca
* **Geração de imagem** - Gerar imagens personalizadas usando o Adobe Firefly
* **Variações de conteúdo** - Produza várias variações para teste A/B
* **Alinhamento da marca** - Verifique se o conteúdo gerado corresponde às diretrizes da sua marca
* **Suporte a modelos** - Utilize seus modelos de email existentes

### Práticas recomendadas

* **Seja específico** - Forneça prompts claros e detalhados para obter melhores resultados
* **Carregar ativos da marca** - Use PDFs, imagens ou arquivos ZIP (máx. 50 MB) para manter a consistência da marca
* **Usar modelos personalizados** - Utilize modelos específicos da marca com até 8-10 imagens
* **Fornecer feedback** - Classifique as saídas para ajudar a melhorar os modelos de IA
* **Revisar todo o conteúdo** - Sempre revise a precisão do conteúdo gerado pela IA antes de publicar

[Saiba mais sobre a geração de conteúdo de IA](../content-management/gs-generative.md)

## Otimização de tempo de envio {#send-time-optimization}

Use a IA para prever o momento ideal para enviar cada mensagem com base em padrões de comportamento individuais do cliente, maximizando o engajamento.

### Como funciona

A Otimização de tempo de envio analisa os dados históricos de engajamento (aberturas e cliques) para prever quando cada cliente tem maior probabilidade de se engajar com suas mensagens. O sistema programa automaticamente o delivery dentro da janela de tempo especificada.

### Quando usá-lo

**Recomendado para:**

* Campanhas de marketing e informativos
* Mensagens promocionais
* Conteúdo educacional
* Campanhas de engajamento

**Não recomendado para:**

* Mensagens operacionais com detecção de hora (confirmações de pedidos, redefinições de senha)
* Notificações urgentes (atrasos nos voos, alertas de emergência)
* Mensagens baseadas em eventos com requisitos de tempo específicos

### Dicas de configuração

* **Aguarde 30 dias** - Colete pelo menos 30 dias de emails históricos ou dados de push antes de habilitar
* **Definir tempos de espera ideais** - Use de 6 a 24 horas para obter melhores resultados (otimização de limites mais curtos; quanto mais longo, maior poderá resultar em conteúdo desatualizado)
* **Escolha a métrica correta** - Otimizar para cliques (mensagens de ação) ou Aberturas (mensagens de reconhecimento)
* **Agendar envios de manhã** - Para notificações por push, comece cedo no dia para evitar entrega noturna

[Saiba mais sobre a Otimização de tempo de envio](../building-journeys/send-time-optimization.md)

## Modelos de IA para decisão {#ai-decisioning}

Crie modelos de classificação inteligentes que otimizam automaticamente quais ofertas mostrar para cada cliente, maximizando os objetivos de negócios.

### Tipos de modelo

**Otimização automática** - Aprende com as interações do cliente para melhorar automaticamente o desempenho da oferta ao longo do tempo

**Otimização personalizada** - Usa atributos e comportamento do perfil do cliente para prever a melhor oferta para cada indivíduo

### Exigências

* Pelo menos 2 ofertas com dados de interação suficientes:
   * Mais de 100 eventos de exibição
   * Mais de 5 eventos de clique
   * Nos últimos 14 dias
* Máximo de 5 modelos de classificação de IA por organização

[Saiba mais sobre os modelos de IA para a tomada de decisão](../experience-decisioning/ranking/ai-models.md)

## Experimentação de conteúdo com IA {#experimentation}

O **Acelerador de experimentos** ajuda você a executar experimentos mais rapidamente com insights e recomendações orientados por IA, identificando variações de conteúdo vencedoras mais rapidamente.

Principais recursos:

* Gerar várias variações de conteúdo automaticamente
* Receba recomendações de IA para o design de experimentos
* Obter indicadores antecipados de tendências de desempenho
* Acelere o tempo de obtenção de significância estatística

[Saiba mais sobre o Acelerador de experimento](../content-management/experiment-accelerator-gs.md)

## Manuais de estratégia de casos de uso {#playbooks}

Os manuais de casos de uso são fluxos de trabalho pré-criados que ajudam a implementar cenários de marketing comuns rapidamente. Cada manual inclui jornadas, mensagens, esquemas e segmentos prontos para uso.

### Como os manuais funcionam

1. **Navegue** pela biblioteca do manual para encontrar casos de uso que correspondam às suas metas
2. **Habilitar** um manual para gerar automaticamente todos os recursos necessários
3. **Personalize** os ativos gerados para corresponder à sua marca e requisitos
4. **Implantar** para produção ou teste em uma sandbox de desenvolvimento

### Playbooks disponíveis

Procurar nos manuais do Journey Optimizer cenários comuns, como:

* Recuperação do carrinho abandonado
* Série de boas-vindas para novos clientes
* Compromisso pós-compra
* Mensagens de aniversário
* Campanhas de reengajamento

### Pré-requisitos

* Sandbox com permissões apropriadas
* Configurações de canal para email, push e/ou SMS
* Permissões de usuário para criar jornadas e mensagens

![Interface de manuais de caso de uso](assets/playbooks-filter.png)

[Exibir todos os manuais disponíveis](https://experienceleague.adobe.com/docs/experience-platform/use-case-playbooks/playbooks/playbooks-list.html?lang=pt-BR){target="_blank"} | [Saiba mais na documentação do Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/use-case-playbooks/playbooks/overview.html){target="_blank"}

## Recursos adicionais de IA {#additional-capabilities}

### Conversor de imagem para HTML

Transforme designs de imagem estática (JPEG, PNG) em modelos de email editáveis do HTML usando tecnologia de conversão habilitada por IA.

[Saiba mais sobre imagem para o HTML](../email/image-to-html.md)

### Classificação de alinhamento à marca

Avalie como seu conteúdo se alinha às diretrizes da sua marca usando a pontuação alimentada por IA que mede a consistência do tom, da voz e da mensagem.

[Saiba mais sobre o Alinhamento da marca](../content-management/brands-score.md)

## Perguntas frequentes {#faq}

+++**Quais permissões são necessárias para os recursos de IA?**

* **Assistente de IA para geração de conteúdo** - Requer a permissão &quot;Gerar conteúdo&quot;
* **Conhecimento sobre o produto Assistente de IA** - Requer o consentimento das Diretrizes de usuário da IA geradora da Adobe
* **Agente de Análise de Jornada** - Requer permissões para Exibir/Gerenciar Jornadas e Exibir/Gerenciar Segmentos
* **Agente de experimentação** - Requer permissões para Exibir experimentos e Gerenciar metadados de experimento

Todos os agentes de IA exigem acesso ao Assistente de IA e concordam com as Diretrizes de usuário da IA gerativa da Adobe Experience Cloud.

[Saiba mais sobre permissões](../administration/ootb-permissions.md)

+++

+++**O conteúdo gerado por IA é sempre preciso?**

Não. Sempre revise o conteúdo gerado por IA em busca de precisão e adequação da marca. Use as ferramentas de feedback (polegares para cima/para baixo) para ajudar a melhorar os modelos.

+++

+++**Quais são as principais limitações?**

* **Otimização de Tempo de Envio** - Disponível apenas para email e push em jornadas; requer um período de treinamento de 30 dias
* **Geração de conteúdo de IA** - Não disponível para correspondência direta, cartões de conteúdo, LINE ou WhatsApp
* **Modelos de classificação de IA** - Máximo de 5 modelos por organização; requer um mínimo de dados de interação

+++

+++**Como obter acesso a esses recursos?**

A maioria dos recursos de IA está incluída no Adobe Journey Optimizer. Alguns recursos, como Otimização de tempo de envio ou Agentes de IA, podem exigir a ativação pela Adobe. Entre em contato com seu representante da Adobe para obter detalhes sobre sua licença específica e os recursos disponíveis.

+++

>[!MORELIKETHIS]
>
>* [Introdução ao Assistente de IA para geração de conteúdo](../content-management/gs-generative.md)
>* [Assistente de IA no Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/ai-assistant/home){target="_blank"}
>* [Documentação do Jornada Analyze Agent](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent-analyze){target="_blank"}
>* [Documentação do agente de experimentação](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-experiment){target="_blank"}
>* [Guia de Otimização de Tempo de Envio](../building-journeys/send-time-optimization.md)
>* [Criar modelos de classificação de IA](../experience-decisioning/ranking/create-ai-models.md)
>* [Documentação dos manuais de caso de uso](https://experienceleague.adobe.com/docs/experience-platform/use-case-playbooks/playbooks/overview.html){target="_blank"}

