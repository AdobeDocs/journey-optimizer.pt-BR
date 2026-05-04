---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Notas de versão do Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: d975d9cd95d33ea8972cf9388e7f868009c4fb95
workflow-type: tm+mt
source-wordcount: '1990'
ht-degree: 20%

---

# Notas de versão {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novidades"
>abstract="O **Adobe Journey Optimizer** fornece continuamente novos recursos, melhorias nos recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão."

O [!DNL Adobe Journey Optimizer] segue um modelo de entrega contínua, permitindo que a Adobe forneça novos recursos, melhorias e correções de forma contínua. Essa abordagem permite uma implantação escalável e em fases de recursos para garantir desempenho e estabilidade em todos os ambientes.

Devido a esse modelo, as notas de versão são atualizadas entre as versões mensais. Para obter detalhes completos sobre o ciclo de lançamento e as fases de disponibilidade, consulte o [ciclo de lançamento do Journey Optimizer](releases.md).

O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

## Notas de versão de abril de 2026 {#april-26-rn}

<!--
**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.
-->

Os novos recursos e aprimoramentos lançados no início de abril são anunciados com a data de disponibilidade.

**Data de lançamento**: 28 a 29 de abril de 2026

### Novos recursos {#april-26-features}

<table>
<thead>
<tr>
<th><strong>Integrações</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O recurso <b>Integrações</b> permite conectar fontes de dados de terceiros diretamente ao Adobe Journey Optimizer. Ao simplificar a forma como você obtém dados externos e <b>conteúdo de composição</b>, esse recurso facilita a entrega de mensagens personalizadas e dinâmicas em todos os canais.</p>
<p>Anteriormente lançado na versão beta, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<p>Para obter mais informações, consulte a <a href="../integrations/integrations.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 4 de maio de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Atividade de query incremental em campanhas orquestradas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>As campanhas orquestradas</strong> agora oferecem suporte a uma atividade de <strong>Consulta incremental</strong> que segmenta somente perfis ou eventos que são recém-qualificados desde a última execução.

Isso mantém as campanhas recorrentes focadas nos novos públicos-alvo (novas inscrições, membros de fidelidade recém-qualificados e segmentos semelhantes), reduzindo as cargas de trabalho de consulta e evitando envios redundantes ao longo do tempo.</p>
<p>Para obter mais informações, consulte a <a href="../orchestrated/activities/incremental-query.md#incremental-query-configuration">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Parâmetros de remetente no cabeçalho do email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Com o Journey Optimizer, agora é possível enviar emails em que a entidade de transmissão (Remetente) difere da entidade de criação (De). Os clientes de email que oferecem suporte a isso normalmente o renderizarão como "Remetente em nome de De" ou exibirão um indicador "via". Preencha os campos opcionais <strong>Cabeçalhos do remetente</strong> nas configurações do canal de email para configurar este recurso.</p>
<p><img src="assets/do-not-localize/sender-headers.gif"></p>
<p>Para obter mais informações, consulte a <a href="../email/header-parameters.md#sender-header">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Campo CC nas configurações do canal de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode configurar um campo CC (cópia carbono) opcional nas configurações de canal de email. Ao contrário do Cco, os recipients do CC estão visíveis para o recipient principal, permitindo comunicação transparente e propriedade mais clara.</p>
<p>Isso permite copiar automaticamente a parte interessada certa em cada mensagem, como um gerente de relacionamento ou proprietário de conta, garantindo que o cliente saiba com quem entrar em contato para obter acompanhamento.</p>
<p>O campo CC oferece suporte à personalização, de modo que uma única configuração pode rotear cópias dinamicamente com base nos dados do perfil, tornando-o escalável em vários casos de uso sem configuração adicional.</p>
<p><img src="../configuration/assets/email-config-cc.png"></p>
<p>Para obter mais informações, consulte a <a href="../configuration/cc-email-field.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Copiar campanhas orquestradas em sandboxes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As ferramentas de sandbox agora permitem empacotar e copiar campanhas orquestradas de uma sandbox para outra. Isso elimina a necessidade de reconstruir manualmente as campanhas em cada ambiente. Quando uma campanha é empacotada, seus principais objetos dependentes, como políticas de mesclagem, mensagens, são incluídos automaticamente, de modo que a campanha importada chega pronta para configuração e validação. Para proteger ambientes de produção, todas as campanhas importadas são enviadas com o status de rascunho na sandbox de destino, dando às equipes uma etapa de revisão e aprovação antes de qualquer campanha entrar em vigor.</p>
<p><img src="assets/do-not-localize/oc-sandbox.gif"></p>
<p>Para obter mais informações, consulte a <a href="../configuration/copy-objects-to-sandbox.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integração do Journey Optimizer AI Agent via MCP</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A Adobe Journey Optimizer agora fornece um <strong>servidor MCP (Model Context Protocol)</strong> que revela operações de campanha, configuração de canal e sandbox diretamente dentro de qualquer aplicativo compatível com MCP. Com essa integração, diferentes personalidades podem colaborar em torno dos mesmos dados de orquestração. Em vez de escrever consultas na API REST do Adobe Journey Optimizer ou navegar por várias telas de interface do usuário, você pode descrever sua intenção em conversação e permitir que o LLM chame as ferramentas de MCP apropriadas. Esse recurso está disponível atualmente no Claude Web e Desktop.</p>
<p>Esse recurso está disponível para todos os clientes no Public Beta.</p>
<p>Para obter mais informações, consulte a <a href="../integrations/ajo-mcp.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Arbitragem de Jornada - Modelos de IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode usar <strong>modelos de IA</strong> nas fórmulas de classificação para aumentar automaticamente as pontuações de prioridade de jornada com base nos atributos do perfil do cliente e em fatores contextuais, garantindo que os clientes insiram as jornadas mais relevantes.</p>
<p>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.</p>
<p><img src="assets/do-not-localize/journey-arbitration-ai-models.gif"></p>
<p>Para obter mais informações, consulte a <a href="../conflict-prioritization/journey-ai-models.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integração do Adobe Express</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A <b>integração do Adobe Express</b> no Adobe Journey Optimizer permite que você use as ferramentas de edição da Adobe Express diretamente durante a criação do conteúdo, permitindo que você redimensione, remova planos de fundo, corte e converta ativos em JPEG ou PNG.
</p>
<p>Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<p><img src="assets/do-not-localize/express_resize.gif"></p>
<p>Para obter mais informações, consulte a <a href="../integrations/express.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 23 de abril de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Otimizar email para caixas de entrada de IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Adobe Journey Optimizer agora inclui um novo recurso que garante que seus emails sejam estruturados de maneira ideal para caixas de entrada alimentadas por IA, como o Apple Intelligence e o Google Gemini no Gmail.</p>
<p>Como os assistentes de IA controlam cada vez mais como os recipients leem e agem no email, esse recurso ajuda a gerar e criar conteúdo que tenha bom desempenho em tarefas de IA de downstream, incluindo resumo, triagem, priorização e extração de intenção.</p>
<p><img src="assets/do-not-localize/optimize-for-ai.gif"></p>
<p>Para obter mais informações, consulte <a href="../email/llm-email-optimizer.md">Otimizar email para caixas de entrada de IA</a>.</p>
<p>Data de disponibilidade: 17 de abril de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Assistente de IA para expressões Personalization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>[!DNL Adobe Journey Optimizer] agora inclui o <strong>Assistente de IA</strong> diretamente no editor de personalização e no Designer de email, que converte prompts de linguagem natural em expressões de personalização e lógica condicional válidas, sem a necessidade de conhecimento especializado sobre sintaxe. Descreva a personalização que deseja realizar e a IA gera um código pronto para uso que pode ser aplicado imediatamente ou refinado por meio de prompts de acompanhamento.</p>
<p>O assistente também trabalha de forma inversa. Selecione qualquer expressão existente e solicite que ela explique a lógica, identifique problemas ou sugira melhorias. Isso o torna útil não apenas para a criação de novas expressões, mas para revisar e depurar as existentes na sua equipe.</p>
<p><img src="assets/do-not-localize/assistant-perso.gif"></p>
<p>Para obter mais informações, consulte o <a href="../content-management/generative-personalization-expressions.md">Assistente de IA para expressões Personalization</a>.</p>
<p>Data de disponibilidade: 13 de abril de 2026</p>
</td>
</tr>
</tbody>
</table>

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
<p>Data de disponibilidade: 7 de abril de 2026</p>
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
<p>Data de disponibilidade: 7 de abril de 2026</p>
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
<p>Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral). Com esta versão de Disponibilidade geral, as mirror pages agora são compatíveis.</p>
<p><img src="assets/do-not-localize/exd-email.gif"></p>
<p>Para obter mais informações, consulte a <a href="../experience-decisioning/create-decision-policy.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 6 de abril de 2026</p>
</td>
</tr>
</tbody>
</table>

### Aprimoramentos {#april-26-improv}

<!--
#### AI

* **Brand alignment score in Campaign dashboard** - You can now assess your brand alignment score directly within your Campaign dashboard to ensure content stays on-brand. This allows you to verify guidelines at a glance without having to open the content designer.

* **Prompt Assistant enhancement** - Prompt Assistant enhances AI content generation by analyzing user prompts in real time and identifying gaps in clarity, completeness, and context. It suggests improved rewrites and provides actionable guidance to enrich prompts with key details like audience, tone, and intent. The feature also asks targeted clarifying questions to help users refine their inputs before generation. This results in more accurate, high-quality outputs with fewer iterations. [Learn more](../content-management/ai-assistant-prompting-guide.md)
-->

#### Push

* **Personalizar ID do aplicativo nas configurações do canal** - Nas configurações do canal de push, agora é possível personalizar o campo **ID do aplicativo** para que cada destinatário possa receber uma notificação por push da marca apropriada com base nas informações do perfil. [Leia mais](../push/push-configuration.md#app-id-personalization)

#### Tomada de decisão

* **Anexar fragmentos a itens de decisão** - O Journey Optimizer agora oferece a capacidade de anexar fragmentos a itens de decisão, que podem ser aproveitados em campanhas de email e experiências baseadas em código por meio de políticas de decisão. [Leia mais](../experience-decisioning/fragments-decision-policies.md)

  Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).

* **Fragmentos temporariamente indisponíveis são ignorados** - Ao usar fragmentos em itens de decisão, se um fragmento estiver temporariamente indisponível no Edge, ele será ignorado e a jornada ou campanha continuará a ser renderizada em vez de falhar. [Leia mais](../experience-decisioning/fragments-decision-policies.md#temporary-unavailable-fragments)

  Data de disponibilidade: 14 de abril de 2026

<!--
#### SMS

* **Character Count** - In Adobe Journey Optimizer, you can now use the Character Count to monitor the length of your SMS messages in real time. It helps you see when a message will be split into multiple segments to better manage formatting and avoid unexpected increases in sending costs. [Read more](../sms/create-sms.md)

* **Opt-out and consent at phone number and sender** - For SMS, Journey Optimizer now records marketing consent and opt-out at the level of both the profile's phone number and short code. 

  This capability is currently only available for Sinch SMS configurations. [Read more](../sms/sms-configuration-sinch.md)

* **SMS inbounds to a custom dataset** - In **SMS API credentials**, route **inbound SMS** to a **custom, profile-enabled Experience Event dataset** you select instead of only the default tracking dataset. [Read more](../sms/sms-webhook.md)

* **Webhook interface enhancement** - When configuring SMS webhooks, the user interface now includes a built-in setup guide with practical examples, making it easier to align provider payloads and troubleshoot issues without leaving the configuration flow. [Read more](../sms/sms-webhook.md)

#### WhatsApp

* **WhatsApp interactive buttons and tracking** - WhatsApp in Journey Optimizer now supports interactive buttons required by your templates and use cases, along with built-in interaction tracking so you can measure engagement and analyze performance alongside your other channel reporting.
-->

#### Integrações do Adobe Experience Manager

* **Suporte à variação de fragmento de conteúdo do Adobe Experience Manager** - Você pode selecionar **variações de fragmento de conteúdo** (por exemplo, variantes de idioma ou canal) ao inserir fragmentos de conteúdo do Adobe Experience Manager, com manipulação aprimorada para localidade e cenários multilíngues. [Leia mais](../integrations/aem-fragments.md#aem-variations)

  Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).

* **Contexto de Fragmento de conteúdo do Adobe Experience Manager durante a criação** - Sua seleção de Fragmento de conteúdo permanece ativa à medida que você se move entre campos de texto e blocos de conteúdo, para que você possa adicionar mais campos de fragmento sem reabrir o **Abrir o AEM Content advisor** toda vez. [Leia mais](../integrations/aem-fragments.md)

  Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).

#### Design de email

* **Editor avançado de HTML para conteúdo de email** - O modo Avançado de HTML permite editar a fonte HTML do seu conteúdo no Designer de email, adicionar expressões avançadas (como condições) na fonte e alternar entre o modo de exibição HTML e o modo de exibição Desktop sem perder as alterações.

  Disponível anteriormente somente para modelos de conteúdo de email, esse recurso agora está implantado no conteúdo de **email** no Designer de email (por exemplo, emails criados em jornadas e campanhas), além de modelos de conteúdo de email. No momento, a disponibilidade é limitada — entre em contato com o representante da Adobe para obter acesso. [Leia mais](../email/email-expert-mode.md)

  Data de disponibilidade: 9 de abril de 2026

#### Otimização do caminho de Jornada

* **Tipo de experimento** - Agora é possível escolher entre um experimento A/B (divisão fixa no início) ou um bandit multicampo (divisão automática com atualizações de peso semanais) ao configurar um experimento de caminho. [Leia mais](../building-journeys/path-experimentation.md)

  Data de disponibilidade: 7 de abril de 2026

* **Experimentação de caminho: dimensionar o vencedor** - Agora é possível implantar automática ou manualmente o caminho vencedor de um experimento em todo o seu público-alvo. Uma vez determinado o vencedor, você pode ampliar seu alcance e eficácia sem monitorar constantemente o experimento. [Leia mais](../building-journeys/path-experimentation.md#scale-winner)

  Esse recurso está disponível somente em jornadas unitárias (acionadas por eventos e qualificações de Público-alvo). Não está disponível para jornadas Read audience.

  Data de disponibilidade: 7 de abril de 2026

* **Condições** - A atividade [Otimizar](../building-journeys/optimize.md) é o novo veículo para a criação de caminhos condicionais no jornada. Substitui a antiga atividade **Condição**, que foi removida da interface do usuário. Toda lógica condicional é retida e agora é tratada por meio das condições da atividade **Otimizar**. [Leia mais](../building-journeys/conditions.md)

  Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).

  Data de disponibilidade: 7 de abril de 2026

#### Campanhas orquestradas

* **Variáveis globais em Campanhas orquestradas** - As Campanhas orquestradas agora oferecem suporte a variáveis globais que podem ser definidas uma vez e reutilizadas em todas as atividades de um fluxo de trabalho, simplificando a configuração e garantindo a consistência em valores dinâmicos, expressões e personalização de conteúdo. [Leia mais](../orchestrated/global-variables.md)
* **Aprimoramentos do Data Modeler** - Os esquemas relacionais orquestrados agora oferecem suporte a chaves compostas que abrangem vários campos. O carregamento de um esquema de um arquivo DDL também traz enumerações, e o carregamento de um arquivo DDL ou do Excel cria automaticamente relações compostas entre as tabelas. Na visualização de relacionamento da entidade, os links compostos agora exibem o conjunto completo de pares de campos entre tabelas depois que um arquivo é carregado. [Leia mais](../orchestrated/gs-schemas.md)

## Em breve {#coming-soon}

Os recursos e aprimoramentos a seguir estão programados para serem lançados nos próximos dias. **As informações estão sujeitas a alterações**. Links, telas e documentação atualizados serão compartilhados assim que essas atualizações estiverem ativas na produção.

### Novos recursos {#comming-soon-features}

<table>
<thead>
<tr>
<th><strong>Simulação de jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode definir sua jornada como <strong>Simulação</strong>. Este modo permite validar sua lógica usando <strong>usuários simulados</strong>. Esses são perfis temporários criados especificamente para a simulação, permitindo que você teste livremente sem precisar gerenciar perfis de teste persistentes no Adobe Experience Platform.</p>
<p>Esse recurso está disponível para todos os clientes como uma Disponibilidade limitada com recursos essenciais.</p>
<!--p><img src="assets/do-not-localize/simulate-user.gif"></p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Deeplinks no Designer de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível adicionar deep links ao seu conteúdo de email por meio de uma opção dedicada no Designer de email.</p><p>Isso garante que os usuários sejam direcionados diretamente para o conteúdo correto no aplicativo, em vez de serem redirecionados para navegadores ou lojas de aplicativos, preservando o contexto e o engajamento.</p>
<!--<p><img src="assets/do-not-localize/forms.gif"></p>-->
<p>Para obter mais informações, consulte a <a href="../email/message-tracking.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 7 de maio de 2026</p>
</td>
</tr>
</tbody>
</table>

