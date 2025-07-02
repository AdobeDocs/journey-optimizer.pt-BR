---
solution: Journey Optimizer
product: journey optimizer
title: Iniciar e monitorar campanhas orquestradas com o Adobe Journey Optimizer
description: Saiba como iniciar e monitorar campanhas orquestradas com o Adobe Journey Optimizer.
hide: true
hidefromtoc: true
exl-id: 5fc2d1d6-75c3-4b45-bb2b-09982b9bd5ed
source-git-commit: d8b83bc46526f721d4dfaf62cf8ba4cbf5a56ce7
workflow-type: tm+mt
source-wordcount: '667'
ht-degree: 7%

---

# Iniciar e monitorar campanhas orquestradas {#start-monitor}

>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="Publicar campanha orquestrada"
>abstract="Para iniciar a campanha, você deve publicá-la. Certifique-se de que todos os avisos foram resolvidos antes da publicação."

+++ Sumário

| Bem-vindo às campanhas orquestradas | Lançar a primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](gs-orchestrated-campaigns.md)<br/><br/>[Etapas de configuração](configuration-steps.md)<br/><br/>[Acessar e gerenciar campanhas orquestradas](access-manage-orchestrated-campaigns.md) | [Etapas principais para a criação de campanha orquestrada](gs-campaign-creation.md)<br/><br/>[Criar e agendar a campanha](create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](orchestrate-activities.md)<br/><br/><b>[Iniciar e monitorar a campanha](start-monitor-campaigns.md)</b><br/><br/>[Relatórios](reporting-campaigns.md) | [Trabalhar com o construtor de regras](orchestrated-rule-builder.md)<br/><br/>[Criar a primeira consulta](build-query.md)<br/><br/>[Editar expressões](edit-expressions.md) | [Introdução às atividades](activities/about-activities.md)<br/><br/>Atividades:<br/>[And-join](activities/and-join.md) - [Criar público](activities/build-audience.md) - [Alterar dimensão](activities/change-dimension.md) - [Atividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Eliminação de Duplicação](activities/deduplication.md) - [Enriquecimento](activities/enrichment.md) - [Bifurcação](activities/fork.md) - [Reconciliação](activities/reconciliation.md) - [Divisão](activities/split.md) - [Aguardar](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Depois de criar as tarefas orquestradas e projetadas para execução na tela, é possível publicá-las e monitorar como elas estão sendo executadas.

Você também pode executar a campanha no modo de teste para verificar sua execução e o resultado das diferentes atividades.

## Teste sua campanha antes de publicar {#test}

O Journey Optimizer permite testar campanhas orquestradas antes de elas serem ativadas. No modo de teste, todas as atividades na tela são executadas, exceto **[!UICONTROL Salvar público-alvo]** atividades e atividades de canal. Não há impacto funcional nos seus dados ou público-alvo.

Para testar uma campanha:

1. Abra a campanha orquestrada.
2. Clique em **[!UICONTROL Start]**.

![](assets/campaign-start.png){zoomable="yes"}

Cada atividade na campanha é executada sequencialmente até que o final do diagrama seja atingido. Durante a execução do teste, é possível gerenciar a campanha usando a barra de ação na tela. A partir daí, você pode:

* **Parar** a execução a qualquer momento.
* **Inicie** a execução novamente.
* **Retomar** a execução se ela tiver sido pausada anteriormente devido a um problema.

Se ocorrer um erro ou aviso durante a execução, você será notificado por meio do ícone **[!UICONTROL Alertas]** / **[!UICONTROL Aviso]** na barra de ferramentas da tela.

![](assets/campaign-warning.png){zoomable="yes"}

Você também pode identificar rapidamente as atividades com falha usando os [indicadores visuais de status](#activities) exibidos diretamente em cada atividade. Para obter uma solução de problemas detalhada, abra os [logs da campanha](#logs-tasks), que fornecem informações detalhadas sobre o erro e seu contexto.

## Publicar a campanha {#publish}

Depois que sua campanha for testada e estiver pronta, clique em **[!UICONTROL Publicar]** para ativá-la.

![](assets/campaign-publish.png){zoomable="yes"}

O fluxo visual é reiniciado e os perfis reais começam a fluir pela jornada em tempo real.

## Monitorar a execução da campanha {#monitor}

### Monitoramento visual de fluxo {#flow}

Durante a execução (no modo de teste ou em tempo real), o fluxo visual mostra como os perfis se movem pela jornada em tempo real. O número de perfis que estão fazendo a transição entre tarefas é exibido.

![](assets/workflow-execution.png){zoomable="yes"}

Os dados transportados de uma atividade para outra por meio de transições são armazenados em uma tabela de trabalho temporária. Esses dados podem ser exibidos para cada transição. Para inspecionar dados transmitidos entre atividades:

1. Selecione uma transição.
1. No painel de propriedades, clique em **[!UICONTROL Visualizar esquema]** para exibir o esquema da tabela de trabalho. Selecione **[!UICONTROL Visualizar resultados]** para ver os dados transportados.

![](assets/transition.png){zoomable="yes"}

### Indicadores de execução da atividade {#activities}

Os indicadores visuais de status ajudam você a entender o desempenho de cada atividade:

| Indicador visual | Descrição |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | A atividade está sendo executada no momento. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | A atividade requer sua atenção. Isso pode envolver a confirmação do envio de um delivery ou a tomada de uma ação necessária. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | A atividade encontrou um erro. Para resolver o problema, abra os logs de campanha orquestradas para obter mais informações. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | A atividade foi executada com sucesso. |

### Logs e tarefas {#logs-tasks}

>[!CONTEXTUALHELP]
>id="ajo_campaign_logs"
>title="Logs e tarefas"
>abstract="A tela **Logs and tasks** fornece um histórico da execução de campanha orquestrada, registrando todas as ações de usuário e encontrando erros."

O monitoramento de logs e tarefas é uma etapa essencial para analisar campanhas orquestradas e garantir que elas estejam sendo executadas corretamente. Os logs e as tarefas podem ser acessados pelo botão **[!UICONTROL Logs]**, que está disponível nos modos de teste e ativo na barra de ferramentas da tela ou no painel de propriedades de cada atividade.

A tela **[!UICONTROL Logs and tasks]** fornece um histórico completo da execução de campanha, registrando todas as ações de usuário e erros encontrados.

![](assets/workflow-logs.png){zoomable="yes"}

Dois tipos de informações estão disponíveis:

* A guia **[!UICONTROL Log]** contém o histórico cronológico de todas as operações e erros.
* A guia **[!UICONTROL Tasks]** detalha a sequência de execução passo a passo das atividades.

Em ambas as guias, você pode escolher as colunas exibidas e sua ordem, aplicar filtros e usar o campo de pesquisa para localizar rapidamente as informações desejadas.
