---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão de 2026
description: Notas de versão de 2026 do Journey Optimizer
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 65ca94cf-8e17-4a25-90f3-238083f81477
source-git-commit: eb1056b57e72ab1cff5e32bff31b9cba5604f695
workflow-type: tm+mt
source-wordcount: '1371'
ht-degree: 87%

---

# Notas de versão de 2026 {#release-notes-2026}

Esta página lista todos os recursos e melhorias da versão de 2026 do [!DNL Journey Optimizer].

## Notas de versão de janeiro de 2026 {#jan-26-rn}

<!--**Release date**: January 27-28, 2026-->

### Novos recursos {#jan-26-01-features}


<table>
<thead>
<tr>
<th><strong>Suporte à decisão no canal push</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode personalizar e otimizar o conteúdo de suas <strong>Notificações por push</strong> com a <strong>Decisão</strong>. Use Pontuações de prioridade, Fórmulas ou Modelos de IA para exibir o melhor conteúdo para os clientes.</p>
<p>O Experience Decisioning com notificações por push requer uma versão específica do Mobile SDK. Antes de implementar este recurso, verifique as <a href="https://developer.adobe.com/client-sdks/home/release-notes/" target="_blank">notas de versão</a> para identificar a versão necessária e se você atualizou adequadamente. Você também pode exibir todas as versões do SDK disponíveis para sua plataforma <a href="https://developer.adobe.com/client-sdks/home/current-sdk-versions/" target="_blank">nesta seção</a>.</p>
<p>Para obter mais informações, consulte a <a href="../experience-decisioning/create-decision.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 30 de janeiro de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal de correspondência direta em jornadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Anteriormente limitado a campanhas, o canal <strong>Correspondência direta</strong> agora está disponível na tela de jornada, permitindo que você incorpore correspondência direta às jornadas. A Correspondência direta agora pode ser usada em <strong>cenários de jornada em lote e 1:1</strong>, com suporte para configuração de extração de arquivos e configurações de frequência baseadas em tempo.</p>
<p>Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<p><img src="assets/do-not-localize/dm-journey.gif"/></p>
<p>Para obter mais informações, consulte a <a href="../direct-mail/get-started-direct-mail.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: sexta-feira, 29 de janeiro de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Períodos de silêncio (exclusões com base no tempo)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Os <strong>Períodos de silêncio</strong> permitem definir exclusões baseadas em tempo para canais de email, SMS, notificações por push e WhatsApp. Eles garantem que nenhuma mensagem seja enviada durante períodos específicos, ajudando a respeitar as preferências do cliente e os requisitos de conformidade. É possível aplicar períodos de silêncio por meio de <strong>conjuntos de regras</strong>, que podem ser atribuídos a ações individuais em campanhas ou jornadas para proporcionar um controle preciso.</p>
<p>Anteriormente lançado com disponibilidade limitada, esse recurso agora está disponível para todos os ambientes. Nesta versão de disponibilidade geral, o recurso agora permite colocar uma ação de campanha na fila até a conclusão do Horário de silêncio e inclui a capacidade de pré-visualizar a regra de Horário de silêncio ativada.</p>
<p><img src="assets/do-not-localize/quiet-hour-ga.gif"/></p>
<p>Para obter mais informações, consulte a <a href="../conflict-prioritization/quiet-hours.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: sexta-feira, 29 de janeiro de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Exportação de mensagem</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Um novo recurso <strong>Exportação de mensagem</strong> está disponível para canais de email e SMS. Esse recurso permite exportar automaticamente o conteúdo da mensagem enviada para um conjunto de dados dedicado da Experience Platform, permitindo:</p>
<ul>
<li>Atender aos requisitos de conformidade normativa (como a HIPAA)</li>
<li>Arquivar mensagens para solicitações legais e consultas do atendimento ao cliente</li>
<li>Reter cópias de conteúdo personalizado enviadas a indivíduos</li>
</ul>
<p>Os registros são retidos no conjunto de dados de exportação de mensagens do AJO por sete dias corridos a partir da ingestão. Durante esse período de retenção, você pode exportá-los para seu próprio armazenamento por meio dos destinos do Experience Platform. O recurso é habilitado no nível de configuração de canais, fornecendo a você <strong>controle granular</strong> sobre quais mensagens são exportadas.</p>
<p>Esse recurso está disponível apenas para os canais de email e SMS, para organizações que adquiriram o complemento de Exportação de mensagem. Para obter mais informações, entre em contato com o(a) representante da Adobe.</p>
<p><img src="assets/do-not-localize/message-export.gif"/></p>
<p>Para obter mais informações, consulte a <a href="../configuration/message-export.md#message-export">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 28 de janeiro de 2026</p>
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
<p>O canal de correspondência direta agora está disponível em campanhas orquestradas. A atividade <strong>Correspondência direta</strong> facilita o envio de correspondência direta dentro da campanha orquestrada, tanto para mensagens únicas quanto recorrentes. Ela serve para automatizar o processo de geração do <strong>arquivo de extração</strong> exigido pelos fornecedores de correspondência direta. É possível combinar atividades de canal na tela da campanha orquestrada para criar campanhas entre canais que podem acionar ações com base no comportamento e nos dados do cliente.</p>
<p><img src="assets/do-not-localize/dm-oc.gif"/></p>
<p>Para obter mais informações, consulte a <a href="../orchestrated/activities/channels.md#channel">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 28 de janeiro de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent: criar uma jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Agent agora oferece recursos de criação, permitindo que os usuários do Journey Optimizer criem e configurem jornadas de marketing por meio de uma <strong>interface de linguagem natural</strong>. Com essas novas habilidades, os profissionais podem criar jornadas rapidamente descrevendo seus requisitos em <strong>prompts de conversa</strong>. Essa inovação simplifica o processo de criação de jornadas, permitindo que os profissionais de marketing se concentrem na estratégia em vez da configuração técnica.</p>
<p>Para obter mais informações, consulte a <a href="../start/ai-features.md#journey-agent">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 12 de janeiro de 2026</p>
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
<p>Uma nova API do Journey Optimizer já está disponível, permitindo que você recupere e inspecione programaticamente <strong>dados relacionados à campanha</strong>, como detalhes, versões e configurações.</p>
<p>Para obter mais informações, consulte a <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/" target="_blank">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 24 de novembro de 2025</p>
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
<p>Agora você pode aplicar rapidamente <strong>temas pré-aprovados</strong> para garantir a <strong>consistência da marca</strong> em todos os emails, acelerar o processo de criação de campanhas e produzir emails de alta qualidade de forma independente, reduzindo a dependência de equipes de design.</p>
<p><img src="assets/do-not-localize/themes.gif"/></p>
<p>Lançado anteriormente na versão beta, esse recurso agora está disponível para algumas organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.</p>
<p>Para obter mais informações, consulte a <a href="../email/apply-email-themes.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 5 de novembro de 2025</p>
</td>
</tr>
</tbody>
</table>

### Aprimoramentos {#jan-26-01-improv}

#### IA

* **Verificações de qualidade de conteúdo do Assistente de IA**: além do alinhamento da marca, você agora pode avaliar a <strong>qualidade do conteúdo</strong> geral para descobrir possíveis problemas de <strong>legibilidade</strong>, coesão e eficácia, independentemente das diretrizes da marca. Essas verificações automatizadas ajudam a identificar mensagens não claras, tom inconsistente ou falhas estruturais. [Leia mais](../content-management/brands-score.md#validate-quality).

  [Conheça este recurso no vídeo](https://video.tv.adobe.com/v/3470551/?captions=por_br&learn=on).

#### Jornadas

* **Combinar ações de mensagens nativas e do Adobe Campaign**: o Journey Optimizer agora permite combinar ações de mensagem do <strong>Adobe Campaign v7/v8</strong> com <strong>ações de canal nativo</strong> na mesma jornada. [Leia mais](../building-journeys/using-adobe-campaign-v7-v8.md)

  Data de disponibilidade: quarta-feira, 27 de janeiro de 2026.

* **Conteúdo de resposta de erro de ação personalizada**: agora você pode definir um <strong>conteúdo de resposta de erro</strong> opcional para ações personalizadas. Quando uma chamada falha, o conteúdo do erro é exposto no contexto da jornada (no nó errorResponse da ação) e está disponível na <strong>ramificação de tempo limite/erro</strong>, juntamente com `jo_status_code`, para oferecer suporte a uma lógica de fallback e depuração mais avançadas. [Leia mais](../action/about-custom-action-configuration.md#define-the-message-parameters)

  Data de disponibilidade: quarta-feira, 27 de janeiro de 2026.

* **Validação do tamanho do conteúdo da jornada em jornadas**: o Journey Optimizer agora valida <strong>tamanhos de conteúdo</strong> para ajudar a garantir desempenho e estabilidade de sistema ideais. Ao criar ou publicar jornadas, você receberá <strong>avisos e erros</strong> claros se os tamanhos de conteúdo se aproximarem ou excederem os limites recomendados, juntamente com orientações acionáveis para otimizar a configuração de jornada. Essa validação proativa ajuda a identificar problemas em potencial antecipadamente e a manter o desempenho da jornada. [Leia mais](../start/guardrails.md#journey-payload-size)

  Data de disponibilidade: quarta-feira, 27 de janeiro de 2026.


* **Alertas de jornada**: novos <strong>alertas pré-configurados</strong> estão disponíveis para jornadas.
   * <strong>Taxa de descarte de perfis excedida</strong>: a proporção de perfis descartados em relação aos perfis inseridos nos últimos 5 minutos excedeu o limite
   * <strong>Taxa de erros de ação personalizada excedida</strong>: a proporção de erros de ação personalizada em relação às chamadas HTTP bem-sucedidas nos últimos 5 minutos excedeu o limite
   * <strong>Taxa de erro de perfil excedida</strong>: a proporção de perfis com erro em relação aos perfis inseridos nos últimos 5 minutos excedeu o limite

  Para obter mais informações, consulte a [documentação detalhada](../reports/alerts.md).

  Data de disponibilidade: 14 de outubro de 2025.

#### Campanhas orquestradas

* **Herança de rótulo de uso de dados para públicos-alvo**: os rótulos aplicados na Adobe Experience Platform agora são transferidos automaticamente ao salvar <strong>públicos-alvo</strong> em campanhas orquestradas, reduzindo a <strong>marcação DULE</strong> manual. [Leia mais](../orchestrated/activities/save-audience.md)

* **Filtros predefinidos com parâmetros**: agora você pode criar <strong>filtros predefinidos</strong> com <strong>parâmetros</strong> em campanhas orquestradas para regras editáveis e reutilizáveis. [Leia mais](../orchestrated/predefined-filters.md)

* **Selecionar atributos e copiar valores de distribuição**: agora é possível <strong>selecionar ou copiar valores</strong> diretamente da tela <strong>Distribuição de valores</strong> em campanhas orquestradas. [Leia mais](../orchestrated/build-query.md)

* **Confirmação de mensagem antes do envio**: uma <strong>etapa de confirmação</strong> agora está habilitada por padrão antes de enviar campanhas orquestradas para reduzir envios acidentais. [Leia mais](../orchestrated/activities/channels.md#confirm-message-sending)

* **Filtros de redirecionamento predefinidos**: para facilitar o redirecionamento de casos de uso de campanhas orquestradas, esta versão introduz novos <strong>filtros de feedback de campanha</strong>. Esses filtros permitem direcionar públicos-alvo diretamente com base no <strong>engajamento de mensagens</strong>, como enviado, aberto somente, aberto ou clicado, ou aberto e clicado, e selecionar a campanha específica ou a campanha em transição que você deseja redirecionar. [Leia mais](../orchestrated/retarget.md)

* **Suporte ao controle de taxa**: as campanhas orquestradas agora oferecem suporte ao <strong>controle de taxa</strong> para ajudar você a acompanhar as entregas e alinhar-se às <strong>restrições de volume</strong>. [Leia mais](../orchestrated/activities/channels.md#rate-control)

* **Botão Reiniciar**: as campanhas orquestradas agora incluem um <strong>botão Reiniciar</strong> para que você possa <strong>reiniciar as execuções</strong> rapidamente quando necessário, antes de publicar a campanha. [Leia mais](../orchestrated/start-monitor-campaigns.md)

* **Suporte a metadados gerados pelo usuário**: a <strong>função auxiliar executionMetadata</strong> agora está disponível no editor de personalização para campanhas orquestradas, permitindo que você anexe informações contextuais a qualquer ação nativa e armazene-a em um conjunto de dados para exportação para sistemas externos. [Leia mais](../personalization/functions/helpers.md#execution-metadata)

  Data de disponibilidade: quarta-feira, 27 de janeiro de 2026.

* **Reverter campanhas ativas para o status de rascunho** - Agora é possível reverter campanhas orquestradas em tempo real para o status de rascunho quando elas encontram erros de execução ou quando é necessário modificar campanhas agendadas antes de começarem a ser executadas. Essa opção estará disponível até que a primeira mensagem seja enviada. [Leia mais](../orchestrated/start-monitor-campaigns.md#back-to-draft)

#### Campanhas

* **Agendar campanha usando o Fuso Horário do Perfil** - O agendamento de campanha agora pode usar o <strong>fuso horário</strong> de cada perfil para entregar mensagens no horário local desejado. [Leia mais](../campaigns/campaign-schedule.md)

  **Observação**: esta melhoria só estará disponível para um conjunto de organizações (Disponibilidade Limitada).

  Data de disponibilidade: quarta-feira, 27 de janeiro de 2026.

#### Permissões

* **Impedir a autoaprovação para jornadas e campanhas**: adição de uma opção ao criar ou definir a <strong>Política de aprovação</strong> para impedir que os criadores de jornadas ou campanhas <strong>aprovem seus próprios objetos</strong>. [Leia mais](../test-approve/approval-policies.md)

  Data de disponibilidade: quarta-feira, 27 de janeiro de 2026.
