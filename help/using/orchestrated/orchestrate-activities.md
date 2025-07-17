---
solution: Journey Optimizer
product: journey optimizer
title: Criar campanhas orquestradas com o Adobe Journey Optimizer
description: Saiba como criar campanhas orquestradas com o Adobe Journey Optimizer
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: d1d64125-cf00-49c2-a71d-1494ede16f61
source-git-commit: 1aa4f3e24a4cb7594232c0b25da8c9fd2e62c1de
workflow-type: tm+mt
source-wordcount: '994'
ht-degree: 1%

---

# Orquestrar atividades de campanha {#orchestrate}

+++ Sumário

| Bem-vindo às campanhas orquestradas | Lançar a primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](gs-orchestrated-campaigns.md)<br/><br/>Criar e gerenciar Esquemas e Conjuntos de Dados relacionais:</br> <ul><li>[Esquema manual](manual-schema.md)</li><li>[Esquema de carregamento de arquivo](file-upload-schema.md)</li><li>[Assimilar dados](ingest-data.md)</li></ul><br/><br/>[Acesse e gerencie campanhas orquestradas](access-manage-orchestrated-campaigns.md)<br/><br/>[Etapas principais para criar uma campanha orquestrada](gs-campaign-creation.md) | [Criar e agendar a campanha](create-orchestrated-campaign.md)<br/><br/><b>[Orquestrar atividades](orchestrate-activities.md)</b><br/><br/>[Iniciar e monitorar a campanha](start-monitor-campaigns.md)<br/><br/>[Relatórios](reporting-campaigns.md) | [Trabalhar com o construtor de regras](orchestrated-rule-builder.md)<br/><br/>[Criar a primeira consulta](build-query.md)<br/><br/>[Editar expressões](edit-expressions.md)<br/><br/>[Redirecionamento](retarget.md) | [Introdução às atividades](activities/about-activities.md)<br/><br/>Atividades:<br/>[And-join](activities/and-join.md) - [Criar público](activities/build-audience.md) - [Alterar dimensão](activities/change-dimension.md) - [Atividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Desduplicação](activities/deduplication.md) - [Enriquecimento](activities/enrichment.md) - [Bifurcação](activities/fork.md) - [Reconciliação](activities/reconciliation.md) - [Salvar público](activities/save-audience.md) - [Divisão](activities/split.md) - [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

O conteúdo desta página não é final e pode estar sujeito a alterações.

>[!ENDSHADEBOX]

Depois que você tiver [criado uma campanha orquestrada](gs-campaign-creation.md), poderá começar a orquestrar as diferentes tarefas que ela executará. Para fazer isso, uma tela visual é fornecida, permitindo que você construa um diagrama de campanha orquestrado. Neste diagrama, é possível adicionar várias atividades e conectá-las em ordem sequencial.

## Adicionar atividades {#add}

Nessa etapa da configuração, o diagrama é exibido com um ícone de início, representando o início da campanha orquestrada. Para adicionar sua primeira atividade, clique no botão **+** conectado ao ícone de início.

Uma lista de atividades que podem ser adicionadas ao diagrama é exibida. As atividades disponíveis dependem da sua posição no diagrama de campanha orquestrada. Por exemplo, ao adicionar sua primeira atividade, é possível iniciar a campanha orquestrada direcionando um público, dividindo o caminho da campanha orquestrada ou definindo uma atividade **Wait** para atrasar a execução da campanha orquestrada. Por outro lado, depois de uma atividade **Criar público-alvo**, você pode refinar seu público-alvo com atividades de direcionamento, enviar uma entrega para seu público com atividades de canal ou organizar o processo de campanha orquestrada com atividades de controle de fluxo.

![](assets/orchestrated-start.png){zoomable="yes"}

Depois que uma atividade é adicionada ao diagrama, um painel direito é exibido, permitindo que você a configure com configurações específicas. Informações detalhadas sobre como configurar cada atividade estão disponíveis em [esta seção](activities/about-activities.md).

![](assets/orchestrated-configure-activities.png){zoomable="yes"}

Repita esse processo para adicionar quantas atividades desejar, dependendo das tarefas que deseja que sua campanha orquestrada execute. Observe que você também pode inserir uma nova atividade entre duas atividades. Para fazer isso, clique no botão **+** na transição entre as atividades, selecione a atividade desejada e a configure no painel direito.

Você tem a opção de personalizar o nome das transições entre cada atividade. Para fazer isso, selecione a transição e altere seu rótulo no painel direito.

![](assets/canvas-transition.png)

### A barra de ferramentas da tela {#toolbar}

A barra de ferramentas da tela fornece opções para manipular facilmente as atividades e navegar na tela:

![](assets/orchestrated-toolbar.png)

![Ícone do modo de seleção múltipla](assets/do-not-localize/canvas-multiple.svg) Selecione várias atividades para excluí-las de uma vez ou copie-as e cole-as. [Saiba como copiar e colar atividades](#copy)

![Ícone Girar](assets/do-not-localize/canvas-rotate.svg) Alterne a tela verticalmente.

![Ícone Ajustar à tela](assets/do-not-localize/canvas-fit.svg) Adapte o nível de zoom da tela à tela.

![Ícone de menos zoom](assets/do-not-localize/canvas-zoomout.svg) ![Ícone de mais zoom](assets/do-not-localize/canvas-zoomin.svg) Menos zoom ou na tela.

![Ícone de configurações do Campaign](assets/do-not-localize/canvas-map.svg) Abre um instantâneo da tela mostrando que você está localizado.

### Gerenciar atividades {#manage}

Ao adicionar atividades, os botões de ação ficam disponíveis no painel de propriedades, permitindo que você execute várias operações.

![](assets/activity-action.png)

![Ícone Excluir](assets/do-not-localize/activity-delete.svg) Exclua a atividade da tela.

![Ícone Desabilitar](assets/do-not-localize/activity-disable.svg) ![Ícone Habilitar](assets/do-not-localize/activity-enable.svg) Desabilitar/Habilitar a atividade. Quando a campanha orquestrada é executada, as atividades desabilitadas e as atividades a seguir no mesmo caminho não são executadas e a campanha orquestrada é interrompida.

![Ícone de Pausar](assets/do-not-localize/activity-pause.svg) ![Ícone Retomar](assets/do-not-localize/activity-resume.svg) Pausar/Retomar a atividade. Quando a campanha orquestrada é executada, ela é pausada na atividade pausada. A tarefa correspondente, bem como todas as que a seguem no mesmo caminho, não são executadas.

    Você pode usar qualquer atividade na tela como um ponto de interrupção para pausar a execução da campanha. Isso significa que a campanha será executada somente até essa atividade e, em seguida, pausará a execução. Ao pausar a execução, o mecanismo de segmentação mantém os dados temporários disponíveis para visualização. É possível selecionar a transição de entrada antes da atividade pausada para visualizar os dados transportados. Saiba mais nesta seção: [Monitoramento de fluxo visual](../orchestrated/start-monitor-campaigns.md#flow).

![Ícone Copiar](assets/do-not-localize/activity-copy.svg) Copiar a atividade. [Saiba como copiar e colar atividades](#copy)

![Ícone de logs e tarefas](assets/do-not-localize/activity-logs.svg) Acesse os logs e tarefas da atividade.

Várias atividades de **Direcionamento**, como **Combinar** ou **Desduplicação**, permitem processar a população restante e incluí-la em uma transição de saída adicional. Por exemplo, se você estiver usando uma atividade **Split**, o complemento consiste na população que não corresponde a nenhum dos subconjuntos definidos anteriormente. Para usar este recurso, ative a opção **[!UICONTROL Gerar complemento]**.

### Atividades de copiar e colar {#copy}

Você pode copiar atividades e colá-las em qualquer tela de campanha orquestrada. A campanha de destino pode estar em uma guia do navegador diferente.

* Para copiar uma atividade, clique no botão ![Copiar ícone](assets/do-not-localize/activity-copy.svg) no painel de propriedades da atividade.
* Para copiar várias atividades, clique no ícone ![Modo de seleção múltipla](assets/do-not-localize/canvas-multiple.svg) na barra de ferramentas da tela.

| Copiar uma atividade | Copiar várias atividades |
|  ---  |  ---  |
| ![](assets/orchestrated-copy-1.png){width="200" align="center" zoomable="yes"} | ![](assets/orchestrated-copy-2.png){width="200" align="center" zoomable="yes"} |

Para colar as atividades, clique no botão **+** em uma transição e selecione &quot;Colar atividade x&quot;.

![](assets/orchestrated-copy-3.png){zoomable="yes"}{width="50%"}

## Exemplo de diagrama {#example}

Este é um exemplo de campanha orquestrada criado para enviar um email a todos os clientes que fizeram uma compra de pelo menos 100$, enquanto exclui todos os clientes que têm menos de 50 pontos de fidelidade.

![](assets/canvas-example-diagram.png){zoomable="yes"}

Para isso, as atividades abaixo foram adicionadas:

* Uma atividade **[!UICONTROL Fork]** divide a campanha orquestrada em três caminhos.
* As atividades de **[!UICONTROL criação de público-alvo]** visam os três conjuntos de clientes:

   * Clientes com um email,
   * Clientes que tenham feito uma compra de pelo menos 100$,
   * Clientes com menos de 50 pontos de fidelidade.

* Uma atividade **[!UICONTROL Combinar]** agrupa clientes com um email e aqueles que fizeram uma compra de pelo menos 100$,
* Uma atividade **[!UICONTROL Combine]** exclui clientes com menos de 50 pontos de fidelidade,
* Uma atividade de **[!UICONTROL Entrega de email]** envia um email para os clientes resultantes.

## Próximas etapas {#next}

Depois de criar com sucesso o diagrama de campanha orquestrada, você pode executar a campanha orquestrada e acompanhar o progresso de suas várias tarefas. [Saiba como iniciar uma campanha orquestrada e monitorar sua execução](start-monitor-campaigns.md)
