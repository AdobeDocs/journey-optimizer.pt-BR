---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Notas de versão do Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 79e9023a9b555a75a13c4f5da2db1b7dbb04c344
workflow-type: tm+mt
source-wordcount: '1726'
ht-degree: 17%

---

# Notas de versão {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novidades"
>abstract="O **Adobe Journey Optimizer** está sempre fornecendo novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão."

O [!DNL Adobe Journey Optimizer] segue um modelo de entrega contínua, permitindo que a Adobe forneça novos recursos, melhorias e correções também de forma contínua. Essa abordagem permite uma implantação escalável e em fases de recursos para garantir desempenho e estabilidade em todos os ambientes.

Devido a esse modelo, as notas de versão são atualizadas entre as versões mensais. Para obter detalhes completos sobre o ciclo de lançamento e as fases de disponibilidade, consulte o [ciclo de lançamento do Journey Optimizer](releases.md).

O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

## Notas de pré-lançamento de janeiro de 2026 {#latest-rn}

**Data de lançamento**: 27 a 28 de janeiro de 2026

**As notas de pré-lançamento abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade da versão**. Links, telas e a documentação atualizada são publicados nas notas de versão na data de lançamento.

Consulte também as [Notas de pré-lançamento da Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

### Novos recursos {#jan-26-01-features}

<table>
<thead>
<tr>
<th><strong>Horas de silêncio (exclusões com base no tempo)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Quiet hours permite definir <strong>exclusões com base no tempo</strong> para canais de email, SMS, push e WhatsApp. Elas garantem que nenhuma mensagem seja enviada durante períodos específicos, ajudando você a respeitar as preferências do cliente e os requisitos de conformidade. Você pode aplicar horas de silêncio por meio de <strong>conjuntos de regras</strong>, que podem ser atribuídos a ações individuais em campanhas ou jornadas para obter um controle preciso.</p>
<p>Lançado anteriormente em Disponibilidade limitada, esse recurso agora está disponível para todos os ambientes (Disponibilidade geral). Com esta versão de Disponibilidade geral, o recurso agora inclui a capacidade de os clientes enfileirarem uma ação de campanha até a conclusão do Período de silêncio e a capacidade de pré-visualizar a regra de Período de silêncio ativada.</p>
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
<p>Anteriormente limitado às campanhas, o <strong>canal de Correspondência Direta</strong> agora está disponível na tela de jornada, permitindo que você incorpore a Correspondência Direta às suas jornadas. A correspondência direta agora pode ser usada em cenários de jornada em lote e 1:1, com suporte para configuração de extração de arquivos e configurações de frequência baseadas em tempo.</p>
<p>Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
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
<p>O canal de correspondência direta agora está disponível em campanhas orquestradas. A <strong>Atividade de correspondência direta</strong> facilita o envio de correspondência direta dentro da campanha orquestrada para mensagens recorrentes e únicas. Ele automatiza a geração do <strong>arquivo de extração</strong> exigido por provedores de correspondência direta. Você pode combinar atividades de canal na tela de campanha orquestrada para criar campanhas entre canais que acionam ações com base no comportamento do cliente e nos dados.</p>
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
<p>Agora você pode adicionar <strong>Políticas de decisão</strong> em jornadas e campanhas de SMS. As políticas de decisão são recipientes para as suas ofertas que utilizam o mecanismo de tomada de decisão para retornar dinamicamente o melhor conteúdo a ser entregue a cada membro do público-alvo.</p>
<p>Esse recurso está disponível em Disponibilidade limitada para um conjunto de organizações. Entre em contato com seu representante Adobe. </p>
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
<th><strong>Journey Agent - Criar uma Jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Agent agora oferece recursos de criação, permitindo que os usuários do Journey Optimizer criem e configurem jornadas de marketing por meio de uma <strong>interface de linguagem natural</strong>. Os profissionais podem criar jornadas rapidamente descrevendo seus requisitos em prompts conversacionais. Isso simplifica o processo de criação de jornadas, permitindo que os profissionais de marketing se concentrem na estratégia em vez da configuração técnica.</p>
</td>
</tr>
</tbody>
</table>

### Aprimoramentos {#jan-26-01-improv}

Os aprimoramentos incluídos nesta versão estão listados abaixo.

#### IA

* **Verificações de Qualidade de Conteúdo do Assistente de IA** - Além do alinhamento da marca, agora você pode avaliar a <strong>qualidade do conteúdo</strong> geral para descobrir possíveis problemas de legibilidade, coesão e eficácia, independentemente das diretrizes da sua marca. Essas verificações automatizadas ajudam a identificar mensagens não claras, tom inconsistente ou lacunas estruturais.

* **Atualizar marcas com a nova guia de cores** - As diretrizes de marca ajudam a garantir que sua marca seja apresentada de forma consistente em todos os pontos de contato. A nova seção <strong>Cores</strong> define os padrões do sistema de cores da sua marca, descrevendo como as cores são selecionadas, organizadas e aplicadas entre experiências. Ela garante o uso consistente de cores primárias, secundárias, de ênfase e neutras para respaldar uma identidade de marca coesa, acessível e reconhecível.

#### Canais

#### Campanhas

* **Agendar campanha usando o Fuso Horário do Perfil** - O agendamento de campanha agora pode usar o <strong>fuso horário</strong> de cada perfil para entregar mensagens no horário local desejado.

  **Observação**: esta melhoria está disponível somente para um conjunto de organizações (Disponibilidade Limitada).


#### Experience Decisioning

* **Anexar fragmentos a itens de decisão** - O Journey Optimizer agora fornece a capacidade de anexar <strong>fragmentos</strong> a itens de decisão, que podem ser aproveitados em campanhas de experiência baseadas em código por meio de políticas de decisão.

  **Observação**: anteriormente lançada em Disponibilidade Limitada, essa melhoria agora está disponível para todos os ambientes (Disponibilidade Geral).

#### Jornadas

* **Aproveite uma carga de resposta de falha nas Ações Personalizadas do jornada** - Agora você pode definir uma <strong>carga de resposta de erro</strong> opcional para ações personalizadas. Quando uma chamada falha, a carga de erro é exposta no contexto de jornada e está disponível na ramificação tempo limite/erro, junto com o `jo_status_code`, para oferecer suporte a uma lógica de fallback e depuração mais avançadas.

* **Combinar ações de mensagens nativas e do Adobe Campaign** - o Journey Optimizer agora permite combinar ações de mensagem do Adobe Campaign v7/v8 com ações de canal nativas na mesma jornada.

* **Validação do tamanho da carga da Jornada no jornada** - a Journey Optimizer agora valida os tamanhos de carga da jornada para ajudar a garantir desempenho e estabilidade de sistema ideais. Ao criar ou publicar jornadas, você receberá avisos e erros claros se os tamanhos de carga se aproximarem ou excederem os limites recomendados, juntamente com orientações acionáveis para otimizar a configuração da jornada. Essa validação proativa ajuda a identificar problemas em potencial antecipadamente e a manter o desempenho do jornada.

#### Campanhas orquestradas

* **Selecionar atributos e copiar valores de distribuição** - Agora é possível selecionar ou copiar valores diretamente da exibição de distribuição de valores em campanhas orquestradas.

* **Herança de rótulo de uso de dados para públicos-alvo** - Os rótulos aplicados no Adobe Experience Platform agora são transferidos automaticamente ao salvar públicos-alvo em campanhas orquestradas, reduzindo a marcação DULE manual.

* **Filtros de redirecionamento predefinidos** - Para facilitar o redirecionamento de casos de uso de campanhas orquestradas, esta versão introduz novos <strong>filtros de comentários de campanha</strong>. Esses filtros permitem direcionar públicos diretamente com base no envolvimento da mensagem, como enviado, aberto somente, aberto ou clicado, ou aberto e clicado, e selecionar a campanha específica ou a campanha em transição que deseja redirecionar.

* **Filtros predefinidos com parâmetros** - Agora você pode criar filtros predefinidos com <strong>parâmetros</strong> em campanhas orquestradas para regras editáveis e reutilizáveis.

* **Confirmação de mensagem antes de enviar** - Uma <strong>etapa de confirmação</strong> agora está habilitada por padrão antes de enviar campanhas orquestradas para reduzir envios acidentais.

* **Suporte a metadados gerados pelo usuário** - A <strong>função auxiliar executionMetadata</strong> agora está disponível no editor de personalização para campanhas orquestradas, permitindo que você anexe informações contextuais a qualquer ação nativa e armazene-a em um conjunto de dados para exportação para sistemas externos.

* **Botão Reiniciar** - As campanhas orquestradas agora incluem um <strong>botão Reiniciar</strong> para que você possa reiniciar rapidamente as execuções quando necessário antes de publicar a campanha.

* **Suporte ao controle de taxa** - As campanhas orquestradas agora oferecem suporte ao <strong>controle de taxa</strong> para ajudar você a acompanhar as entregas e alinhar-se às restrições de volume.

#### Permissões

* **Impedir autoaprovação para jornadas e campanhas** - Adição de uma opção ao criar ou definir a Política de Aprovação para impedir que os criadores de jornadas ou campanhas aprovem seus próprios objetos.

## Em breve {#jan-26-01-coming-soon}

Os recursos e aprimoramentos a seguir estão programados para serem lançados nos próximos dias. **As informações estão sujeitas a alterações**. Links, telas e documentação atualizados serão compartilhados assim que essas atualizações estiverem ativas na produção.

<table>
<thead>
<tr>
<th><strong>Exportação de mensagens</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Um novo recurso <strong>Exportação de Mensagem</strong> estará disponível para canais de email e SMS. Esse recurso permite exportar automaticamente o conteúdo da mensagem enviada para um conjunto de dados dedicado do Experience Platform, permitindo:</p>
<ul>
<li>Atender aos requisitos de conformidade normativa (como a HIPAA)</li>
<li>Arquivar mensagens para solicitações legais e consultas do atendimento ao cliente</li>
<li>Reter cópias de conteúdo personalizado enviadas a indivíduos</li>
</ul>
<p>Os registros são retidos no conjunto de dados de exportação de mensagens do AJO por 7 dias corridos a partir da assimilação. Durante esse período de retenção, você pode exportar os dados para seu próprio armazenamento por meio dos destinos do Experience Platform. O recurso é ativado no nível de configuração do canal, fornecendo controle granular sobre quais mensagens são exportadas.</p>
<p>Esse recurso só está disponível para o canal de email e SMS, para organizações que compraram a oferta complementar Exportação de mensagens. Para obter mais informações, entre em contato com o seu representante da Adobe.</p>
<p>Data de disponibilidade: quinta-feira, 28 de janeiro de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Webhooks de SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Webhooks</strong> terão suporte em todos os provedores de SMS. Você poderá configurar cada webhook com base na finalidade pretendida: webhooks de entrada para capturar mensagens de entrada e webhooks de feedback para receber confirmações de entrega, atualizações de status e outros eventos relacionados à mensagem.</p>
<p>Data de disponibilidade: quinta-feira, 28 de janeiro de 2026</p>
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
<p>O Adobe Journey Optimizer oferecerá suporte a <strong>Notificações por push da Web</strong>, expandindo o canal de push para além dos dispositivos móveis. Você poderá enviar notificações para navegadores móveis e de desktop, permitindo que alcançar os clientes diretamente em seus dispositivos sem exigir um aplicativo. Esse aprimoramento ajudará você a envolver os usuários com mensagens oportunas e personalizadas em tempo real, aproveitando os mesmos fluxos de trabalho de criação e recursos de direcionamento já disponíveis para push móvel.</p>
<p>Anteriormente lançado no Beta, esse recurso estará disponível para todos os ambientes (Disponibilidade geral).</p>
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
<p><strong>As APIs de ferramentas de migração</strong> estarão disponíveis para migrar programaticamente entidades de Gestão de decisões para o Decisioning, apresentando:</p>
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
<th><strong>Geração de conteúdo no Journey Agent</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Com a tecnologia do Adobe Experience Platform Agent Orchestrator, o <strong>Journey Agent</strong> estará disponível no Journey Optimizer e permitirá que você analise jornadas por meio de uma interface de linguagem natural. Você poderá gerar e gerenciar conteúdo específico de canal diretamente no Journey Agent, criando conteúdo para canais como email e push, aplicando e visualizando modelos, refinando o tom e o estilo por meio de prompts e abrindo conteúdo no <strong>Content Designer</strong> para edição em contexto.</p>
<p>Data de disponibilidade: terça-feira, 2 de fevereiro de 2026</p>
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
<p>Você poderá personalizar e otimizar o conteúdo de suas mensagens de push com a <strong>Decisão</strong>. Use as <strong>Pontuações de prioridade</strong>, as Fórmulas ou os Modelos de IA para exibir o melhor conteúdo para seus clientes.</p>
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
<p>Uma nova <strong>Atividade de decisão de conteúdo</strong> estará disponível na tela de jornada para integrar ofertas personalizadas diretamente às jornadas do cliente. Essa atividade permite fornecer conteúdo baseado em decisão e fazer referência a essas ofertas em toda a jornada, nas condições para criar ramificações baseadas em elegibilidade, nas ações personalizadas para transmitir dados de oferta a sistemas externos e em outras atividades para criar experiências do cliente totalmente personalizadas.</p>
<p>Esse recurso estará disponível para todos os ambientes (Disponibilidade geral).</p>
<p>Data de disponibilidade: quarta-feira, 3 de fevereiro de 2026</p>
</td>
</tr>
</tbody>
</table>
