---
solution: Journey Optimizer
product: journey optimizer
title: Trabalhar com atividades de campanha orquestradas
description: Saiba como organizar atividades de campanha
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 02f986b2-8200-4e0e-8918-44e528a6a3ec
source-git-commit: b620d479548791df97912b143e7dbe7557ab4acc
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 32%

---

# Sobre atividades de campanha orquestrada {#ms-campaign-activities}

As atividades de campanha orquestradas são agrupadas em três categorias. Dependendo do contexto, as atividades disponíveis podem ser diferentes.

Todas as atividades estão detalhadas nas seções abaixo:

* [Atividades de direcionamento](#targeting)
* [Atividades do canal](#channel)
* [Atividades de controle de fluxo](#flow-control)

![Lista de atividades disponíveis na tela](../assets/workflow-activities.png){width="80%" align="left"}

## Atividades de direcionamento {#targeting}

Essas atividades são específicas para direcionamento. Elas permitem criar uma ou mais direções definindo um público-alvo e dividindo ou combinando esses públicos-alvo usando operações de interseção, união ou exclusão.

![Lista de atividades de direcionamento](../assets/targeting-activities.png){width="40%" align="left"}

* [Criar público-alvo](build-audience.md): defina sua população de destino. Você pode selecionar um público existente ou usar o modelador de consultas para definir sua própria consulta.
* [Alterar dimensão](change-dimension.md): altere a targeting dimension enquanto você estiver criando sua campanha orquestrada.
* [Combinar](combine.md): executar segmentação na população de entrada. Você pode usar uma união, uma interseção ou uma exclusão.
* [Desduplicação](deduplication.md): excluir duplicados no(s) resultado(s) das atividades de entrada.
* [Enriquecimento](enrichment.md): defina dados adicionais para processar em sua campanha orquestrada. Com essa atividade, você pode aproveitar a transição de entrada e configurar a atividade para concluir a transição de saída com dados adicionais.
* [Reconciliação](reconciliation.md): defina o vínculo entre os dados nos dados do Journey Optimizer e os dados em uma tabela de trabalho, por exemplo, dados carregados de um arquivo externo.
* [Split](split.md): segmente a população de entrada em vários subconjuntos.

## Atividades do canal {#channel}

O Adobe Journey Optimizer permite automatizar e executar campanhas de marketing em vários canais. Você pode combinar atividades de canal na tela para criar uma campanha orquestrada entre canais que pode acionar ações com base no comportamento do cliente. As seguintes atividades do **Canal** estão disponíveis: notificações por push de email, SMS, Android e iOS. [Saiba como criar uma ação de canal no contexto de uma campanha orquestrada](channels.md).

## Atividades de controle de fluxo {#flow-control}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_end"
>title="Atividade de término"
>abstract="A Atividade de **término** permite marcar graficamente o fim de uma campanha orquestrada. Essa atividade não tem impacto funcional e, portanto, é opcional."

![Lista de atividades de controle de fluxo](../assets/flow-control-activities.png){width="30%" align="left"}

As atividades a seguir são específicas para organizar e executar campanhas orquestradas. Sua principal tarefa é coordenar as outras atividades:

* [And-join](and-join.md): sincroniza várias ramificações de execução de uma campanha orquestrada.
* [Bifurcação](fork.md): crie transições de saída para iniciar várias atividades ao mesmo tempo.
  <!--* [Test](test.md): Enable transitions based on specified conditions.-->
* [Aguardar](wait.md): pausar momentaneamente a execução de uma parte de uma campanha orquestrada.

>[!NOTE]
>A atividade **End** marca graficamente o fim de uma campanha orquestrada. Esta atividade não tem impacto funcional e, portanto, é opcional
