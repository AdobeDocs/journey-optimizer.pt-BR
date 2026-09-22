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
source-git-commit: 777b1057b68827000c8c20db9678e8b5473b1c42
workflow-type: tm+mt
source-wordcount: '3223'
ht-degree: 61%
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

## Atualizações de setembro de 2026 {#sep-26-updates}

### Gerenciamento de conteúdo {#sep-26-content-management}

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

* **Desafios de fidelidade &quot;para sempre&quot;** - Os desafios de fidelidade agora podem ser executados indefinidamente. Defina **Fim do desafio** como **Sem data de término** ao configurar o agendamento, e o desafio nunca expirará. [Saiba mais](../loyalty-challenges/create-challenges.md#schedule)

  Data de disponibilidade: 1º de setembro de 2026

* **Fidelidade disponível para clientes do Healthcare Shield e do Privacy and Security Shield** - o Journey Optimizer Loyalty agora está disponível para clientes do Healthcare Shield e do Privacy and Security Shield. [Saiba mais](../loyalty-challenges/get-started.md)

  Data de disponibilidade: 15 de setembro de 2026

### Jornadas {#sep-26-journeys}

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

* **Nova função dateDiff no editor de expressão de jornada** - O editor de expressão de jornada agora inclui a função `dateDiff`, que calcula a diferença entre duas datas em número de dias. Essa função é útil para uma lógica baseada no tempo, como criar prazos, calcular durações de ciclo de vida do cliente ou criar cronômetros de contagem regressiva em condições de jornada.  [Saiba mais](../building-journeys/functions/date-functions.md#dateDiff)

  Data de disponibilidade: 1º de setembro de 2026

* **Suporte para atividades de salto em jornadas de qualificação de público-alvo** - Agora você pode usar atividades de salto em jornadas que começam com um nó de Qualificação de público-alvo para ir para jornadas baseadas em eventos. Esse recurso está sendo progressivamente distribuído às organizações. Se você não vir isso em seu ambiente, talvez esteja usando públicos em lote em Qualificações de público-alvo. [Saiba mais](../building-journeys/jump.md)

  Data de disponibilidade: 22 de setembro de 2026.

* **Analisar habilidade de Anomalias de Jornada** - O CX Co-worker pode detectar picos, quedas ou linhas achatadas inesperados nas contagens de entrada, saída ou envio de mensagem de uma jornada em relação às linhas de base históricas usando a habilidade **Analisar anomalias de Jornada**. Depois que uma anomalia real é confirmada, a habilidade executa diagnósticos somente leitura para mostrar uma causa básica provável e uma recomendação. [Saiba mais](../building-journeys/journeys-coworker-skills.md#journey-analyze)

  Data de disponibilidade: 2 de setembro de 2026

* **Acionar após a avaliação do público-alvo em lotes** - Para jornadas recorrentes direcionadas a públicos-alvo em lotes, é possível configurar uma janela de espera de até 6 horas para uma nova avaliação em lotes antes da execução da jornada. Se uma avaliação estiver em andamento, a jornada aguardará sua conclusão; se o instantâneo mais recente tiver sido usado pela execução anterior, ele aguardará um lote mais recente. Se nenhum público novo estiver disponível no final da janela de espera, essa ocorrência será ignorada. [Saiba mais](../building-journeys/read-audience.md)

  Data de disponibilidade: 18 de setembro de 2026

### Campanhas {#sep-26-campaigns}

* **Redesign do fluxo de criação da Campanha de ação**: o fluxo de criação da Campanha de ação do Adobe Journey Optimizer foi reprojetado para fornecer uma experiência do usuário significativamente mais intuitiva, eficiente e contínua.

+++ Em breve — **as informações abaixo estão sujeitas a alterações.**

<table>
<thead>
<tr>
<th><strong>Simulação de experiência de entrada em Campanhas de ação</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível simular ações de canal de entrada em Campanhas de ação antes de entrar em atividade. Use o modo de simulação para testar sua configuração com usuários simulados e visualizar a experiência renderizada, incluindo um URL gerado e um código QR, para que você possa validar regras, decisões e renderização de conteúdo de ponta a ponta.</p>
<p>No momento, esse recurso está em Private Beta e disponível para um conjunto limitado de organizações. Entre em contato com o representante da Adobe para obter mais informações.</p>
</td>
</tr>
</tbody>
</table>

* **Pastas para Campanhas de Ação** - Agora você pode organizar suas Campanhas de Ação em pastas para melhorar a navegação e o gerenciamento na interface.

* **Substituir os campos de execução padrão em Campanhas de ação** - Anteriormente disponíveis no nível de jornada, agora é possível substituir os campos de execução padrão configurados globalmente para suas entregas de email, SMS e WhatsApp nos parâmetros da Campanha de ação.

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

### Personalização {#sep-26-personalization}

* **Corrigir sintaxe com IA** - Quando um erro de validação de sintaxe do PQL é detectado, o Editor do Personalization agora fornece uma opção &quot;Corrigir com IA&quot; para ajudar a resolver o problema diretamente do editor.

  Data de disponibilidade: 22 de setembro de 2026

### Melhorias de usabilidade {#sep-26-usability}

* **Desanexar e associar ramificações com mais facilidade na nova tela de jornada** - Agora é possível desanexar uma ramificação do restante da jornada sem excluí-la e associá-la novamente mais tarde em outro ponto, selecionando uma atividade qualificada diretamente na tela ou selecionando-a em uma lista de ramificações desconectadas ou já usadas. [Saiba mais](../building-journeys/using-the-journey-designer.md#join-and-detach-branches)

  Data de disponibilidade: 1º de setembro de 2026

## Notas de versão de agosto de 2026 {#aug-26-updates}

### Gerenciamento de conteúdo

Os seguintes recursos e melhorias foram introduzidos no gerenciamento de conteúdo nesta versão.

<table>
<thead>
<tr>
<th><strong>Obtenção flexível de imagens para geração de conteúdo por IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A geração de conteúdo no Journey Optimizer agora usa imagens aprovadas pela marca diretamente do Adobe Experience Manager Assets Essentials e versões posteriores. Três modos controlam o equilíbrio: Equilibrado (primeiro gerenciamento de ativos digitais, IA preenche lacunas, padrão), Ativos (fonte de gerenciamento de ativos digitais) e Criativo (IA).</p>
<p><img src="../content-management/assets/image-mode-3.png"></p>
<p>Para obter mais informações, consulte a <a href="../content-management/generative-uc.md#image-mode">documentação detalhada</a>.</p>
<p> Data de disponibilidade: 5 de agosto de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Aviso de tamanho da variante de conteúdo**: o Journey Optimizer agora exibe um aviso de limite flexível quando uma variante de conteúdo excede seu limite de tamanho recomendado — 1200 KB para modelos e mensagens, 700 KB para fragmentos e 1000 KB para páginas de destino. As ações Salvar e publicar não estão bloqueadas. [Saiba mais](../start/guardrails.md#content-authoring)

  Data de disponibilidade: 25 de agosto de 2026

* **Limites de contagem de fragmentos no conteúdo**: o Journey Optimizer agora valida o número de fragmentos únicos usados em um conteúdo: até 60 por variante e até 120 em todas as variantes de uma única mensagem. Os avisos são exibidos em 75% de cada limite; a publicação é bloqueada quando o limite rígido é atingido. [Saiba mais](../start/guardrails.md#fragments-guardrails)

  Data de disponibilidade: 25 de agosto de 2026

### Jornadas {#aug-26-journeys}


* **Datas de início e término no cabeçalho da jornada**: quando datas de início e/ou término são configuradas em uma jornada, elas agora são exibidas no cabeçalho da jornada, ao lado do indicador de status. O rótulo exibido se adapta com base no fato de cada data ser futura ou já ter passado. [Leia mais](../building-journeys/journey-properties.md#dates)

  Data de disponibilidade: 20 de agosto de 2026

* **Novas funções de lista no editor de expressão avançado** - Duas novas funções estão disponíveis no editor de expressão avançado: `mergeLists` combina duas listas, com ou sem desduplicação, e `differenceLists` retorna os itens de uma lista que não estão presentes em outra. [Saiba mais](../building-journeys/functions/list-functions.md)

  Data de disponibilidade: 13 de agosto de 2026

* **Otimização de horário de envio na atividade de espera**: a otimização de horário de envio agora está disponível na atividade de espera, permitindo que a IA da Adobe determine o momento ideal para continuar com qualquer atividade downstream. [Saiba mais](../building-journeys/wait-activity.md#sto-wait)

  Data de disponibilidade: 13 de agosto de 2026

### Campanhas {#aug-26-campaigns}

Os recursos e melhorias a seguir foram introduzidos nas Campanhas nesta versão.

<table>
<thead>
<tr>
<th><strong>Anexos PDF personalizados em emails disparados por API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora oferece suporte a até <b>cinco anexos do PDF</b> no total por email em campanhas acionadas por API, incluindo PDFs estáticos e específicos de destinatários. Os arquivos PDF específicos do destinatário são obtidos com segurança da Zona de Aterrissagem de Dados e anexados no momento do envio, com a localização de cada arquivo transmitida diretamente no conteúdo da API. Isso permite que os sistemas de geração de documentos upstream existentes permaneçam em vigor, com o Journey Optimizer lidando com a entrega.</p>
<p>Os casos de uso aceitos incluem faturas, demonstrativos, tíquetes, contratos, etiquetas de envio e documentos semelhantes que variam de acordo com o destinatário. Anexos PDF personalizados estão disponíveis apenas para campanhas de email transacionais acionadas por API e não são aceitos em jornadas ou campanhas orquestradas.</p>
<p>Volumes e tamanhos de anexo maiores são aceitos por meio do complemento de anexo de PDF; para obter mais informações, entre em contato com o representante da Adobe.</p>
<p>Para obter mais informações, consulte a <a href="../email/pdf-attachments.md#personalized-attachments">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 12 de agosto de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Assinaturas de alerta de ciclo de vida por campanha**: agora é possível assinar alertas de ciclo de vida de campanha com suporte para uma única campanha, além da assinatura em nível de sandbox existente. Essas assinaturas permitem monitorar campanhas individuais de alta prioridade sem receber o mesmo alerta para cada campanha na sandbox. [Saiba mais](../reports/alerts.md#subscribe-alerts)

  Data de disponibilidade: 13 de agosto de 2026

### Campanhas orquestradas {#august-26-oc}

As seguintes funcionalidades e melhorias foram introduzidas nas Campanhas orquestradas nesta versão.

<table>
<thead>
<tr>
<th><strong>Suporte a período de silêncio</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode aplicar Períodos de silêncio. Os Períodos de silêncio permitem definir exclusões com base no tempo para evitar que as mensagens sejam enviadas durante períodos específicos, ajudando você a respeitar as preferências do cliente e os requisitos de conformidade em casos de uso da orquestração de campanha.</p>
<p>Para obter mais informações, consulte a <a href="../conflict-prioritization/quiet-hours.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 18 de agosto de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Envio usando ondas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode agendar mensagens de saída para serem entregues em lotes controlados ao longo do tempo. Ideal para campanhas de alto volume ou com prazos restritos, o envio em ondas também favorece uma melhor capacidade de entrega e ajuda a manter uma reputação sólida de remetente, reduzindo o risco de ser sinalizado como spam. </p>
<p>Para obter mais informações, consulte a <a href="../delivery/send-using-waves.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 18 de agosto de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Suporte ao canal LINE (Disponibilidade limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível adicionar ações LINE às campanhas orquestradas. Esta nova atividade permite criar e entregar conteúdo altamente personalizado, incluindo texto, adesivos, imagens, vídeos, dados de localização e mensagens flexíveis avançadas, para envolver seus clientes de maneira integrada na plataforma LINE. Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.</p>
<p>Para obter mais informações, consulte a <a href="../orchestrated/activities/channels.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 12 de agosto de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Capacidade de gerenciar dimensões de destino do perfil**: agora é possível excluir uma Dimensão de destino do perfil ou editar e trocar seu namespace de identidade configurado, fornecendo maior controle e flexibilidade sobre as configurações de dados. [Saiba mais](../orchestrated/target-dimension.md)

  Data de disponibilidade: 18 de agosto de 2026

<!-- * **New public APIs** - New API specifications are now available. These APIs allow you to programmatically create, manage, and trigger orchestrated campaigns, enabling deeper integration with external systems and automation pipelines. Documentation link: TBD -->

* **Personalizar detalhes do remetente de email por destinatário e campanha (Disponibilidade limitada)**: as campanhas orquestradas agora oferecem suporte à personalização dos campos do cabeçalho do email, incluindo nome do remetente, prefixo do endereço de email do remetente, nome do endereço de resposta e endereço de resposta, além do endereço de execução, usando atributos de perfil ou dados relacionais. Isso permite que os detalhes do remetente reflitam o consultor, o local ou a filial relevante para cada destinatário, em vez de encaminhar todos os envios por meio de um único endereço corporativo. Os valores do cabeçalho podem ser definidos no nível do canal e substituídos por campanha usando dados contextuais para obter um controle mais preciso. [Saiba mais](../orchestrated/activities/channels.md#configuration)

  Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada).

  Data de disponibilidade: 18 de agosto de 2026

* **Simplificação da dimensão de destino**: a dimensão de direcionamento ativa agora é mostrada na tela do fluxo de trabalho, para que você possa ver qual dimensão é usada por uma atividade de canal. O fluxo de segmentação de várias entidades é mais simples, pois você não precisa mais de uma atividade Mudar dimensão separada. Além disso, agora você pode escolher explicitamente se as mensagens são enviadas no nível do perfil ou em um nível de dimensão secundário. [Saiba mais](../orchestrated/activities/channels.md#add)

  Data de disponibilidade: 18 de agosto de 2026

### Fidelidade {#aug-26-loyalty}

<table>
<thead>
<tr>
<th><strong>Habilidade do Loyalty Insights</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A Journey Optimizer apresenta o <strong>Loyalty Insights</strong>, uma nova habilidade do CX Co-worker, que faz perguntas sobre o desempenho de desafio e outros dados de programa de fidelidade assimilados nos grupos de campos de Fidelidade do Adobe Experience Platform.</p>
<p>Para obter mais informações, consulte a <a href="../loyalty-challenges/loyalty-coworker-skills.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 31 de agosto de 2026</p>
</td>
</tr>
</tbody>
</table>

### Canais {#august-26-channels}

* **Metadados de execução de atividade ao vivo (executionMetadata)**: as campanhas de atividade ao vivo acionadas por API (Transacional e Marketing) agora oferecem suporte a um campo executionMetadata opcional em cada destinatário. Isso permite anexar dados de chave/valor personalizados, como uma ID de pedido, nível de fidelidade ou código de região, a uma execução. [Saiba mais](../mobile-live/create-mobile-live.md#metadata)

  Data de disponibilidade: 19 de agosto de 2026

* **Complemento de desempenho para taxa de transferência - Push**: um novo modo de mensagens transacionais de alta taxa de transferência está disponível em campanhas acionadas por API. Esse modo é projetado para mensagens transacionais em tempo real de grande escala e aceita até 5.000 transações por segundo com maior disponibilidade. Anteriormente disponível apenas para o canal de email, esse recurso agora também está disponível para o canal de push, para organizações que adquiriram a oferta complementar de Mensagens transacionais com alta taxa de transferência da Adobe. Entre em contato com o representante da Adobe para obter mais informações. [Saiba mais](../campaigns/api-triggered-high-throughput.md)

  Data de disponibilidade: 11 de agosto de 2026

### Configuração {#august-26-configuration}

* **Suporte a várias SANs na geração de CSR para configuração de subdomínio personalizado** - Ao configurar ou migrar um subdomínio personalizado usando o método de delegação Personalizado, a Solicitação de Assinatura de Certificado (CSR) agora é gerada automaticamente com `data.{subdomain}` e `cdn.{subdomain}` como Nomes Alternativos da Entidade (SANs). Anteriormente, o CSR gerado incluía apenas `data.{subdomain}`, exigindo a adição manual de `cdn.{subdomain}` antes do envio para a Autoridade de Certificação. [Saiba mais](../configuration/custom-subdomain-migration.md#send-csr-to-ca)

  Data de disponibilidade: 20 de agosto de 2026

### Tomada de decisão {#decisioning-august}

* **Limite de frequência no nível de posicionamento na Decisão**: as regras de limite de frequência na Decisão agora podem ser segmentadas para posicionamentos individuais, fornecendo controle mais fino sobre a frequência com que uma oferta é exibida em determinada superfície. Dois modos estão disponíveis: **limite específico de posicionamento**, que define um limite que se aplica somente quando a oferta é exibida em um posicionamento selecionado, e **limite por posicionamento**, que aplica um limite independentemente em cada posicionamento em que a oferta é exibida, de modo que cada posicionamento mantém seu próprio contador de limite. Observe que o limite relacionado à disposição não se aplica a ofertas limitadas usando regras baseadas em dados do Adobe Experience Platform. [Saiba mais](../experience-decisioning/items.md#capping)

  Data de disponibilidade: 24 de agosto de 2026

* **Mirror pages em fragmentos visuais**: agora é possível inserir mirror pages em um fragmento visual. Os atributos de decisão são renderizados corretamente no link da mirror page, mesmo quando o fragmento é usado em uma campanha de email que usa a Decisão. A mirror page deve ser adicionada ao fragmento visual antes de o fragmento ser publicado para que os atributos de decisão sejam exibidos. [Saiba mais](../email/message-tracking.md#decisioning-mirror-page)

  Data de disponibilidade: 11 de agosto de 2026

### Designer de email {#august-26-email-designer}

* **Aumentar contagens de colunas sem perder conteúdo no Designer de Email** - Agora é possível aumentar a contagem de colunas de uma estrutura existente — por exemplo, de 2 colunas para 3 — sem excluí-la e perder seu conteúdo. [Saiba mais](../email/content-from-scratch.md)

  Data de disponibilidade: 5 de agosto de 2026

* **Mais opções de posicionamento de imagem de plano de fundo no Email Designer** - Quatro novas opções de posicionamento de imagem estão disponíveis para imagens de plano de fundo: Largura total - Superior, Largura total - Inferior, Altura total - Esquerda e Altura total - Direita. Cada uma dimensiona a imagem proporcionalmente ao longo de um eixo, como as opções existentes de Largura total e Altura total, mas a ancora em uma borda específica em vez de centralizá-la, fornecendo mais controle sobre qual parte de uma imagem principal permanece na exibição. [Saiba mais](../email/backgrounds.md)

  Data de disponibilidade: 4 de agosto de 2026

### Melhorias de usabilidade {#august-26-usability}

* **Várias seleções na nova tela de jornada**: a nova experiência de tela de jornada apresenta uma seleção simplificada de vários nós: mantenha a tecla Shift pressionada e arraste para selecionar vários nós de uma só vez, em vez de selecioná-los individualmente. Isso permite que ações em massa, como copiar, excluir ou salvar como um fragmento de jornada, sejam executadas com eficiência em vários nós. [Saiba mais](../building-journeys/using-the-journey-designer.md#canvas-capabilities)

  Data de disponibilidade: 17 de agosto de 2026

* **Operações em massa no inventário de jornadas**: agora é possível executar novas ações em massa diretamente da lista de inventário de jornadas, agilizando o gerenciamento de várias jornadas de uma só vez. Selecione várias jornadas e aplique qualquer uma destas novas ações em uma única etapa: **adicionar ao pacote**, **excluir**, **mover para a pasta**, **editar tags** ou **gerenciar acesso**. Isso reduz a necessidade de repetir a mesma ação uma jornada por vez, simplificando o gerenciamento de jornadas para equipes que trabalham com um grande número de jornadas. [Saiba mais](../building-journeys/journey-ui.md)

  Data de disponibilidade: 12 de agosto de 2026

* **Nova experiência de Simulação de conteúdo para testes de conteúdo**: o fluxo de trabalho **Simular conteúdo** apresenta uma experiência reprojetada; todas as variantes agora são renderizadas juntas em uma única grade rolável (lado a lado, empilhadas ou com layouts dispostos), substituindo o modo de exibição uma variante de cada vez. Uma única barra de ações na parte inferior consolida a navegação entre variantes de teste, o zoom, a alternância de visualização (desktop/dispositivo móvel), a mudança de localidade, a adição de exemplos de entrada, a geração de variantes com IA, a seleção e o salvamento de usuários simulados, bem como a importação ou exportação de variantes. Remover o painel esquerdo e recolher camadas de cabeçalho extras oferece visualizações com muito mais espaço. A opção **Alternar para experiência clássica** na barra de ação inferior permite reverter para a experiência anterior a qualquer momento. [Saiba mais](../test-approve/simulate-content-variations.md)

  Data de disponibilidade: 11 de agosto de 2026


