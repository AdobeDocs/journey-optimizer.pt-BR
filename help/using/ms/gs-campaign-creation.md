---
solution: Journey Optimizer
product: journey optimizer
title: Princípios-chave da criação de campanha orquestrada
description: Saiba mais sobre os principais princípios de campanhas orquestradas com o Adobe Journey Optimizer
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: b04aa15a-71bf-4683-bcbf-f611c189ffe1
source-git-commit: 03af80bbaa347237059abe74f26274df5ab39caa
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 32%

---

# Princípios fundamentais {#ms-campaign-creation}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="Campanha orquestrada"
>abstract="Nesta tela, é possível acessar a lista completa de campanhas orquestradas, verificar o status atual, as datas da última/próxima execução e criar uma nova campanha orquestrada."

Você pode criar campanhas orquestradas em uma tela visual para projetar processos entre canais, como segmentação, execução de campanha e processamento de arquivos.

## Acessar campanhas orquestradas

No menu **[!UICONTROL Campanhas]**, navegue até a guia Várias etapas para acessar a lista completa de campanhas orquestradas.

Cada campanha orquestrada na lista exibe informações sobre seu [status](#status) atual, a última vez que foi executada ou modificada e a data e hora da próxima execução agendada.

É possível personalizar as colunas exibidas clicando no ícone **[!UICONTROL Configurar coluna para um layout personalizado]** localizado no canto superior direito da lista. Isso permite adicionar mais informações à lista, como a última atividade com erro para cada campanha orquestrada ou o targeting dimension aplicado.

Além disso, uma barra de pesquisa e filtros estão disponíveis para facilitar a pesquisa na lista. Por exemplo, você pode filtrar as campanhas orquestradas para exibir apenas aquelas pertencentes a uma campanha ou aquelas processadas durante um intervalo de datas específico.

Para duplicar ou excluir uma campanha orquestrada, clique no botão de reticências e selecione **[!UICONTROL Duplicar]** ou **[!UICONTROL Excluir]**.

>[!NOTE]
>
>Quando uma campanha orquestrada está em andamento, você pode duplicá-la, mas não pode excluí-la.


## O que há dentro de uma campanha orquestrada? {#gs-ms-campaign-inside}

A tela orquestrada da campanha é uma representação do que deveria acontecer. Ele descreve as várias tarefas a serem executadas e como elas estão vinculadas.

![](assets/workflow-example.png){zoomable="yes"} {zoomable="yes"}

Cada campanha orquestrada contém:

* **Atividades**: uma atividade é uma tarefa a ser executada. As várias atividades são representadas no diagrama por ícones. Cada atividade tem propriedades específicas e outras propriedades que são comuns a todas as atividades.

  Em um diagrama de campanha orquestrado, uma determinada atividade pode produzir várias tarefas, principalmente quando há um loop ou ações recorrentes.

* **Transições**: as transições vinculam uma atividade de origem a uma atividade de destino e definem sua sequência.

* **Tabelas de trabalho**: as tabelas de trabalho contêm todas as informações transportadas pela transição. Cada campanha orquestrada usa várias tabelas de trabalho. Os dados transmitidos nessas tabelas podem ser usados durante o ciclo de vida da campanha orquestrada.


## Status e ciclo de vida {#status}

As campanhas podem ter vários status:

* **[!UICONTROL Rascunho]**: A campanha orquestrada foi criada e salva.
* **[!UICONTROL Em andamento]**: a campanha orquestrada está em execução no momento.
* **[!UICONTROL Concluído]**: a execução da campanha orquestrada foi concluída.
* **[!UICONTROL Pausado]**: a campanha orquestrada foi pausada.
* **[!UICONTROL Erro]**: a campanha orquestrada encontrou um erro. Abra a campanha orquestrada e acesse os logs e as tarefas para identificar o erro e resolvê-lo.
