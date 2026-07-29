---
solution: Journey Optimizer
product: journey optimizer
title: Monitorar o desempenho de desafio de fidelidade
description: Saiba como usar os painéis de relatórios de Desafios de fidelidade para rastrear o desempenho de desafios e insights no Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: a1b2c3d4-e5f6-7890-abcd-ef1234567890
feature_v2: []
subfeature_v2: []
source-git-commit: b08de542c4f952f82a503103c783e54196c6d5b6
workflow-type: tm+mt
source-wordcount: 511
ht-degree: 0%

---

# Monitorar o desempenho de desafio de fidelidade {#loyalty-reporting}

Use os relatórios de Desafios de fidelidade para ver o desempenho de seus desafios. Verifique quem está se inscrevendo, quem está concluindo os desafios e quanta receita seu programa está gerando — tudo em um só lugar. Os dados vêm do Adobe Customer Journey Analytics.

Para abrir os painéis de relatórios, vá para **[!UICONTROL Desafios de Fidelidade]** no Journey Optimizer e selecione **[!UICONTROL Relatórios de fidelidade]** na navegação à esquerda.

A interface de relatórios tem duas guias:

* **[Relatórios](#reports-view)**: números e gráficos para seus desafios.
* **[Insights](#insights-cards)**: cartões que destacam o que merece sua atenção neste momento.

## Exibição de relatórios {#reports-view}

A guia **Relatórios** fornece uma visão geral de como seu programa está se saindo no período selecionado. Use o seletor de datas na parte superior da página e selecione o botão **[!UICONTROL Aplicar filtro]** para alterar o período do relatório e ver os números e gráficos atualizados.

![](assets/reporting-challenge-key.png)

A área **Métricas principais** mostra quatro números de imediato. Cada métrica também exibe uma alteração de porcentagem em comparação ao período anterior.

* **Membros de fidelidade**: quantos membros de fidelidade estavam ativos durante o período.
* **Inscrições no desafio**: quantas vezes os membros se inscreveram em um desafio.
* **Receita**: receita total vinculada à atividade de desafio.
* **Taxa média de conclusão**: a porcentagem de membros inscritos que concluíram pelo menos um desafio.

O painel **Últimos insights** à direita mostra os insights gerados pela IA mais recentes do seu programa. Selecione **[!UICONTROL Exibir todos]** para abrir a guia completa **Insights**.

Abaixo das métricas principais, a seção **Desafios** oferece duas visualizações da atividade de desafio.

![](assets/reporting-challenge-challenges.png)

* **Envolvimento do desafio**: uma linha do tempo mostrando quantos membros iniciaram, estão em andamento e concluíram desafios durante o período.
* **Relatórios de desafios**: uma tabela de todos os seus desafios com detalhes como tipo, tarefas, status e números de inscrição. Use a barra de pesquisa para encontrar um desafio específico. Selecione um desafio para ver seu relatório completo com tendências de envolvimento e detalhes de desempenho.

  +++Exemplo de relatório de desafio

  ![](assets/reporting-challenge-report.png)

  +++

## Guia Insights {#insights-cards}

A guia **Insights** exibe cartões gerados por IA que sinalizam anomalias, tendências e oportunidades em seu programa de fidelidade. Cada cartão representa uma única observação e é classificado de acordo com a sua importância em relação aos dados atuais do programa.

![](assets/reporting-insights.png)

Um carimbo de data/hora **Último rastreo** na parte superior direita mostra quando o mecanismo do insight processou os dados do programa pela última vez.

### Ações do cartão {#insight-card-actions}

Cada cartão tem um menu ![](assets/do-not-localize/Smock_More_18_N.svg) com duas ações:

* **Dispensar**: remove permanentemente o cartão da lista de insights.
* **Adiar**: oculta o cartão temporariamente. Escolha adiar por **1 dia**, **3 dias** ou **7 dias**. O cartão reaparece após o término do período de adiamento.

<!--
### Priority badges {#insight-badges}

Each card has a priority badge — **High**, **Medium**, or **Low** — based on how significant the underlying signal is relative to your current program data. These levels are relative: there are always a few **High** cards, even in a quiet week. **High** means "most relevant right now", not that a fixed threshold was crossed.
-->

### Tags de categoria {#insight-category-tags}

Cada cartão contém uma **marca de categoria** que identifica a qual parte do programa a insight está relacionada.

| Categoria | O que ele cobre |
| --- | --- |
| **Em todo o programa** | Integridade geral e desempenho do seu programa de fidelidade |
| **Nível** | Taxas de ganho, movimentação e distribuição entre níveis de membros |
| **Desafio** | Atividade, taxas de conclusão e anomalias para um desafio específico ou entre desafios |
| **Produto** | Desempenho do catálogo de produtos, incluindo exibições, resgates e tendências no nível do catálogo |
| **Ciclo de vida do membro** | Como os membros avançam nos estágios de inscrição, engajamento e churn |
| **Tendência** | Padrões com base no tempo, como ciclos semanais, picos sazonais ou reversões de tendência |

