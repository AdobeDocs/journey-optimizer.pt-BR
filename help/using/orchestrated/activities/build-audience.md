---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade Criar público-alvo
description: Saiba como usar a atividade Criar público-alvo em uma campanha orquestrada
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 3959b5fa-0c47-42a5-828f-4d7ca9b7e72d
source-git-commit: 6439be00315dfde7ab385d7f848b7031d95060f4
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 27%

---

# Criar público-alvo {#build-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience"
>title="Atividade Criar público-alvo"
>abstract="A atividade **Criar público-alvo** permite definir o público-alvo que entrará na campanha orquestrada. Ao enviar mensagens no contexto de uma campanha orquestrada, o público-alvo da mensagem não é definido na atividade de canal, mas em uma atividade **Criar público-alvo**."

+++ Sumário

| Bem-vindo às campanhas orquestradas | Lançar a primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](gs-orchestrated-campaigns.md)<br/><br/>[Etapas de configuração](configuration-steps.md)<br/><br/>[Acessar e gerenciar campanhas orquestradas](access-manage-orchestrated-campaigns.md) | [Etapas principais para a criação de campanha orquestrada](gs-campaign-creation.md)<br/><br/>[Criar e agendar a campanha](create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](orchestrate-activities.md)<br/><br/><b>[Iniciar e monitorar a campanha](start-monitor-campaigns.md)</b><br/><br/>[Relatórios](reporting-campaigns.md) | [Trabalhar com o construtor de regras](orchestrated-rule-builder.md)<br/><br/>[Criar a primeira consulta](build-query.md)<br/><br/>[Editar expressões](edit-expressions.md)<br/><br/>[Redirecionamento](retarget.md) | [Introdução às atividades](activities/about-activities.md)<br/><br/>Atividades:<br/>[And-join](activities/and-join.md) - [Criar público](activities/build-audience.md) - [Alterar dimensão](activities/change-dimension.md) - [Atividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Desduplicação](activities/deduplication.md) - [Enriquecimento](activities/enrichment.md) - [Bifurcação](activities/fork.md) - [Reconciliação](activities/reconciliation.md) - [Salvar público](save-audience.md) - [Divisão](activities/split.md) - [Espera](activities/wait.md) |

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
