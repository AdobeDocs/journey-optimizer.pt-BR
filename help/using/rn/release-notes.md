---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Notas de versão do Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 21231a10389a6238cff6d71966ce2bab8379ea59
workflow-type: tm+mt
source-wordcount: '2096'
ht-degree: 28%

---

# Notas de versão {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novidades"
>abstract="O **Adobe Journey Optimizer** está sempre fornecendo novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão."

O [!DNL Adobe Journey Optimizer] segue um modelo de entrega contínua, permitindo que a Adobe forneça novos recursos, melhorias e correções também de forma contínua. Essa abordagem permite uma implantação escalável e em fases de recursos para garantir desempenho e estabilidade em todos os ambientes.

Devido a esse modelo, as notas de versão são atualizadas entre as versões mensais. Para obter detalhes completos sobre o ciclo de lançamento e as fases de disponibilidade, consulte o [ciclo de lançamento do Journey Optimizer](releases.md).

O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/latest){target="_blank"}.

## Notas de pré-lançamento de janeiro de 2026 {#latest-rn}

**Data de lançamento**: quarta-feira, 27 de janeiro de 2026

**As notas de pré-lançamento abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade da versão**. Links, telas e a documentação atualizada são publicados nas notas de versão na data de lançamento.

Consulte também as [Notas de pré-lançamento da Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

### Novos recursos {#jan-26-01-features}

<table>
<thead>
<tr>
<th><strong>Atividade de ação em jornadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer oferece suporte a uma nova <strong>Atividade de ação</strong> genérica que permite configurar ações únicas e <strong>grupos de ação de entrada de várias ações</strong>, permitindo a configuração de ação simplificada na tela de jornada. Em especial, este novo recurso permite:</p>
<ul>
<li>Uma configuração de ação nativa simplificada na tela da jornada.</li>
<li>A capacidade de criar grupos de ação de entrada multiação.</li>
<li>A capacidade de adicionar otimização a qualquer ação de canal integrada.</li>
<li>A capacidade de adicionar opções de experimentação e multilíngues a qualquer ação.</li>
</ul>
<p>Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
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
<p>Obtenha um insight mais profundo sobre a integridade e o desempenho dos endpoints de ação personalizados com um novo <strong>painel de monitoramento</strong> e dados de evento de etapa do jornada aprimorados. Rastreie chamadas bem-sucedidas, erros, taxa de transferência, tempos de resposta e tempos de espera da fila para entender rapidamente quando, onde e por que ocorrem anomalias.</p>
<p>Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Período de silêncio/ Exclusões com base no tempo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Quiet hours permite definir <strong>exclusões com base no tempo</strong> para canais de email, SMS, push e WhatsApp. Elas garantem que nenhuma mensagem seja enviada durante períodos específicos, ajudando você a respeitar as preferências do cliente e os requisitos de conformidade. Você pode aplicar horas de silêncio por meio de <strong>conjuntos de regras</strong>, que podem ser atribuídos a ações individuais em campanhas ou jornadas para obter um controle preciso.</p>
<p><strong>Observação</strong>: não há suporte para o Período de Silêncio em campanhas Orquestradas.</p>
<p>Anteriormente lançado com disponibilidade limitada, esse recurso agora está disponível para todos os ambientes. Com esta versão de Disponibilidade geral, o recurso agora inclui a capacidade de o cliente colocar uma ação de campanha na fila até a conclusão do Período de silêncio e a capacidade de pré-visualizar a regra de Período de silêncio ativada.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal de correspondência direta no jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Anteriormente limitado a Campanhas, o <strong>canal de Correspondência Direta</strong> agora está disponível na <strong>tela de jornada</strong>, permitindo que você incorpore a Correspondência Direta às suas jornadas. A correspondência direta agora pode ser usada em cenários de jornada em lote e 1:1, com suporte para configuração de extração de arquivos e configurações de frequência baseadas em tempo.</p>
<p>Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
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
<p>O Adobe Journey Optimizer agora oferece suporte a <strong>Notificações por push da Web</strong>, expandindo o canal de push para além dos dispositivos móveis. Você pode enviar notificações facilmente para navegadores móveis e de desktop, permitindo que alcançar os clientes diretamente em seus dispositivos sem exigir um aplicativo. Esse aprimoramento permite que você interaja com os usuários com mensagens personalizadas e oportunas em tempo real, aproveitando os mesmos fluxos de trabalho de criação e recursos de segmentação já disponíveis para push móvel.</p>
<p>Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<p><strong>Observação</strong>: a notificação silenciosa ainda não tem suporte para notificações por push da Web.</p>
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
<p>Agora você pode adicionar <strong>Políticas de decisão</strong> em jornadas e campanhas de push e SMS. As políticas de decisão são recipientes para as suas ofertas que utilizam o mecanismo de tomada de decisão para retornar dinamicamente o melhor conteúdo a ser entregue a cada membro do público-alvo.</p>
<p>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.</p>
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
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Novos conectores de origem para aplicativos de fidelidade</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Novos <strong>conectores de origem</strong> já estão disponíveis no Adobe Experience Platform para os aplicativos de fidelidade Talon.One, Capillary e Kobie. Esses conectores permitem transmitir dados de fidelidade continuamente para a Adobe Experience Platform e usar esses dados no Journey Optimizer.</p>
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
<p>Um novo recurso <strong>Exportação de Mensagem</strong> está disponível para canais de email e SMS. Esse recurso permite exportar automaticamente o conteúdo da mensagem enviada para um conjunto de dados dedicado do Experience Platform, permitindo:</p>
<ul>
<li>Atender aos requisitos de conformidade normativa (como a HIPAA)</li>
<li>Arquivar mensagens para solicitações legais e consultas do atendimento ao cliente</li>
<li>Reter cópias de conteúdo personalizado enviadas a indivíduos</li>
</ul>
<p>Os registros são retidos no Conjunto de Dados de Exportação de Mensagens do AJO por <strong>7 dias a partir da assimilação</strong>. Durante esse período de retenção, você pode exportar os dados para seu próprio armazenamento por meio dos destinos do Experience Platform. O recurso é ativado no nível de configuração do canal, fornecendo controle granular sobre quais mensagens são exportadas.</p>
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
<p>O Agente de criação de Jornada permite que os usuários do Journey Optimizer criem e configurem jornadas de marketing usando uma interface de linguagem natural. Com o Jornada Create Agent, os profissionais podem criar jornadas rapidamente descrevendo seus requisitos em prompts de conversa. O agente simplifica a criação de jornadas, permitindo que os profissionais de marketing se concentrem na estratégia em vez da configuração técnica.</p>
<p><a href="https://experienceleague.adobe.com/pt-br/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent#journey-create-agent-skill-overview-and-user-guide" target="_blank">Saiba mais</a></p>
<p>Data de disponibilidade: terça-feira, 12 de janeiro de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nova API para recuperar Campanhas de ação</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Uma nova <strong>API do Journey Optimizer</strong> está disponível, permitindo recuperar e inspecionar programaticamente dados relacionados à campanha, como detalhes, versões e configurações.</p>
<p>Para obter mais informações, consulte a <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/">documentação detalhada</a>.</p>
<p>Data de disponibilidade: terça-feira, 24 de novembro de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Novos alertas de jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Três novos <strong>alertas de jornada</strong> já estão disponíveis para ajudá-lo a monitorar e rastrear os eventos de ciclo de vida da jornada e o desempenho da ação personalizada:</p>
<ul>
<li><strong>Jornada publicada</strong>: receba notificações quando uma jornada for publicada por um profissional na tela de jornada.</li>
<li><strong>Jornada concluída</strong>: receba alertas quando uma jornada for concluída, com definições específicas baseadas no tipo de jornada (Público-alvo de leitura ou acionada por evento).</li>
<li><strong>Limite de ação personalizada acionado</strong>: receba uma notificação quando o limite for ativado em um ponto de acesso de ação personalizada.</li>
</ul>
<p>É possível se inscrever nesses alertas no nível da organização ou para jornadas específicas.</p>
<p>Para obter mais informações, consulte a <a href="../reports/alerts.md#journey-alerts">documentação detalhada</a>.</p>
<p>Data de disponibilidade: quinta-feira, 5 de novembro de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Temas no Designer de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode aplicar rapidamente <strong>temas pré-aprovados</strong> para garantir a consistência da marca em todos os emails, acelerar o processo de criação de campanha e produzir emails de alta qualidade de forma independente, reduzindo a dependência de equipes de design.</p>
<p>Lançado anteriormente na versão beta, esse recurso agora está disponível para algumas organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Para obter mais informações, consulte a <a href="../email/apply-email-themes.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: quinta-feira, 5 de novembro de 2025</p>
</td>
</tr>
</tbody>
</table>

### Aprimoramentos {#jan-26-01-improv}

Os aprimoramentos incluídos nesta versão estão listados abaixo.

#### IA

* **Verificações de Qualidade de Conteúdo do Assistente de IA** - Além do alinhamento da marca, agora você pode avaliar a <strong>qualidade do conteúdo</strong> geral para descobrir possíveis problemas de legibilidade, coesão e eficácia, independentemente das diretrizes da sua marca. Essas verificações automatizadas ajudam a identificar mensagens não claras, tom inconsistente ou lacunas estruturais.

* **Atualizar marcas com a nova guia de cores** - As diretrizes de marca ajudam a garantir que sua marca seja apresentada de forma consistente em todos os pontos de contato. A nova seção <strong>Cores</strong> define os padrões do sistema de cores da sua marca, descrevendo como as cores são selecionadas, organizadas e aplicadas entre experiências. Ela garante o uso consistente de cores primárias, secundárias, de ênfase e neutras para respaldar uma identidade de marca coesa, acessível e reconhecível.

#### Campanhas

* **Agendar campanha usando o Fuso Horário do Perfil** - O agendamento de campanha agora pode usar o <strong>fuso horário</strong> de cada perfil para entregar mensagens no horário local desejado. A programação usando fusos horários do perfil está disponível para canais de email, push, SMS, WhatsApp e LINE.

  **Observação**: esta melhoria está disponível somente para um conjunto de organizações (Disponibilidade Limitada).

#### Canais

* **Webhooks de SMS: Fase II** - Descrição a ser fornecida.

#### Email Designer

* **Correções no local no Designer de email** - Ao gerenciar conteúdo com a diretriz da sua marca, as <strong>Sugestões de conteúdo automático habilitado por IA</strong> agora estarão disponíveis quando violações forem detectadas durante a validação de conteúdo. Se o conteúdo for sinalizado como desalinhado às diretrizes da marca ou falhar nos critérios de qualidade, o sistema gera proativamente alternativas corrigidas que podem ser revisadas e aplicadas em linha, melhorando a conformidade e acelerando a produção.

#### Experience Decisioning

* **APIs de ferramentas de migração de autoatendimento** - Um novo conjunto de <strong>APIs de ferramentas de migração</strong> está disponível para migrar entidades de gerenciamento de ofertas para o Experience Decisioning. A ferramenta permite a migração perfeita entre sandboxes com recursos de resolução de dependência e reversão.

* **Anexar fragmentos a itens de decisão** - O Journey Optimizer agora fornece a capacidade de anexar <strong>fragmentos</strong> a itens de decisão que podem ser aproveitados em campanhas de experiência baseadas em código por meio de políticas de decisão.

  **Observação**: anteriormente lançada em Disponibilidade Limitada, essa melhoria agora está disponível para todos os ambientes (Disponibilidade Geral).

#### Jornadas

* **Aproveite uma carga de resposta de falha nas Ações Personalizadas do jornada** - Agora você pode definir uma <strong>carga de resposta de erro</strong> opcional para ações personalizadas. Quando uma chamada falha, a carga de erro é exposta no contexto da jornada e está disponível na ramificação tempo limite/erro para oferecer suporte a uma lógica de fallback e depuração mais avançadas.

* **Combinar ações de mensagens nativas e do Adobe Campaign** - o Journey Optimizer agora permite combinar ações de mensagem do Adobe Campaign v7/v8 com ações de canal nativas na mesma jornada.

* **Validação do tamanho da carga da Jornada no jornada** - a Journey Optimizer agora fornece a <strong>validação do tamanho da carga</strong> para ajudar a garantir desempenho e estabilidade de sistema ideais. Ao criar ou publicar jornadas, você receberá avisos e erros claros se os tamanhos de carga se aproximarem ou excederem os limites recomendados, juntamente com orientações acionáveis para otimizar a configuração da jornada. Essa validação proativa ajuda a identificar problemas em potencial antecipadamente e a manter o desempenho do jornada.

* **Várias ações de entrada no jornada** - Para simplificar sua orquestração de jornadas, agora é possível definir <strong>várias ações de entrada</strong> em uma única jornada. Anteriormente disponível em campanhas, esse recurso permite que você forneça várias experiências baseadas em código, mensagens no aplicativo, Cartões de conteúdo ou ações da Web a locais diferentes ao mesmo tempo, cada ação contendo um conteúdo específico.

  **Observação**: anteriormente lançada em Disponibilidade Limitada, essa melhoria agora está disponível para todos os ambientes (Disponibilidade Geral).

#### Campanhas orquestradas

* **Selecionar atributos e copiar valores de distribuição** - Agora é possível selecionar ou copiar valores diretamente da exibição de distribuição de valores em campanhas orquestradas.

* **Herança de rótulo de uso de dados para públicos-alvo** - <strong>Os rótulos de uso de dados</strong> aplicados no Adobe Experience Platform agora são transferidos automaticamente ao salvar públicos-alvo em campanhas orquestradas, reduzindo a marcação DULE manual.

* **Filtros de redirecionamento predefinidos** - Para facilitar o redirecionamento de casos de uso de campanhas orquestradas, esta versão introduz novos <strong>filtros de redirecionamento</strong>. Esses filtros permitem direcionar públicos diretamente com base no envolvimento da mensagem, como enviado, aberto somente, aberto ou clicado, ou aberto e clicado, e selecionar a campanha específica ou a campanha em transição que deseja redirecionar.

* **Filtros predefinidos com parâmetros** - Agora você pode criar <strong>filtros com parâmetros</strong> em campanhas orquestradas para regras editáveis e reutilizáveis.

* **Confirmação de mensagem antes de enviar** - Uma <strong>etapa de confirmação</strong> agora está habilitada por padrão antes de enviar campanhas orquestradas para reduzir envios acidentais.

* **Suporte a metadados gerados pelo usuário** - A <strong>função auxiliar executionMetadata</strong> agora está disponível no editor de personalização para Campanhas Orquestradas, permitindo que você anexe informações contextuais a qualquer ação nativa e armazene-a em um conjunto de dados para exportação para sistemas externos.

* **Botão Reiniciar** - As campanhas orquestradas agora incluem um <strong>botão Reiniciar</strong> para que você possa reiniciar rapidamente as execuções quando necessário antes de publicar a campanha.

* **Suporte ao controle de taxa** - As campanhas orquestradas agora oferecem suporte ao <strong>controle de taxa</strong> para ajudar você a acompanhar as entregas e alinhar-se às restrições de volume.

#### Permissões

* **Impedir a autoaprovação para jornadas e campanhas** - Agora é possível exigir que os criadores não aprovem suas próprias jornadas ou campanhas, melhorando a <strong>separação de tarefas</strong> nos fluxos de trabalho de aprovação.

## Em breve {#jan-26-01-coming-soon}

Os recursos e aprimoramentos a seguir estão programados para serem lançados nos próximos dias. **As informações estão sujeitas a alterações**. Links, telas e documentação atualizados serão compartilhados assim que essas atualizações estiverem ativas na produção.

<table>
<thead>
<tr>
<th><strong>Geração de conteúdo no Journey Agent</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Desenvolvido pela Adobe Experience Platform Agent Orchestrator, o <strong>Journey Agent</strong> está disponível no Journey Optimizer e permite que você analise jornadas por meio de uma interface de linguagem natural. Agora, também é possível gerar e gerenciar conteúdo específico do canal diretamente no Journey Agent, criando conteúdo para canais como email e push, aplicando e visualizando modelos, refinando o tom e o estilo por meio de prompts e abrindo conteúdo no Designer de Conteúdo para edição em contexto.</p>
<p>Data de disponibilidade: terça-feira, 2 de fevereiro de 2026</p>
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
<p>Agora você pode incluir <strong>ofertas personalizadas</strong> em suas jornadas por meio de uma atividade dedicada de Decisão de conteúdo na tela de jornada e usá-las em atividades de jornada, incluindo condições e ações personalizadas.</p>
<p>Esse recurso estará disponível para todos os ambientes (Disponibilidade geral).</p>
<p>Data de disponibilidade: quarta-feira, 3 de fevereiro de 2026</p>
</td>
</tr>
</tbody>
</table>
