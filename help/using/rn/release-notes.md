---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Notas de versão do Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
TQID: https://experienceleague.adobe.com/YJKQFYUi8Kw7yZZKm8blcM-1G9uYsqcsEsopH0hOMhA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
    internal-label: Administration
subfeature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
    internal-label: Journey Optimizer release notes
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 8a0943c7362859a4431f35b6b6163b2d947fff43
workflow-type: tm+mt
source-wordcount: '3141'
ht-degree: 16%
---
# Notas de versão {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novidades"
>abstract="O **Adobe Journey Optimizer** oferece continuamente novos recursos, melhorias nos recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão."

O [!DNL Adobe Journey Optimizer] segue um modelo de entrega contínua, permitindo que a Adobe forneça novos recursos, melhorias e correções de forma contínua. Essa abordagem permite uma implantação escalável e em fases de recursos para garantir desempenho e estabilidade em todos os ambientes. Devido a esse modelo, as notas de versão são atualizadas entre as versões mensais. Para obter detalhes completos sobre o ciclo de lançamento e as fases de disponibilidade, consulte o [ciclo de lançamento do Journey Optimizer](releases.md).

O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

>[!NOTE]
>
>Os recursos listados nestas notas de versão incluem uma **Data de disponibilidade** indicando quando cada alteração se torna acessível no ambiente. As entradas nos acordeões **Em breve** são esperadas nos próximos dias ou semanas. As informações nessas seções estão sujeitas a alterações.

## Notas de versão de setembro de 2026 {#sep-26-updates}

### Gerenciamento de conteúdo {#sep-26-content-management}

O recurso a seguir está chegando ao gerenciamento de conteúdo nesta versão.

<table>
<thead>
<tr>
<th><strong>Plug-in de Conteúdo do Canal no Colaborador</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Um novo plug-in de <strong>Conteúdo do Canal</strong> já está disponível no Co-worker, que reúne as habilidades de cópia da campanha, imagem e email montado no HTML em um plug-in, da estratégia à implantação. As seguintes habilidades estão disponíveis no plug-in <b>Conteúdo do canal</b>:</p>
<ul>
<li><strong>Orquestrar Criação De Conteúdo</strong>.</li>
<li><strong>Explorar a estratégia de conteúdo</strong></li>
<li><strong>Resumo do conteúdo</strong></li>
<li><strong>Gerar conteúdo</strong></li>
<li><strong>Verificar prontidão do conteúdo</strong></li>
<li><strong>Revisar e regenerar conteúdo</strong></li>
<li><strong>Gerar imagem</strong></li>
<li><strong>Avaliar o design de conteúdo</strong></li>
<li><strong>Salvar conteúdo do canal</strong></li>
<li><strong>Criar e-mail no Figma</strong></li>
<li><strong>Pesquisa de marca</strong> </li>
</ul>
<p>Para obter mais informações, consulte a <a href="../content-management/content-management-coworker-skills.md#content-management#ce-channel-content">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 24 de setembro de 2026</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Ferramentas MCP para gerenciamento de conteúdo no CX Co-worker</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O CX Co-worker agora tem um novo conjunto de <strong>ferramentas de MCP de gerenciamento de conteúdo</strong>, permitindo que você descubra e gerencie ativos de conteúdo do Journey Optimizer por meio de prompts de linguagem natural. Solicite que ele liste ou recupere modelos de conteúdo, fragmentos, páginas de aterrissagem e conteúdo de mensagem integrada do jornada/campaign. Ele também pode criar conteúdo, atualizar modelos e criar, atualizar, clonar e publicar fragmentos, além de atualizar o conteúdo da ação de canal em linha diretamente no jornada e no Campaign.</p>
<p>Para obter mais informações, consulte a <a href="../content-management/content-management-coworker-skills.md#content-management">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 3 de setembro de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Caixa de seleção de consentimento obrigatório para páginas de aterrissagem** - Agora é possível tornar uma caixa de seleção obrigatória no componente de formulário da página de aterrissagem, exigindo que os visitantes a selecionem (por exemplo, para dar consentimento) antes que possam enviar o formulário. [Saiba mais](../landing-pages/lp-content.md#use-form-component)

  Data de disponibilidade: 4 de setembro de 2026

* **Palavras-chave reservadas adicionais na sintaxe de personalização** - A lista de palavras-chave reservadas no Profile Query Language (PQL) foi expandida para incluir palavras-chave gerais, unidades de tempo e operadores booleanos/lógicos. Se o esquema XDM contiver um nome de campo que corresponda a uma dessas palavras-chave, coloque-o entre acentos graves para fazer referência a ele em uma expressão de personalização. [Saiba mais](../personalization/personalization-syntax.md#reserved-keywords)

  Data de disponibilidade: 1º de setembro de 2026

### Fidelidade {#sep-26-loyalty}

<table>
<thead>
<tr>
<th><strong>Atualizações de mapeamento de evento de fidelidade</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A criação ou edição de um Mapeamento de evento agora usa um novo **construtor de mapeamento visual**: selecione um esquema, escolha campos de um seletor de campo pesquisável, mapeie cada campo para um campo de evento de fidelidade com status de conexão por linha e visualize a expressão JSONata gerada automaticamente, com a opção de alternar para a edição JSONata manual a qualquer momento.</p><p>Além disso, as "Definições de evento" no Admin de fidelidade foram renomeadas para "Mapeamentos de evento", com uma exibição de lista atualizada que mostra o nome de esquema do evento de experiência legível.</p>
<p>Para obter mais informações, consulte a <a href="../loyalty-challenges/loyalty-admin.md#event-mappings">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 22 de setembro de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Desafios de fidelidade &quot;para sempre&quot;** - Os desafios de fidelidade agora podem ser executados indefinidamente. Defina **Fim do desafio** como **Sem data de término** ao configurar o agendamento, e o desafio nunca expirará. [Saiba mais](../loyalty-challenges/create-challenges.md#schedule)

  Data de disponibilidade: 1º de setembro de 2026

* **Fidelidade disponível para clientes do Healthcare Shield e do Privacy and Security Shield** - o Journey Optimizer Loyalty agora está disponível para clientes do Healthcare Shield e do Privacy and Security Shield. [Saiba mais](../loyalty-challenges/get-started.md)

  Data de disponibilidade: 15 de setembro de 2026

+++ Em breve — **as informações abaixo estão sujeitas a alterações.**

<table>
<thead>
<tr>
<th><strong>Recomendações de desafio</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O menu Desempenho de fidelidade agora inclui as guias **Oportunidades** e **Tendência**, que mostram tendências e lacunas detectadas pela IA, como atrito de progressão de nível ou queda de tarefa de desafio, cada uma com um impacto projetado e uma ação "Criar com IA" de um clique para gerar um desafio que atenda a isso.</p><p>Além disso, os profissionais de marketing podem solicitar **oportunidades de desafio** diretamente na interface conversacional do Colaborador, obtendo ideias de desafio baseadas em tendências de programas de fidelidade reais e transformando-as em desafios ao vivo sem sair do bate-papo.</p>
</td>
</tr>
</tbody>
</table>

* **Prazos de conclusão do desafio de fidelidade por membro** - Os desafios de fidelidade agora oferecem suporte aos prazos de conclusão por membro: escolha &quot;Dentro de um número de dias após a aceitação&quot; em Requisitos de conclusão para que o prazo de cada membro seja calculado a partir de sua própria data de aceitação, em vez de uma data de término fixa em todo o programa. Se uma data final de desafio e essa janela de aceitação forem definidas, o prazo de cada membro será o primeiro. <!-- Documentation link: TBD -->

+++

### Jornadas {#sep-26-journeys}

<table>
<thead>
<tr>
<th><strong>Simulação de Jornada no Colaborador</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A <strong>habilidade de Simulação de Jornada</strong> do Colaborador automatiza a validação completa da jornada e permite que você interprete facilmente os resultados. Observe que esse recurso atualmente suporta apenas o fluxo de Simulação rápida e não substitui totalmente a experiência de simulação manual do Journey Optimizer.</p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/journeys-coworker-skills.md#journey-simulation">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 23 de setembro de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Controle no nível da jornada (disponibilidade limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode configurar um grupo de controle para suas jornadas diretamente das propriedades da jornada. Um controle é uma porcentagem configurável do público-alvo que é excluído da entrada na jornada e não recebe nenhuma comunicação. Ao comparar perfis de controle com perfis ativos nos relatórios do Customer Journey Analytics, é possível medir o aumento incremental, o impacto real, que a jornada oferece.</p>
<p>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe. Para obter detalhes completos sobre o ciclo de lançamento e as fases de disponibilidade, consulte o <a href="releases.md">ciclo de lançamento do Journey Optimizer</a>.</p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/journey-properties.md#performance-management">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 1º de setembro de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Gerar expressões com IA em jornadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O editor de expressão avançado do jornada agora integra a geração de expressões alimentadas por IA: descreva a expressão que você deseja criar em linguagem natural e o editor gera um código pronto para uso que pode ser aplicado imediatamente ou refinado por meio de prompts de acompanhamento.</p>
<p>Anteriormente lançado em disponibilidade limitada, este recurso agora está disponível para todos os ambientes (disponibilidade geral).</p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/expression/generate-expression.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 1º de setembro de 2026</p>
</td>
</tr>
</tbody>
</table>


* **Suporte para atividades de salto em jornadas de qualificação de público-alvo** - Agora você pode usar atividades de salto em jornadas que começam com um nó de Qualificação de público-alvo para ir para jornadas baseadas em eventos. Esse recurso está sendo progressivamente distribuído às organizações. Se você não vir isso em seu ambiente, talvez esteja usando públicos em lote em Qualificações de público-alvo. [Saiba mais](../building-journeys/jump.md)

  Data de disponibilidade: 22 de setembro de 2026.

* **Acionar após a avaliação do público-alvo em lotes** - Para jornadas recorrentes direcionadas a públicos-alvo em lotes, é possível configurar uma janela de espera de até 6 horas para uma nova avaliação em lotes antes da execução da jornada. Se uma avaliação estiver em andamento, a jornada aguardará sua conclusão; se o instantâneo mais recente tiver sido usado pela execução anterior, ele aguardará um lote mais recente. Se nenhum público novo estiver disponível no final da janela de espera, essa ocorrência será ignorada. [Saiba mais](../building-journeys/read-audience.md)

  Data de disponibilidade: 18 de setembro de 2026

* **A Decisão na simulação de Jornada** - Experimentação de Caminho, como parte da atividade **Otimizar**, agora é compatível com a Simulação. O roteamento é manipulado pela Decisão e é aleatório e não determinístico por usuário simulado.

  [Saiba mais](../building-journeys/simulate-journey-gs.md)

  Data de disponibilidade: 15 de setembro de 2026

* **Alerta de Nova Anomalia de Jornada Detectada** - Um novo alerta do sistema agora avisa quando o tráfego diário de uma jornada em tempo real se desvia de sua própria linha de base histórica ou cai para zero inesperadamente, entre Entradas de Jornada, Saídas de Jornada e Envios de evento. Este alerta está disponível atualmente somente em sandboxes de produção.

  [Saiba mais](../reports/alerts.md)

  Data de disponibilidade: 15 de setembro de 2026

* **Decisão na simulação de Jornada** - Agora é possível simular jornadas que dependem da Decisão, com os seguintes itens recém-suportados:

  * Os nós de Decisão de conteúdo agora são compatíveis com a Simulação.
  * O método de regra de Direcionamento da atividade Otimizar agora é compatível com a Simulação.
  * Ações com conteúdo decidido pela Adobe Journey Optimizer (por exemplo, email usando uma política de decisão) agora são compatíveis com a Simulação.
  * As políticas de decisão que usam a Qualificação de oferta e a classificação por regra, público-alvo, prioridade ou fórmula são totalmente compatíveis. Classificação por modelo de IA - o Personalization também é compatível, embora as ofertas retornadas possam variar entre as execuções.

  [Saiba mais](../building-journeys/simulate-journey-gs.md)

  Data de disponibilidade: 8 de setembro de 2026

* **Analisar habilidade de Anomalias de Jornada** - O CX Co-worker pode detectar picos, quedas ou linhas achatadas inesperados nas contagens de entrada, saída ou envio de mensagem de uma jornada em relação às linhas de base históricas usando a habilidade **Analisar anomalias de Jornada**. Depois que uma anomalia real é confirmada, a habilidade executa diagnósticos somente leitura para mostrar uma causa básica provável e uma recomendação. [Saiba mais](../building-journeys/journeys-coworker-skills.md#journey-analyze)

  Data de disponibilidade: 2 de setembro de 2026

* **Nova função dateDiff no editor de expressão de jornada** - O editor de expressão de jornada agora inclui a função `dateDiff`, que calcula a diferença entre duas datas em número de dias. Essa função é útil para uma lógica baseada no tempo, como criar prazos, calcular durações de ciclo de vida do cliente ou criar cronômetros de contagem regressiva em condições de jornada.  [Saiba mais](../building-journeys/functions/date-functions.md#dateDiff)

  Data de disponibilidade: 1º de setembro de 2026

+++ Em breve — **as informações abaixo estão sujeitas a alterações.**

<table>
<thead>
<tr>
<th><strong>Visualização de conteúdo na tela de jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A análise do conteúdo do canal hoje em dia requer a abertura de cada atividade individualmente, uma de cada vez — lenta e sujeita a erros em jornadas com muitas atividades de canal, especialmente quando a personalização significa a verificação de vários tratamentos ou variantes por atividade. A <strong>visualização de conteúdo</strong> remove esse atrito ao exibir uma miniatura de conteúdo para cada atividade de canal diretamente na tela, com um modal de tela cheia para inspecionar e alternar entre tratamentos e variantes.</p>
<p>Data de disponibilidade do Target: 28 de setembro de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Habilidade da Análise de Higiene** - O CX Coworker agora pode verificar suas jornadas ativas e de rascunho em busca de configurações corrompidas, falhas silenciosas e ativos em decomposição ou não utilizados, como jornadas de rascunho obsoletas, fontes de dados órfãs e erros de ação personalizados persistentes, e apresentar correções recomendadas diretamente no chat. <!-- Documentation link: TBD -->

* **O suporte à ID complementar na simulação de Jornada** - **A ID complementar** agora tem suporte na simulação de Jornada, permitindo que você teste cenários de usuário complexos para jornadas acionadas por evento e público-alvo de leitura.

+++

### Campanhas {#sep-26-campaigns}

+++ Em breve — **as informações abaixo estão sujeitas a alterações.**

* **Pastas para Campanhas de Ação** - Agora você pode organizar suas Campanhas de Ação em pastas para melhorar a navegação e o gerenciamento na interface.

* **Substituir os campos de execução padrão em Campanhas de ação** - Anteriormente disponíveis no nível de jornada, agora é possível substituir os campos de execução padrão configurados globalmente para suas entregas de email, SMS e WhatsApp nos parâmetros da Campanha de ação.

+++


### Canais {#sep-26-channels}

Os seguintes recursos e melhorias estão chegando aos canais nesta versão.

+++ Em breve — **as informações abaixo estão sujeitas a alterações.**

<table>
<thead>
<tr>
<th><strong>Atividades ativas para atualizações do Android Live</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A Journey Optimizer agora expande seus recursos de personalização móvel em tempo real estendendo o suporte à <strong>Atividade em tempo real para o Android</strong>. Você pode fornecer atualizações de progresso em tempo real diretamente aos usuários, como rastreamento de pedidos, status de voo, atualizações de eventos ao vivo e pontuações de esportes em tempo real.</p>
<p>Além do suporte às atividades do iOS Live, a Journey Optimizer agora gerencia tokens de push temporários para atualizações do Android Live em todas as configurações da plataforma. Ele é compatível com fluxos de atualização transacionais e de transmissão usando campanhas acionadas por API e APIs headless.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Melhorias nos modelos de notificações por push do Android</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As notificações por push do Android eram renderizadas anteriormente com um layout único e fixo: as imagens sempre eram cortadas ao centro e o texto do corpo longo era truncado. Essa versão apresenta um seletor de modelo no momento da criação, permitindo que os profissionais de marketing controlem o layout das notificações por push do Android.</p>
<p>As seguintes melhorias estão disponíveis:</p>
<ul>
<li><b>Seleção de layout</b>: novo seletor de layout de notificação por push (Padrão/Expandido) ao criar um push do Android.</li>
<li><b>Layout padrão com "Mostrar imagem inteira"</b>: escolha recortado para preenchimento vs. dimensionado para ajuste.</li>
<li><b>Layout expandido</b>: corpo de texto multilinha sem truncamento, além de miniatura de ícone grande opcional.</li>
<li><b>Corpo recolhido (Layout expandido)</b>: defina um texto de corpo separado e mais curto para o estado recolhido.</li>
</ul>
</td>
</tr>
</tbody>
</table>

* **Flexibilidade de autenticação BYOP de SMS personalizado** - Agora você pode configurar **cabeçalhos de autenticação personalizados** ao conectar a configuração OAuth do seu provedor de SMS, incluindo onde o token é colocado nas mensagens de saída e como a própria solicitação de token é formatada.

+++

### Campanhas orquestradas {#sep-26-orchestrated-campaigns}

<table>
<thead>
<tr>
<th><strong>Alertas para campanhas orquestradas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As campanhas orquestradas agora oferecem suporte a <strong>alertas automatizados</strong> por meio da mesma estrutura de alertas usada em jornadas e campanhas. Os alertas são acionados quando a execução de uma campanha falha, atinge o tempo limite e cada alerta inclui o que aconteceu, quando, onde e um link direto para a Tela para verificar mais detalhes nos logs.</p>
<p>Para obter mais informações, consulte a <a href="../orchestrated/start-monitor-campaigns.md#alerting">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 22 de setembro de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Conteúdo condicional com dados relacionais em campanhas orquestradas** - Ao criar conteúdo condicional no Designer de email para campanhas orquestradas, agora é possível criar condições diretamente nos dados relacionais, como registros relacionados associados a um perfil, não apenas nos atributos de perfil padrão. [Saiba mais](../orchestrated/activities/channels.md#add-personalization)

  Data de disponibilidade: 22 de setembro de 2026

* **Junções diretas em coleções em Campanhas Orquestradas** - Ao adicionar um atributo de uma coleção relacionada, agora é possível escolher entre três modos de junção — um novo padrão que avisa sobre o impacto potencial no desempenho de produtos cartesianos, além dos modos Agregado e Avançado existentes — facilitando a compreensão das compensações da consulta antes da compilação. [Saiba mais](../orchestrated/build-query.md#links)

  Data de disponibilidade: 22 de setembro de 2026

+++ Em breve — **as informações abaixo estão sujeitas a alterações.**


<table>
<thead>
<tr>
<th><strong>OU participe de atividades para campanhas orquestradas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A <strong>Atividade de ingresso</strong> em campanhas orquestradas agora oferece suporte às condições de ingresso AND e OR. Com a lógica OR, um perfil que conclui qualquer ramificação upstream, em vez de todas, continua ao longo de um único caminho downstream compartilhado. Isso permite modelar "se A ou B ou C, faça isso" padrões diretamente na tela sem duplicar etapas downstream em ramificações separadas.</p>
</td>
</tr>
</tbody>
</table>

* **Canal LINE para campanhas orquestradas** - O LINE agora está disponível como um canal de saída nativo em campanhas orquestradas, junto com email, SMS e push. Você pode criar e entregar mensagens LINE diretamente da tela da campanha, incluindo texto, adesivos, imagens, vídeos, dados de localização e mensagens do Flex, apoiando casos de uso de engajamento promocional, transacional e contínuo em mercados dominados pelo LINE, como Japão e APAC. Lançado anteriormente com disponibilidade limitada, esse recurso agora está disponível no mercado.


* **Monitoramento da Orquestração de Campanha** — Uma nova interface de usuário está disponível para rastrear o status de assimilação e a atualização dos dados do armazenamento relacional usados pela Segmentação Orquestrada do Campaign. Ele oferece visibilidade direta da integridade dos dados que alimentam os públicos-alvo em lote. Uma nova guia Orquestração de campanha no painel Monitoramento da Adobe Experience Platform exibe a integridade dos fluxos de dados do armazenamento relacional (registros assimilados/atualizados/excluídos/com falha/ignorados), com gráficos detalhados e um detalhamento por fluxo de dados/conjunto de dados, incluindo linhagem.


+++

### Integração {#sep-26-onboarding}

A seguinte melhoria está chegando à integração nesta versão.

<table>
<thead>
<tr>
<th><strong>Recursos guiados para integração de emails e jornadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Os recursos guiados para integração de emails e jornadas agora incluem as seguintes melhorias:</p>
<ul>
<li>Ao migrar um email, o [!DNL Journey Optimizer] identifica os blocos de conteúdo referenciados por esse email e os exibe como itens de ação, para que você possa migrar os blocos de conteúdo ao lado do email.</li>
<li>A interface foi aprimorada para tornar a integração guiada mais intuitiva.</li></ul>
<p>Para obter mais informações, consulte a <a href="../start/onboarding-hub.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 23 de setembro de 2026</p>
</td>
</tr>
</tbody>
</table>

### Relatório {#sep-26-reporting}

O recurso a seguir está chegando aos relatórios nesta versão.

+++ Em breve — **as informações abaixo estão sujeitas a alterações.**

<table>
<thead>
<tr>
<th><strong>Novos gráficos de monitoramento de entrada no Gerenciamento de dados</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível monitorar a integridade dos dados de entrada diretamente em <strong>Gerenciamento de Dados &gt; Monitoramento &gt; Edge</strong>, com seis novos gráficos que abrangem eventos de taxa de transferência, latência e proposta:</p>
<ul>
<li><strong>Taxa de Transferência de Entrada do AJO</strong> — taxa de transferência de entrada geral (registros por segundo) ao longo do tempo.</li>
<li><strong>Detalhamento de Taxa de Transferência de Entrada do AJO</strong> — taxa de transferência de entrada dividida por localização.</li>
<li><strong>Latência de Entrada do AJO</strong> — latência de solicitação de entrada (em milissegundos), dividida pela distribuição de valores (P50, P90 e mais).</li>
<li><strong>Taxa de Transferência de Eventos de Apresentação de Entrada do AJO</strong> — taxa de transferência de eventos de apresentação (sinais de rastreamento gerados quando um usuário interage com o, visualiza ou aciona ofertas personalizadas) ao longo do tempo.</li>
<li><strong>Taxa de Transferência de Eventos de Apresentação de Entrada do AJO por Canal</strong> — a taxa de transferência de eventos de apresentação é dividida por canal de entrada (CBE, no aplicativo, cartões de conteúdo).</li>
<li><strong>Taxa de Transferência de Eventos de Apresentação de Entrada do AJO por Tipo de Evento</strong> — a taxa de transferência de eventos de apresentação é dividida por tipo de evento (descartada, suprimida, exibida, acionada, interagida, enviada).</li>
</ul>
</td>
</tr>
</tbody>
</table>

+++

### Integrações {#sep-26-integrations}

Os recursos a seguir estão chegando às integrações nesta versão.

+++ Em breve — **as informações abaixo estão sujeitas a alterações.**


* **Substituição dinâmica de token para fragmentos de Experience Manager** - As referências de Fragmento de Conteúdo do Experience Manager agora oferecem suporte a um atributo **tokenSubstitution**. Quando definido como `false`, a personalização dentro dos campos do fragmento é resolvida diretamente, sem um mapa de token na referência. O padrão é `true`, que mantém o comportamento existente.

  Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.

* **Suporte a fragmentos de conteúdo do AEM Managed Services na Decisão** - Os fragmentos de conteúdo do AEM Managed Services agora são aceitos na Decisão ao gerenciar itens de decisão.


+++

### Personalização {#sep-26-personalization}

* **Corrigir sintaxe com IA** - Quando um erro de validação de sintaxe do PQL é detectado, o Editor do Personalization agora fornece uma opção &quot;Corrigir com IA&quot; para ajudar a resolver o problema diretamente do editor.

  Data de disponibilidade: 22 de setembro de 2026

### Tomada de decisão {#sep-26-decisioning}

Os seguintes recursos e melhorias estão chegando à decisão nesta versão.

<table>
<thead>
<tr>
<th><strong>Suporte à decisão no canal da Web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>A Decisão agora está disponível no canal da web. Você pode usar políticas de decisão diretamente no editor visual da web para fornecer as ofertas mais relevantes a cada visitante.</p>
<p>Para obter mais informações, consulte a <a href="../experience-decisioning/use-decision-policy.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 22 de setembro de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Fragmentos de conteúdo do AEM no Decisioning disponíveis para clientes do Managed Services** - Anteriormente, os Fragmentos de conteúdo do AEM no Decisioning estavam disponíveis somente para clientes que usavam a integração do **Adobe Experience Manager as a Cloud Service**. Este recurso também está disponível para clientes que usam o **Adobe Experience Manager Managed Services**. [Saiba mais](../experience-decisioning/items.md#attributes)

  Data de disponibilidade: 23 de setembro de 2026

* **Suporte para perfis Adobe Experience Platform na simulação de fórmula de Regra e Classificação** - Ao simular uma Regra ou Fórmula de Classificação, agora é possível selecionar um perfil Adobe Experience Platform para preencher automaticamente os atributos de uma variante de dados de teste, em vez de inseri-los manualmente. [Saiba mais](../experience-decisioning/ranking/ranking-formulas.md#simulate-ranking-formula)

  Data de disponibilidade: 22 de setembro de 2026

### Públicos-alvo {#sep-26-audiences}

O lembrete a seguir se aplica aos públicos-alvo nesta versão.

* **Futura alteração para públicos-alvo de enriquecimento da Composição de Público-alvo** - Durante a versão de outubro (fim de outubro), o Journey Optimizer interromperá jornadas e campanhas que usam ou fazem referência a um público-alvo da Composição de Público-alvo cujo conjunto de dados de origem não tem um **descritor de identidade principal**. A partir desse ponto, somente os públicos-alvo de Composição de público-alvo criados com um descritor de identidade principal são compatíveis com jornadas e campanhas. Se você precisar que essas jornadas ou campanhas permaneçam ativas, entre em contato com o representante da Adobe — nossa equipe de produtos pode ajudá-lo a migrar. <!-- Documentation link: TBD -->

### Administração {#sep-26-administration}

O lembrete a seguir se aplica à administração nesta versão.

* **Garantia de vida útil do conjunto de dados (TTL) — sandboxes existentes** - A proteção de vida útil (TTL) para conjuntos de dados gerados pelo sistema da Journey Optimizer (90 dias no repositório de perfis, 13 meses no data lake) será aplicada às sandboxes e organizações do cliente existentes a partir de 1º de outubro de 2026.

### Melhorias de usabilidade {#sep-26-usability}

* **Visão geral da IA em alertas de validação de fragmento** - A caixa de diálogo de alertas de validação de fragmento agora inclui uma visão geral da IA que resume e explica os problemas de validação (por exemplo, expressões malformadas, campos de perfil ausentes e JSON inválido) para que os usuários possam solucionar os problemas com mais rapidez.

  Data de disponibilidade: 22 de setembro de 2026

* **Desanexar e associar ramificações com mais facilidade na nova tela de jornada** - Agora é possível desanexar uma ramificação do restante da jornada sem excluí-la e associá-la novamente mais tarde em outro ponto, selecionando uma atividade qualificada diretamente na tela ou selecionando-a em uma lista de ramificações desconectadas ou já usadas. [Saiba mais](../building-journeys/using-the-journey-designer.md#join-and-detach-branches)

  Data de disponibilidade: 1º de setembro de 2026

