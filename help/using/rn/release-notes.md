---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Notas de versão do Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: c54eab2698cce9f8d0f1e72762dd7ff3e5ebc296
workflow-type: tm+mt
source-wordcount: '1843'
ht-degree: 21%

---

# Notas de versão {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novidades"
>abstract="O **Adobe Journey Optimizer** está sempre fornecendo novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão."

O [!DNL Adobe Journey Optimizer] segue um modelo de entrega contínua, permitindo que a Adobe forneça novos recursos, melhorias e correções também de forma contínua. Essa abordagem permite uma implantação escalável e em fases de recursos para garantir desempenho e estabilidade em todos os ambientes.

Devido a esse modelo, as notas de versão são atualizadas entre as versões mensais. Para obter detalhes completos sobre o ciclo de lançamento e as fases de disponibilidade, consulte o [ciclo de lançamento do Journey Optimizer](releases.md).

O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

## Notas de versão de janeiro de 2026 {#latest-rn}

**Data de lançamento**: 27 a 28 de janeiro de 2026

As seções [Recursos](#jan-26-01-features) e [Melhorias](#jan-26-01-improv) abordam os recursos já disponíveis, enquanto o [Em breve](#jan-26-01-coming-soon) lista os itens agendados para uma data de disponibilidade posterior.

<!-- **The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date. 

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

### Novos recursos {#jan-26-01-features}

<table>
<thead>
<tr>
<th><strong>Exportação de mensagens</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Um novo recurso <strong>Exportação de Mensagem</strong> está disponível para canais de email e SMS. Esse recurso permite exportar automaticamente o conteúdo da mensagem enviada para um conjunto de dados dedicado do Experience Platform, permitindo:</p>
<ul>
<li>Atender aos requisitos de conformidade normativa (como a HIPAA)</li>
<li>Arquivar mensagens para solicitações legais e consultas do atendimento ao cliente</li>
<li>Reter cópias de conteúdo personalizado enviadas a indivíduos</li>
</ul>
<p>Os registros são retidos no conjunto de dados de exportação de mensagens do AJO por 7 dias corridos a partir da assimilação. Durante esse período de retenção, você pode exportá-los para seu próprio armazenamento por meio dos destinos do Experience Platform. O recurso é habilitado no nível de configuração de canal, fornecendo a você <strong>controle granular</strong> sobre quais mensagens são exportadas.</p>
<p>Esse recurso só está disponível para o canal de email e SMS, para organizações que compraram a oferta complementar Exportação de mensagens. Para obter mais informações, entre em contato com o seu representante da Adobe.</p>
<p><img src="assets/do-not-localize/message-export.gif"/></p>
<p>Para obter mais informações, consulte a <a href="../configuration/message-export.md#message-export">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal de notificações por push da Web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Adobe Journey Optimizer agora oferece suporte a <strong>Notificações por push da Web</strong>, expandindo o canal de push para além dos dispositivos móveis. Você pode enviar notificações facilmente para <strong>navegadores móveis e para desktop</strong>, permitindo que você alcance os clientes diretamente em seus dispositivos sem exigir um aplicativo. Esse aprimoramento permite que você interaja com os usuários com mensagens personalizadas e oportunas em tempo real, aproveitando os mesmos fluxos de trabalho de criação e recursos de segmentação já disponíveis para push móvel.</p>
<p><img src="assets/do-not-localize/web-push.gif"/></p>
<p>Anteriormente lançado na versão beta, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<p>Para obter mais informações, consulte a <a href="../push/push-configuration-web.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal de correspondência direta em campanhas orquestradas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O canal de correspondência direta agora está disponível em campanhas orquestradas. A <strong>Atividade de correspondência direta</strong> facilita o envio de correspondência direta dentro da campanha Orquestrada, tanto para mensagens únicas quanto para mensagens recorrentes. Ele serve para automatizar o processo de geração do <strong>arquivo de extração</strong> exigido por provedores de correspondência direta. É possível combinar atividades de canal na tela da campanha orquestrada para criar campanhas entre canais que podem acionar ações com base no comportamento e nos dados do cliente.</p>
<p><img src="assets/do-not-localize/dm-oc.gif"/></p>
<p>Para obter mais informações, consulte a <a href="../orchestrated/activities/channels.md#channel">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent - Criar uma Jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Agent agora oferece recursos de criação, permitindo que os usuários do Journey Optimizer criem e configurem jornadas de marketing por meio de uma <strong>interface de linguagem natural</strong>. Com essas novas habilidades, os profissionais podem criar jornadas rapidamente descrevendo seus requisitos em <strong>prompts de conversa</strong>. Essa inovação simplifica o processo de criação de jornadas, permitindo que os profissionais de marketing se concentrem na estratégia em vez da configuração técnica.</p>
<p>Para obter mais informações, consulte a <a href="../start/ai-features.md#journey-agent">documentação detalhada</a>.</p>
<p>Data de disponibilidade: terça-feira, 12 de janeiro de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API de recuperação da campanha de ação</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Uma nova API do Journey Optimizer agora está disponível, permitindo recuperar e inspecionar programaticamente <strong>dados relacionados à campanha</strong>, como detalhes, versões e configurações.</p>
<p>Para obter mais informações, consulte a <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/" target="_blank">documentação detalhada</a>.</p>
<p>Data de disponibilidade: terça-feira, 24 de novembro de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Temas do Designer de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode aplicar rapidamente <strong>temas pré-aprovados</strong> para garantir a <strong>consistência da marca</strong> em todos os emails, acelerar o processo de criação de campanha e produzir emails de alta qualidade de maneira independente, reduzindo a dependência de equipes de design.</p>
<p><img src="assets/do-not-localize/themes.gif"/></p>
<p>Lançado anteriormente na versão beta, esse recurso agora está disponível para algumas organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.</p>
<p>Para obter mais informações, consulte a <a href="../email/apply-email-themes.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: quinta-feira, 5 de novembro de 2025</p>
</td>
</tr>
</tbody>
</table>

### Aprimoramentos {#jan-26-01-improv}

#### IA

* **Verificações de Qualidade de Conteúdo do Assistente de IA** - Além do alinhamento da marca, você agora pode avaliar a <strong>qualidade do conteúdo</strong> geral para descobrir possíveis problemas com a <strong>legibilidade</strong>, coesão e eficácia, independentemente das diretrizes da sua marca. Essas verificações automatizadas ajudam a identificar mensagens não claras, tom inconsistente ou lacunas estruturais. [Leia mais](../content-management/brands-score.md#validate-quality). [Descubra este recurso no vídeo](https://video.tv.adobe.com/v/3470551/?captions=por_br&learn=on).

#### Experience Decisioning

* **Anexar fragmentos a itens de decisão** - A Journey Optimizer agora fornece a capacidade de anexar <strong>fragmentos</strong> a <strong>itens de decisão</strong> que podem ser aproveitados em campanhas de experiência baseadas em código por meio de políticas de decisão. [Leia mais](../experience-decisioning/items.md)

  **Observação**: anteriormente lançada em Disponibilidade Limitada, essa melhoria agora está disponível para todos os ambientes (Disponibilidade Geral).

#### Jornadas

* **Combinar ações de mensagens nativas e do Adobe Campaign** - o Journey Optimizer agora permite combinar <strong>ações de mensagem do Adobe Campaign v7/v8</strong> com <strong>ações de canal nativo</strong> na mesma jornada. [Leia mais](../building-journeys/using-adobe-campaign-v7-v8.md)

* **Carga de resposta de erro de ação personalizada** - Agora você pode definir uma <strong>carga de resposta de erro</strong> opcional para ações personalizadas. Quando uma chamada falha, a carga do erro é exposta no contexto de jornada (no nó errorResponse da ação) e está disponível na <strong>ramificação de tempo limite/erro</strong>, juntamente com `jo_status_code`, para oferecer suporte a uma lógica de fallback e depuração mais avançadas. [Leia mais](../action/action-response.md)

* **Validação do tamanho da carga do Jornada no jornada** - o Journey Optimizer agora valida <strong>tamanhos de carga</strong> para ajudar a garantir desempenho e estabilidade de sistema ideais. Ao criar ou publicar jornadas, você receberá <strong>avisos e erros</strong> claros se os tamanhos de carga se aproximarem ou excederem os limites recomendados, juntamente com orientações acionáveis para otimizar sua configuração de jornada. Essa validação proativa ajuda a identificar problemas em potencial antecipadamente e a manter o desempenho do jornada. [Leia mais](../start/guardrails.md#journey-payload-size)

* **Alertas de Jornada** - Novos <strong>alertas pré-configurados</strong> estão disponíveis para o jornada.
   * <strong>Taxa de Descarte de Perfil Excedida</strong> - A taxa de descartes de perfil para perfis inseridos nos últimos 5 minutos excedeu o limite
   * <strong>Taxa de Erro de Ação Personalizada Excedida</strong> - Taxa de erros de ação personalizada para chamadas HTTP bem-sucedidas nos últimos 5 minutos excedeu o limite
   * <strong>Taxa de Erro de Perfil Excedida</strong> - A taxa de perfis com erro em relação aos perfis inseridos nos últimos 5 minutos excedeu o limite

  Para obter mais informações, consulte a [documentação detalhada](../reports/alerts.md).

  Data de disponibilidade: 14 de outubro de 2025.

#### Campanhas orquestradas

* **Herança de rótulo de uso de dados para públicos-alvo** - Os rótulos aplicados no Adobe Experience Platform agora são transferidos automaticamente ao salvar <strong>públicos-alvo</strong> em campanhas orquestradas, reduzindo a <strong>marcação DULE</strong> manual. [Leia mais](../orchestrated/activities/save-audience.md)

* **Filtros predefinidos com parâmetros** - Agora você pode criar <strong>filtros predefinidos</strong> com <strong>parâmetros</strong> em campanhas orquestradas para regras editáveis e reutilizáveis. [Leia mais](../orchestrated/predefined-filters.md)

* **Selecionar atributos e copiar valores de distribuição** - Agora você pode <strong>selecionar ou copiar valores</strong> diretamente da exibição <strong>distribuição de valores</strong> em campanhas orquestradas. [Leia mais](../orchestrated/build-query.md)

* **Confirmação de mensagem antes de enviar** - Uma <strong>etapa de confirmação</strong> agora está habilitada por padrão antes de enviar campanhas orquestradas para reduzir envios acidentais. [Leia mais](../orchestrated/activities/channels.md#confirm-message-sending)

* **Filtros de redirecionamento predefinidos** - Para facilitar o redirecionamento de casos de uso de campanhas orquestradas, esta versão introduz novos <strong>filtros de comentários de campanha</strong>. Esses filtros permitem direcionar públicos diretamente com base em <strong>envolvimento de mensagens</strong>, como enviado, aberto somente, aberto ou clicado, ou aberto e clicado, e selecionar a campanha específica ou a campanha em transição que deseja redirecionar. [Leia mais](../orchestrated/retarget.md)

* **Suporte ao controle de taxa** - As campanhas orquestradas agora oferecem suporte ao <strong>controle de taxa</strong> para ajudar você a acompanhar as entregas e alinhar-se às <strong>restrições de volume</strong>. [Leia mais](../orchestrated/activities/channels.md#rate-control)

* **Botão Reiniciar** - As campanhas orquestradas agora incluem um <strong>botão Reiniciar</strong> para que você possa <strong>reiniciar as execuções</strong> rapidamente quando necessário, antes de publicar a campanha. [Leia mais](../orchestrated/start-monitor-campaigns.md)

* **Suporte a metadados gerados pelo usuário** - A <strong>função auxiliar executionMetadata</strong> agora está disponível no editor de personalização para campanhas Orquestradas, permitindo que você anexe informações contextuais a qualquer ação nativa e armazene-a em um conjunto de dados para exportação para sistemas externos. [Leia mais](../personalization/functions/helpers.md#execution-metadata)

#### Campanhas

* **Agendar campanha usando o Fuso Horário do Perfil** - O agendamento de campanha agora pode usar o <strong>fuso horário</strong> de cada perfil para entregar mensagens no horário local desejado. [Leia mais](../campaigns/campaign-schedule.md)

  **Observação**: esta melhoria só estará disponível para um conjunto de organizações (Disponibilidade Limitada).

#### Permissões

* **Impedir a autoaprovação para jornadas e campanhas** - Adição de uma opção ao criar ou definir a <strong>Política de Aprovação</strong> para impedir que os criadores de jornadas ou campanhas <strong>aprovem seus próprios objetos</strong>. [Leia mais](../test-approve/approval-policies.md)

## Em breve {#jan-26-01-coming-soon}

Os recursos e aprimoramentos a seguir estão programados para serem lançados nos próximos dias. **As informações estão sujeitas a alterações**. Links, telas e documentação atualizados serão compartilhados assim que essas atualizações estiverem ativas na produção.

### Recursos

<table>
<thead>
<tr>
<th><strong>Canal de correspondência direta no jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Anteriormente limitado a Campanhas, o canal <strong>Correspondência direta</strong> agora está disponível na tela de jornada, permitindo que você incorpore correspondência direta às suas jornadas. A Correspondência Direta agora pode ser usada em <strong>cenários de jornada em lote e 1:1</strong>, com suporte para configuração de extração de arquivos e configurações de frequência baseadas em tempo.</p>
<p>Anteriormente lançado com disponibilidade limitada, esse recurso estará disponível para todos os ambientes (disponibilidade geral).</p>
<p>Data de disponibilidade: quinta-feira, 28 de janeiro de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Horas de silêncio (exclusões com base no tempo)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O <strong>Período de silêncio</strong> permite definir exclusões com base no tempo para os canais de email, SMS, push e WhatsApp. Elas garantem que nenhuma mensagem seja enviada durante períodos específicos, ajudando você a respeitar as preferências do cliente e os requisitos de conformidade. Você pode aplicar horas de silêncio por meio de <strong>conjuntos de regras</strong>, que podem ser atribuídos a ações individuais em campanhas ou jornadas para obter um controle preciso.</p>
<p>Anteriormente lançado com disponibilidade limitada, esse recurso agora está disponível para todos os ambientes. Com esta versão de Disponibilidade geral, o recurso agora inclui a capacidade de o cliente colocar uma ação de campanha na fila até a conclusão do Período de silêncio e a capacidade de pré-visualizar a regra de Período de silêncio ativada.</p>
<p>Data de disponibilidade: quinta-feira, 28 de janeiro de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>APIs de ferramentas de migração de autoatendimento</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>As APIs de ferramentas de migração</strong> agora estão disponíveis para migrar de forma programática entidades de gestão de decisões para o Decisioning, apresentando:</p>
<ul>
<li>Escopos de migração flexíveis (nível de sandbox, oferta ou decisão)</li>
<li>Análise e validação automatizadas de dependências</li>
<li>Suporte à reversão para migrações concluídas</li>
<li>Relatórios de migração detalhados com mapeamentos de objetos</li>
</ul>
<p>Data de disponibilidade: quinta-feira, 28 de janeiro de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Monitoramento de ação personalizada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Insight Saiba mais sobre a integridade e o desempenho de seus <strong>pontos de extremidade de ação personalizados</strong> com um novo painel de monitoramento e dados de evento de etapa do jornada aprimorados. Rastreie chamadas bem-sucedidas, erros, taxa de transferência, tempos de resposta e tempos de espera da fila para entender rapidamente quando, onde e por que ocorrem anomalias.</p>
<p>Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<p>Data de disponibilidade: quinta-feira, 28 de janeiro de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Geração de conteúdo no Journey Agent</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Desenvolvido pela Adobe Experience Platform Agent Orchestrator, o <strong>Journey Agent</strong> está disponível no Journey Optimizer e permite que você analise jornadas por meio de uma interface de linguagem natural. Agora você também pode <strong>gerar e gerenciar conteúdo</strong> diretamente no Journey Agent, criar conteúdo para canais como email e push, aplicar e visualizar modelos, refinar o tom e o estilo por meio de prompts e abrir conteúdo no Designer de Conteúdo para edição em contexto.</p>
<p>Data de disponibilidade: terça-feira, 2 de fevereiro de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Suporte à decisão em canais Push e SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode personalizar e otimizar o conteúdo de suas <strong>Mensagens por push e SMS</strong> com a <strong>Decisão</strong>. Use Pontuações de prioridade, Fórmulas ou Modelos de IA para exibir o melhor conteúdo para seus clientes.</p>
<p>Data de disponibilidade: quarta-feira, 3 de fevereiro de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Atividade de decisão de conteúdo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Uma nova <strong>Atividade de decisão de conteúdo</strong> está disponível na tela de jornada para integrar <strong>ofertas personalizadas</strong> diretamente às jornadas do cliente. Essa atividade permite fornecer conteúdo baseado em decisão e fazer referência a essas ofertas em toda a jornada, em condições para criar ramificações baseadas em elegibilidade, em ações personalizadas para transmitir dados de oferta a sistemas externos e em outras atividades para criar experiências do cliente totalmente personalizadas.</p>
<p>Esse recurso estará disponível para todos os ambientes (Disponibilidade geral).</p>
<p>Data de disponibilidade: quarta-feira, 3 de fevereiro de 2026</p>
</td>
</tr>
</tbody>
</table>

### Aprimoramentos

* Agora há suporte para **Webhooks de SMS** - <strong>Webhooks</strong> em todos os provedores de SMS. Você pode configurar cada webhook com base na finalidade pretendida, webhooks de entrada para capturar mensagens de entrada e webhooks de feedback para receber confirmações de entrega, atualizações de status e outros eventos relacionados à mensagem.

  Data de disponibilidade: 28 de janeiro de 2026.
