---
solution: Journey Optimizer
product: journey optimizer
title: Iniciar e monitorar campanhas orquestradas com o Adobe Journey Optimizer
description: Saiba como iniciar e monitorar campanhas orquestradas com o Adobe Journey Optimizer.
hide: true
hidefromtoc: true
exl-id: 5fc2d1d6-75c3-4b45-bb2b-09982b9bd5ed
source-git-commit: 445194fcc08efacdbf5f97a425d01229f82d11ea
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 9%

---

# Iniciar e monitorar campanhas orquestradas {#start-monitor}

>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="Publicar campanha orquestrada"
>abstract="Para iniciar a campanha, você deve publicá-la. Certifique-se de que todos os avisos foram resolvidos antes da publicação."

+++ Sumário

| Bem-vindo às campanhas orquestradas | Lançar a primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução às campanhas orquestradas](gs-orchestrated-campaigns.md)<br/><br/>[Etapas de configuração](configuration-steps.md)<br/>&lt;br/[Acessar e gerenciar campanhas orquestradas](access-manage-orchestrated-campaigns.md) | [Etapas principais para a criação de campanha orquestrada](gs-campaign-creation.md)<br/><br/>[Criar e agendar a campanha](create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](orchestrate-activities.md)<br/><br/>[Enviar mensagens com campanhas orquestradas](send-messages.md)<br/><br/><b>[Iniciar e monitorar a campanha](start-monitor-campaigns.md)</b><br/><br/>[Relatórios](reporting-campaigns.md) | [Trabalhar com o construtor de regras](orchestrated-rule-builder.md)<br/><br/>[Criar a primeira consulta](build-query.md)<br/><br/>[Editar expressões](edit-expressions.md) | [Introdução às atividades](activities/about-activities.md)<br/><br/>Atividades:<br/>[And-join](activities/and-join.md) - [Criar público](activities/build-audience.md) - [Alterar dimensão](activities/change-dimension.md) - [Combinar](activities/combine.md) - [Eliminação de Duplicação](activities/deduplication.md) - [Enriquecimento](activities/enrichment.md) - [Bifurcação](activities/fork.md) - [Reconciliação](activities/reconciliation.md) - [Divisão](activities/split.md) - [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Depois de criar as tarefas orquestradas e projetadas para execução na tela, é possível publicá-las e monitorar como elas estão sendo executadas.

## Iniciar uma campanha orquestrada {#start}

Para iniciar uma campanha orquestrada, navegue até a guia **[!UICONTROL Orquestração]** do menu **[!UICONTROL Campanhas]** e selecione a campanha a ser iniciada e clique no botão **[!UICONTROL Reproduzir]**, no canto superior direito da tela.

Quando a campanha orquestrada estiver em execução, cada atividade na tela será executada em ordem sequencial, até que o final da campanha orquestrada seja atingido.

Você pode acompanhar o progresso de perfis direcionados em tempo real usando um fluxo visual. Isso permite identificar rapidamente o status de cada atividade e o número de perfis em transição entre elas.

![](assets/workflow-execution.png){zoomable="yes"}

Em campanhas orquestradas, os dados transportados de uma atividade para outra por meio de transições são armazenados em uma tabela de trabalho temporária. Esses dados podem ser exibidos para cada transição. Para fazer isso, selecione uma transição para abrir as propriedades no lado direito da tela.

* Clique em **[!UICONTROL Visualizar esquema]** para exibir o esquema da tabela de trabalho.
* Clique em **[!UICONTROL Visualizar resultados]** para visualizar os dados transportados na transição selecionada.

![](assets/transition.png){zoomable="yes"}

## Monitorar a execução da campanha

### Monitorar execução da atividade {#activities}

Os indicadores visuais no canto superior direito de cada caixa de atividade permitem verificar a execução:

| Indicador visual | Descrição |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | A atividade está sendo executada no momento. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | A atividade requer sua atenção. Isso pode envolver a confirmação do envio de um delivery ou a tomada de uma ação necessária. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | A atividade encontrou um erro. Para resolver o problema, abra os logs de campanha orquestradas para obter mais informações. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | A atividade foi executada com sucesso. |

### Monitorar logs e tarefas {#logs-tasks}

>[!CONTEXTUALHELP]
>id="ajo_campaign_logs"
>title="Logs e tarefas"
>abstract="A tela **Logs e tarefas** fornece um histórico da execução da campanha orquestrada, registrando todas as ações do usuário e erros encontrados."

O monitoramento de logs e tarefas é uma etapa essencial para analisar campanhas orquestradas e garantir que elas estejam sendo executadas corretamente. Eles podem ser acessados pelo ícone **[!UICONTROL Logs]**, que está disponível na barra de ferramentas de ações e no painel de propriedades de cada atividade.

O menu **[!UICONTROL Logs and tasks]** fornece um histórico da execução de campanha orquestrada, registrando todas as ações de usuário e encontrando erros.

![](assets/workflow-logs.png){zoomable="yes"}

Dois tipos de informações estão disponíveis:

* A guia **[!UICONTROL Log]** contém o histórico de execução de todas as atividades de campanha orquestradas. Ele indexa as operações realizadas e os erros de execução por ordem cronológica.
* A guia **[!UICONTROL Tasks]** detalha a sequência de execução das atividades.

Em ambas as guias, você pode escolher as colunas exibidas e sua ordem, aplicar filtros e usar o campo de pesquisa para localizar rapidamente as informações desejadas.

## Comandos de execução de campanha orquestrados {#execution-commands}

A barra de ação no canto superior direito fornece comandos que permitem gerenciar a execução orquestrada da campanha. É possível:

* **[!UICONTROL Iniciar]** / **[!UICONTROL Retomar]** a execução do   campanha orquestrada, que então assume o status In progress. Se a campanha orquestrada tiver sido pausada, ela será retomada, caso contrário, ela será iniciada e as atividades iniciais serão ativadas.

* **[!UICONTROL Pausar]** a execução da campanha orquestrada, que então assume o status Pausado. Nenhuma nova atividade será ativada até que seja retomada, mas as operações em andamento não são suspensas.

* **[!UICONTROL Parar]** uma campanha orquestrada que está sendo executada, que assumirá o status Concluído. Se possível, as operações em andamento são interrompidas. Não é possível retomar da campanha orquestrada do mesmo local em que ela foi interrompida.
