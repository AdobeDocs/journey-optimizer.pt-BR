---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade AND-join
description: Saiba como usar a atividade AND-join em uma campanha orquestrada
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 1b99313e-f131-44f7-a129-f85e1977fb05
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 34%

---

# AND-join {#join}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join"
>title="Atividade AND-join"
>abstract="A Atividade **AND-join** permite sincronizar várias ramificações de execução de uma campanha orquestrada. Ela é acionada quando todas as atividades anteriores forem concluídas. Isso permite que você se certifique de que determinadas atividades foram concluídas antes de continuar a execução da campanha orquestrada."


+++ Sumário

| Bem-vindo às campanhas orquestradas | Lançar a primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](../gs-orchestrated-campaigns.md)<br/><br/>Criar e gerenciar Esquemas e Conjuntos de Dados relacionais:</br> <ul><li>[Introdução a Esquemas e Conjuntos de Dados](../gs-schemas.md)</li><li>[Esquema manual](../manual-schema.md)</li><li>[Esquema de carregamento de arquivo](../file-upload-schema.md)</li><li>[Assimilar dados](../ingest-data.md)</li></ul>[Acessar e gerenciar campanhas orquestradas](../access-manage-orchestrated-campaigns.md) | [Etapas principais para criar uma campanha orquestrada](../gs-campaign-creation.md)<br/><br/>[Criar e agendar a campanha](../create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](../orchestrate-activities.md)<br/><br/>[Iniciar e monitorar a campanha](../start-monitor-campaigns.md)<br/><br/>[Relatórios](../reporting-campaigns.md) | [Trabalhar com o construtor de regras](../orchestrated-rule-builder.md)<br/><br/>[Criar a primeira consulta](../build-query.md)<br/><br/>[Editar expressões](../edit-expressions.md)<br/><br/>[Redirecionamento](../retarget.md) | [Introdução às atividades](about-activities.md)<br/><br/>Atividades:<br/><b>[And-join](and-join.md)</b> - [Criar público](build-audience.md) - [Alterar dimensão](change-dimension.md) - [Atividades de canal](channels.md) - [Combinar](combine.md) - [Desduplicação](deduplication.md) - [Enriquecimento](enrichment.md) - [Bifurcação](fork.md) - [Reconciliação](reconciliation.md) - [Salvar público](save-audience.md) - [Divisão](split.md) - [Espera](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

O conteúdo desta página não é final e pode estar sujeito a alterações.

>[!ENDSHADEBOX]

A atividade **[!UICONTROL AND-join]** é uma atividade de **[!UICONTROL Controle de fluxo]**. Ele permite sincronizar várias ramificações de execução de uma campanha orquestrada.

Essa atividade só acionará a transição de saída depois que todas as transições de entrada estiverem ativadas, ou seja, depois que todas as atividades anteriores estiverem concluídas. Isso permite verificar se determinadas atividades foram concluídas antes de continuar a executar a campanha orquestrada.

## Configurar a atividade AND-join{#and-join-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join_merging"
>title="Opções de mesclagem"
>abstract="Selecione de quais atividades deseja juntar. No menu suspenso **Conjunto principal**, escolha a população de transição de entrada que deseja manter."

Siga estas etapas para configurar a atividade **[!UICONTROL AND-join]**:

![](../assets/workflow-andjoin.png)

1. Adicione várias atividades, como atividades de canal, para criar pelo menos duas ramificações de execução distintas.

1. Insira uma atividade **[!UICONTROL AND-join]** em uma das ramificações.

1. Na seção **[!UICONTROL Opções de mesclagem]**, selecione todas as atividades anteriores nas quais deseja ingressar.

1. No menu suspenso **[!UICONTROL Conjunto principal]**, escolha a população de transição de entrada que deseja manter.

## Exemplo{#and-join-example}

Este exemplo ilustra duas ramificações de campanha coordenadas, cada uma com um delivery de email, um direcionando membros gold e o outro silver. O **[!UICONTROL AND-join]** é ativado assim que ambas as transições de entrada são acionadas e o SMS é enviado somente após a conclusão de ambas as entregas de email, seguindo um atraso de 7 dias.

![](../assets/workflow-andjoin-example.png){zoomable="yes"}
