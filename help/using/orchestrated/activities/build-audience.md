---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade Criar público-alvo
description: Saiba como usar a atividade Criar público-alvo em uma campanha orquestrada
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 3959b5fa-0c47-42a5-828f-4d7ca9b7e72d
source-git-commit: 62f16b6f582e6bf5620b75df4a75d4c15441ca4a
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 24%

---

# Criar público-alvo {#build-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience"
>title="Atividade Criar público-alvo"
>abstract="A atividade **Criar público-alvo** permite definir o público-alvo que entrará na campanha orquestrada. Ao enviar mensagens no contexto de uma campanha orquestrada, o público-alvo da mensagem não é definido na atividade de canal, mas em uma atividade **Criar público-alvo**."


>[!CONTEXTUALHELP]
>id="acw_orchestration_read_audience"
>title="Atividade Criar público-alvo"
>abstract="A atividade **Ler público-alvo** permite selecionar um público-alvo existente que entrará na campanha orquestrada. Ao enviar mensagens no contexto de uma campanha orquestrada, o público da mensagem não é definido na atividade de canal, mas em uma atividade de **Leitura de público** ou de **Criação de público**."


+++ Sumário

| Bem-vindo às campanhas orquestradas | Lançar a primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](../gs-orchestrated-campaigns.md)<br/><br/>[Etapas de configuração](../configuration-steps.md)<br/><br/>[Etapas principais para a criação de campanhas orquestradas](../gs-campaign-creation.md) | [Criar uma campanha orquestrada](../create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](../orchestrate-activities.md)<br/><br/>[Enviar mensagens com campanhas orquestradas](../send-messages.md)<br/><br/>[Iniciar e monitorar a campanha](../start-monitor-campaigns.md)<br/><br/>[Relatórios](../reporting-campaigns.md) | [Trabalhar com o Query Modeler](../orchestrated-rule-builder.md)<br/><br/>[Criar sua primeira consulta](../build-query.md)<br/><br/>[Editar expressões](../edit-expressions.md) | [Introdução às atividades](about-activities.md)<br/><br/>Atividades:<br/>[And-join](and-join.md) - [Criar público](build-audience.md) - [Alterar dimensão](change-dimension.md) - [Combinar](combine.md) - [Eliminação de Duplicação](deduplication.md) - [Enriquecimento](enrichment.md) - [Bifurcação](fork.md) - [Reconciliação](reconciliation.md) - [Divisão](split.md) - [Espera](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Como profissional de marketing, você pode criar segmentos complexos de público-alvo por meio de uma interface intuitiva, permitindo direcionar usuários com base em uma grande variedade de critérios e comportamentos para adaptar suas campanhas com mais eficiência.

Para fazer isso, use a atividade de direcionamento **[!UICONTROL Criar público]**. Essa atividade define o público-alvo que entra na campanha orquestrada. Ao enviar mensagens como parte de uma campanha orquestrada, o público-alvo é definido na atividade **[!UICONTROL Criar público]**, não dentro da campanha orquestrada.

## Configurar a atividade Criar público-alvo {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience_audienceselector"
>title="Público-alvo"
>abstract="Selecione o público-alvo assim como faz ao criar uma nova entrega. "

Siga estas etapas para configurar a atividade **[!UICONTROL Criar público-alvo]**:

1. Adicione uma atividade **[!UICONTROL Criar público-alvo]**.

   ![](../assets/build-audience.png)

1. Defina um **[!UICONTROL Rótulo]**.

1. Configure seu público seguindo as etapas detalhadas nas guias abaixo.

1. Escolha a **[!UICONTROL Dimensão de direcionamento]**. O targeting dimension permite definir a população-alvo da operação: destinatários, beneficiários(as) de contrato, operadores(as), assinantes, etc. Por padrão, o público-alvo é selecionado entre os destinatários.

1. Clique em **[!UICONTROL Continuar]**.

1. Use o modelador de consultas para definir sua consulta. [Saiba mais sobre o modelador de consultas nesta seção](../orchestrated-rule-builder.md)

1. Especifique se uma transição de saída deve ser gerada quando o público-alvo estiver vazio.

## Exemplos{#build-audience-examples}

Este é um exemplo de uma campanha orquestrada com duas atividades **[!UICONTROL Build audience]**. O primeiro é direcionado a perfis que têm itens em seus carrinhos, seguidos por um delivery de email. O segundo é direcionado a perfis com uma lista de desejos, seguido de um delivery de SMS.

![](../assets/build-audience-2.png)
