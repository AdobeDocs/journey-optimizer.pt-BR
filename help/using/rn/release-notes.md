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
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: d00e9f03-e50b-4162-b143-0c0817c937c2id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: ee485d872299b592e27cf40cd3cde9b362bc85d2
workflow-type: tm+mt
source-wordcount: 2694
ht-degree: 21%

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
>Os recursos listados nestas notas de versão incluem uma **Data de disponibilidade** indicando quando cada alteração se torna acessível em seu ambiente. As entradas nas opções **Em breve** serão esperadas nos próximos dias ou semanas. As informações contidas nessas seções estão sujeitas a alterações.


## Atualizações de junho de 2026 {#june-26-updates}

<table>
<thead>
<tr>
<th><strong>Jornada fragmentos (disponibilidade geral)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode criar <strong>Fragmentos de Jornada</strong> no Adobe Journey Optimizer. Os fragmentos de jornada são conjuntos reutilizáveis de nós de jornada que você pode criar uma vez e soltar em qualquer jornada na sandbox. Seja uma verificação de elegibilidade, uma lógica de roteamento de canal preferencial ou uma sequência de boas-vindas, os fragmentos ajudam as equipes a se moverem mais rápido e a permanecerem consistentes, sem reconstruir a mesma lógica do zero todas as vezes.</p>
<p>Depois de criados, os fragmentos são armazenados em um <strong>Inventário de Fragmentos</strong> dedicado e podem ser inseridos em qualquer jornada usando a atividade <strong>Fragmentos de Jornada</strong>.</p>
<p>Anteriormente disponível em Disponibilidade limitada, esse recurso agora está disponível para todos os clientes. Os fragmentos de jornada também são compatíveis com a <strong>ferramenta Sandbox</strong>, permitindo empacotar e exportar fragmentos em sandboxes.</p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/journey-fragments.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 9 de junho de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Suporte à decisão no canal de correspondência direta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível adicionar políticas de decisão a jornadas e campanhas de correspondência direta. As políticas de decisão são containers para suas ofertas que aproveitam o mecanismo de decisão para retornar dinamicamente o melhor conteúdo para cada membro do público. A decisão de correspondência direta também aceita casos de uso de decisão em lote, permitindo exportar os itens de oferta correspondentes para cada perfil em um determinado público-alvo da Adobe Experience Platform. </p>
<p><img src="assets/do-not-localize/exd-dm.gif"></p>
<p>Para obter mais informações, consulte a <a href="../experience-decisioning/use-decision-policy.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 3 de junho de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Assistente de IA para expressões de Jornada (Beta público)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Assistente de IA agora opera no editor de expressão avançado do jornada para converter prompts de linguagem natural em expressões válidas e lógica condicional. Descreva a expressão que deseja criar e o AI Assistant gera um código pronto para uso, que pode ser aplicado imediatamente ou refinado por meio de prompts de acompanhamento.</p>
<p>Esse recurso está disponível para todos os clientes como um Beta público.</p>
<p><img src="assets/do-not-localize/expression-assistant.gif"></p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/expression/expression-agent.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 3 de junho de 2026</p> 
</td>
</tr>
</tbody>
</table>


* **Autenticação Personalizada Baseada em Certificado em ações personalizadas** - As ações personalizadas agora oferecem suporte à Autenticação Personalizada Baseada em Certificado. Ao adicionar `subType: "certificateCredential"` a uma configuração de autorização personalizada, o Journey Optimizer usa o certificado gerenciado da Adobe para assinar uma declaração de cliente JWT e trocá-la por um token de acesso — não é necessário nenhum segredo de cliente. Projetado para APIs empresariais que impõem a verificação de identidade baseada em certificados, como o Microsoft Entra ID. [Saiba mais](../datasource/external-data-sources.md#certificate-credential)

  Data de disponibilidade: 4 de junho de 2026



## Notas de versão de maio de 2026 {#may-26-rn}

### Jornadas {#may-26-journeys}

Os recursos e melhorias a seguir foram adicionados às jornadas nesta versão. Alterações adicionais também são esperadas nos próximos dias ou semanas.

<table>
<thead>
<tr>
<th><strong>Jornada fragmentos (disponibilidade limitada)</strong><br/></th>
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
<th><strong>Simulação de jornada (disponibilidade limitada)</strong><br/></th>
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

+++ Em breve — **As informações abaixo estão sujeitas a alterações.**

Os seguintes recursos do jornada são esperados nos próximos dias ou semanas.

<!--
<table>
<thead>
<tr>
<th><strong>Journey path optimization – Targeting (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Use the new <strong>Optimize</strong> node to target specific audiences to determine the best path to meet your business-centric KPIs.</p>
<p>This tool allows you to develop more effective marketing campaigns that are more likely to resonate at the 1:1 level, improve marketing personalization efforts for customers and enhance critical customer engagement KPIs, such as conversions and revenue.</p>
<p>Previously available in Limited Availability, this capability is now available to all environments.</p>
<p>Availability date: June 1, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Arbitration – ranking formulas (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use formulas to automatically boost journey priority scores based on customer profile attributes and contextual factors, ensuring customers enter the most relevant journeys.</p>
<p>Previously available in Limited Availability, this capability is now available to all environments.</p>
<p>Availability date: June 1, 2026</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Simulação de Jornada (Disponibilidade Geral)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Anteriormente lançado com Disponibilidade limitada, a Simulação de Jornada agora está disponível para todos os ambientes. Com esta versão de Disponibilidade geral, agora é possível usar o Journey Agent para gerar usuários e eventos simulados diretamente no menu Simulação.</p>
<p>Data de disponibilidade: início de junho de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Conclusão automática para jornadas de Leitura de Público não recorrentes** - **Leitura de Público** Não recorrentes agora as jornadas fazem a transição automática para o status **Interrompido** quando o último perfil ativo existe. Anteriormente, essas jornadas permaneciam **Ativas** até que o tempo limite global de 91 dias expirasse — mesmo quando nenhum perfil estava fluindo mais por elas. Com essa melhoria, o status da jornada reflete o estado de execução real assim que é concluída, mantendo o inventário da jornada preciso sem intervenção manual.

  Observe que esse comportamento não se aplica a jornadas que incluem nós que causam períodos de espera, como nós de espera, nós de reação ou transições acionadas por evento. Essas jornadas permanecem sujeitas ao tempo limite global padrão de 91 dias.

  Data de disponibilidade: início de junho de 2026

* **Suporte de identificador complementar para públicos externos** - Os identificadores complementares no jornada agora têm suporte para públicos externos, incluindo públicos importados de um arquivo CSV e públicos criados com a Composição de Público Federado. Você pode designar qualquer atributo que não seja de identidade ou atributo de identidade que não seja de pessoa do público-alvo como a ID complementar; nenhum rótulo de esquema é necessário.

  Data de disponibilidade: início de junho de 2026

+++

### Campanhas orquestradas {#may-26-oc}

Os recursos e melhorias a seguir foram adicionados às campanhas orquestradas nesta versão. Alterações adicionais também são esperadas nos próximos dias ou semanas.

<table>
<thead>
<tr>
<th><strong>Campanhas orquestradas encadeadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As campanhas orquestradas agora podem ser vinculadas acionando uma campanha orquestrada diretamente da <strong>Atividade final</strong> de outra campanha orquestrada.</p>
<p>Isso permite dividir a lógica de orquestração complexa em fluxos menores e reutilizáveis que podem ser chamados de várias campanhas principais, em vez de serem reconstruídos a cada vez. O payload transmitido no tempo de execução está disponível para segmentação e personalização na campanha downstream, portanto, cada campanha vinculada pode se comportar com base no contexto que recebe.</p>
<p><img src="assets/do-not-localize/oc-trigger.gif"></p>
<p>Para obter mais informações, consulte a <a href="../orchestrated/trigger-orchestrated-campaign.md#signal-end">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 20 de maio de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Adicionar links na atividade de Enriquecimento** - A funcionalidade Adicionar Link agora está disponível na Atividade de Enriquecimento para Campanhas Orquestradas. Isso permite criar uma relação direta entre os dados da tabela de trabalho e as tabelas do banco de dados existente.

  Data de disponibilidade: 20 de maio de 2026

<!--
+++ Coming soon — **Information below is subject to change.**

The following orchestrated campaign capability is expected in the upcoming days or weeks.

<table>
<thead>
<tr>
<th><strong>File-based targeting for orchestrated campaigns (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Orchestrated campaigns now support loading a CSV or TXT file directly into the campaign canvas as the targeting audience, without first ingesting the file into Adobe Experience Platform. The file data is consumed at execution time and is not persisted as an Adobe Experience Platform dataset. During file setup, you can define column mappings, data types, NULL handling, and per-column error policies. This supports ad-hoc sends or partner list campaigns where building a full ingestion pipeline is not practical.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>Availability date: June 1, 2026</p>
</td>
</tr>
</tbody>
</table>

* **Loop-based personalization for relational data** - The personalization editor now supports a Loop block that iterates over relational collections, such as orders, accounts, or bookings, and renders one content block per record inside a single email or SMS. Collections are configured through the data picker using personalization tokens, with no expression writing required.

  Availability date: Early June, 2026

* **Personalize email sender details per recipient and campaign** - Orchestrated campaigns now support personalization of email header fields, including From name, From address, and Reply-To, using profile attributes or relational data. This allows sender details to reflect the relevant advisor, location, or branch for each recipient, rather than routing all sends through a single corporate address.

  Header values can be set at the channel level and overridden per campaign using contextual data for more precise control.

  Availability date: Early June, 2026

+++
-->

### Campanhas {#may-26-campaigns}

* **Alertas de clientes para eventos de ciclo de vida de campanha** - Novos alertas do sistema agora notificam você sobre eventos-chave do ciclo de vida para campanhas acionadas por ação e API. Assine no nível da sandbox. [Leia mais](../reports/alerts.md)

  Data de disponibilidade: 1 de junho de 2026

<!--
+++ Coming soon — **Information below is subject to change.**

* **Override the default execution field in campaigns** - Previously available at the journey level, you can now override the default execution field set globally for your Email, SMS and WhatsApp deliveries in the campaign parameters.

  Availability date: Early June, 2026

+++
-->

### Tomada de decisão {#may-26-decisioning}

Os recursos e melhorias a seguir foram adicionados ao Decisioning nesta versão. Alterações adicionais também são esperadas nos próximos dias ou semanas.

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
<p><img src="assets/do-not-localize/rule-ai.gif"></p>
<p>Para obter mais informações, consulte a <a href="../start/ai-features.md#decisioning-optimization">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 5 de maio de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Fragmentos de conteúdo do Adobe Experience Manager na Decisão** - Agora é possível mapear fragmentos de conteúdo do Adobe Experience Manager para itens de decisão na Decisão e aproveitá-los nas políticas de decisão para fornecer o fragmento certo ao cliente certo, na hora certa. [Leia mais](../integrations/aem-fragments.md#aem-decisioning)

  Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.

  Data de disponibilidade: 20 de maio de 2026

* **Detalhes da política de decisão do resumo da campanha** - Na página de resumo da campanha, agora é possível revisar a estrutura completa de cada política de decisão, incluindo estratégias de seleção, itens de decisão e ofertas substitutas, sem duplicar ou editar a campanha. Você também pode copiar um resumo JSON para a área de transferência para solucionar problemas com o Suporte da Adobe ou com sua equipe de engenharia. [Leia mais](../experience-decisioning/use-decision-policy.md#decision-policy-summary)

  Data de disponibilidade: 20 de maio de 2026

* **APIs de fluxo de trabalho de migração de decisão** - O contrato de API para criação de análise de dependência e fluxos de trabalho de migração foi atualizado: passe **`request-level`** como **parâmetro de consulta** na URL de solicitação (`sandbox`, `offer` ou `decision`). O nível de solicitação não deve mais ser enviado no corpo JSON. [Leia mais](../experience-decisioning/decisioning-migration-api.md)

  Data de disponibilidade: 6 de maio de 2026

### Canal de email {#may-26-email}

Os seguintes recursos e melhorias foram adicionados ao canal de email nesta versão. Alterações adicionais também são esperadas nos próximos dias ou semanas.

<table>
<thead>
<tr>
<th><strong>Deep links no Designer de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível adicionar deep links ao seu conteúdo de email por meio de uma opção dedicada no Designer de email. Isso garante que os usuários sejam direcionados diretamente para o conteúdo correto no aplicativo, em vez de serem redirecionados para navegadores ou lojas de aplicativos, preservando o contexto e o engajamento.</p>
<p>Observe que, embora a opção Deeplink esteja disponível para todos os clientes, os deep links só funcionarão se você tiver concluído as etapas de configuração e implementação de aplicativos móveis necessárias.</p>
<p><img src="assets/do-not-localize/deeplinks.gif"></p>
<p>Para obter mais informações, consulte a <a href="../email/deeplinks.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 12 de maio de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Restringir a quebra de herança nos fragmentos** - Ao criar ou editar um fragmento, agora é possível escolher se ele pode ser modificado quando usado em emails. Bloquear um fragmento garante que ele permaneça sincronizado em todos os locais onde aparece, evitando edições locais que poderiam quebrar os padrões da marca ou os requisitos de conformidade. Essa configuração pode ser atualizada posteriormente, aplicando-se a usos futuros. [Leia mais](../content-management/create-fragments.md#lock-visual-fragment)

  Data de disponibilidade: 21 de maio de 2026

### Mensagens por dispositivo móvel (SMS, MMS e RCS) {#may-26-mobile}

Os seguintes recursos e melhorias foram adicionados ao sistema de mensagens móveis nesta versão.

<table>
<thead>
<tr>
<th><strong>Novo canal de mensagens móveis e mensagens RCS aprimoradas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>SMS, MMS e RCS agora estão unificados em uma única ação de <strong>Mensagem móvel</strong> no Adobe Journey Optimizer, facilitando o gerenciamento de todos os tipos de mensagens móveis em um único local. Como parte dessa atualização, agora você pode criar mensagens RCS de mídia avançada, incluindo imagens, carrosséis e ações sugeridas, diretamente no Journey Optimizer por meio de uma nova experiência de criação nativa.</p>
<p>Para obter mais informações, consulte a <a href="../mobile/get-started-mobile.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 20 de maio de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Contagem de caracteres**: no Adobe Journey Optimizer, agora você pode usar a Contagem de caracteres para monitorar o comprimento de suas mensagens SMS em tempo real. Isso ajuda a ver quando uma mensagem será dividida em vários segmentos para gerenciar melhor a formatação e evitar aumentos inesperados nos custos de envio. [Leia mais](../mobile/create-mobile-message.md)

* **Entrada de SMS para um conjunto de dados personalizado**: em **credenciais de API de SMS**, encaminhe **SMS de entrada** para um **conjunto de dados de Evento de Experiência personalizado e habilitado para perfil** que você escolher, em vez de apenas o conjunto de dados de rastreamento padrão. [Leia mais](../mobile/mobile-webhook.md)

* **Aprimoramento da interface do webhook**: ao configurar webhooks de SMS, a interface agora inclui um guia de instalação integrado com exemplos práticos, facilitando o alinhamento do conteúdo do provedor e a solução de problemas sem sair do fluxo de configuração. [Leia mais](../mobile/mobile-webhook.md)

* **Deep links no conteúdo de SMS** - Agora é possível adicionar deep links ao conteúdo de SMS usando a função auxiliar de URL. Isso garante que os recipients sejam direcionados diretamente ao conteúdo no aplicativo desejado, sem roteá-los por meio de um navegador da Web ou uma loja de aplicativos, desde que você tenha concluído as etapas de configuração e implementação de aplicativos móveis necessárias. [Leia mais](../email/deeplinks.md)

### Canal do WhatsApp {#may-26-whatsapp}

As seguintes melhorias foram adicionadas ao canal do WhatsApp nesta versão.

* **Suporte e rastreamento de botões do WhatsApp** - Os modelos do WhatsApp agora oferecem suporte para **Resposta rápida**, **Call to action - URL** e **Call to action - phone**, **Não há suporte para**. O Journey Optimizer envia botões e rastreia interações compatíveis junto com seus outros relatórios de canal.

* **Dados de contexto do canal do WhatsApp** - O Journey Optimizer agora captura dados adicionais de interação retornados do canal do WhatsApp e os armazena no **Conjunto de Dados do AJO EmailTrackingExperienceEvent** no grupo de campos `whatsAppChannelContext`. [Leia mais](../whatsapp/send-whatsapp.md#whatsapp-channel-context)

  +++ Os campos a seguir são capturados e podem ser usados para construir públicos e analisar o engajamento do WhatsApp

   * **`messageType`** - Tipo de mensagem do WhatsApp (ex: `templateBased`, `response`)
   * **`inboundMessage`** - Conteúdo de resposta de entrada (por exemplo, `stop`, `start`, `subscribe`)
   * **`inboundNumber`** - ID do remetente em que a mensagem de entrada foi recebida
   * **`channelType`** - Categoria de canal (`Utility`, `Marketing` ou `Promotional`)
   * **`profileNumber`** - Número de telefone do qual a mensagem de entrada foi recebida
   * **`origTimestamp`** - Carimbo de data e hora original do Meta / WhatsApp
   * **`status`** - Status de entrega incluindo feedback de provedor padronizado (`sent`, `delivered`, `bounce`, `error`, `delay`, `duplicate`, `denylist`, `exclude` ou `unknown`) e a mensagem de status de provedor bruto
   * **`reactionEvent`** - Conteúdo da resposta do usuário: emoji para reações ou texto da mensagem para respostas a uma mensagem específica
   * **`reactionMessageID`** - ID da mensagem original que está sendo respondida
   * **`reactionActionName`** - Tipo de ação de resposta (`react`, `unreact` ou `reply`)
   * **`interactiveSelectedTitle`** - Título selecionado pelo usuário de uma mensagem interativa do WhatsApp
   * **`interactiveType`** - Tipo de mensagem interativa (`list reply`, `button reply` ou `button`)
   * **`interactiveSelectedDescription`** - Descrição da opção interativa do WhatsApp selecionada
   * **`interactiveSelectedID`** - ID da opção selecionada do WhatsApp

  +++

### Conteúdo e integrações {#may-26-content}

Os seguintes recursos e melhorias foram adicionados ao gerenciamento de conteúdo e integrações nesta versão.

<table>
<thead>
<tr>
<th><strong>Seletor do Supervisor de Conteúdo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora usa o <strong>seletor do Supervisor de conteúdo</strong>, um modal unificado para selecionar fragmentos de conteúdo e Experience Manager Assets. O novo seletor inclui:</p>
<ul>
<li><strong>Navegar, pesquisar e filtrar </strong> em todos os ativos e fragmentos.</li>
<li><strong>Pesquisa semântica de IA</strong>: descreva o que você precisa em linguagem simples, por exemplo, "café nas montanhas", para exibir ativos contextualmente relevantes com base no significado e no conteúdo, não apenas correspondências de texto. Consultas multilíngues também são compatíveis.</li>
<li><strong>Upload breve</strong>: faça upload de um resumo de marketing para exibir automaticamente ativos que se alinham ao contexto da campanha com base no conteúdo e nos requisitos.</li>
<li><strong>Representações do Dynamic Media</strong>: escolha e aplique representações de imagem para ativos dinâmicos sem sair do seletor.</li>
</ul>
<p>Para obter mais informações, consulte a <a href="../integrations/aem-content-advisor.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 19 de maio de 2026</p>
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

* **Acesso ao repositório entre organizações no Seletor de Assets** - Agora é possível selecionar ativos facilmente de repositórios em várias organizações diretamente no Seletor de ativos do Adobe Experience Manager.

### Administração {#may-26-admin}

* **Criptografia do parâmetro de URL** - Agora é possível criptografar parâmetros de URL em links de páginas de destino e rastreamento adicionados às suas mensagens de email. Isso fornece uma camada adicional de segurança para dados de parâmetros confidenciais. Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral). [Leia mais](../personalization/url-parameter-encryption.md)

  Data de disponibilidade: 1 de junho de 2026

* **Novas permissões para o Registro de chave** - Duas novas permissões agora são necessárias para acessar e gerenciar as chaves necessárias para a criptografia de parâmetros de URL: **Gerenciar Registro de Chave** e **Exibir Registro de Chave**. [Leia mais](../administration/high-low-permissions.md#administration-permissions)

  Data de disponibilidade: 1 de junho de 2026

<!--
+++ Coming soon — **Information below is subject to change.**

* **Message Feedback Event Dataset moving to batch ingestion** - The `AJO Message Feedback Event Dataset` is transitioning from streaming to batch ingestion mode. This change ensures that data ingestion does not exceed streaming ingestion limits. If you use this dataset in Customer Journey Analytics reports or run queries against it, expect an increase in data latency of up to 2 hours going forward.

  Availability date: June 1, 2026

+++
-->

### Melhorias de usabilidade {#may-26-usability}

As seguintes melhorias de usabilidade também foram lançadas em maio de 2026.

#### Listas

* **Ações em massa** - Agora é possível selecionar vários itens de uma só vez nas listas de **Campanhas**, **Fragmentos** e **Modelos** e executar operações em massa a partir de uma única barra de ação, incluindo adicionar itens a um pacote, movê-los para uma pasta, editar marcas, gerenciar o acesso e arquivá-los ou excluí-los. [Saiba mais](../start/search-filter-categorize.md#bulk-actions)

  ![](../start/assets/bulk-actions-campaigns.png)

* **Classificação e redimensionamento de coluna** - As listas **Campanhas**, **Fragmentos** e **Modelos** agora oferecem suporte à classificação clicando em qualquer cabeçalho de coluna. Na exibição das pastas de Campanhas, também estão disponíveis a classificação e filtragem por **[!UICONTROL Prioridade]** e **[!UICONTROL Configuração de canal]**. As larguras de coluna nas listas **Fragmentos** e **Modelos** também são redimensionáveis — arraste a borda da coluna para ajustar os dados mais importantes para você. [Saiba mais](../start/search-filter-categorize.md#filter-lists)

#### Criação de conteúdo

* **Edição de atributo de perfil em linha** - A edição de atributo de perfil em linha no Designer de email foi lançada inicialmente em abril. Como parte da versão de maio, esse recurso foi dissociado do Assistente de IA e estendido para o editor do canal de push. [Saiba mais](../personalization/personalize.md#inline-personalization)

  ![](../personalization/assets/inline-profile-attributes.png)

* **Dica de ferramenta de URL do link no editor do canal de push** - Quando uma URL em qualquer campo de link ou mídia é muito longa para ser exibida, um ícone de dica de ferramenta fica sempre visível ao lado do campo. Passe o mouse sobre ela para ver a URL completa. [Saiba mais](../push/design-push.md#on-click-behavior)

  ![](../rn/assets/do-not-localize/push-link-tooltip.png)

<!--
#### Simulation & Preview

* **Redesigned preview experience** - The content preview screen has been redesigned with a side-by-side layout that lets you compare how your content renders across multiple profiles at a glance, enabling quicker and more confident reviews before sending. [Learn more](../test-approve/simulate-sample-input.md#preview)

  ![](../test-approve/assets/simulation-preview-redesign.png)
-->

+++ Em breve — **As informações abaixo estão sujeitas a alterações.**

* **Pastas para jornadas e campanhas** - Agora é possível organizar suas jornadas e campanhas em pastas para melhorar a navegação e o gerenciamento na interface.

  Data de disponibilidade: início de junho de 2026

+++

