---
solution: Journey Optimizer
product: journey optimizer
title: Relatório de jornada
description: Saiba como usar os dados do relatório de jornada
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: a2219bf7791bc5c598228af883d0507180628abf
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 0%

---

# Relatório de jornada {#journey-global-report}

O **relatório de Jornadas** funciona como um painel abrangente, fornecendo uma análise das métricas essenciais associadas à sua jornada. Isso inclui detalhes como a contagem de perfis inseridos e instâncias de jornadas individuais com falha, oferecendo um insight abrangente sobre a eficácia e o nível de engajamento da jornada.

O **relatório de Jornadas** pode ser acessado diretamente da sua jornada com o botão **[!UICONTROL Exibir relatório]**.

![](assets/gs-cja-report-3.png)

Para saber mais sobre o Customer Journey Analytics Workspace e como filtrar e analisar dados, consulte [esta página](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/home).

## Visão geral da jornada {#journey-global}

O relatório **[!UICONTROL Jornada]** fornece uma visão clara dos dados de rastreamento mais importantes sobre sua jornada.

### Jornada KPIs {#journey-perfomance}

![](assets/cja-journey-kpis.png)

Os Indicadores Principais de Desempenho (KPIs) da **[!UICONTROL Jornada]** funcionam como um painel abrangente, fornecendo uma análise das métricas essenciais associadas à sua jornada. Isso inclui detalhes como a contagem de perfis inseridos e instâncias de jornadas individuais com falha, oferecendo um insight abrangente sobre a eficácia e o nível de engajamento da jornada.

+++ Saiba mais sobre métricas de KPIs do Jornada

* **[!UICONTROL Participação na Jornada]**: número total de pessoas que interagiram com as mensagens enviadas pela jornada

* **[!UICONTROL Entradas de Jornada]**: número total de pessoas físicas que atingiram o evento de entrada da jornada.

* **[!UICONTROL Saídas da Jornada]**: número total de indivíduos que saíram da jornada.

* **[!UICONTROL Falhas de Jornada]**: número total de jornadas individuais que não foram executadas com êxito.

+++

### Estatísticas da jornada {#journey-stats}

![](assets/cja-journey-stats.png)

A tabela **[!UICONTROL Estatísticas de Jornada]** oferece um resumo detalhado de dados cruciais sobre suas jornadas. Ele inclui métricas principais como o número de falhas e entradas bem-sucedidas, fornecendo insights valiosos sobre o desempenho e o alcance de seus emails e jornadas.

+++ Saiba mais sobre métricas de Estatísticas do Jornada

* **[!UICONTROL Engajamento na Jornada]**: número total de pessoas que interagiram com as mensagens enviadas pela jornada.

* **[!UICONTROL Entradas de Jornada]**: número total de pessoas físicas que atingiram o evento de entrada da jornada.

* **[!UICONTROL Saídas da Jornada]**: número total de indivíduos que saíram da jornada.

* **[!UICONTROL Falhas de Jornada]**: número total de jornadas individuais que não foram executadas com êxito.

* **[!UICONTROL Entradas de Jornada exclusivas]**: número total de pessoas físicas que atingiram o evento de entrada da jornada; várias interações de um perfil não são consideradas.

* **[!UICONTROL Saídas de Jornadas exclusivas]**: número total de indivíduos que saíram da jornada; várias interações de um perfil não são consideradas.

* **[!UICONTROL Falhas de Jornada exclusivas]**: número total de jornadas individuais que não foram executadas com êxito, várias interações de um perfil não são consideradas.

+++

## Jornada tela {#journey-canvas}

![](assets/cja-journey-canvas.png)

O widget **[!UICONTROL Tela de Jornada]** permite rastrear visualmente a trajetória dos perfis direcionados à medida que eles navegam pela jornada. [Saiba mais na documentação do Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/journey-canvas/journey-canvas)

Aprimore sua personalização da tela com as seguintes opções:

* Adicione ou remova o tipo de atividade desejado, como mensagens ou condições, do menu suspenso **[!UICONTROL Tipo de nó]**.
* Ajuste o **[!UICONTROL valor percentual]** para determinar a distribuição de fluxo entre caminhos de jornada diferentes.
* Personalize suas **[!UICONTROL Configurações de seta]** para incluir rótulos, condições ou optar por uma exibição limpa.
* Habilite a opção **[!UICONTROL Mostrar fallout]** para visualizar os perfis que saíram da sua jornada diretamente na tela.

As seguintes regras se aplicam ao usar a Filtragem **[!UICONTROL Tipo de Nó]**:

* Ao criar um segmento em um nó, ele ainda englobará nós de estágios anteriores da jornada, mesmo que esses nós tenham sido excluídos por meio do filtro **[!UICONTROL Tipo de nó]**.

* Não é possível criar segmentos formados por uma seta se os nós em estágios anteriores da jornada tiverem sido excluídos por meio do filtro **[!UICONTROL Tipo de nó]**. Nesse caso, a funcionalidade de clicar com o botão direito do mouse será desativada nessas setas.

## Desempenho da ação {#action-performance}

### Desempenho ao longo do tempo {#action-overtime}

![](assets/cja-journey-action-performance.png)

O gráfico **[!UICONTROL Desempenho ao longo do tempo]** permite identificar e analisar o número de perfis que atendem aos critérios para serem considerados perfis de destino para suas ações. Essa visualização fornece insights valiosos sobre a eficácia de suas estratégias e ajuda a tomar decisões orientadas por dados para otimizar seu desempenho.

### Visão geral da ação {#action-overview}

![](assets/cja-journey-action-overview.png)

A tabela **[!UICONTROL Visão geral das ações]** serve como um painel abrangente, que oferece uma análise das métricas principais relacionadas às ações da sua jornada. Isso inclui detalhes cruciais, como o número de interações e a taxa de cliques

+++ Saiba mais sobre Métricas de visão geral de ação

* **[!UICONTROL Pessoas]**: número de perfis de usuário qualificados como perfis de destino para suas ações.

* **[!UICONTROL Taxa de transferência de cliques]**: porcentagem de usuários que interagiram com a ação.

* **[!UICONTROL Cliques]**: número de vezes que um conteúdo foi clicado em suas ações.

* **[!UICONTROL Entregues]**: número de ações enviadas com êxito em relação ao número total de ações enviadas.

+++

## Desempenho de eventos {#events-performance}

### Desempenho ao longo do tempo {#event-overtime}

![](assets/cja-journey-performance-event.png)

O gráfico **[!UICONTROL Desempenho ao longo do tempo]** permite identificar e analisar o número de perfis qualificados como perfis de destino para seus eventos. Essa poderosa ferramenta ajuda a rastrear tendências e padrões ao longo do tempo, fornecendo insights valiosos para otimizar suas estratégias de eventos.

### Visão geral do evento {#event-overview}

![](assets/cja-journey-events-overview.png)

A tabela **[!UICONTROL Visão geral do evento]** mostra quantos perfis atendem aos seus critérios de evento ao longo do tempo. Essa ferramenta ajuda a identificar padrões nas taxas de qualificação para refinar sua estratégia de eventos.

+++ Saiba mais sobre métricas de Estatísticas do Jornada

* **[!UICONTROL Pessoas]**: número de perfis de usuário qualificados como perfis de destino para seus eventos.

+++
