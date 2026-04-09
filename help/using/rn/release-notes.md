---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Notas de versão do Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 3076a7ffeeed8224044f1c09b6788c6826638cac
workflow-type: tm+mt
source-wordcount: '2268'
ht-degree: 21%

---

# Notas de versão {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novidades"
>abstract="O **Adobe Journey Optimizer** fornece continuamente novos recursos, melhorias nos recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão."

O [!DNL Adobe Journey Optimizer] segue um modelo de entrega contínua, permitindo que a Adobe forneça novos recursos, melhorias e correções de forma contínua. Essa abordagem permite uma implantação escalável e em fases de recursos para garantir desempenho e estabilidade em todos os ambientes.

Devido a esse modelo, as notas de versão são atualizadas entre as versões mensais. Para obter detalhes completos sobre o ciclo de lançamento e as fases de disponibilidade, consulte o [ciclo de lançamento do Journey Optimizer](releases.md).

O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

## Atualizações de abril de 2026 {#april-26-rn}

### Novos recursos {#april-26-features}

<table>
<thead>
<tr>
<th><strong>Jornada experimentação de caminho</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Use o novo nó <strong>Otimizar</strong> para executar testes A/B ou experimentos de bandit com vários braços para determinar o melhor caminho para atender aos KPIs centrados nos negócios. Essa ferramenta permite testar, variar e personalizar as comunicações, o sequenciamento e o momento para melhor alcançar os clientes.
</p>
<p>Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<p>Como parte da Disponibilidade Geral, esta versão introduz a seleção <strong>tipo de experimento</strong> (A/B ou bandit de vários braços) e <strong>Dimensione o vencedor</strong> para jornadas unitárias.</p>
<p><img src="assets/do-not-localize/optimize-experiment.gif"></p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/path-experimentation.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: quarta-feira, 7 de abril de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Caixa de entrada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A <strong>Caixa de Entrada</strong> é uma funcionalidade móvel, disponível com Cartões de Conteúdo, que permite aos clientes criar um local centralizado no aplicativo ou site para exibir mensagens enviadas aos usuários. Isso estende a vida útil das comunicações de marketing, garantindo que as mensagens permaneçam acessíveis mesmo após serem descartadas.</p>
<p><img src="assets/do-not-localize/inbox.gif"/></p>
<p>Para obter mais informações, consulte a <a href="../inbox/inbox-gs.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: quarta-feira, 7 de abril de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Otimizar texto de email para caixas de entrada de IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Adobe Journey Optimizer agora inclui um novo recurso que garante que seus emails sejam estruturados de maneira ideal para caixas de entrada alimentadas por IA, como o Apple Intelligence e o Google Gemini no Gmail.</p>
<p>Como os assistentes de IA controlam cada vez mais como os recipients leem e agem no email, esse recurso ajuda a criar conteúdo que tenha bom desempenho em tarefas de IA de downstream, incluindo resumo, triagem, priorização e extração de intenção.</p>
<p><img src="assets/do-not-localize/text-optimizer.gif"></p>
<p>Para obter mais informações, consulte <a href="../email/llm-email-optimizer.md">Otimizar texto de email para caixas de entrada de IA</a>.</p>
<p>Data de disponibilidade: sábado, 3 de abril de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Suporte à decisão no canal de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode usar a <strong>Decisão</strong> para personalizar e otimizar o conteúdo de suas mensagens de email. Aproveite as Pontuações de prioridade, as Fórmulas ou os Modelos de IA para exibir as ofertas e o conteúdo mais relevantes para cada recipient.</p>
<p>Anteriormente lançado com disponibilidade limitada, esse recurso agora está disponível para todos os ambientes (disponibilidade geral). Com esta versão de Disponibilidade geral, as mirror pages agora são compatíveis.</p>
<p><img src="assets/do-not-localize/exd-email.gif"></p>
<p>Para obter mais informações, consulte a <a href="../experience-decisioning/create-decision-policy.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: terça-feira, 6 de abril de 2026</p>
</td>
</tr>
</tbody>
</table>

### Aprimoramentos {#april-26-improv}

#### Otimização do caminho de Jornada

* **Tipo de experimento** - Agora é possível escolher entre um experimento A/B (divisão fixa no início) ou um bandit multicampo (divisão automática com atualizações de peso semanais) ao configurar um experimento de caminho. [Leia mais](../building-journeys/path-experimentation.md)

  Data de disponibilidade: quarta-feira, 7 de abril de 2026

* **Experimentação de caminho: dimensionar o vencedor** - Agora é possível implantar automática ou manualmente o caminho vencedor de um experimento em todo o seu público-alvo. Uma vez determinado o vencedor, você pode ampliar seu alcance e eficácia sem monitorar constantemente o experimento. [Leia mais](../building-journeys/path-experimentation.md#scale-winner)

  Esse recurso está disponível somente em jornadas unitárias (acionadas por eventos e qualificações de Público-alvo). Não está disponível para jornadas Read audience.

  Data de disponibilidade: quarta-feira, 7 de abril de 2026

* **Condições** - A atividade [Otimizar](../building-journeys/optimize.md) é o novo veículo para a criação de caminhos condicionais no jornada. Substitui a antiga atividade **Condição**, que foi removida da interface do usuário. Toda lógica condicional é retida e agora é tratada por meio das condições da atividade **Otimizar**. [Leia mais](../building-journeys/conditions.md)

  Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).

  Data de disponibilidade: quarta-feira, 7 de abril de 2026

<!--
* **Adobe Experience Manager Content Fragment context while authoring** - Your Content Fragment selection stays active as you move between text fields and content blocks, so you can add more fragment fields without reopening **Open AEM Content advisor** each time. [Read more](../integrations/aem-fragments.md)

  Availability date: April 1, 2026
-->

#### Integrações do Adobe Experience Manager

* **Suporte à variação de fragmento de conteúdo do Adobe Experience Manager** - Você pode selecionar **variações de fragmento de conteúdo** (por exemplo, variantes de idioma ou canal) ao inserir fragmentos de conteúdo do Adobe Experience Manager, com manipulação aprimorada para localidade e cenários multilíngues. [Leia mais](../integrations/aem-fragments.md#aem-variations)

  Data de disponibilidade: sábado, 3 de abril de 2026


## Notas de versão de março de 2026 {#march-26-rn}

As seções [Novos recursos](#march-26-features) e [Melhorias](#march-26-improv) abordam recursos já disponíveis. A seção [Em breve](#coming-soon) lista os recursos e as melhorias agendadas para lançamento no final de março.

<!--
**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform pre-release notes](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.
-->

**Data de lançamento**: 24 a 25 de março de 2026

### Novos recursos {#march-26-features}

<table>
<thead>
<tr>
<th><strong>Criptografia de parâmetro de URL</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Os parâmetros de URL em links de rastreamento e de página de aterrissagem adicionados às suas mensagens de email agora podem ser criptografados, fornecendo uma camada adicional de segurança para dados de parâmetros confidenciais.</p>
<ul>
<li>Registre e gerencie chaves de criptografia no Registro <strong>Administração</strong> dedicado.</li>
<li>Use a nova função auxiliar "Encrypt" em expressões para criptografar dados confidenciais em URLs para os parâmetros de consulta que você deseja proteger no momento da renderização.</li>
</ul>
<p>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.</p>
<p><img src="assets/do-not-localize/encrypt-helper.gif"></p>
<p>Para obter mais informações, consulte a <a href="../personalization/url-parameter-encryption.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: quarta-feira, 31 de março de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Converter imagens em modelos de conteúdo de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível converter imagens em modelos de conteúdo de email diretamente no Journey Optimizer. Use a análise baseada em IA para gerar automaticamente modelos estruturados do HTML a partir de referências visuais, reduzindo significativamente o tempo de design de email.</p>
<p>Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<p><img src="assets/do-not-localize/image-converter.gif"></p>
<p>Para obter mais informações, consulte a <a href="../content-management/image-to-html.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: quarta-feira, 31 de março de 2026</p>
</td>
</tr>
</tbody>
</table>
<table>
<thead>
<tr>
<th><strong>Caixa de entrada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A <strong>Caixa de Entrada</strong> é uma funcionalidade móvel, disponível com Cartões de Conteúdo, que permite aos clientes criar um local centralizado no aplicativo ou site para exibir mensagens enviadas aos usuários. Isso estende a vida útil das comunicações de marketing, garantindo que as mensagens permaneçam acessíveis mesmo após serem descartadas.</p>
<p><img src="assets/do-not-localize/inbox.gif"/></p>
<p>Para obter mais informações, consulte a <a href="../inbox/inbox-gs.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: quarta-feira, 31 de março de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Formulários personalizados de página de destino</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Com o [!DNL Journey Optimizer], você pode capturar atributos de perfil por meio das páginas de aterrissagem.</p>
<p>Crie, projete e gerencie formulários personalizados adaptados às suas necessidades com base em um conjunto de dados específico. Em seguida, é possível usar esses formulários em páginas de destino para adicionar os atributos de perfil de sua escolha ao conjunto de dados definido para cada formulário.</p>
<p>Anteriormente lançado com disponibilidade limitada para clientes nos Estados Unidos e na Austrália, esse recurso agora está disponível para todos os ambientes (disponibilidade geral).</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>Para obter mais informações, consulte a <a href="../landing-pages/lp-forms.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: sexta-feira, 26 de março de 2026.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Atividade de teste em campanhas orquestradas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Uma nova atividade <strong>Test</strong> está disponível em Campanhas Orquestradas. Essa atividade roteia a execução do fluxo de trabalho para diferentes ramificações com base em condições definidas, permitindo validar a lógica e as configurações da campanha antes de ativar os deliveries ativos.</p>
<p><img src="../orchestrated/assets/test-1.png"></p>
<p>Para obter mais informações, consulte a <a href="../orchestrated/activities/test.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Suporte à pesquisa de conjunto de dados no jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Uma nova atividade de <strong>Pesquisa de conjunto de dados</strong> no jornada permite recuperar dinamicamente dados de conjuntos de dados de registros Adobe Experience Platform no tempo de execução, fornecendo acesso a informações que não fazem parte do perfil ou da carga do evento, de modo que as interações com o cliente permaneçam relevantes e oportunas.</p>
<p>Anteriormente lançada em Disponibilidade limitada para um conjunto restrito de organizações, a atividade de pesquisa do conjunto de dados no jornada agora está disponível para todos os clientes autorizados a [pesquisa do conjunto de dados](../data/lookup-aep-data.md), enquanto permanece em Disponibilidade limitada.</p>
<p><img src="../building-journeys/assets/aep-data-activity.png"></p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/dataset-lookup.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>A atividade Action substitui atividades de jornada específicas do canal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Após a Disponibilidade geral da <strong>Atividade de ação</strong> em fevereiro de 2026, as atividades de canal nativas herdadas (Email, Push, SMS, No aplicativo, Web, Experiência baseada em código e Cartão de conteúdo) na tela de jornada foram descontinuadas.</p>
<p>Agora você deve usar a atividade única Action para configurar todas as ações de canal, substituindo a necessidade de nós específicos do canal separados.</p>
<p>As jornadas existentes que usam atividades de canal herdadas continuam a funcionar sem nenhuma alteração ou migração necessária.</p>
<p><img src="assets/do-not-localize/action-activity.gif"></p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/journey-action.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Editor avançado do HTML para modelos de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O modo HTML avançado para modelos de conteúdo de email permite editar a origem de HTML do seu conteúdo no Designer de email, adicionar expressões avançadas (como condições) na origem e alternar entre a exibição do HTML e a exibição da área de trabalho sem perder as alterações.</p>
<p>Esse recurso está disponível em modelos de conteúdo somente para o canal de email. No momento, a disponibilidade é limitada — entre em contato com o representante da Adobe para obter acesso.</p>
<p><img src="assets/do-not-localize/expert-mode.gif"/></p>
<p>Para obter mais informações, consulte a <a href="../content-management/email-template-expert-mode.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: quarta-feira, 10 de março de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integração de modelos personalizados do Firefly e modelos de geração de imagens de terceiros</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Permita a integração perfeita de modelos Firefly padrão e personalizados, juntamente com modelos de imagem de terceiros aprovados, para oferecer maior flexibilidade, controle e alinhamento de marca ao gerar imagens.</p>
<p>Escolha o modelo certo para suas necessidades:</p>
<ul><li> <strong>Modelo do Adobe</strong> (desenvolvido pela Firefly Image Model 4) para geração imediata de imagens sem configuração adicional</li><li> <strong>Modelo de parceiro</strong> (viabilizado pelo Gemini 2.5 Flash) para recursos especializados</li><li><strong>Modelos personalizados</strong> (modelos específicos da marca treinados em seus próprios ativos) para geração de itens sob marca que se alinham precisamente à identidade, ao estilo e às diretrizes visuais da sua marca.</li></ul>
<p>Para obter mais informações, consulte a <a href="../content-management/generative-models.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: terça-feira, 2 de março de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Atividade online para iOS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Traga experiências em tempo real diretamente para o Lock Screens e Dynamic Island de seus clientes com a <strong>Atividade do iOS Live</strong> no Adobe Journey Optimizer. Forneça atualizações em tempo real, desde o rastreamento de pedidos e o status do voo até a contagem regressiva de eventos, pontuações em tempo real e o progresso do delivery, sem exigir que os usuários abram seu aplicativo. Mantenha seu público informado e engajado no momento exato, exatamente onde eles estão.</p>
<p>Anteriormente lançado na versão beta, esse recurso agora está disponível para todos os ambientes (Disponibilidade geral).</p>
<p>Para obter mais informações, consulte a <a href="../mobile-live/get-started-mobile-live.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: quarta-feira, 3 de março de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent: criação de conteúdo de canal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Com a tecnologia <strong>Adobe Experience Platform Agent Orchestrator</strong>, o <strong>Journey Agent</strong> está disponível no Journey Optimizer e permite que você analise jornadas por meio de uma interface de linguagem natural. Agora você também pode gerar e gerenciar conteúdo específico de canal diretamente no Journey Agent, criando conteúdo para canais como email e push, aplicando e visualizando modelos, refinando o tom e o estilo por meio de prompts e abrindo conteúdo no <strong>Content Designer</strong> para edição em contexto.</p>
<p>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.</p>
<p>Para obter mais informações, consulte a <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent.html?lang=pt-BR" target="_blank">documentação detalhada</a>.</p>
<p>Data de disponibilidade: quinta-feira, 4 de março de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Monitoramento do modelo de IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora permite monitorar a integridade, o status do treinamento e o desempenho dos modelos de IA de decisão. Isso permite verificar o sucesso do treinamento, solucionar problemas de falhas e entender o impacto em seus resultados, a fim de selecionar as melhores ofertas para cada cliente que usa a IA. Observe que esse recurso está disponível somente para <strong>Decisão</strong> (não para modelos herdados do Gerenciamento de decisões).</p>
<p>Este recurso está disponível atualmente apenas para <strong>modelos de otimização personalizada</strong> (não de otimização automática).</p>
<p><img src="assets/do-not-localize/ai-model-observability.gif"/></p>
<p>Para obter mais informações, consulte a <a href="../experience-decisioning/ranking/ai-model-observability.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: terça-feira, 9 de março de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Acionar campanhas orquestradas usando um sinal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As campanhas orquestradas agora podem ser acionadas por meio de um <strong>sinal de API</strong>. Para configurar isso, configure a campanha do target como <strong>Acionada por um sinal</strong>, publique-a e acione-a usando uma chamada de API. Todos os parâmetros incluídos na chamada da API estão disponíveis como variáveis na campanha em execução. Observe que as campanhas orquestradas acionadas por sinal permanecem <strong>campanhas em lote</strong> e são distintas das campanhas acionadas por API.</p>
<p><img src="assets/do-not-localize/oc-triggered.gif"></p>
<p>Para obter mais informações, consulte a <a href="../orchestrated/trigger-orchestrated-campaign.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Categoria transacional em campanhas orquestradas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Em Campanhas orquestradas, agora é possível definir uma atividade de canal para a categoria <strong>Transacional</strong>. Isso aplica configurações de canal transacional a essa atividade e é útil quando as regras de negócios não devem se aplicar ou quando a aceitação dos clientes não é necessária.</p>
<p><img src="assets/do-not-localize/oc-transactional.gif"></p>
<p>Para obter mais informações, consulte a <a href="../orchestrated/activities/channels.md#add">documentação detalhada</a>.</p>
<p>Esse recurso será gradualmente distribuído a todas as regiões nos próximos dias.</p>
</td>
</tr>
</tbody>
</table>

### Aprimoramentos {#march-26-improv}

Os aprimoramentos incluídos nesta versão estão listados abaixo.

#### Personalização

* **Personalização completa/básica da URL** - Você pode personalizar URLs de destino usando atributos de perfil (por exemplo, para o domínio ou caminho). Para ativar esse recurso, forneça à Adobe sua lista de domínios aceitos. [Leia mais](../personalization/personalization-build-expressions.md#where)

  Anteriormente lançado com disponibilidade limitada para uso no jornada, esse recurso agora está disponível para todos os ambientes (disponibilidade geral).

  Data de disponibilidade: quinta-feira, 1 de abril de 2026

#### Relatórios

* **Otimização de Tempo de Envio: a localização dos controles atualizados e o novo relatório de aumento** - os controles de Otimização de Tempo de Envio (STO) foram realocados para o menu de configuração Ação. Além disso, um novo relatório de aumento está disponível nos relatórios do Jornada para medir o impacto do STO nas métricas de desempenho da campanha. [Leia mais](../reports/channel-report-cja.md#optimization-models)

  Data de disponibilidade: sábado, 27 de março de 2026

<!--
* **Exclude bot clicks for email and SMS reporting** - Email and SMS reporting now automatically filters out bot clicks from click metrics, providing more accurate engagement data and preventing automated traffic from inflating your performance figures.

#### Email Designer

* **Email Designer displayed in Unified Shell** - The Email Designer is now displayed within the Unified Shell experience, providing a consistent navigation and header experience that aligns with other Adobe applications.

* **Text mode support in fragments** - To support text-based email workflows, you can now create and manage text versions of your visual fragments for optimal use in the plain text version of emails that include that fragment.

  **Caution:** When using a fragment that was created before the current release, the fragment text version may be incorrectly rendered—both in the Email Designer and in the final email delivered to your recipients. For best results with older fragments, edit, save and republish each fragment.
-->
<!--
#### Decisioning

* **Optional fragments in decision items** - When using fragments in decision items, you can now make a fragment optional so that if it is temporarily unavailable on Edge, it is skipped and the journey or campaign continues rendering instead of failing.
-->

#### Configuração

<!--* **Folders for journeys and campaigns** - You can now organize your journeys and campaigns into folders, enabling structured navigation and easier management for teams working with large volumes of content. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.-->

* **Renovação de certificados de domínio do AJO mal sucedida** - Agora você pode assinar para receber alertas do sistema, por email ou na central de notificações da Journey Optimizer, quando um certificado de domínio usado para entrega de email estiver perto de expirar ou já tiver expirado. [Leia mais](../reports/alerts.md#alert-certificates-renewal-unsuccessful)

  Data de disponibilidade: sexta-feira, 26 de março de 2026

* **Conjunto de Dados do Evento de Feedback de Destinatário Secundário do AJO renomeado** - O Conjunto de Dados `AJO Email BCC Feedback Event` foi renomeado para Conjunto de Dados `AJO Secondary Recipient Feedback Event`. O impacto varia dependendo da sua situação:

   * **Usuários existentes**: somente o nome para exibição é atualizado. O nome da tabela subjacente permanece inalterado.
   * **Novos usuários e sandboxes**: o nome de exibição e o nome da tabela refletem o novo nome.
   * **Usuários existentes com novas sandboxes**: o nome de exibição e o nome da tabela são atualizados para o novo nome.

  >[!NOTE]
  >
  >Novos conjuntos de dados mostram o novo nome imediatamente. Para nomes mais antigos de conjuntos de dados, o preenchimento retroativo e a reconciliação acontecem gradualmente e podem levar várias semanas para serem concluídos.

  Data de disponibilidade: terça-feira, 2 de março de 2026


#### Jornadas

* **Ação Atualizar Perfil: suporte para vários atributos de perfil** - A atividade de ação **Atualizar Perfil** agora oferece suporte à atualização de até cinco atributos de perfil em um único nó. Anteriormente, cada ação só podia atualizar um atributo por vez, o que exigia que vários nós atualizassem vários atributos. Use o novo botão **Atualizar outro campo** para adicionar outros pares de campo/valor, reduzindo a complexidade da tela e melhorando o desempenho. [Saiba mais](../building-journeys/update-profiles.md)

* **Envio de mensagens de saída em ondas no jornada** - Agora é possível agendar mensagens do Journey Optimizer jornada para serem entregues em lotes controlados ao longo do tempo. [Saiba mais](../building-journeys/send-using-waves.md)

  Anteriormente lançado com disponibilidade limitada para uso no jornada, esse recurso agora está disponível para todos os ambientes (disponibilidade geral).

  Data de disponibilidade: terça-feira, 16 de março de 2026

* **Detalhes de pausa e retomada nos detalhes técnicos da jornada** - Os **detalhes técnicos** da jornada agora incluem informações adicionais de pausa e retomada: a data e a hora da última pausa e retomada, o nome para exibição e o identificador interno do usuário que executou cada ação e um conjunto completo de configurações de jornada pausadas, como comportamento de pausa, duração máxima da pausa e estado de retomada automática. [Saiba mais](../building-journeys/journey-properties.md)

  Data de disponibilidade: terça-feira, 2 de março de 2026

#### Tomada de decisão

* **Migração de decisão — oferta e atributos de contexto** - O mapeamento de entidade da API de migração agora lista **atributos de oferta** (`migratedofferattributes` no esquema de item de oferta personalizada) e **atributos de contexto** (`migratedcontextattributes` no esquema de conjunto de dados de migração). [Leia mais](../experience-decisioning/decisioning-migration-api.md#entity-mapping)

  Data de disponibilidade: quarta-feira, 31 de março de 2026

<!--
## Coming soon {#coming-soon}

The features and improvements below are planned for release later in March/early April. Release dates and scope are **subject to change without prior notice**.


WAITING RELEASE DATE CONFIRMATION * **Target dimension simplification in Orchestrated Campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.


WAITING RELEASE DATE CONFIRMATION
* **Target dimension simplification in Orchestrated Campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.
-->

