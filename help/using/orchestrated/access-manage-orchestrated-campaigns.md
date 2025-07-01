---
solution: Journey Optimizer
product: journey optimizer
title: Acessar e gerenciar campanha orquestrada
description: Saiba mais sobre os principais princípios da criação de campanhas orquestradas com o Adobe Journey Optimizer
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 7b42d317-cd01-4c6a-b61e-5b03e5a8ff3c
source-git-commit: a1da25455621c02656706b95dcefe241370a6ac6
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 20%

---

# Acessar e gerenciar campanha orquestrada {#orchestrated-campaign-creation}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="Campanha orquestrada"
>abstract="Nesta tela, é possível acessar a lista completa de campanhas orquestradas, verificar o status atual, as datas da última/próxima execução e criar uma nova campanha orquestrada."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_campaign_action"
>title="Ação"
>abstract="Esta seção lista todas as ações usadas na campanha orquestrada."

+++ Sumário

| Bem-vindo às campanhas orquestradas | Lançar a primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](gs-orchestrated-campaigns.md)<br/><br/>[Etapas de configuração](configuration-steps.md)<br/><br/><b>[Acessar e gerenciar campanhas orquestradas](access-manage-orchestrated-campaigns.md)</b> | [Etapas principais para a criação de campanha orquestrada](gs-campaign-creation.md)<br/><br/>[Criar e agendar a campanha](create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](orchestrate-activities.md)<br/><br/>[Enviar mensagens com campanhas orquestradas](send-messages.md)<br/><br/>[Iniciar e monitorar a campanha](start-monitor-campaigns.md)<br/><br/>[Relatórios](reporting-campaigns.md) | [Trabalhar com o construtor de regras](orchestrated-rule-builder.md)<br/><br/>[Criar a primeira consulta](build-query.md)<br/><br/>[Editar expressões](edit-expressions.md) | [Introdução às atividades](activities/about-activities.md)<br/><br/>Atividades:<br/>[And-join](activities/and-join.md) - [Criar público](activities/build-audience.md) - [Alterar dimensão](activities/change-dimension.md) - [Combinar](activities/combine.md) - [Eliminação de Duplicação](activities/deduplication.md) - [Enriquecimento](activities/enrichment.md) - [Bifurcação](activities/fork.md) - [Reconciliação](activities/reconciliation.md) - [Divisão](activities/split.md) - [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

## Acessar campanhas orquestradas

Navegue até o menu **[!UICONTROL Campanhas]** e selecione a guia **[!UICONTROL Orquestração]** para acessar a lista completa de campanhas orquestradas.

![imagem mostrando o inventário de campanhas orquestradas](assets/inventory.png){zoomable="yes"}{zoomable="yes"}

Cada campanha orquestrada na lista exibe informações como o [status](#status) atual da campanha, o canal e as tags associados ou a última vez que ela foi modificada. Você pode personalizar as colunas exibidas clicando no botão ![Configurar layout](assets/do-not-localize/inventory-configure-layout.svg).

Além disso, uma barra de pesquisa e filtros estão disponíveis para facilitar a pesquisa na lista. Por exemplo, você pode filtrar as campanhas orquestradas para exibir somente aquelas associadas a um determinado canal ou tag, ou aquelas criadas durante um intervalo de datas específico.

A ![imagem que mostra o botão Mais ações](assets/do-not-localize/rule-builder-icon-more.svg) no inventário de campanhas permite executar várias operações detalhadas abaixo.

![imagem do inventário de campanhas](assets/inventory-actions.png)

* **[!UICONTROL Exibir o relatório de todos os tempos]** / **[!UICONTROL Exibir o relatório das últimas 24 horas]** - Acesse relatórios para medir e visualizar o impacto e o desempenho de suas campanhas orquestradas. [Saiba mais sobre relatórios de campanhas orquestradas](../orchestrated/reporting-campaigns.md)
* **[!UICONTROL Editar marcas]** - Edita as marcas associadas à campanha.
* **[!UICONTROL Duplicar]** - Em alguns casos, pode ser necessário duplicar uma campanha orquestrada, por exemplo, para executar uma campanha que foi interrompida ou para alterar a frequência de execução de uma campanha agendada.
* **[!UICONTROL Excluir]** - Excluir a campanha. Estas ações estão disponíveis somente para campanhas do **[!UICONTROL Rascunho]**.
* **[!UICONTROL Arquivar]** - Arquivar a campanha. Todas as campanhas arquivadas são excluídas em uma reprogramação contínua 30 dias após sua última data modificada. Esta ação está disponível para todas as campanhas, exceto as campanhas de **[!UICONTROL Rascunho]**.

## O que há dentro de uma campanha orquestrada? {#gs-ms-campaign-inside}

A tela orquestrada da campanha é uma representação do que deveria acontecer. Ele descreve as várias tarefas a serem executadas e como elas estão vinculadas.

![imagem mostrando uma tela de campanha orquestrada](assets/canvas-example.png)

Cada campanha orquestrada contém:

* **Atividades**: uma atividade é uma tarefa a ser executada. As várias atividades são representadas no diagrama por ícones. Cada atividade tem propriedades específicas e outras propriedades que são comuns a todas as atividades.

  Em um diagrama de campanha orquestrado, uma determinada atividade pode produzir várias tarefas, principalmente quando há um loop ou ações recorrentes.

* **Transições**: as transições vinculam uma atividade de origem a uma atividade de destino e definem sua sequência.

* **Tabelas de trabalho**: as tabelas de trabalho contêm todas as informações transportadas pela transição. Cada campanha orquestrada usa várias tabelas de trabalho. Os dados transmitidos nessas tabelas podem ser usados durante o ciclo de vida da campanha orquestrada.

## Status das campanhas {#status}

As campanhas orquestradas podem ter vários status:

* **[!UICONTROL Rascunho]**: A campanha orquestrada foi criada. Ele ainda não foi publicado.
* **[!UICONTROL Publicação]**: a campanha orquestrada está sendo publicada.
* **[!UICONTROL Live]**: a campanha orquestrada foi publicada e está sendo executada.
* **[!UICONTROL Agendado]**: a execução da campanha orquestrada foi agendada.
* **[!UICONTROL Concluído]**: a execução da campanha orquestrada foi concluída. O status Completed é atribuído automaticamente até 3 dias após uma campanha concluir o envio de mensagens sem erro.
* **[!UICONTROL Fechado]**: esse status é exibido quando uma campanha recorrente é fechada. A campanha continua sua execução até que todas as atividades tenham sido concluídas, mas nenhum perfil mais pode entrar na campanha.
* **[!UICONTROL Arquivado]**: a campanha orquestrada foi arquivada. Todas as campanhas arquivadas são excluídas em uma reprogramação contínua 30 dias após a última data modificada. Você pode duplicar uma campanha arquivada, se necessário, para continuar trabalhando nela.
* **[!UICONTROL Parado]**: a execução da campanha orquestrada foi interrompida. Para iniciar a campanha novamente, você precisa duplicá-la. si erreur, triângulo avec restera
