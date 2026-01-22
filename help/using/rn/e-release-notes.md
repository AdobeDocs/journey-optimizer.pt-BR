---
solution: Journey Optimizer
product: journey optimizer
title: Notas de pré-lançamento do Journey Optimizer
description: Notas de pré-lançamento do Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 86bd616a9331c5225c78ccf52c5d26a063fa8654
workflow-type: tm+mt
source-wordcount: '2080'
ht-degree: 29%

---

# Notas de pré-lançamento {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas no fim de cada mês nas [notas de versão](release-notes.md).


## Pré-notas de versão de janeiro de 2026 {#jan-26-01-rn}

**As notas de pré-lançamento abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade da versão**. Links, telas e a documentação atualizada são publicados nas notas de versão na data de lançamento.

Consulte também as [Notas de pré-lançamento da Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data de lançamento**: terça-feira, 26 de janeiro de 2026

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
<p>O Journey Optimizer oferece suporte a uma nova Action atividade<strong> genérica </strong>que permite configurar tanto ações <strong>únicas quanto grupos de ação de entrada com várias</strong> ações, permitindo uma configuração de ação simplificada na tela da jornada. Em especial, este novo recurso permite:</p>
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
<p>Faça uma insight mais profunda na saúde e no desempenho de seus endpoints de ação personalizadas com um novo <strong>painel</strong> de monitoramento e etapas de jornada enriquecidas dados do evento. Rastrear chamadas, erros, taxa de transferência, tempos de resposta e fila tempos de espera para entender rapidamente quando, onde e por que as anomalias ocorrem.</p>
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
<p>Horas de silêncio permitem definir <strong>exclusões baseadas</strong> em tempo para os canais Email, SMS, Push e WhatsApp. Eles garantem que nenhuma mensagem seja enviada durante períodos específicos de tempo, ajudando você a respeitar as preferências do cliente e os requisitos de conformidade. Você pode aplicar horas de silêncio por meio de <strong>conjuntos de regras</strong>, que podem ser atribuídos a ações individuais em campanhas ou jornadas para obter um controle preciso.</p>
<p>Anteriormente lançado com disponibilidade limitada, esse recurso agora está disponível para todos os ambientes. Com esta versão de Disponibilidade geral, o recurso agora inclui a capacidade de o cliente colocar uma ação de campanha na fila até a conclusão do Período de silêncio e a capacidade de pré-visualizar a regra de Período de silêncio ativada.</p>
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
<p>Anteriormente limitada a Campanhas, o <strong>canal</strong> de Mala direta agora está disponível na tela<strong> da jornada, permitindo incorporar o </strong>Direct Mail às suas jornadas. A Correspondência direta agora pode ser usada em cenários de jornada em lote e 1:1, com suporte para configuração extração de arquivo e configurações de frequência com base no tempo.</p>
<p>Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>canal de notificações por push na Web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Systems Journey Optimizer agora oferece <strong>suporte às notificações por push na</strong> Web, expandindo o canal para além do mobile. Você pode enviar notificações para navegadores móveis e desktop, permitindo que você acesse clientes diretamente em seus dispositivos sem precisar de um aplicativo. Esse aprimoramento permite que você interaja com os usuários com mensagens personalizadas e oportunas em tempo real, aproveitando os mesmos fluxos de trabalho de criação e recursos de segmentação já disponíveis para push móvel.</p>
<p>Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Mensagens básicas do RCS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Com a nova <strong>oferta de complemento</strong> básico do RCS, agora você pode fornecer serviços básicos de comunicação avançada (RCS) mensagens está no Journey Optimizer, permitindo as seguintes capacidades aprimoradas de mensagens sujeitas ao suporte a provedores e operadoras:</p>
<ul>
<li>Suporte a remetentes com marca e verificados: envie mensagens usando perfis de negócios verificados com elementos de marca (logotipo, nome do remetente, etc.).</li>
<li>Insights de entregas de mensagens: receba relatórios de entrega detalhados, incluindo atualizações de status de mensagem (por exemplo, enviado, entregue, lido).</li>
<li>Rastreamento de link: incorpore e rastreie URLs em mensagens RCS para análise de engajamento.</li>
<li>Fallback para SMS: retorno automático para SMS quando o dispositivo do perfil não dá suporte a RCS ou está temporariamente inacessível via RCS.</li>
<li>Composição básica de mensagens: envie mensagens RCS básicas baseadas em texto.</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Suporte a decisões nos canais Push e SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode adicionar <strong>políticas</strong> de decisão em jornadas e campanhas de PUSH e SMS. As políticas de decisão são recipientes para as suas ofertas que utilizam o mecanismo de tomada de decisão para retornar dinamicamente o melhor conteúdo a ser entregue a cada membro do público-alvo.</p>
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
<th><strong>Formulários personalizados de página de destino</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Com o Journey Optimizer, agora você pode capturar <strong>perfil atributos</strong> nas suas páginas iniciais. Criar, design e gerenciar <strong>formulários personalizados</strong> adaptados às suas necessidades com base em um conjunto de dados específico. Em seguida, é possível usar esses formulários em páginas de destino para adicionar os atributos de perfil de sua escolha ao conjunto de dados definido para cada formulário.</p>
<p>Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
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
<p><strong>Novo conectores</strong> de origem estão disponíveis em Adobe Experience Platform para os aplicativos de fidelidade Talon.One, Capillary e Kobie. Esses conectores permitem transmitir dados de fidelidade continuamente para a Adobe Experience Platform e usar esses dados no Journey Optimizer.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Exportação de mensagens</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível <strong>exportar entregas enviadas</strong> para um conjunto de dados específico, para fins de arquivamento e conformidade. Essa capacidade está disponível não apenas para email, mas também para outros canais, como SMS. A retenção de dados para o conjunto de dados de exportação de mensagens agora é de <strong>7 dias</strong>.</p>
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
<p>Uma nova <strong>API</strong> do Journey Optimizer está disponível, permitindo que você recupere e inspecione de forma programática dados relacionados a campanha, como detalhes, versões e configurações.</p>
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
<p>Agora você pode aplicar <strong>rapidamente temas</strong> pré-aprovados para garantir que consistência da marca em todos os emails, acelere seu processo de criação de campanha e produza e-mails de alta qualidade independentemente, ao mesmo tempo em que reduz a dependência de equipes de design.</p>
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

* **Verificações** de qualidade de conteúdo assistente de IA - Além do alinhamento marca, agora é possível avaliar a qualidade<strong> conteúdo geral </strong>para descobrir possíveis problemas de leitura, coesão e eficácia, independentemente das diretrizes de marca. Essas verificações automatizadas ajudam a identificar mensagens não claros, tom inconsistente ou lacunas estruturais.
* **Atualize marcas com novas guia** de cores - As diretrizes de marca ajudam a garantir que suas marca são apresentadas de forma consistente em todos os pontos de contato. A nova <strong>seção</strong> Cores define os padrões para o sistema de cores da marca, explicando como as cores são selecionadas, organizadas e aplicadas nas experiências. Garante o uso consistente de cores primárias, secundárias, de acentos e neutras para oferecer suporte a um identidade da marca coeso, acessível e reconhecível.

#### Campanhas

* **Agendar campanha usando o Fuso Horário do Perfil** - O agendamento de campanha agora pode usar o <strong>fuso horário</strong> de cada perfil para entregar mensagens no horário local desejado.

  **Observação**: esta melhoria está disponível somente para um conjunto de organizações (Disponibilidade Limitada).

#### Canais

* **Webhooks SMS: Fase II** - Descrição a ser fornecido.

* **Oferta** de Revenda do WhatsApp - Descrição a ser fornecida.

#### Email Designer

* **Correções no designer** de Email - <strong>Sugestões</strong> de conteúdo automáticas com IA estão disponíveis no Designer de email quando violações são detectadas durante conteúdo validação. Se conteúdo for marcada como desalinhada com diretrizes de marca ou falhar critérios de qualidade, o sistema gera proativamente alternativas corrigidas que podem ser revisadas e aplicadas em linha, melhorando a conformidade e acelerando a produção.

#### Tomada de decisão da experiência

* **Arbitragem de jornada** - Agora você pode usar <strong>fórmulas e modelos</strong> de IA para aumentar automaticamente as pontuações de prioridade da jornada com base em atributos de perfil do cliente e fatores contextuais, garantindo que os clientes entrem nas jornadas mais relevantes.

  **Observação**: essa melhoria só está disponível para um conjunto de organizações (Disponibilidade limitada).

* **documentação de ferramentas sandbox exd - update** - Descrição a ser fornecida.

* **APIs** de ferramentas de migração de autoatendimento - Um novo conjunto de APIs<strong> de ferramentas de </strong>migração está disponível para migrar entidades de gerenciamento de ofertas para a Experience Decisioning. A ferramenta permite a migração perfeita entre sandboxes com resolução de dependência e recursos de reversão.

* **Anexar fragmentos aos itens** de decisão - o Journey Optimizer agora fornece a capacidade de anexar <strong>fragmentos</strong> a itens de decisão que podem ser aproveitados em campanhas de experiência baseadas em código por meio de políticas de decisão.

  **Observação**: anteriormente lançada em Disponibilidade Limitada, essa melhoria agora está disponível para todos os ambientes (Disponibilidade Geral).

#### Jornadas

* **Aproveite uma carga de resposta de falha nas Ações** personalizadas da jornada - agora você pode definir uma carga<strong> de resposta de erro opcional </strong>para ações personalizadas. Quando uma chamada falha, a carga de erro é exposta no contexto da jornada e está disponível no tempo limite/erro ramificação para suportar uma lógica de fallback e depuração mais ricas.

* **Combinar ações de mensagens nativas e do Adobe Campaign** - o Journey Optimizer agora permite combinar ações de mensagem do Adobe Campaign v7/v8 com ações de canal nativas na mesma jornada.

* **Validação do tamanho da carga da Jornada no jornada** - a Journey Optimizer agora fornece a <strong>validação do tamanho da carga</strong> para ajudar a garantir desempenho e estabilidade de sistema ideais. Ao criar ou publicar jornadas, você receberá avisos e erros claros se os tamanhos de carga se aproximarem ou excederem os limites recomendados, juntamente com orientações acionáveis para otimizar a configuração da jornada. Essa validação proativa ajuda a identificar problemas em potencial antecipadamente e a manter o desempenho do jornada.

* **Várias ações de entrada em jornadas - Para simplificar sua orquestração de jornadas** , agora você pode definir <strong>várias ações</strong> de entrada em uma única jornada. Anteriormente disponível em campanhas, esse recurso permite oferecer várias experiências baseadas em código, mensagens no aplicativo, Cartões de conteúdo ou ações da Web para diferentes locais ao mesmo tempo, cada ação contendo uma conteúdo específica.

  **Observação**: lançado anteriormente na Disponibilidade limitada, essa melhoria agora está disponível para todos os ambientes (Disponibilidade geral).

#### Campanhas orquestradas

* **Selecionar atributos e copiar valores** de distribuição - Agora é possível selecionar ou copiar valores diretamente da distribuição de valores visualização em campanhas orquestradas.

* **Herança do rótulo de uso de dados para públicos-alvo -** Os rótulos<strong> de uso de dados aplicados</strong> no Adobe Experience Platform agora recorram automaticamente ao salvar públicos-alvo em campanhas orquestradas, reduzindo o marcação manual de DULE.

* **Redefinição predefinida filtros** - Para facilitar a redefinição de direcionamento para casos de uso de campanha orquestrados, esta versão apresenta uma nova <strong>segmentação filtros</strong>. Esses filtros permitem Direcionamento diretamente os públicos-alvo com base em envolvimento de mensagem, como enviado, aberto, aberto ou clicado, ou aberto e clicado, além de selecionar as campanha específicas ou as transição in-campanha que você deseja redirecionar.

* **Filtros predefinidos com parâmetros** - Agora é possível criar <strong>filtros com parâmetros em campanhas</strong> orquestradas para regras reutilizáveis e editáveis.

* **Enviar mensagem confirmação antes do envio** - Uma <strong>etapa</strong> de confirmação agora está ativada por padrão antes de enviar campanhas orquestradas para reduzir envios acidentais.

* **Suporte** metadados gerado pelo usuário - A <strong>função</strong> de ajuda executionMetadata está disponível no personalização editor para Campanhas orquestradas, permitindo anexar informações contextuais a qualquer nativo ação e armazenamento-la em um conjunto de dados de exportação para sistemas externos.

* **Botão Reiniciar** - As campanhas orquestradas agora incluem um <strong>botão Reiniciar</strong> para que você possa reiniciar rapidamente as execuções quando necessário antes de publicar a campanha.

* **Suporte ao controle de taxa** - As campanhas orquestradas agora oferecem suporte ao <strong>controle de taxa</strong> para ajudar você a acompanhar as entregas e alinhar-se às restrições de volume.

#### Permissões

* **Impedir a auto-aprovação para jornadas e campanhas** - agora você pode exigir que os criadores não possam aprovar suas próprias jornadas ou campanhas, melhorando <strong>a separação de tarefas</strong> em workflows de aprovação.

## Em breve {#jan-26-01-coming-soon}

Os recursos e aprimoramentos a seguir estão programados para serem lançados nos próximos dias. **As informações estão sujeitas a alterações**. Links, telas e documentação atualizados serão compartilhados assim que essas atualizações estiverem ativas na produção.

<table>
<thead>
<tr>
<th><strong>Geração de conteúdo no Agente da jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Com a tecnologia Adobe Experience Platform Agente Orquestrador, <strong>o Agente</strong> da Jornada está disponível no Journey Optimizer e permite analisar jornadas por meio de uma interface de linguagem natural. Agora, também é possível gerar e gerenciar conteúdo específico do canal diretamente no Journey Agent, criando conteúdo para canais como email e push, aplicando e visualizando modelos, refinando o tom e o estilo por meio de prompts e abrindo conteúdo no Designer de Conteúdo para edição em contexto.</p>
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
<p>Agora é possível incluir <strong>ofertas personalizadas</strong> em suas jornadas por meio de uma decisão dedicada de Conteúdo atividade na tela da jornada e usá-las em atividades de jornada, incluindo condições e ações personalizadas.</p>
<p>Data de disponibilidade: terça-feira, 2 de fevereiro de 2026</p>
</td>
</tr>
</tbody>
</table>
