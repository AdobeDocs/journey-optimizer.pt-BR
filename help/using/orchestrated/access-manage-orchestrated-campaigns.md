---
solution: Journey Optimizer
product: journey optimizer
title: Acessar e gerenciar campanhas orquestradas
description: Saiba mais sobre os principais princípios da criação de campanhas orquestradas com o Adobe Journey Optimizer
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 7b42d317-cd01-4c6a-b61e-5b03e5a8ff3c
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 91%

---

# Acessar e gerenciar campanhas orquestradas {#orchestrated-campaign-creation}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="Campanha orquestrada"
>abstract="Nesta tela, é possível acessar a lista completa de campanhas orquestradas, verificar o status atual, as datas da última/próxima execução e criar uma nova campanha orquestrada."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_campaign_action"
>title="Ação"
>abstract="Esta seção lista todas as ações usadas na campanha orquestrada."

+++ Índice 

| Bem-vindo(a) às campanhas orquestradas | Lançar a sua primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](gs-orchestrated-campaigns.md)<br/><br/>Criar e gerenciar Esquemas e Conjuntos de Dados relacionais:</br> <ul><li>[Introdução a Esquemas e Conjuntos de Dados](gs-schemas.md)</li><li>[Esquema manual](manual-schema.md)</li><li>[Esquema de carregamento de arquivo](file-upload-schema.md)</li><li>[Assimilar dados](ingest-data.md)</li></ul><br/><br/><b>[Acesse e gerencie campanhas orquestradas](access-manage-orchestrated-campaigns.md)</b><br/><br/>[Etapas principais para criar uma campanha orquestrada](gs-campaign-creation.md) | [Criar e programar a campanha](create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](orchestrate-activities.md)<br/><br/>[Iniciar e monitorar a campanha](start-monitor-campaigns.md)<br/><br/>[Geração de relatórios](reporting-campaigns.md) | [Trabalhar com o construtor de regras](orchestrated-rule-builder.md)<br/><br/>[Criar a sua primeira consulta](build-query.md)<br/><br/>[Editar expressões](edit-expressions.md)<br/><br/>[Redirecionamento](retarget.md) | [Introdução às atividades](activities/about-activities.md)<br/><br/>Atividades:<br/>[Associação](activities/and-join.md) - [Criar público-alvo](activities/build-audience.md) - [Mudar dimensão](activities/change-dimension.md) - [Atividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Desduplicação](activities/deduplication.md) - [Enriquecimento](activities/enrichment.md) - [Bifurcação](activities/fork.md) - [Reconciliação](activities/reconciliation.md) - [Salvar público-alvo](activities/save-audience.md) - [Divisão](activities/split.md) - [Aguardar](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

O conteúdo desta página não é final e pode estar sujeito a alterações.

>[!ENDSHADEBOX]

## Acessar campanhas orquestradas

Navegue até o menu **[!UICONTROL Campanhas]** e selecione a guia **[!UICONTROL Orquestração]** para acessar a lista completa de campanhas orquestradas.

![imagem mostrando o inventário de campanhas orquestradas](assets/inventory.png){zoomable="yes"}{zoomable="yes"}

Cada campanha orquestrada da lista exibe informações, como o [status](#status) atual da campanha, o canal e as tags associados, ou a última vez que ela foi modificada. Você pode personalizar as colunas exibidas, clicando no botão ![Configurar layout](assets/do-not-localize/inventory-configure-layout.svg).

Além disso, uma barra de pesquisa e filtros estão disponíveis para facilitar a pesquisa na lista. Por exemplo, você pode filtrar as campanhas orquestradas para exibir somente as associadas a um determinado canal ou tag, ou as criadas durante um intervalo de datas específico.

A ![imagem que mostra o botão “Mais ações”](assets/do-not-localize/rule-builder-icon-more.svg) no inventário de campanhas permite executar as diversas operações detalhadas abaixo.

![imagem do inventário de campanhas](assets/inventory-actions.png)

* **[!UICONTROL Visualizar o relatório de todo o histórico]** / **[!UICONTROL Visualizar o relatório das últimas 24 horas]**: acesse os relatórios para medir e visualizar o impacto e o desempenho das suas campanhas orquestradas. [Saiba mais sobre a geração de relatórios de campanhas orquestradas](../orchestrated/reporting-campaigns.md)
* **[!UICONTROL Editar tags]**: edite as tags associadas à campanha.
* **[!UICONTROL Duplicar]**: em alguns casos, pode ser necessário duplicar uma campanha orquestrada, como, por exemplo, para executar uma campanha que foi interrompida ou alterar a frequência de execução de uma campanha programada.
* **[!UICONTROL Excluir]**: exclua a campanha. Essas ações estão disponíveis somente para **[!UICONTROL Rascunhos]** de campanha.
* **[!UICONTROL Arquivar]**: arquive a campanha. Todas as campanhas arquivadas são excluídas em um prazo contínuo 30 dias após a data da última modificação. Essa ação está disponível para todas as campanhas, exceto **[!UICONTROL Rascunhos]** de campanha.

## O que há dentro de uma campanha orquestrada? {#gs-ms-campaign-inside}

A tela da campanha orquestrada é uma representação do que deveria acontecer. Ele descreve as várias tarefas a serem executadas e como elas estão vinculadas.

![imagem mostrando a tela de uma campanha orquestrada](assets/canvas-example.png)

Cada campanha orquestrada contém:

* **Atividades**: uma atividade é uma tarefa a ser executada. As várias atividades são representadas no diagrama por ícones. Cada atividade tem propriedades específicas e outras propriedades que são comuns a todas as atividades.

  No diagrama de uma campanha orquestrada, uma determinada atividade pode gerar várias tarefas, principalmente quando há ações contínuas ou recorrentes.

* **Transições**: as transições vinculam uma atividade de origem a uma atividade de destino e definem sua sequência.

* **Tabelas de trabalho**: as tabelas de trabalho contêm todas as informações transportadas pela transição. Cada campanha orquestrada usa várias tabelas de trabalho. Os dados transmitidos nessas tabelas podem ser usados durante todo o ciclo de vida da campanha orquestrada.

## Status das campanhas {#status}

As campanhas orquestradas podem ter vários status:

* **[!UICONTROL Rascunho]**: a campanha orquestrada foi criada. Ela ainda não foi publicada.
* **[!UICONTROL Publicando]**: a campanha orquestrada está sendo publicada.
* **[!UICONTROL Ativa]**: a campanha orquestrada foi publicada e está sendo executada.
* **[!UICONTROL Programada]**: a execução da campanha orquestrada foi programada.
* **[!UICONTROL Concluída]**: a execução da campanha orquestrada foi concluída. O status “Concluída” é atribuído automaticamente até três dias após uma campanha concluir o envio de mensagens sem erros.
* **[!UICONTROL Encerrada]**: este status é exibido quando uma campanha recorrente é encerrada. A campanha continua sendo executada até que todas as atividades tenham sido concluídas, mas nenhum outro perfil poderá entrar na campanha.
* **[!UICONTROL Arquivada]**: a campanha orquestrada foi arquivada. Todas as campanhas arquivadas são excluídas dentro de um prazo contínuo 30 dias após a data da última modificação. Você pode duplicar uma campanha arquivada, se necessário, para continuar trabalhando nela.
* **[!UICONTROL Interrompida]**: a execução da campanha orquestrada foi interrompida. Para iniciar a campanha novamente, você precisa duplicá-la.
