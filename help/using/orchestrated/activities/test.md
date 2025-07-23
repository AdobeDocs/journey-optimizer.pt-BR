---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade Testar nas suas campanhas orquestradas
description: Saiba como usar a atividade Testar
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: edd70849-0a21-45f2-91f3-4774a0cad9dd
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 91%

---

# Testar {#test}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test"
>title="Atividade de teste"
>abstract="A atividade **Teste** é uma atividade de **Controle de fluxo**. Ela permite habilitar transições com base nas condições especificadas."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test_conditions"
>title="Condições"
>abstract="A atividade **Teste** pode ter várias transições de saída. Durante a execução da campanha orquestrada, cada condição é testada sequencialmente até que uma delas seja satisfeita. Se nenhuma das condições for atendida, a campanha orquestrada continuará com base na **[!UICONTROL Condição padrão]**. Se nenhuma condição padrão for ativada, a campanha orquestrada será interrompida nesse ponto."

+++ Índice 

| Bem-vindo(a) às campanhas orquestradas | Lançar a sua primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](../gs-orchestrated-campaigns.md)<br/><br/>Criar e gerenciar Esquemas e Conjuntos de Dados relacionais:</br> <ul><li>[Introdução a Esquemas e Conjuntos de Dados](../gs-schemas.md)</li><li>[Esquema manual](../manual-schema.md)</li><li>[Esquema de carregamento de arquivo](../file-upload-schema.md)</li><li>[Assimilar dados](../ingest-data.md)</li></ul>[Acessar e gerenciar campanhas orquestradas](../access-manage-orchestrated-campaigns.md) | [Etapas principais para criar uma campanha orquestrada](../gs-campaign-creation.md)<br/><br/>[Criar e programar a campanha](../create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](../orchestrate-activities.md)<br/><br/>[Iniciar e monitorar a campanha](../start-monitor-campaigns.md)<br/><br/>[Geração de relatórios](../reporting-campaigns.md) | [Trabalhar com o construtor de regras](../orchestrated-rule-builder.md)<br/><br/>[Criar a sua primeira consulta](../build-query.md)<br/><br/>[Editar expressões](../edit-expressions.md)<br/><br/>[Redirecionamento](../retarget.md) | [Introdução às atividades](about-activities.md)<br/><br/>Atividades:<br/>[Associação](and-join.md) - [Criar público-alvo](build-audience.md) - [Mudar dimensão](change-dimension.md) - [Atividades de canal](channels.md) - [Combinar](combine.md) - [Desduplicação](deduplication.md) - [Enriquecimento](enrichment.md) - [Bifurcação](fork.md) - [Reconciliação](reconciliation.md) - [Salvar público-alvo](save-audience.md) - [Divisão](split.md) - [Aguardar](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

O conteúdo desta página não é final e pode estar sujeito a alterações.

>[!ENDSHADEBOX]

A atividade **[!UICONTROL Teste]** é uma atividade de **[!UICONTROL Controle de fluxo]**. Ela permite habilitar transições com base nas condições especificadas.

## Configurar a atividade Testar {#test-configuration}

Siga estas etapas para configurar a atividade **[!UICONTROL Testar]**:

1. Adicione uma atividade **[!UICONTROL Testar]** à sua campanha orquestrada.

1. Por padrão, a atividade **[!UICONTROL Testar]** apresenta um teste booleano simples. Se a condição definida na transição “Verdadeira” for satisfeita, essa transição será ativada. Caso contrário, uma transição padrão “Falsa” será ativada.

1. Para configurar a condição associada a uma transição, clique no ícone de **[!UICONTROL Abrir caixa de diálogo de personalização]**. Use o editor de expressão para definir as regras necessárias para ativar essa transição. Você também pode utilizar variáveis de evento, condições e funções de data/hora.

   Além disso, você pode modificar o campo **[!UICONTROL Rótulo]** para personalizar o nome da transição na tela dae campanha orquestrada.

   ![](../assets/workflow-test-default.png)

1. Você pode adicionar várias transições de saída a uma atividade **[!UICONTROL Testar]**. Para isso, clique no botão **[!UICONTROL Adicionar condição]** e configure o rótulo e a condição associada para cada transição.
v
1. Durante a execução da campanha orquestrada, cada condição é testada sequencialmente até que uma delas seja satisfeita. Se nenhuma das condições for satisfeita, a campanha orquestrada continuará com base na **[!UICONTROL Condição padrão]**. Se nenhuma condição padrão for ativada, os fluxos de trabalho serão interrompidos nesse ponto.

## Exemplo {#example}

Neste exemplo, transições diferentes são ativadas com base no número de perfis direcionados por uma atividade **[!UICONTROL Criar público-alvo]**:

* Se mais de 10 mil perfis forem direcionados, uma mensagem de email será enviada.
* No caso de mil a 10 mil perfis, um SMS será enviado.
* Se os perfis direcionados ficarem abaixo de mil, eles serão direcionados a uma transição de “não entrar em contato”.

![](../assets/workflow-test-example.png)

Para isso, a variável de evento `vars.recCount` foi utilizada nas condições de “email” e “sms” para contar o número de perfis direcionados e ativar a transição apropriada.

![](../assets/workflow-test-example-config.png)
