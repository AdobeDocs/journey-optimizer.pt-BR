---
solution: Journey Optimizer
product: journey optimizer
title: Trabalhar com atividades da campanha orquestrada
description: Saiba como orquestrar as atividades da campanha
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 02f986b2-8200-4e0e-8918-44e528a6a3ec
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 91%

---

# Sobre atividades da campanha orquestrada {#orchestrated-campaign-activities}


+++ Índice 

| Bem-vindo(a) às campanhas orquestradas | Lançar a sua primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](../gs-orchestrated-campaigns.md)<br/><br/>Criar e gerenciar Esquemas e Conjuntos de Dados relacionais:</br> <ul><li>[Introdução a Esquemas e Conjuntos de Dados](../gs-schemas.md)</li><li>[Esquema manual](../manual-schema.md)</li><li>[Esquema de carregamento de arquivo](../file-upload-schema.md)</li><li>[Assimilar dados](../ingest-data.md)</li></ul>[Acessar e gerenciar campanhas orquestradas](../access-manage-orchestrated-campaigns.md) | [Etapas principais para criar uma campanha orquestrada](../gs-campaign-creation.md)<br/><br/>[Criar e programar a campanha](../create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](../orchestrate-activities.md)<br/><br/>[Iniciar e monitorar a campanha](../start-monitor-campaigns.md)<br/><br/>[Geração de relatórios](../reporting-campaigns.md) | [Trabalhar com o construtor de regras](../orchestrated-rule-builder.md)<br/><br/>[Criar a sua primeira consulta](../build-query.md)<br/><br/>[Editar expressões](../edit-expressions.md)<br/><br/>[Redirecionamento](../retarget.md) | <b>[Introdução às atividades](about-activities.md)</b><br/><br/>Atividades:<br/>[Associação](and-join.md) - [Criar público-alvo](build-audience.md) - [Mudar dimensão](change-dimension.md) - [Atividades de canal](channels.md) - [Combinar](combine.md) - [Desduplicação](deduplication.md) - [Enriquecimento](enrichment.md) - [Bifurcação](fork.md) - [Reconciliação](reconciliation.md) - [Salvar público-alvo](save-audience.md) - [Divisão](split.md) - [Aguardar](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

O conteúdo desta página não é final e pode estar sujeito a alterações.

>[!ENDSHADEBOX]

As atividades da campanha orquestrada são agrupadas em três categorias. Dependendo do contexto, as atividades disponíveis podem ser diferentes.

Todas as atividades estão detalhadas nas seções abaixo:

* [Atividades de direcionamento](#targeting)
* [Atividades de canal](#channel)
* [Atividades de controle do fluxo](#flow-control)

![Lista de atividades disponíveis na tela](../assets/orchestrated-activities.png){width="80%" align="left"}

## Atividades de direcionamento {#targeting}

Estas atividades são especificamente para direcionamento. Elas permitem criar uma ou mais direções definindo um público-alvo e dividindo ou combinando esses públicos-alvo usando operações de interseção, união ou exclusão.

![Lista de atividades de direcionamento](../assets/targeting-activities.png){width="40%" align="left"}

* [Criar público-alvo](build-audience.md): defina a sua população-alvo. Você pode selecionar um público-alvo já existente ou usar o modelador de consultas para definir a sua própria consulta.
* [Mudar dimensão](change-dimension.md): altere a dimensão de direcionamento ao criar a sua campanha orquestrada.
* [Combinar](combine.md): aplique uma segmentação à sua população de entrada. Você pode usar uma união, uma interseção ou uma exclusão.
* [Desduplicação](deduplication.md): exclua duplicatas no(s) resultado(s) das atividades de entrada.
* [Enriquecimento](enrichment.md): defina dados adicionais para processar na sua campanha orquestrada. Com essa atividade, você pode aproveitar a transição de entrada e configurar a atividade para concluir a transição de saída com dados adicionais.
* [Reconciliação](reconciliation.md): defina o vínculo entre os dados do Journey Optimizer e os dados de uma tabela de trabalho, como, por exemplo, dados carregados de um arquivo externo.
* [Divisão](split.md): segmente a população de entrada em vários subconjuntos.

## Atividades de canal {#channel}

O Adobe Journey Optimizer permite automatizar e executar campanhas de marketing em diversos canais. É possível combinar atividades de canal na tela para criar uma campanha orquestrada entre canais que pode iniciar ações com base no comportamento do cliente. As seguintes atividades de **Canal** estão disponíveis: email e SMS. [Saiba como criar uma ação de canal no contexto de uma campanha orquestrada](channels.md).

## Atividades de controle do fluxo {#flow-control}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_end"
>title="Atividade de término"
>abstract="A Atividade de **término** permite marcar graficamente o fim de uma campanha orquestrada. Essa atividade não tem impacto funcional e, portanto, é opcional."

![Lista de atividades de controle do fluxo](../assets/flow-control-activities.png){width="30%" align="left"}

As atividades a seguir são especificamente para organizar e executar campanhas orquestradas. Sua principal tarefa é coordenar as outras atividades:

* [Associação](and-join.md): sincronize várias ramificações de execução de uma campanha orquestrada.
* [Bifurcação](fork.md): crie transições de saída para iniciar várias atividades ao mesmo tempo.
* [Aguardar](wait.md): pause momentaneamente a execução de parte de uma campanha orquestrada.
  <!--* [Test](test.md): Enable transitions based on specified conditions.-->

>[!NOTE]
>A atividade **Finalizar** marca graficamente o fim de uma campanha orquestrada. Esta atividade não tem nenhum impacto funcional e, portanto, é opcional
