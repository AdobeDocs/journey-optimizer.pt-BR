---
solution: Journey Optimizer
product: journey optimizer
title: Trabalhar com atividades de campanha orquestradas
description: Saiba como organizar atividades de campanha
exl-id: 02f986b2-8200-4e0e-8918-44e528a6a3ec
source-git-commit: c1201025af216f8f3019e7696b6eb906962b681b
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 66%

---


# Sobre atividades de campanha orquestradas {#orchestrated-campaign-activities}

As atividades da campanha orquestrada são agrupadas em três categorias. Dependendo do contexto, as atividades disponíveis podem ser diferentes.

Todas as atividades estão detalhadas nas seções abaixo:

* [Atividades de direcionamento](#targeting)
* [Atividades de canal](#channel)
* [Atividades de controle do fluxo](#flow-control)

![Lista de atividades disponíveis na tela](../assets/orchestrated-activities.png){width="80%" align="left"}

## Atividades de direcionamento {#targeting}

Estas atividades são especificamente para direcionamento. Elas permitem criar uma ou mais direções definindo um público-alvo e dividindo ou combinando esses públicos-alvo usando operações de interseção, união ou exclusão.

![Lista de atividades de direcionamento](../assets/targeting-activities.png){width="40%" align="left"}

As atividades de direcionamento disponíveis são:

* [Criar público-alvo](build-audience.md): defina a sua população-alvo. Você pode selecionar um público-alvo existente ou usar o criador de regras para definir sua própria consulta.
* [Alterar dimensão](change-dimension.md): altere a targeting dimension enquanto você estiver criando sua campanha Orquestrada.
* [Combinar](combine.md): aplique uma segmentação à sua população de entrada. Você pode usar uma união, uma interseção ou uma exclusão.
* [Desduplicação](deduplication.md): exclua duplicatas no(s) resultado(s) das atividades de entrada.
* [Enriquecimento](enrichment.md): definir dados adicionais para processar em sua campanha Orquestrada. Com essa atividade, você pode aproveitar a transição de entrada e configurar a atividade para concluir a transição de saída com dados adicionais.
* [Reconciliação](reconciliation.md): defina o vínculo entre os dados do Journey Optimizer e os dados de uma tabela de trabalho, como, por exemplo, dados carregados de um arquivo externo.
* [Divisão](split.md): segmente a população de entrada em vários subconjuntos.

## Atividades de canal {#channel}

O Adobe Journey Optimizer permite automatizar e executar campanhas de marketing em diversos canais. Você pode combinar atividades de canal na tela para criar uma campanha orquestrada entre canais que pode acionar ações com base no comportamento do cliente. As seguintes atividades de **Canal** estão disponíveis: email e SMS. [Saiba como criar uma ação de canal no contexto de uma campanha orquestrada](channels.md).

## Atividades de controle do fluxo {#flow-control}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_end"
>title="Atividade de término"
>abstract="A Atividade de **término** permite marcar graficamente o fim de uma campanha orquestrada. Essa atividade não tem impacto funcional e, portanto, é opcional."

As atividades a seguir são específicas para organizar e executar campanhas orquestradas. Sua principal tarefa é coordenar as outras atividades.

![Lista de atividades de controle do fluxo](../assets/flow-control-activities.png){width="20%" align="left"}

As atividades de controle de fluxo disponíveis são:

* [And-join](and-join.md): sincroniza várias ramificações de execução de uma campanha Orquestrada.
* [Bifurcação](fork.md): crie transições de saída para iniciar várias atividades ao mesmo tempo.
* [Aguardar](wait.md): pausar momentaneamente a execução de uma parte de uma campanha Orquestrada.
  <!--* [Test](test.md): Enable transitions based on specified conditions.-->

>[!NOTE]
>A atividade **End** marca graficamente o fim de uma campanha Orquestrada. Esta atividade não tem nenhum impacto funcional e, portanto, é opcional
