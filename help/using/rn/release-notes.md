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
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
  - id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 4c76084f6e13d8428071d68d41d46c59b5f095d0
workflow-type: tm+mt
source-wordcount: 2625
ht-degree: 80%

---

# Notas de versão {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novidades"
>abstract="O **Adobe Journey Optimizer** oferece continuamente novos recursos, melhorias nos recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão."

O [!DNL Adobe Journey Optimizer] segue um modelo de entrega contínua, permitindo que a Adobe forneça novos recursos, melhorias e correções de forma contínua. Essa abordagem permite uma implantação escalável e em fases de recursos para garantir desempenho e estabilidade em todos os ambientes.

Devido a esse modelo, as notas de versão são atualizadas entre as versões mensais. Para obter detalhes completos sobre o ciclo de lançamento e as fases de disponibilidade, consulte o [ciclo de lançamento do Journey Optimizer](releases.md).

O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

>[!NOTE]
>
>Quer uma prévia do que está por vir? Confira as [notas de pré-lançamento](e-release-notes.md) para ver os recursos futuros antes de eles serem lançados oficialmente.

## Atualizações de maio de 2026 {#may-26-rn}

Os seguintes recursos e melhorias foram lançados em maio de 2026.

<table>
<thead>
<tr>
<th><strong>Jornada fragmentos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode criar <strong>Fragmentos de Jornada</strong> no Adobe Journey Optimizer. Os fragmentos de jornada são conjuntos reutilizáveis de nós de jornada que você pode criar uma vez e soltar em qualquer jornada na sandbox. Seja uma verificação de elegibilidade, uma lógica de roteamento de canal preferencial ou uma sequência de boas-vindas, os fragmentos ajudam as equipes a se moverem mais rápido e a permanecerem consistentes, sem reconstruir a mesma lógica do zero todas as vezes.</p>
<p>Depois de criados, os fragmentos são armazenados em um <strong>Inventário de Fragmentos</strong> dedicado e podem ser inseridos em qualquer jornada usando a atividade <strong>Fragmentos de Jornada</strong>.</p>
<!--<p><img src="assets/do-not-localize/journey-fragments.gif"></p>-->
<p>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.</p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/journey-fragments.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 13 de maio de 2026</p>
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
<p>Agora é possível adicionar deep links ao conteúdo de email por meio de uma opção dedicada no Designer de email.</p><p>Isso garante que os usuários sejam direcionados diretamente para o conteúdo correto no aplicativo, em vez de serem redirecionados para navegadores ou lojas de aplicativos, preservando o contexto e o engajamento.</p>
<p><img src="assets/do-not-localize/deeplinks.gif"></p>
<p>Para obter mais informações, consulte a <a href="../email/deeplinks.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 12 de maio de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Simulação de jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode definir sua jornada como <strong>Simulação</strong>. Este modo permite validar sua lógica usando <strong>usuários simulados</strong>. São perfis temporários criados especificamente para a simulação, permitindo que você teste livremente sem precisar gerenciar perfis de teste persistentes na Adobe Experience Platform.</p>
<p>Esse recurso está disponível para todos os clientes como uma Disponibilidade limitada com recursos essenciais.</p>
<p><img src="assets/do-not-localize/simulate-user.gif"></p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/simulate-journey.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 5 de maio de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Regras de decisão e otimização da IA da fórmula de classificação</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>[!DNL Adobe Journey Optimizer] O agora usa a IA para detectar regras de decisão e fórmulas de classificação que podem ser simplificadas. No inventário, um indicador vermelho aparece em qualquer regra para a qual a IA identificou uma oportunidade de otimização. Clicar no indicador exibe a expressão original junto com a versão sugerida pela IA. A partir daí, você pode baixar um arquivo para revisar como os perfis simulados são avaliados por cada versão, confirmar se eles se comportam de forma idêntica e, em seguida, substituir a expressão pelo otimizado.</p>
<p>Para obter mais informações, consulte a <a href="../start/ai-features.md#decisioning-optimization">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 5 de maio de 2026</p>
</td>
</tr>
</tbody>
</table>

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

### Aprimoramentos {#may-26-improv}

As seguintes melhorias também foram lançadas em maio de 2026.

#### Tomada de decisão

* **APIs de fluxo de trabalho de migração de decisão** - O contrato de API para criação de análise de dependência e fluxos de trabalho de migração foi atualizado: passe **`request-level`** como **parâmetro de consulta** na URL de solicitação (`sandbox`, `offer` ou `decision`). O nível de solicitação não deve mais ser enviado no corpo JSON. [Leia mais](../experience-decisioning/decisioning-migration-api.md)

  Data de disponibilidade: 6 de maio de 2026

#### SMS

<!--
* **Opt-out and consent at phone number and sender** - For SMS, Journey Optimizer now records marketing consent and opt-out at the level of both the profile's phone number and short code. 

  This capability is currently only available for Sinch SMS configurations. [Read more](../sms/sms-configuration-sinch.md)
-->

* **Contagem de caracteres**: no Adobe Journey Optimizer, agora você pode usar a Contagem de caracteres para monitorar o comprimento de suas mensagens SMS em tempo real. Isso ajuda a ver quando uma mensagem será dividida em vários segmentos para gerenciar melhor a formatação e evitar aumentos inesperados nos custos de envio. [Leia mais](../sms/create-sms.md)

* **Entrada de SMS para um conjunto de dados personalizado**: em **credenciais de API de SMS**, encaminhe **SMS de entrada** para um **conjunto de dados de Evento de Experiência personalizado e habilitado para perfil** que você escolher, em vez de apenas o conjunto de dados de rastreamento padrão. [Leia mais](../sms/sms-webhook.md)

* **Aprimoramento da interface do webhook**: ao configurar webhooks de SMS, a interface agora inclui um guia de instalação integrado com exemplos práticos, facilitando o alinhamento do conteúdo do provedor e a solução de problemas sem sair do fluxo de configuração. [Leia mais](../sms/sms-webhook.md)

#### WhatsApp

* **Suporte e rastreamento de botões do WhatsApp** - Os modelos do WhatsApp agora oferecem suporte para **Resposta rápida**, **Call to action - URL** e **Call to action - phone**, **Não há suporte para**. O Journey Optimizer envia botões e rastreia interações compatíveis junto com seus outros relatórios de canal.

<!-- 
## Coming soon {#coming-soon}

The following capabilities and enhancements are scheduled for release in the next few days. **Information is subject to change**. Updated links, screens, and documentation will be shared once these updates are live in production.

### New capabilities {#comming-soon-features}
-->

## Notas de versão de abril de 2026 {#april-26-rn}


**Data de lançamento**: 28 a 29 de abril de 2026

### Novos recursos {#april-26-features}

Os recursos a seguir foram lançados em abril de 2026.

<table>
<thead>
<tr>
<th><strong>Atividade de consulta incremental em campanhas orquestradas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As <strong>campanhas orquestradas</strong> agora oferecem suporte a uma atividade de <strong>Consulta incremental</strong> que segmenta somente perfis ou eventos que são recém-qualificados desde a última execução.

Isso mantém as campanhas recorrentes focadas nos novos públicos-alvo (novas inscrições, membros de fidelidade recém-qualificados e segmentos semelhantes), reduzindo as cargas de trabalho de consulta e evitando envios redundantes ao longo do tempo.</p>
<p>Para obter mais informações, consulte a <a href="../orchestrated/activities/incremental-query.md#incremental-query-configuration">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 30 de abril de 2026</p>
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
<p>Com o Journey Optimizer, agora é possível enviar emails em que a entidade de transmissão (Remetente) difere da entidade de criação (De). Os clientes de email que oferecem suporte a isso normalmente o renderizam como “Remetente em nome de” ou exibem um indicador “via”. Preencha os campos opcionais <strong>Cabeçalhos do remetente</strong> nas configurações do canal de email para configurar este recurso.</p>
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
<p>Agora você pode configurar um campo CC (cópia carbono) opcional nas configurações de canal de email. Ao contrário do BCC, os destinatários em CC são visíveis para o destinatário principal, permitindo uma comunicação transparente e uma responsabilidade mais clara.</p>
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
<p>As ferramentas de sandbox agora permitem empacotar e copiar campanhas orquestradas de uma sandbox para outra. Isso elimina a necessidade de reconstruir manualmente as campanhas em cada ambiente. Quando uma campanha é configurada, seus principais objetos dependentes, como políticas de mesclagem, mensagens, são incluídos automaticamente, de modo que a campanha importada chega pronta para configuração e validação. Para proteger ambientes de produção, todas as campanhas importadas são enviadas com o status de rascunho na sandbox de destino, dando às equipes uma etapa de revisão e aprovação antes de qualquer campanha entrar em vigor.</p>
<p><img src="assets/do-not-localize/oc-sandbox.gif"></p>
<p>Para obter mais informações, consulte a <a href="../configuration/copy-objects-to-sandbox.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integração do Agente de IA do Journey Optimizer via MCP</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A Adobe Journey Optimizer agora fornece um <strong>servidor MCP (Model Context Protocol)</strong> que revela operações de campanha, configuração de canal e sandbox diretamente dentro de qualquer aplicativo compatível com MCP. Com essa integração, diferentes personalidades podem colaborar em torno dos mesmos dados de orquestração. Em vez de escrever consultas na API REST do Adobe Journey Optimizer ou navegar por várias telas de interface, você pode descrever sua intenção em conversação e permitir que o LLM chame as ferramentas de MCP apropriadas. Esse recurso está disponível atualmente no Claude Web e Desktop.</p>
<p>Esse recurso está disponível para todos os clientes no Beta público.</p>
<p>Para obter mais informações, consulte a <a href="../integrations/ajo-mcp.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Arbitragem de jornada: modelos de IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode usar <strong>modelos de IA</strong> nas fórmulas de classificação para aumentar automaticamente as pontuações de prioridade de jornada com base nos atributos do perfil do cliente e em fatores contextuais, garantindo que os clientes entrem nas jornadas mais relevantes.</p>
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
<p>A <b>integração do Adobe Express</b> no Adobe Journey Optimizer permite que você use as ferramentas de edição do Adobe Express diretamente durante a criação de conteúdo, permitindo redimensionar, remover planos de fundo, cortar e converter ativos em JPEG ou PNG.
</p>
<p>Anteriormente lançado em disponibilidade limitada para uso em jornadas, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
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
<p>Como os assistentes de IA controlam cada vez mais como os destinatários leem e agem no email, esse recurso ajuda a gerar e criar conteúdo que tenha bom desempenho em tarefas de IA downstream, incluindo resumo, triagem, priorização e extração de intenção.</p>
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
<th><strong>Assistente de IA para expressões de personalização</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>[!DNL Adobe Journey Optimizer] agora inclui o <strong>Assistente de IA</strong> diretamente no editor de personalização e no Designer de email, que converte prompts de linguagem natural em expressões de personalização e lógica condicional válidas, sem a necessidade de conhecimento especializado sobre sintaxe. Descreva a personalização que deseja realizar e a IA gera um código pronto para uso que pode ser aplicado imediatamente ou refinado por meio de prompts de acompanhamento.</p>
<p>O assistente também trabalha de forma inversa. Selecione qualquer expressão existente e solicite que ela explique a lógica, identifique problemas ou sugira melhorias. Isso o torna útil não apenas para a criação de novas expressões, mas para revisar e depurar as existentes na sua equipe.</p>
<p><img src="assets/do-not-localize/assistant-perso.gif"></p>
<p>Para obter mais informações, consulte o <a href="../content-management/generative-personalization-expressions.md">Assistente de IA para expressões de personalização</a>.</p>
<p>Data de disponibilidade: 13 de abril de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experimentação do caminho da jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Use o novo nó <strong>Otimizar</strong> para executar testes A/B ou experimentos de bandido de vários braços para determinar o melhor caminho para atingir seus KPIs centrados no negócio. Essa ferramenta permite testar, variar e personalizar as comunicações, o sequenciamento e o momento para melhor alcançar os clientes.
</p>
<p>Anteriormente lançado em disponibilidade limitada para uso em jornadas, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<p>Como parte da Disponibilidade geral, esta versão introduz a seleção <strong>tipo de experimento</strong> (A/B ou bandido de vários braços) e <strong>Dimensionar o vencedor</strong> para jornadas unitárias.</p>
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
<p>A <strong>Caixa de entrada</strong> é uma funcionalidade móvel, disponível com Cartões de conteúdo, que permite aos clientes criar um local centralizado no aplicativo ou site para exibir mensagens enviadas aos usuários. Isso estende o tempo de vida das comunicações de marketing, garantindo que as mensagens permaneçam acessíveis mesmo após serem descartadas.</p>
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
<th><strong>Apoio à decisão no canal de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode usar a <strong>Decisão</strong> para personalizar e otimizar o conteúdo de suas mensagens de e-mail. Aproveite as pontuações de prioridade, as fórmulas ou os modelos de IA para exibir as ofertas e o conteúdo mais relevantes para cada destinatário.</p>
<p>Anteriormente lançado em disponibilidade limitada para uso em jornadas, este recurso já está disponível para todos os ambientes (disponibilidade geral). Com esta versão de Disponibilidade geral, as mirror pages agora são compatíveis.</p>
<p><img src="assets/do-not-localize/exd-email.gif"></p>
<p>Para obter mais informações, consulte a <a href="../experience-decisioning/create-decision-policy.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 6 de abril de 2026</p>
</td>
</tr>
</tbody>
</table>

### Aprimoramentos {#april-26-improv}

As seguintes melhorias também foram lançadas em abril de 2026.

#### IA

<!--
* **Brand alignment score in Campaign dashboard** - You can now assess your brand alignment score directly within your Campaign dashboard to ensure content stays on-brand. This allows you to verify guidelines at a glance without having to open the content designer.
-->

* **Aprimoramento do assistente de prompt**: o assistente de prompt aprimora a geração de conteúdo de IA analisando prompts do usuário em tempo real e identificando problemas de clareza, integridade e contexto. Ele sugere regravações aprimoradas e fornece orientação acionável para enriquecer os prompts com detalhes-chave como público-alvo, tom e intenção. O recurso também faz perguntas de esclarecimento direcionadas para ajudar os usuários a refinar suas entradas antes da geração. Essas perguntas geram resultados mais precisos e de alta qualidade com menos iterações. [Saiba mais](../content-management/ai-assistant-prompting-guide.md#prompt-assistant)

  Data de disponibilidade: 5 de maio de 2026

#### Push

* **Personalizar ID do aplicativo nas configurações do canal**: nas configurações do canal de push, agora é possível personalizar o campo **ID do aplicativo** para que cada destinatário possa receber uma notificação por push da marca apropriada com base nas informações do perfil. [Leia mais](../push/push-configuration.md#app-id-personalization)

#### Tomada de decisão

* **APIs de fluxo de trabalho de migração de decisão** - O contrato de API para criação de análise de dependência e fluxos de trabalho de migração foi atualizado: passe **`request-level`** como **parâmetro de consulta** na URL de solicitação (`sandbox`, `offer` ou `decision`). O nível de solicitação não deve mais ser enviado no corpo JSON. [Leia mais](../experience-decisioning/decisioning-migration-api.md)

  Data de disponibilidade: 6 de maio de 2026

* **Anexar fragmentos a itens de decisão**: o Journey Optimizer agora oferece a capacidade de anexar fragmentos a itens de decisão, que podem ser aproveitados em experiências baseadas em código e campanhas de email por meio de políticas de decisão. [Leia mais](../experience-decisioning/fragments-decision-policies.md)

  Anteriormente lançado em disponibilidade limitada para uso em jornadas, este recurso já está disponível para todos os ambientes (disponibilidade geral).

* **Fragmentos temporariamente indisponíveis são ignorados**: ao usar fragmentos em itens de decisão, se um fragmento estiver temporariamente indisponível no Edge, ele é ignorado e a jornada ou campanha continua sendo renderizada em vez de falhar. [Leia mais](../experience-decisioning/fragments-decision-policies.md#temporary-unavailable-fragments)

  Data de disponibilidade: 14 de abril de 2026

#### Integrações do Adobe Experience Manager

* **Suporte à variação de fragmento de conteúdo do Adobe Experience Manager**: você pode selecionar **variações de fragmento de conteúdo** (por exemplo, variantes de idioma ou canal) ao inserir fragmentos de conteúdo do Adobe Experience Manager, com manipulação aprimorada para localidade e cenários multilíngues. [Leia mais](../integrations/aem-fragments.md#aem-variations)

  Anteriormente lançado em disponibilidade limitada para uso em jornadas, este recurso já está disponível para todos os ambientes (disponibilidade geral).

* **Contexto do fragmento de conteúdo do Adobe Experience Manager durante a criação**: a seleção de fragmento de conteúdo permanece ativa à medida que você se move entre campos de texto e blocos de conteúdo, para que você possa adicionar mais campos de fragmento sem ter que reabrir o **Consultor de conteúdo do AEM**. [Leia mais](../integrations/aem-fragments.md)

  Anteriormente lançado em disponibilidade limitada para uso em jornadas, este recurso já está disponível para todos os ambientes (disponibilidade geral).

#### Design de email

* **Editor avançado de HTML para conteúdo de email**: o modo Avançado de HTML permite editar a fonte HTML do conteúdo no Designer de email, adicionar expressões avançadas (como condições) na fonte e alternar entre o modo de exibição HTML e o modo de exibição Desktop sem perder as alterações.

  Disponível anteriormente somente para modelos de conteúdo de email, esse recurso agora está implantado no conteúdo de **email** no Designer de email (por exemplo, emails criados em jornadas e campanhas), além de modelos de conteúdo de email. No momento, a disponibilidade é limitada. Entre em contato com o representante da Adobe para obter acesso. [Leia mais](../email/email-expert-mode.md)

  Data de disponibilidade: 9 de abril de 2026

#### Jornadas

* **Tamanho atual da carga de jornada visível nas propriedades de jornada** - O painel Propriedades de jornada agora exibe o tamanho atual da carga de jornada em comparação ao limite configurado — por exemplo, *1,5 MB (de 4 MB)*. Esse indicador somente leitura ajuda a monitorar a complexidade da jornada antes da publicação e evitar que erros causados pelo limite de tamanho da carga sejam excedidos. [Leia mais](../building-journeys/journey-properties.md#journey-payload-size)

  Data de disponibilidade: 30 de abril de 2026

#### Otimização do caminho da jornada

* **Tipo de experimento**: agora é possível escolher entre um experimento A/B (divisão fixa no início) ou um bandido multiarmado (divisão automática com atualizações de peso semanais) ao configurar um experimento de caminho. [Leia mais](../building-journeys/path-experimentation.md)

  Data de disponibilidade: 7 de abril de 2026

* **Experimentação de caminhos: amplie o vencedor**. Agora você pode implementar automaticamente ou manualmente o caminho vencedor de um experimento para todo o seu público-alvo. Uma vez determinado o vencedor, você pode ampliar seu alcance e eficácia sem monitorar constantemente o experimento. [Leia mais](../building-journeys/path-experimentation.md#scale-winner)

  Esse recurso está disponível somente em jornadas unitárias (acionadas por eventos e qualificações de público-alvo). Não está disponível para jornadas Ler público-alvo.

  Data de disponibilidade: 7 de abril de 2026

* **Condições**: a atividade [Otimizar](../building-journeys/optimize.md) é o novo veículo para a criação de caminhos condicionais em jornadas. Substitui a antiga atividade **Condição**, que foi removida da interface. Toda a lógica condicional é mantida e agora é tratada através das condições da atividade **Otimizar**. [Leia mais](../building-journeys/conditions.md)

  Anteriormente lançado em disponibilidade limitada para uso em jornadas, este recurso já está disponível para todos os ambientes (disponibilidade geral).

  Data de disponibilidade: 7 de abril de 2026

#### Campanhas orquestradas

* **Variáveis globais em Campanhas orquestradas**: as Campanhas orquestradas agora oferecem suporte a variáveis globais que podem ser definidas uma vez e reutilizadas em todas as atividades de um fluxo de trabalho, simplificando a configuração e garantindo a consistência em valores dinâmicos, expressões e personalização de conteúdo. [Leia mais](../orchestrated/global-variables.md)
* **Aprimoramentos do Modelador de dados**: os esquemas relacionais orquestrados agora oferecem suporte a chaves compostas que abrangem vários campos. O carregamento de um esquema de um arquivo DDL também traz listas discriminadas, e o carregamento de um arquivo DDL ou do Excel cria automaticamente relações compostas entre as tabelas. Na visualização de relacionamento da entidade, os links compostos agora exibem o conjunto completo de pares de campos entre tabelas depois que um arquivo é carregado. [Leia mais](../orchestrated/gs-schemas.md)

