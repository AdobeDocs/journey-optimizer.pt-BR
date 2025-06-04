---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade Change dimension
description: Saiba como usar a atividade Change dimension
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
source-git-commit: c46c202d68613f08e2d2b23ea882fb6561669b08
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 19%

---

# Mudar dimensão {#change-dimension}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_dimension_complement"
>title="Gerar um complemento"
>abstract="É possível gerar uma transição de saída adicional com a população restante, que foi excluída como uma duplicata. Para fazer isso, ative a opção **Gerar complemento**"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_change_dimension"
>title="Atividade Mudar dimensão"
>abstract="Essa atividade permite alterar o targeting dimension à medida que você constrói um público-alvo. Ela desloca o eixo dependendo do modelo de dados e da dimensão de entrada. Por exemplo, você pode mudar da dimensão “contratos” para a dimensão “clientes”."

+++ Sumário

| Bem-vindo às campanhas orquestradas | Iniciar sua primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](../gs-orchestrated-campaigns.md)<br/><br/>[Etapas de configuração](../configuration-steps.md)<br/><br/>[Etapas principais para a criação de campanhas orquestradas](../gs-campaign-creation.md) | [Criar uma campanha orquestrada](../create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](../orchestrate-activities.md)<br/><br/>[Enviar mensagens com campanhas orquestradas](../send-messages.md)<br/><br/>[Iniciar e monitorar a campanha](../start-monitor-campaigns.md)<br/><br/>[Relatórios](../reporting-campaigns.md) | [Trabalhar com o Query Modeler](../orchestrated-query-modeler.md)<br/><br/>[Criar sua primeira consulta](../build-query.md)<br/><br/>[Editar expressões](../edit-expressions.md) | [Introdução às atividades](about-activities.md)<br/><br/>Atividades:<br/>[And-join](and-join.md) - [Criar público](build-audience.md) - [Alterar dimensão](change-dimension.md) - [Combinar](combine.md) - [Eliminação de Duplicação](/deduplication.md) - [Enriquecimento](enrichment.md) - [Bifurcação](fork.md) - [Reconciliação](reconciliation.md) - [Divisão](split.md) - [Espera](wait.md) |

{style="table-layout:fixed"}

+++

<br/><br/>

Como profissional de marketing, você pode alternar o targeting dimension de uma entidade para outra entidade vinculada em uma campanha orquestrada e refinar seu direcionamento de público-alvo com base em diferentes conjuntos de dados, como a mudança de perfis de usuários para direcionamento de ações ou reservas específicas.

Para fazer isso, use a atividade de direcionamento **Change dimension**. Essa atividade permite alterar o targeting dimension à medida que você constrói sua campanha orquestrada. Ele desloca o eixo dependendo do template de dados e da dimensão de entrada.

Por exemplo, você pode alternar o targeting dimension de uma campanha orquestrada de &quot;Perfil&quot; para &quot;Contratos&quot; para enviar mensagens ao proprietário do contrato direcionado.

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.-->

## Configurar a atividade Change dimension {#configure}

Siga estas etapas para configurar a atividade **Alterar dimensão**:

1. Adicione uma atividade **Change dimension** à sua campanha orquestrada.

   ![](../assets/change-dimension.png)

1. Defina a **Nova dimensão de destino**. Durante a alteração de dimensão, todos os registros são mantidos.

1. Execute a campanha orquestrada para ver o resultado. Compare os dados nas tabelas antes e depois da atividade de alteração de dimensão e compare a estrutura das tabelas de campanha orquestradas.

## Exemplo {#example}

Neste exemplo, queremos enviar um delivery de SMS para todos os perfis que fizeram uma compra. Para fazer isso, primeiro usamos uma atividade **[!UICONTROL Build audience]** vinculada a uma dimensão de direcionamento &quot;Purchase&quot; personalizada para direcionar todas as compras que ocorreram.

Em seguida, usamos uma atividade **[!UICONTROL Change dimension]** para alternar a targeting dimension de campanha orquestrada para &quot;Recipients&quot;. Isso nos permite direcionar os recipients que correspondem ao query.

![](../assets/change-dimension-example.png)
