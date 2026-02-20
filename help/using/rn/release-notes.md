---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Notas de versão do Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 6c509ef134c4240b243d255fd1ab7ec6bb062bf0
workflow-type: tm+mt
source-wordcount: '1329'
ht-degree: 33%

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

As seções [Novos recursos](#feb-26-01-features) e [Melhorias](#feb-26-01-improv) abordam recursos já disponíveis. A seção [Em breve](#coming-soon) lista os recursos e as melhorias programadas para lançamento no final de fevereiro.

<!--**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

<!--**Release date**: February 17-18, 2026-->

### Novos recursos {#feb-26-01-features}


<!--
<table>
<thead>
<tr>
<th><strong>Mobile Live Activities</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Live Activities</strong> provide real-time updates and interactive experiences within mobile apps, allowing users to stay informed about ongoing events or tasks directly on their device's screen. This feature enhances engagement by delivering live information, such as progress tracking, event updates, or interactive content, without requiring users to open the app.</p>
<p>Previously released in beta, this capability is now available to all environments (General Availability).</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Envio de onda de mensagens de saída</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível agendar mensagens de campanhas ou jornadas do Journey Optimizer para serem entregues em lotes controlados ao longo do tempo.</p>
<p>O Wave sending oferece os seguintes benefícios:</p>
<ul>
<li>Melhor capacidade de entrega - O Spread envia ao longo do tempo para ajudar a manter uma sólida reputação do remetente e reduzir o risco de ser sinalizado como spam.</li>
<li>Controle de carga - Evite sobrecarregar os sistemas de downstream (por exemplo, centrais de atendimento, páginas de aterrissagem) limitando quantas mensagens saem de uma vez.</li>
<li>Casos de uso de alto volume e sensíveis ao tempo — adequados a grandes públicos ou quando é necessário controlar o tempo (por exemplo, capacidade da central de atendimento, aumento ou ofertas vinculadas ao tempo).</li>
</ul>
<p><img src="assets/do-not-localize/waves.gif"/></p>
<p>Em <strong>campanhas</strong>, esse recurso está disponível para todos os ambientes (Disponibilidade Geral). Para obter mais informações, consulte a <a href="../campaigns/send-using-waves.md">documentação detalhada</a>.</p>

<p>No <strong>jornada</strong>, esse recurso só está disponível para algumas organizações (disponibilidade limitada). Para obter acesso, entre em contato com o representante da Adobe. Para obter mais informações, consulte a <a href="../building-journeys/send-using-waves.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: sexta-feira, 19 de fevereiro de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Migrar subdomínios para delegação personalizada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível migrar subdomínios usando o modo de delegação CNAME para delegação personalizada diretamente da interface, para que você possa atender a políticas de segurança mais rigorosas, de acordo com as diretrizes de sua empresa, sem recriar configurações de canal.</p>
<p><img src="assets/do-not-localize/subdomain-migration.gif"/></p>
<p>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.</p>
<p>Para obter mais informações, consulte a <a href="../configuration/custom-subdomain-migration.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: sexta-feira, 19 de fevereiro de 2026</p>
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
<p>O Adobe Journey Optimizer agora oferece suporte a <strong>notificações por push na Web</strong>, expandindo o canal de push para além dos dispositivos móveis. Você pode enviar notificações perfeitamente para <strong>navegadores móveis e de desktop</strong>, permitindo que você alcance os clientes diretamente em seus dispositivos sem precisar de um aplicativo. Esse aprimoramento permite interagir com os usuários com mensagens personalizadas e oportunas em tempo real, aproveitando os mesmos fluxos de trabalho de criação e recursos de direcionamento já disponíveis para notificações por push em dispositivos móveis.</p>
<p><img src="assets/do-not-localize/web-push.gif"/></p>
<p>Anteriormente lançado no Beta, esse recurso estará disponível para todos os ambientes (Disponibilidade geral).</p>
<p>Para obter mais informações, consulte a <a href="../push/push-configuration-web.md">documentação detalhada</a>.</p>
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
<p>Uma nova <strong>Atividade de decisão de conteúdo</strong> está disponível na tela de jornada para integrar ofertas personalizadas diretamente às jornadas do cliente. Essa atividade permite fornecer conteúdo baseado em decisão e fazer referência a essas ofertas em toda a jornada, em condições para criar ramificações baseadas em elegibilidade, em ações personalizadas para transmitir dados de oferta a sistemas externos e em outras atividades para criar experiências do cliente totalmente personalizadas.</p>
<p>Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<p><img src="assets/do-not-localize/content-decision.gif"/></p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/content-decision.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: quarta-feira, 10 de fevereiro de 2026</p>
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
<p>As APIs de ferramentas de migração agora estão disponíveis para migrar programaticamente entidades do <strong>Gerenciamento de decisão</strong> para a <strong>Decisão</strong>, apresentando:</p>
<ul>
<li>Escopos de migração flexíveis (nível de sandbox, oferta ou decisão)</li>
<li>Análise e validação automatizadas de dependências</li>
<li>Suporte à reversão para migrações concluídas</li>
<li>Relatórios de migração detalhados com mapeamentos de objeto</li>
</ul>
<p>Para obter mais informações, consulte a <a href="../experience-decisioning/decisioning-migration-api.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 3 de fevereiro de 2026</p>
</td>
</tr>
</tbody>
</table>

### Aprimoramentos {#feb-26-01-improv}

Os aprimoramentos incluídos nesta versão estão listados abaixo.

#### Configuração

* **Uso do evento de experiência em expressões de jornada** - A partir de 1º de abril de 2026, o uso de atributos de evento de experiência em expressões de jornada não será mais suportado para organizações que não usaram esse recurso nos últimos 90 dias. Esse recurso já está indisponível para novas organizações de clientes desde 8 de julho de 2025. Para obter alternativas, consulte [Pesquisa de evento de experiência no jornada](../building-journeys/exp-event-lookup.md).

#### Designer de email

* **Recuo de texto** - Agora é possível aplicar recuo à esquerda personalizável à primeira linha de parágrafos em componentes de texto diretamente do painel de propriedades. <!--The new **Indentation** control lets you define indentation in pixels or percentage via a numeric input or slider, with live preview on the canvas. -->Isso melhora a legibilidade de conteúdo de forma longa, como editoriais e artigos.

  Data de disponibilidade: 18 de fevereiro de 2026.

#### Modelos de conteúdo

* **Usar temas para converter imagens em modelos de email** - Ao converter uma imagem em um modelo de email no Journey Optimizer, agora é possível usar um tema como entrada para que o HTML gerado siga os parâmetros da sua marca. Estilos como cor de fundo, cor do botão, fontes, espaçamento entre linhas, margens e preenchimento são aplicados automaticamente, reduzindo o trabalho manual de design e fornecendo um modelo pronto para uso com edições mínimas. [Leia mais](../content-management/image-to-html.md)

  Data de disponibilidade: 17 de fevereiro de 2026.


#### Escolha de experiências

* **Suporte de entrada do Edge para o uso de dados do Adobe Experience Platform no Decisioning** - O uso de dados do Adobe Experience Platform no Decisioning agora oferece suporte a casos de uso de entrada de borda, além de email e ações personalizadas no jornada. [Leia mais](../experience-decisioning/aep-data-exd.md)

  **Observação**: este recurso só está disponível para um conjunto de organizações (<strong>Disponibilidade Limitada</strong>). Para obter acesso, entre em contato com um representante da Adobe.


* **Anexar fragmentos a itens de decisão**: o Journey Optimizer agora oferece a capacidade de anexar fragmentos a itens de decisão que podem ser aproveitados em campanhas de experiência baseada em código por meio de políticas de decisão. [Leia mais](../experience-decisioning/fragments-decision-policies.md)

  **Observação**: anteriormente lançado com disponibilidade limitada, esse recurso agora está disponível para todos os ambientes (Disponibilidade geral).

  Data de disponibilidade: 12 de fevereiro de 2026.

## Em breve {#coming-soon}

Os recursos e as melhorias abaixo estão planejados para lançamento no final de fevereiro. As datas de lançamento e o escopo podem mudar sem aviso prévio.

<table>
<thead>
<tr>
<th><strong>Journey Agent: criação de conteúdo de canal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Com a tecnologia <strong>Adobe Experience Platform Agent Orchestrator</strong>, o <strong>Journey Agent</strong> está disponível no Journey Optimizer e permite que você analise jornadas por meio de uma interface de linguagem natural. Agora você também pode gerar e gerenciar conteúdo específico de canal diretamente no Journey Agent, criando conteúdo para canais como email e push, aplicando e visualizando modelos, refinando o tom e o estilo por meio de prompts e abrindo conteúdo no <strong>Content Designer</strong> para edição em contexto.</p>
<p>Data de disponibilidade: sábado, 20 de fevereiro de 2026</p>
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
<p>Agora você pode usar <strong>fórmulas de classificação</strong> e <strong>modelos de IA</strong> para aumentar automaticamente as pontuações de prioridade de jornada com base nos atributos do perfil do cliente e em fatores contextuais, garantindo que os clientes insiram as jornadas mais relevantes.</p>
<p>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.</p>
<p>Data de disponibilidade: quarta-feira, 24 de fevereiro de 2026</p>
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
<p>O Journey Optimizer oferece suporte a uma nova <strong>Atividade de ação</strong> genérica que permite configurar ações únicas e grupos de ação de entrada de várias ações, permitindo uma configuração de ação simplificada na tela de jornada. Em especial, este novo recurso permite:</p>
<ul>
<li>Uma configuração de ação nativa simplificada na tela da jornada.</li>
<li>A capacidade de criar grupos de ação de entrada multiação.</li>
<li>A capacidade de adicionar otimização a qualquer ação de canal integrada.</li>
<li>A capacidade de adicionar opções de experimentação e multilíngues a qualquer ação.</li>
</ul>
<p>Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<p>Data de disponibilidade: sábado, 20 de fevereiro de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Monitoramento do modelo de IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora permite monitorar a integridade, o status do treinamento e o desempenho dos modelos de IA de decisão. Isso permite verificar o sucesso do treinamento, solucionar problemas de falhas e entender o impacto em seus resultados, a fim de selecionar as melhores ofertas para cada cliente que usa a IA. Observe que esse recurso está disponível somente para <strong>Decisão</strong> (não para modelos herdados do Gerenciamento de decisões).</p>
<p>Este recurso está disponível atualmente apenas para <strong>modelos de otimização personalizada</strong> (não de otimização automática).</p>
<p>Data de disponibilidade: sábado, 20 de fevereiro de 2026</p>
</td>
</tr>
</tbody>
</table>

### Aprimoramentos {#coming-soon-improv}

* **Visualização do Experience Decisioning no canal de experiência baseado em código** - Agora é possível visualizar itens de decisão ao configurar o Experience Decisioning com o canal de experiência baseado em código. A visualização está disponível diretamente na interface de criação antes de entrar em funcionamento.

  Data de disponibilidade: 20 de fevereiro de 2026.

* **Integração de modelos personalizados de Firefly e modelos de geração de imagem de terceiros** - Habilite a integração perfeita de modelos padrão e personalizados de Firefly, juntamente com modelos de imagem de terceiros aprovados (por exemplo, NanoBanana), para oferecer maior flexibilidade, controle e alinhamento de marca ao gerar imagens. Isso permite selecionar o melhor modelo para cada caso de uso: Firefly padrão para necessidades gerais, Firefly personalizado para geração na marca ou modelos aprovados de terceiros para cenários especializados ou experimentais.

  Data de disponibilidade: 20 de fevereiro de 2026.

