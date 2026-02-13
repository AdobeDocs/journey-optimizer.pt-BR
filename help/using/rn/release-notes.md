---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Notas de versão do Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: b53f9279a8698e99683cd6e75a7e746102e3e094
workflow-type: tm+mt
source-wordcount: '1534'
ht-degree: 29%

---

# Notas de versão {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novidades"
>abstract="O **Adobe Journey Optimizer** está sempre fornecendo novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão."

O [!DNL Adobe Journey Optimizer] segue um modelo de entrega contínua, permitindo que a Adobe forneça novos recursos, melhorias e correções também de forma contínua. Essa abordagem permite uma implantação escalável e em fases de recursos para garantir desempenho e estabilidade em todos os ambientes.

Devido a esse modelo, as notas de versão são atualizadas entre as versões mensais. Para obter detalhes completos sobre o ciclo de lançamento e as fases de disponibilidade, consulte o [ciclo de lançamento do Journey Optimizer](releases.md).

O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

## Notas de versão de fevereiro de 2026 {#feb-26-01-rn}

**As notas de pré-lançamento abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade da versão**. Links, telas e a documentação atualizada são publicados nas notas de versão na data de lançamento.

Consulte também as [Notas de pré-lançamento da Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data de lançamento**: quarta-feira, 17 de fevereiro de 2026

### Novos recursos {#feb-26-01-features}

<table>
<thead>
<tr>
<th><strong>Envio de onda de mensagens de saída</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Você pode agendar mensagens de saída de <strong>campanhas</strong> ou <strong>jornadas</strong> para serem entregues em <strong>lotes</strong> controlados ao longo do tempo.</p>
<p>O Wave sending oferece os seguintes benefícios:</p>
<ul>
<li>Melhor <strong>entregabilidade</strong> - O Spread envia ao longo do tempo para ajudar a manter uma <strong>sólida reputação do remetente</strong> e reduzir o risco de ser sinalizado como spam.</li>
<li><strong>Controle de carga</strong> - Evite sobrecarregar os sistemas downstream (por exemplo, centrais de atendimento, páginas de aterrissagem) limitando quantas mensagens saem de uma vez.</li>
<li>Casos de uso de alto volume e sensíveis ao tempo — adequados a grandes públicos ou quando é necessário controlar o tempo (por exemplo, capacidade da central de atendimento, aumento ou ofertas vinculadas ao tempo).</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Arbitragem de jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode usar <strong>fórmulas</strong> e <strong>modelos de IA</strong> para aumentar automaticamente as <strong>pontuações de prioridade de jornada</strong> com base nos atributos do perfil do cliente e em fatores contextuais, garantindo que os clientes insiram as jornadas mais relevantes.</p>
<p>Este recurso só está disponível para um conjunto de organizações (<strong>Disponibilidade Limitada</strong>). Para obter acesso, entre em contato com um representante da Adobe.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent: criação de conteúdo do canal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Com a tecnologia <strong>Adobe Experience Platform Agent Orchestrator</strong>, o <strong>Journey Agent</strong> está disponível no Journey Optimizer e permite que você analise jornadas por meio de uma <strong>interface de linguagem natural</strong>. Agora você também pode gerar e gerenciar conteúdo específico de canal diretamente no Journey Agent, criando conteúdo para canais como email e push, aplicando e visualizando modelos, refinando o tom e o estilo por meio de prompts e abrindo conteúdo no <strong>Content Designer</strong> para edição em contexto.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Atividades móveis ao vivo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As <strong>Atividades em tempo real</strong> fornecem <strong>atualizações em tempo real</strong> e experiências interativas dentro de aplicativos móveis, permitindo que os usuários permaneçam informados sobre eventos ou tarefas em andamento diretamente na tela de seus dispositivos. Esse recurso aprimora o engajamento fornecendo informações em tempo real, como monitoramento de progresso, atualizações de eventos ou conteúdo interativo, sem exigir que os usuários abram o aplicativo.</p>
<p>Anteriormente lançado na versão beta, esse recurso agora está disponível para todos os ambientes (<strong>Disponibilidade geral</strong>).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Atividade de ação em jornadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer oferece suporte a uma nova <strong>atividade de Ação</strong> genérica que permite configurar ações únicas e <strong>grupos de ação de entrada de várias ações</strong>, permitindo a configuração de ação simplificada na <strong>tela de jornada</strong>. Em especial, este novo recurso permite:</p>
<ul>
<li>Uma configuração de ação nativa simplificada na tela da jornada.</li>
<li>A capacidade de criar grupos de ação de entrada multiação.</li>
<li>A capacidade de adicionar <strong>otimização</strong> a qualquer ação de canal interna.</li>
<li>A capacidade de adicionar opções de <strong>experimentação</strong> e <strong>multilíngues</strong> a qualquer ação.</li>
</ul>
<p>Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal de notificações por push na web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Adobe Journey Optimizer agora é compatível com <strong>Notificações por push na web</strong>, expandindo o canal de push para além dos dispositivos móveis. Você pode enviar notificações facilmente para navegadores móveis e de desktop, permitindo alcançar clientes diretamente em seus dispositivos sem precisar de um aplicativo. Esse aprimoramento permite envolver os usuários com mensagens oportunas e personalizadas em tempo real, aproveitando os mesmos <strong>fluxos de trabalho de criação</strong> e <strong>recursos de direcionamento</strong> já disponíveis para push móvel.</p>
<p>Anteriormente lançado na versão beta, esse recurso agora está disponível para todos os ambientes (<strong>Disponibilidade geral</strong>).</p>
<p>Data de disponibilidade: sábado, 13 de fevereiro de 2026</p>
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
<p>Uma nova <strong>Atividade de decisão de conteúdo</strong> está disponível na <strong>tela de jornada</strong> para integrar <strong>ofertas personalizadas</strong> diretamente às jornadas do seu cliente. Essa atividade permite fornecer conteúdo baseado em decisão e fazer referência a essas ofertas em toda a jornada, em condições para criar ramificações baseadas em elegibilidade, em ações personalizadas para transmitir dados de oferta a sistemas externos e em outras atividades para criar experiências do cliente totalmente personalizadas.</p>
<p>Lançado anteriormente como Limited Availability, esse recurso agora está disponível para todos os ambientes (<strong>General Availability</strong>).</p>
<p><img src="assets/do-not-localize/content-decision.gif"/></p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/content-decision.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: quinta-feira, 11 de fevereiro de 2026</p>
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
<p><strong>As APIs de ferramentas de migração</strong> agora estão disponíveis para migrar programaticamente entidades do <strong>Gerenciamento de decisão</strong> para a <strong>Decisão</strong>, apresentando:</p>
<ul>
<li>Escopos de migração flexíveis (<strong>sandbox</strong>, <strong>oferta</strong> ou nível <strong>decisão</strong>)</li>
<li><strong>análise de dependência</strong> e validação automatizadas</li>
<li><strong>Suporte de reversão</strong> para migrações concluídas</li>
<li>Relatórios de migração detalhados com mapeamentos de objeto</li>
</ul>
<p>Para obter mais informações, consulte a <a href="../experience-decisioning/decisioning-migration-api.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 3 de fevereiro de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Monitoramento de ação personalizado</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Insight Saiba mais sobre a integridade e o desempenho de seus <strong>pontos de extremidade de ação personalizados</strong> com um novo <strong>painel de monitoramento</strong> e <strong>dados de evento de etapa de jornada</strong> aprimorados. Monitore chamadas bem-sucedidas, erros, taxa de transferência, tempos de resposta e tempos de espera na fila para entender rapidamente quando, onde e por que ocorrem anomalias.</p>
<p>Lançado anteriormente como Limited Availability, esse recurso agora está disponível para todos os ambientes (<strong>General Availability</strong>).</p>
<p>Para obter mais informações, consulte a <a href="../action/reporting.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 3 de fevereiro de 2026</p>
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
<p>Agora você pode personalizar e otimizar o conteúdo de suas <strong>mensagens SMS</strong> com a <strong>Decisão</strong>. Use as <strong>Pontuações de Prioridade</strong>, as <strong>Fórmulas</strong> ou os <strong>Modelos de IA</strong> para exibir o melhor conteúdo para seus clientes.</p>
<p>Para obter mais informações, consulte a <a href="../experience-decisioning/create-decision.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 2 de fevereiro de 2026</p>
</td>
</tr>
</tbody>
</table>

### Aprimoramentos {#feb-26-01-improv}

Os aprimoramentos incluídos nesta versão estão listados abaixo.

#### Configuração

* **Uso do evento de experiência em expressões de jornada** - A partir de 1º de abril de 2026, o uso de atributos de evento de experiência em expressões de jornada não será mais suportado para organizações que não usaram esse recurso nos últimos 90 dias. Esse recurso já está indisponível para novas organizações de clientes desde 8 de julho de 2025. Para obter alternativas, consulte [Pesquisa de evento de experiência no jornada](../building-journeys/exp-event-lookup.md).


* **Alternância de método de delegação de subdomínio** - Agora é possível alternar de um método de <strong>delegação de subdomínio</strong> para outro. Isso permite migrar domínios usando o modo de <strong>delegação de CNAME</strong> para o método de <strong>delegação personalizada</strong> para aderir às políticas de segurança da sua empresa.

  **Observação**: este recurso só está disponível para um conjunto de organizações (<strong>Disponibilidade Limitada</strong>). Para obter acesso, entre em contato com um representante da Adobe.


#### Designer de email

* **Usar um tema de marca para converter uma imagem em um modelo de email** - Ao converter uma imagem em um modelo de email no Journey Optimizer, agora você pode usar um <strong>tema</strong> como entrada para que o HTML gerado siga seus <strong>parâmetros de marca</strong>. Estilos como cor de fundo, cor do botão, fontes, espaçamento entre linhas, margens e preenchimento são aplicados automaticamente, reduzindo o trabalho manual de design e fornecendo um modelo pronto para uso com edições mínimas.


* **Atualize as marcas com a nova guia de cores** - <strong>Diretrizes de marca</strong> ajudam a garantir que sua marca seja apresentada de forma consistente em todos os pontos de contato. A nova <strong>seção Cores</strong> define os padrões do sistema de cores da sua marca, descrevendo como as cores são selecionadas, organizadas e aplicadas entre experiências. Ela garante o uso consistente de cores primárias, secundárias, de destaque e neutras para promover uma identidade de marca coesa, acessível e reconhecível.


#### IA

* **Integração de modelos personalizados de Firefly e modelos de geração de imagens de terceiros** - Habilite a integração perfeita de <strong>modelos Firefly</strong> padrão e personalizados, juntamente com <strong>modelos de imagens de terceiros</strong> aprovados (por exemplo, NanoBanana), para oferecer maior flexibilidade, controle e alinhamento de marca ao gerar imagens. Isso permite selecionar o melhor modelo para cada caso de uso: Firefly padrão para necessidades gerais, Firefly personalizado para geração na marca ou modelos aprovados de terceiros para cenários especializados ou experimentais.


#### Escolha de experiências

* **Suporte de entrada do Edge para usar dados do Adobe Experience Platform no Decisioning** - O suporte de decisão da <strong>pesquisa de dados do Experience Platform</strong> agora inclui casos de uso de canal de <strong>entrada de borda</strong>. O recurso permanece com a disponibilidade limitada; a disponibilidade geral do recurso subjacente de pesquisa de dados ainda não foi anunciada (dependência de AEP/produto).

  **Observação**: este recurso só está disponível para um conjunto de organizações (<strong>Disponibilidade Limitada</strong>). Para obter acesso, entre em contato com um representante da Adobe.


* **Visualização do Experience Decisioning no canal de Experiência baseada em Código** - Agora você pode visualizar <strong>itens de decisão</strong> ao configurar o <strong>Experience Decisioning</strong> com o canal <strong>Experiência baseada em Código</strong>. A visualização está disponível diretamente na interface de criação antes de entrar em funcionamento.


* **Observação do modelo de IA de classificação de oferta** - o Journey Optimizer agora permite monitorar a <strong>integridade</strong>, o <strong>status do treinamento</strong> e o <strong>desempenho</strong> dos seus <strong>modelos de IA</strong> na Decisão. Assim, você pode verificar o sucesso do treinamento, solucionar falhas e entender o impacto nos seus resultados. Esse recurso está disponível somente para modelos de otimização personalizados (não para otimização automática).


* **Anexar fragmentos a itens de decisão** - A Journey Optimizer agora fornece a capacidade de anexar <strong>fragmentos</strong> a <strong>itens de decisão</strong>, que podem ser aproveitados em campanhas de experiência baseadas em código por meio de <strong>políticas de decisão</strong>.

  **Observação**: anteriormente lançado com disponibilidade limitada, esse recurso agora está disponível para todos os ambientes (Disponibilidade geral).

  Data de disponibilidade: 12 de fevereiro de 2026.


#### Jornadas

* **Várias ações de entrada no jornada** - Para simplificar sua orquestração de jornadas, agora é possível definir várias <strong>ações de entrada</strong> em uma única jornada. Disponível anteriormente em campanhas, esse recurso permite que você forneça várias <strong>experiências baseadas em código</strong>, <strong>mensagens no aplicativo</strong>, <strong>cartões de conteúdo</strong> ou <strong>ações da Web</strong> a locais diferentes ao mesmo tempo, cada ação contendo conteúdo específico.

  **Observação**: anteriormente lançado com disponibilidade limitada, esse recurso agora está disponível para todos os ambientes (Disponibilidade geral).


* **Webhooks de SMS**: <strong>Webhooks</strong> agora são compatíveis com todos os provedores de SMS. Você pode configurar cada webhook com base na finalidade pretendida: <strong>webhooks de entrada</strong> para capturar mensagens de entrada e <strong>webhooks de comentários</strong> para receber confirmações de entrega, atualizações de status e outros eventos relacionados à mensagem. [Leia mais](../sms/sms-webhook.md)

  Data de disponibilidade: 2 de fevereiro de 2026.