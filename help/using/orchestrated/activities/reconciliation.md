---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade de reconciliação
description: Saiba como usar a atividade de Reconciliação em uma campanha orquestrada
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 0d5cfffe-bc6c-40bc-b3e1-5b44368ac76f
source-git-commit: a19fe429d34a88c6159ab3b2b4dfa3768bcd24ad
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 32%

---

# Reconciliação {#reconciliation}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation"
>title="Atividade de reconciliação"
>abstract="A Atividade **reconciliação** é uma atividade de **direcionamento** que permite definir o vínculo entre o Adobe Journey Optimizer e os dados em uma tabela de trabalho."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_field"
>title="Campo de seleção de reconciliação"
>abstract="Campo de seleção de reconciliação"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_condition"
>title="Condição de criação de reconciliação"
>abstract="Condição de criação de reconciliação"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_complement"
>title="Complemento de geração de reconciliação"
>abstract="Complemento de geração de reconciliação"


+++ Sumário

| Bem-vindo às campanhas orquestradas | Lançar a primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](../gs-orchestrated-campaigns.md)<br/><br/>[Etapas de configuração](../configuration-steps.md)<br/><br/>[Acessar e gerenciar campanhas orquestradas](../access-manage-orchestrated-campaigns.md) | [Etapas principais para criar uma campanha orquestrada](../gs-campaign-creation.md)<br/><br/>[Criar e agendar a campanha](../create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](../orchestrate-activities.md)<br/><br/>[Iniciar e monitorar a campanha](../start-monitor-campaigns.md)<br/><br/>[Relatórios](../reporting-campaigns.md) | [Trabalhar com o construtor de regras](../orchestrated-rule-builder.md)<br/><br/>[Criar a primeira consulta](../build-query.md)<br/><br/>[Editar expressões](../edit-expressions.md)<br/><br/>[Redirecionamento](../retarget.md) | [Introdução às atividades](about-activities.md)<br/><br/>Atividades:<br/>[And-join](and-join.md) - [Criar público](build-audience.md) - [Alterar dimensão](change-dimension.md) - [Atividades de canal](channels.md) - [Combinar](combine.md) - [Desduplicação](deduplication.md) - [Enriquecimento](enrichment.md) - [Bifurcação](fork.md) - <b>[Reconciliação](reconciliation.md)</b> - [Salvar público](save-audience.md) - [Divisão](split.md) - [Espera](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

A atividade **[!UICONTROL Reconciliation]** é uma atividade **[!UICONTROL Targeting]** que permite definir o vínculo entre os dados no Adobe Journey Optimizer e os dados em uma tabela de trabalho, por exemplo, dados carregados de um arquivo externo.

A atividade **[!UICONTROL Enrichment]** permite adicionar dados adicionais à campanha orquestrada, por exemplo, combinando dados de várias fontes ou vinculando a um recurso temporário. Por outro lado, a atividade **[!UICONTROL Reconciliation]** é usada para corresponder dados não identificados ou externos com recursos existentes no banco de dados.

**[!UICONTROL A reconciliação]** requer que os registros relacionados já existam no sistema. Por exemplo, se você importar um arquivo de compra listando produtos, carimbos de data e hora e informações do cliente, os produtos e os clientes já deverão estar presentes no banco de dados para estabelecer o link.

## Configurar a atividade de reconciliação {#reconciliation-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting"
>title="Dimensão de direcionamento"
>abstract="Selecione a nova dimensão de direcionamento. Uma dimensão permite definir a população direcionada: destinatários, assinantes de aplicativos, operadores, assinantes etc. Por padrão, a dimensão de direcionamento atual é selecionada."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_rules"
>title="Regras de reconciliação"
>abstract="Selecione as regras de reconciliação a serem usadas para a desduplicação. Para usar atributos, selecione a opção **Atributos simples** e escolha os campos origem e destino. Para criar sua própria condição de reconciliação usando o modelador de consultas, selecione a opção **Condições de reconciliação avançadas**."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/campaign-web/v8/query-database/query-modeler-overview" text="Trabalhar com o modelador de consultas"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting_selection"
>title="Selecione a dimensão de direcionamento"
>abstract="Selecione a dimensão de direcionamento com a qual seus dados de entrada devem se reconciliar."
>additional-url="https://experienceleague.adobe.com/docs/campaign-web/v8/audiences/gs-audiences-recipients.html?lang=pt-BR#targeting-dimensions" text="Dimensões de direcionamento"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_keep_unreconciled_data"
>title="Manter dados não reconciliados"
>abstract="Por padrão, os dados não reconciliados são mantidos na transição de saída e disponibilizados na tabela de trabalho para uso futuro. Para remover dados não reconciliados, desative a opção **Manter dados não reconciliados**."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_attribute"
>title="Atributo de reconciliação"
>abstract="Selecione o atributo a ser usado para reconciliar dados e clique em Confirmar."

Siga estas etapas para configurar a atividade **[!UICONTROL Reconciliação]**:

1. Adicione uma atividade de **[!UICONTROL Reconciliação]** ao seu fluxo de trabalho.

1. Escolha uma nova targeting dimension para definir seu público alvo, como recipients ou assinantes.

1. Defina os campos a serem usados para corresponder seus dados de entrada com perfis existentes.

1. Para corresponder dados usando campos básicos, selecione **[!UICONTROL Atributos simples]**.

1. Defina os campos correspondentes:

   * **[!UICONTROL Source]**: lista os campos de dados de entrada.

   * **[!UICONTROL Destino]**: refere-se aos campos na targeting dimension selecionada.

   Uma correspondência ocorre quando ambos os valores são iguais, por exemplo, correspondendo por **[!UICONTROL Email]** para identificar perfis.

   ![](../assets/workflow-reconciliation-criteria.png)

1. Para adicionar mais regras correspondentes, clique em **[!UICONTROL Adicionar regra]**. Todas as condições devem ser atendidas para que uma correspondência ocorra.

1. Para condições mais complexas, escolha **[!UICONTROL Condições avançadas de reconciliação]**. Use o [modelador de consultas](../orchestrated-rule-builder.md) para definir uma lógica personalizada.

1. Para filtrar quais dados reconciliar, clique em **[!UICONTROL Criar filtro]** e defina sua condição no modelador de consultas.

1. Por padrão, os registros sem correspondência são mantidos na transição de saída e armazenados na tabela de trabalho. Para removê-los, habilite a opção **[!UICONTROL Manter dados não reconciliados]**.

## Exemplo {#example-reconciliation}

Este exemplo usa a atividade **[!UICONTROL Reconciliação]** no Adobe Journey Optimizer para garantir que os emails sejam enviados somente para clientes reconhecidos. Os dados fluem por meio de uma atividade **[!UICONTROL Ler público-alvo]** que direciona os usuários com pedidos anteriores. A atividade **[!UICONTROL Reconciliation]** então corresponde esses dados de entrada aos perfis existentes no banco de dados usando o campo de email.

![](../assets/workflow-reconciliation-sample-1.0.png)
