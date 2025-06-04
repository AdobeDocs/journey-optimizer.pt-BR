---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade de reconciliação
description: Saiba como usar a atividade de Reconciliação em uma campanha orquestrada
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 0d5cfffe-bc6c-40bc-b3e1-5b44368ac76f
source-git-commit: 2935e611bb9682256a324485b28e7dd2552e1dd2
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 42%

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

| Bem-vindo às campanhas orquestradas | Iniciar sua primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](gs-orchestrated-campaigns.md)<br/><br/>[Etapas de configuração](configuration-steps.md)<br/><br/>[Etapas principais para a criação de campanhas orquestradas](gs-campaign-creation.md) | [Criar uma campanha orquestrada](create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](orchestrate-activities.md)<br/><br/>[Enviar mensagens com campanhas orquestradas](send-messages.md)<br/><br/>[Iniciar e monitorar a campanha](start-monitor-campaigns.md)<br/><br/>[Relatórios](reporting-campaigns.md) | [Trabalhar com o Query Modeler](orchestrated-query-modeler.md)<br/><br/>[Criar sua primeira consulta](build-query.md)<br/><br/>[Editar expressões](edit-expressions.md) | [Introdução às atividades](activities/about-activities.md)<br/><br/>Atividades:<br/>[And-join](activities/and-join.md) - [Criar público](activities/build-audience.md) - [Alterar dimensão](activities/change-dimension.md) - [Combinar](activities/combine.md) - [Eliminação de Duplicação](activities/deduplication.md) - [Enriquecimento](activities/enrichment.md) - [Bifurcação](activities/fork.md) - [Reconciliação](activities/reconciliation.md) - [Divisão](activities/split.md) - [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/><br/>

A atividade **Reconciliation** é uma atividade **Targeting** que permite definir o vínculo entre os dados no Adobe Journey Optimizer e os dados em uma tabela de trabalho, por exemplo, dados carregados de um arquivo externo.

## Práticas recomendadas {#reconciliation-best-practices}

Embora a atividade **Enrichment** permita a definição de dados adicionais para serem processados na campanha orquestrada (você pode usar uma atividade **Enrichment** para combinar dados provenientes de vários conjuntos ou para criar links para um recurso temporário), a atividade **Reconciliation** permite vincular dados não identificados aos recursos existentes.

>[!NOTE]
>A operação de reconciliação implica que os dados das dimensões vinculadas já estão no banco de dados.  Por exemplo, se você importar um arquivo de compras que mostre qual produto foi comprado, em que momento, por qual cliente, etc., o produto e o cliente já deverão existir no banco de dados.

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

Siga estas etapas para configurar a atividade **Reconciliação**:

1. Adicione uma atividade de **Reconciliação** à campanha orquestrada.

1. Selecione a nova dimensão de direcionamento. Uma dimensão permite definir a população direcionada: recipients, assinantes de aplicativos, operadores, assinantes, etc.

1. Selecione os campos a serem usados para a reconciliação. É possível usar um ou mais critérios de reconciliação.

   1. Para usar atributos para reconciliar dados, selecione a opção **Atributos simples**. O campo **Source** lista os campos disponíveis na transição de entrada, que devem ser reconciliados. O campo **Destination** corresponde aos campos da targeting dimension selecionada. Os dados são reconciliados quando a origem e o destino são iguais. Por exemplo, selecione os campos **Email** para desduplicar perfis com base em seus endereços de email.

      Para adicionar outro critério de reconciliação, clique no botão **Adicionar regra**. Se várias condições de associação forem especificadas, TODAS elas deverão ser verificadas para que os dados possam ser vinculados.

      ![](../assets/workflow-reconciliation-criteria.png)

   1. Para usar outros atributos para reconciliar dados, selecione a opção **Condições avançadas de reconciliação**. Em seguida, você pode criar sua própria condição de reconciliação usando o modelador de consultas.

1. Você pode filtrar dados para reconciliar usando o botão **Criar filtro**. Isso permite criar uma condição personalizada usando o modelador de consultas.

Por padrão, os dados não reconciliados são mantidos na transição de saída e disponibilizados na tabela de trabalho para uso futuro. Para remover dados não reconciliados, desative a opção **Manter dados não reconciliados**.
