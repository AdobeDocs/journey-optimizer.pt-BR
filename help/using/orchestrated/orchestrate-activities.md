---
solution: Journey Optimizer
product: journey optimizer
title: Criar campanhas orquestradas com o Adobe Journey Optimizer
description: Saiba como criar campanhas orquestradas com o Adobe Journey Optimizer
exl-id: d1d64125-cf00-49c2-a71d-1494ede16f61
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 56%

---


# Atividades da campanha orquestrada {#orchestrate}

Depois que você tiver [criado uma campanha Orquestrada](gs-campaign-creation.md), poderá começar a orquestrar as diferentes tarefas que ela executará. Para fazer isso, uma tela visual é fornecida, permitindo que você crie um diagrama de campanha Orquestrado. Nesse diagrama, é possível adicionar várias atividades e conectá-las em ordem sequencial.

## Adicionar atividades {#add}

Nessa etapa da configuração, o diagrama é exibido com um ícone de início, representando o início da campanha Orquestrada. Para adicionar a primeira atividade, clique no botão **+** conectado ao ícone de início.

Uma lista de atividades que podem ser adicionadas ao diagrama é exibida. As atividades disponíveis dependem da sua posição no diagrama Campanha orquestrada. Por exemplo, ao adicionar sua primeira atividade, você pode iniciar a campanha Orquestrada direcionando um público-alvo, dividindo o caminho da campanha Orquestrada ou definindo uma atividade **Wait** para atrasar a execução da campanha Orquestrada. Por outro lado, após uma atividade **Criar público-alvo**, você pode refinar seu público-alvo com atividades de direcionamento, enviar uma entrega para seu público com atividades de canal ou organizar o processo Campanha orquestrada com atividades de controle de fluxo.

![](assets/orchestrated-start.png){zoomable="yes"}

Depois que uma atividade é adicionada ao diagrama, aparece um painel à direita, permitindo que você a ajuste com configurações específicas. Informações detalhadas de como configurar cada atividade estão disponíveis [nesta seção](activities/about-activities.md).

![](assets/orchestrated-configure-activities.png){zoomable="yes"}

Repita esse processo para adicionar quantas atividades desejar, dependendo das tarefas que deseja que sua campanha orquestrada execute. Observe que você também pode inserir uma nova atividade entre duas atividades. Para isso, clique no botão **+** na transição entre as atividades, selecione a atividade desejada e configure-a no painel direito.

Você tem a opção de personalizar o nome das transições entre cada atividade. Para isso, selecione a transição e altere seu rótulo no painel direito.

![](assets/canvas-transition.png)

### A barra de ferramentas da tela {#toolbar}

A barra de ferramentas da tela permite manipular facilmente as atividades e navegar pela tela:

![](assets/orchestrated-toolbar.png)

![Ícone do modo de seleção múltipla](assets/do-not-localize/canvas-multiple.svg) Selecione várias atividades para excluí-las de uma vez ou copiá-las e colá-las. [Saiba como usar as atividades de copiar e colar](#copy)

![Ícone de girar](assets/do-not-localize/canvas-rotate.svg) Coloque a tela na vertical.

![Ícone de ajustar à tela](assets/do-not-localize/canvas-fit.svg) Ajuste o nível de zoom da tela conforme a tela atual.

![Ícone de diminuir zoom](assets/do-not-localize/canvas-zoomout.svg) ![Ícone de aumentar zoom](assets/do-not-localize/canvas-zoomin.svg) Diminua ou aumente o zoom na tela.

![Ícone de configurações da campanha](assets/do-not-localize/canvas-map.svg) Abre um instantâneo da tela, mostrando onde você se encontra.

### Gerenciar atividades {#manage}

Ao adicionar atividades, os botões de ação ficam disponíveis no painel de propriedades, permitindo que você execute várias operações.

![](assets/activity-action.png)

![Ícone de excluir](assets/do-not-localize/activity-delete.svg) Exclua a atividade da tela.

![Ícone de desabilitar](assets/do-not-localize/activity-disable.svg) ![Ícone de habilitar](assets/do-not-localize/activity-enable.svg) Desabilite/habilite a atividade. Quando a campanha Orquestrada é executada, as atividades desativadas e as atividades a seguir no mesmo caminho não são executadas e a campanha Orquestrada é interrompida.

![Ícone de pausar](assets/do-not-localize/activity-pause.svg) ![Ícone de retomar](assets/do-not-localize/activity-resume.svg) Pause/retome a atividade. Quando a campanha Orquestrada é executada, ela pausa na atividade pausada. A tarefa correspondente e todas as seguintes no mesmo caminho não são executadas.

Você pode usar qualquer atividade na tela como um ponto de interrupção para pausar a execução da campanha. Isso significa que a campanha será executada somente até essa atividade e, em seguida, pausará a execução. Ao pausar a execução, o mecanismo de segmentação mantém os dados temporários disponíveis para visualização. É possível selecionar a transição de entrada antes da atividade pausada para visualizar os dados transportados. Saiba mais nesta seção: [Monitoramento de fluxo visual](../orchestrated/start-monitor-campaigns.md#flow)

![Ícone de copiar](assets/do-not-localize/activity-copy.svg) Copie a atividade. [Saiba como usar as atividades de copiar e colar](#copy)

![Ícone de logs e tarefas](assets/do-not-localize/activity-logs.svg) Acesse os logs e tarefas da atividade.

Várias atividades de **Direcionamento**, como **Combinar** ou **Desduplicação**, permitem processar a população restante e incluí-la em uma transição de saída adicional. Por exemplo, se você estiver usando uma atividade **Divisão**, o complemento consiste na população que não correspondeu a nenhum dos subconjuntos definidos anteriormente. Para usar este recurso, ative a opção **[!UICONTROL Gerar complemento]**.

### Atividades de copiar e colar {#copy}

Você pode copiar atividades e colá-las em qualquer tela de campanha orquestrada. A campanha de destino pode estar em uma guia do navegador diferente.

* Para copiar uma atividade, clique no botão do ![Ícone de copiar](assets/do-not-localize/activity-copy.svg), no painel de propriedades da atividade.
* Para copiar mais de uma atividade, clique no ![Ícone de modo de seleção múltipla](assets/do-not-localize/canvas-multiple.svg), na barra de ferramentas da tela.

| Copiar uma atividade | Copiar várias atividades |
|  ---  |  ---  |
| ![](assets/orchestrated-copy-1.png){width="200" align="center" zoomable="yes"} | ![](assets/orchestrated-copy-2.png){width="200" align="center" zoomable="yes"} |

Para colar as atividades, clique no botão **+** em uma transição e selecione “Colar atividade x”.

![](assets/orchestrated-copy-3.png){zoomable="yes"}{width="50%"}

## Exemplo de diagrama {#example}

Este é um exemplo de campanha orquestrada criada para enviar um email a todos os clientes que fizeram uma compra de pelo menos 100$, enquanto exclui todos os clientes que têm menos de 50 pontos de fidelidade.

![](assets/canvas-example-diagram.png){zoomable="yes"}

Para isso, as atividades abaixo foram adicionadas:

* Uma atividade **[!UICONTROL Fork]** divide a campanha Orquestrada em três caminhos.
* As atividades **[!UICONTROL Criar público-alvo]** dirigem-se aos três conjuntos de clientes:

   * Clientes com um email,
   * Clientes que fizeram uma compra de pelo menos USD 100,
   * Clientes que têm menos de 50 pontos de fidelidade.

* Uma atividade **[!UICONTROL Combinar]** agrupa os clientes com email e os que fizeram uma compra de pelo menos USD 100,
* Uma atividade **[!UICONTROL Combinar]** exclui os clientes que têm menos de 50 pontos de fidelidade,
* Uma atividade **[!UICONTROL Entrega de email]** envia um email aos clientes resultantes.

## Próximas etapas {#next}

Depois de criar com sucesso o diagrama de campanha Orquestrado, você pode executar a campanha Orquestrada e acompanhar o progresso de suas várias tarefas. [Saiba como iniciar uma campanha Orquestrada e monitorar sua execução](start-monitor-campaigns.md)
