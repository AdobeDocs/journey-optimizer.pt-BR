---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade Change dimension
description: Saiba como usar a atividade Change dimension
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
source-git-commit: 779c90f0be57749a63da103d18cc642106c5f837
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 25%

---

# Mudar dimensão {#change-dimension}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_dimension_complement"
>title="Gerar um complemento"
>abstract="É possível gerar uma transição de saída adicional com a população restante, que foi excluída como uma duplicata. Para fazer isso, ative a opção **Gerar complemento**"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_change_dimension"
>title="Atividade Mudar dimensão"
>abstract="Essa atividade permite alterar a dimensão de direcionamento à medida que você constrói um público-alvo. Ela desloca o eixo dependendo do modelo de dados e da dimensão de entrada. Por exemplo, você pode mudar da dimensão “contratos” para a dimensão “clientes”."

+++ Sumário

| Bem-vindo às campanhas orquestradas | Lançar a primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](../gs-orchestrated-campaigns.md)<br/><br/>[Etapas de configuração](../configuration-steps.md)<br/><br/>[Acessar e gerenciar campanhas orquestradas](../access-manage-orchestrated-campaigns.md) | [Etapas principais para criar uma campanha orquestrada](../gs-campaign-creation.md)<br/><br/>[Criar e agendar a campanha](../create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](../orchestrate-activities.md)<br/><br/>[Iniciar e monitorar a campanha](../start-monitor-campaigns.md)<br/><br/>[Relatórios](../reporting-campaigns.md) | [Trabalhar com o construtor de regras](../orchestrated-rule-builder.md)<br/><br/>[Criar a primeira consulta](../build-query.md)<br/><br/>[Editar expressões](../edit-expressions.md)<br/><br/>[Redirecionamento](../retarget.md) | [Introdução às atividades](about-activities.md)<br/><br/>Atividades:<br/>[And-join](and-join.md) - [Criar público](build-audience.md) - <b>[Alterar dimensão](change-dimension.md)</b> - [Atividades de canal](channels.md) - [Combinar](combine.md) - [Desduplicação](deduplication.md) - [Enriquecimento](enrichment.md) - [Bifurcação](fork.md) - [Reconciliação](reconciliation.md) - [Salvar público](save-audience.md) - [Divisão](split.md) - [Espera](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

Documentação em andamento

>[!ENDSHADEBOX]

Como profissional de marketing, você pode aprimorar a segmentação de público mudando de uma entidade de dados para uma relacionada em uma campanha orquestrada. Isso permite ir além dos perfis de usuário e se concentrar em comportamentos específicos, como compras, reservas ou outras interações.

Para fazer isso, use a atividade **[!UICONTROL Change dimension]**. Ele permite ajustar o targeting dimension durante a campanha orquestrada.

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.-->

## Configurar a atividade Change dimension {#configure}

Siga estas etapas para configurar a atividade **[!UICONTROL Alterar dimensão]**:

1. Adicione uma atividade **[!UICONTROL Change dimension]** à sua campanha orquestrada.

   ![](../assets/orchestrated-change-dimension.png)

1. Defina a **[!UICONTROL Nova dimensão de destino]**. Durante a alteração de dimensão, todos os registros são mantidos.


## Exemplo {#example}

Esse caso de uso se concentra no envio de um SMS para perfis que criaram uma lista de desejos no mês passado.

Comece com uma atividade **[!UICONTROL Criar público-alvo]**, usando a dimensão de direcionamento **[!UICONTROL Lista de desejos]** para identificar todas as listas de desejos relevantes.

Em seguida, adicione uma atividade **[!UICONTROL Change dimension]** para alternar o targeting dimension de **[!UICONTROL Wishlist]** para **[!UICONTROL Recipient].** Essa etapa garante que a campanha orquestrada segmente os perfis corretos vinculados a essas listas de desejos, permitindo que o SMS seja enviado aos perfis pretendidos.

![](../assets/orchestrated-change-dimension-example.png)
