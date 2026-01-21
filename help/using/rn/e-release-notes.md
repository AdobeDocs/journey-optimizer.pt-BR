---
solution: Journey Optimizer
product: journey optimizer
title: Notas de pré-lançamento do Journey Optimizer
description: Notas de pré-lançamento do Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: f7cdbb8f4a0e43a6a2fa15032d1376faf0424168
workflow-type: tm+mt
source-wordcount: '1990'
ht-degree: 47%

---

# Notas de pré-lançamento {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas no fim de cada mês nas [notas de versão](release-notes.md).


## Notas de pré-lançamento de janeiro de 2026 {#jan-26-01-rn}

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
<p>O Journey Optimizer é compatível com uma nova Atividade de ação genérica que permite configurar ações únicas e grupos de ação de entrada multiação, possibilitando uma configuração de ação simplificada na tela da jornada. Em especial, este novo recurso permite:</p>
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
<th><strong>Atividade de decisão de conteúdo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode incluir ofertas personalizadas em suas jornadas por meio de uma atividade dedicada de Decisão de conteúdo na tela de jornada e usá-las em atividades de jornada, incluindo condições e ações personalizadas.</p>
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
<p>Obtenha um insight mais profundo sobre a integridade e o desempenho de seus endpoints de ação personalizados com um novo painel de monitoramento e dados de evento de etapa do jornada aprimorados. Rastreie chamadas bem-sucedidas, erros, taxa de transferência, tempos de resposta e tempos de espera da fila para entender rapidamente quando, onde e por que ocorrem anomalias.</p>
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
<p>O Período de silêncio permite definir exclusões com base no tempo para canais de email, SMS, Push e WhatsApp. Elas garantem que nenhuma mensagem seja enviada durante períodos específicos, ajudando você a respeitar as preferências do cliente e os requisitos de conformidade. É possível aplicar o período de silêncio por meio de conjuntos de regras que podem ser atribuídas a ações individuais em campanhas ou jornadas para obter um controle preciso.</p>
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
<p>Anteriormente limitado a Campanhas, o canal de correspondência direta agora está disponível na tela de jornada, permitindo que você incorpore a correspondência direta às suas jornadas. A correspondência direta agora pode ser usada em cenários de jornada em lote e 1:1, com suporte para configuração de extração de arquivos e configurações de frequência baseadas em tempo.</p>
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
<p>O Adobe Journey Optimizer agora é compatível com notificações por push na Web, expandindo o canal de push para além dos dispositivos móveis. Você pode enviar notificações facilmente para navegadores móveis e de desktop, permitindo que alcançar os clientes diretamente em seus dispositivos sem exigir um aplicativo. Esse aprimoramento permite que você interaja com os usuários com mensagens personalizadas e oportunas em tempo real, aproveitando os mesmos fluxos de trabalho de criação e recursos de segmentação já disponíveis para push móvel.</p>
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
<p>Com a nova oferta complementar RCS Basic, agora você pode fornecer mensagens básicas RCS (Rich Communication Services) no Journey Optimizer, habilitando os seguintes recursos aprimorados de mensagens sujeitos ao suporte do provedor e da operadora:</p>
<ul>
<li>Suporte a remetentes com marca e verificados: envie mensagens usando perfis de negócios verificados com elementos de marca (logotipo, nome do remetente, etc.).</li>
<li>Insights de entregas de mensagens: receba relatórios de entrega detalhados, incluindo atualizações de status de mensagem (por exemplo, enviado, entregue, lido).</li>
<li>Rastreamento de link: incorpore e rastreie URLs em mensagens RCS para análise de engajamento.</li>
<li>Fallback para SMS: retorno automático para SMS quando o dispositivo do perfil não dá suporte a RCS ou está temporariamente inacessível via RCS.</li>
<li>Composição básica de mensagem: envia mensagens RCS básicas baseadas em texto.</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Suporte à decisão no canal push</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode adicionar políticas de decisão em jornadas e campanhas de notificações por push. As políticas de decisão são recipientes para as suas ofertas que utilizam o mecanismo de tomada de decisão para retornar dinamicamente o melhor conteúdo a ser entregue a cada membro do público-alvo.</p>
<p>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Suporte à decisão no canal de SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode adicionar políticas de Decisão a jornadas e campanhas de SMS. As políticas de decisão são recipientes para as suas ofertas que utilizam o mecanismo de tomada de decisão para retornar dinamicamente o melhor conteúdo a ser entregue a cada membro do público-alvo.</p>
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
<p>O canal de correspondência direta agora está disponível em campanhas orquestradas. A Atividade correspondência direta facilita o envio de correspondência direta na campanha orquestrada, tanto para mensagens únicas quanto recorrentes. Ela serve para automatizar o processo de geração do arquivo de extração exigido pelos provedores de correspondência direta. É possível combinar atividades de canal na tela da campanha orquestrada para criar campanhas entre canais que podem acionar ações com base no comportamento e nos dados do cliente.</p>
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
<p>Com o Journey Optimizer, agora é possível capturar atributos de perfil por meio das páginas de aterrissagem. Crie, projete e gerencie formulários personalizados adaptados às suas necessidades com base em um conjunto de dados específico. Em seguida, é possível usar esses formulários em páginas de destino para adicionar os atributos de perfil de sua escolha ao conjunto de dados definido para cada formulário.</p>
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
<p>Novos conectores de origem agora estão disponíveis na Adobe Experience Platform para os aplicativos de fidelidade Talon.One, Capillary e Kobie. Esses conectores permitem transmitir dados de fidelidade continuamente para a Adobe Experience Platform e usar esses dados no Journey Optimizer.</p>
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
<p>Uma nova API do Journey Optimizer agora está disponível, permitindo recuperar e inspecionar programaticamente dados relacionados à campanha, como detalhes, versões e configurações.</p>
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
<p>Três novos alertas de jornada agora estão disponíveis para ajudar a monitorar e rastrear os eventos de ciclo de vida da jornada e o desempenho da ação personalizada:</p>
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
<p>Agora é possível aplicar temas pré-aprovados rapidamente para garantir a consistência da marca em todos os emails, acelerar o processo de criação de campanha e produzir emails de alta qualidade de forma independente, reduzindo a dependência de equipes de design.</p>
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

* **Verificações de Qualidade de Conteúdo do Assistente de IA** - Além do alinhamento da marca, agora você pode avaliar a qualidade geral do conteúdo para descobrir possíveis problemas de legibilidade, coesão e eficácia, independentemente das diretrizes da sua marca. Essas verificações automatizadas ajudam a identificar mensagens não claras, tom inconsistente ou lacunas estruturais.
* **Atualizar marcas com a nova guia de cores** - As diretrizes de marca ajudam a garantir que sua marca seja apresentada de forma consistente em todos os pontos de contato. A nova seção Cores define os padrões do sistema de cores da sua marca, descrevendo como as cores são selecionadas, organizadas e aplicadas em várias experiências. Ela garante o uso consistente de cores primárias, secundárias, de ênfase e neutras para respaldar uma identidade de marca coesa, acessível e reconhecível.

#### Campanhas

* **Agendar campanha usando o Fuso Horário do Perfil** - O agendamento de campanha agora pode usar o fuso horário de cada perfil para entregar mensagens no horário local pretendido.

  **Observação**: esta melhoria está disponível somente para um conjunto de organizações (Disponibilidade Limitada).

#### Canais

* **Exportação de mensagem** - Agora é possível exportar todas as entregas enviadas para um conjunto de dados específico, para fins de arquivamento e conformidade. Essa capacidade está disponível não apenas para email, mas também para outros canais, como SMS.

* **Webhooks de SMS: Fase II** - Descrição a ser fornecida.

* **Oferta de revenda do WhatsApp** - Descrição a ser fornecida.

#### Email Designer

* **Correções no local - Acrite - Email e Páginas de Aterrissagem** - Descrição a ser fornecida.

#### Experience Decisioning

* **Arbitragem de Jornada - Fórmulas** - Agora você pode usar fórmulas e modelos de IA para aumentar automaticamente as pontuações de prioridade de jornada com base nos atributos do perfil do cliente e em fatores contextuais, garantindo que os clientes insiram as jornadas mais relevantes.

* **documentação de ferramenta de sandbox exd - atualização** - Descrição a ser fornecida.

* **APIs de ferramentas de migração de autoatendimento** - Descrição a ser fornecida.

* **Anexar fragmentos a itens de decisão** - O Journey Optimizer agora oferece a capacidade de anexar fragmentos a itens de decisão, que podem ser aproveitados em campanhas de experiência baseada em código por meio de políticas de decisão.

  **Observação**: anteriormente lançada em Disponibilidade Limitada, essa melhoria agora está disponível para todos os ambientes (Disponibilidade Geral).

#### Jornadas

* **Aproveite uma carga de resposta de falha nas Ações Personalizadas do jornada** - Descrição a ser fornecida.

* **Validação do tamanho da carga da Jornada no jornada** - a Journey Optimizer agora valida os tamanhos de carga da jornada para ajudar a garantir desempenho e estabilidade de sistema ideais. Ao criar ou publicar jornadas, você receberá avisos e erros claros se os tamanhos de carga se aproximarem ou excederem os limites recomendados, juntamente com orientações acionáveis para otimizar a configuração da jornada. Essa validação proativa ajuda a identificar problemas em potencial antecipadamente e a manter o desempenho do jornada.

* **Várias ações de entrada em jornadas**: para simplificar a orquestração de jornada, agora é possível definir várias ações de entrada em uma única jornada. Anteriormente disponível em campanhas, esse recurso permite que você forneça várias experiências baseadas em código, mensagens no aplicativo, Cartões de conteúdo ou ações da Web a locais diferentes ao mesmo tempo, cada ação contendo um conteúdo específico.

  **Observação**: anteriormente lançada em Disponibilidade Limitada, essa melhoria agora está disponível para todos os ambientes (Disponibilidade Geral).

#### Campanhas orquestradas

* **Selecionar atributos e copiar valores de distribuição** - Agora é possível selecionar ou copiar valores diretamente da exibição de distribuição de valores em campanhas orquestradas.

* **Herança de rótulo de uso de dados para públicos-alvo** - Os rótulos aplicados no Adobe Experience Platform agora são transferidos automaticamente ao salvar públicos-alvo em campanhas orquestradas, reduzindo a marcação DULE manual.

* **Filtros de redirecionamento predefinidos** - Para facilitar o redirecionamento de casos de uso de campanhas orquestradas, esta versão introduz novos filtros de comentários de campanha. Esses filtros permitem direcionar públicos diretamente com base no envolvimento da mensagem, como enviado, aberto somente, aberto ou clicado, ou aberto e clicado, e selecionar a campanha específica ou a campanha em transição que deseja redirecionar.

* **Filtros predefinidos com parâmetros** - Agora é possível criar filtros predefinidos com parâmetros em campanhas orquestradas para regras editáveis e reutilizáveis.

* **Confirmação de mensagem antes de enviar** - Uma etapa de confirmação agora está habilitada por padrão antes de enviar campanhas orquestradas para reduzir envios acidentais.

* **Suporte a metadados gerados pelo usuário** - A função auxiliar executionMetadata agora está disponível no editor de personalização para Campanhas Orquestradas, permitindo que você anexe informações contextuais a qualquer ação nativa e armazene-as em um conjunto de dados para exportação para sistemas externos.

* **Botão Reiniciar** - As campanhas orquestradas agora incluem um botão de reinicialização, para que você possa reiniciar rapidamente as execuções quando necessário antes de publicar a campanha.

* **Suporte ao controle de taxa** - As campanhas orquestradas agora oferecem suporte ao controle de taxa para ajudá-lo a acompanhar as entregas e alinhar-se às restrições de volume.

#### Permissões

* **Impedir a autoaprovação para jornadas e campanhas** - Agora é possível exigir que os criadores não aprovem suas próprias jornadas ou campanhas, melhorando a separação de tarefas nos fluxos de trabalho de aprovação.

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
<p>Desenvolvido pela Adobe Experience Platform Agent Orchestrator, o Journey Agent está disponível no Journey Optimizer e permite que você analise jornadas por meio de uma interface de linguagem natural. Agora, também é possível gerar e gerenciar conteúdo específico do canal diretamente no Journey Agent, criando conteúdo para canais como email e push, aplicando e visualizando modelos, refinando o tom e o estilo por meio de prompts e abrindo conteúdo no Designer de Conteúdo para edição em contexto.</p>
</td>
</tr>
</tbody>
</table>