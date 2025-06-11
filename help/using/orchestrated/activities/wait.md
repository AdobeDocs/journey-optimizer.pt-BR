---
solution: Journey Optimizer
product: journey optimizer
title: Use a atividade Wait em campanhas orquestradas
description: Saiba como usar a atividade de espera em campanhas orquestradas
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
source-git-commit: d59643f18a335fe1e094156a1cfee65b717b9fce
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 11%

---

# Aguardar {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="Atividade aguardar"
>abstract="A atividade **Aguardar** é usada para atrasar a transição de uma atividade para outra."

+++ Sumário

| Bem-vindo às campanhas orquestradas | Iniciar sua primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](../gs-orchestrated-campaigns.md)<br/><br/>[Etapas de configuração](../configuration-steps.md)<br/><br/>[Etapas principais para a criação de campanhas orquestradas](../gs-campaign-creation.md) | [Criar uma campanha orquestrada](../create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](../orchestrate-activities.md)<br/><br/>[Enviar mensagens com campanhas orquestradas](../send-messages.md)<br/><br/>[Iniciar e monitorar a campanha](../start-monitor-campaigns.md)<br/><br/>[Relatórios](../reporting-campaigns.md) | [Trabalhar com o Query Modeler](../orchestrated-rule-builder.md)<br/><br/>[Criar sua primeira consulta](../build-query.md)<br/><br/>[Editar expressões](../edit-expressions.md) | [Introdução às atividades](about-activities.md)<br/><br/>Atividades:<br/>[And-join](and-join.md) - [Criar público](build-audience.md) - [Alterar dimensão](change-dimension.md) - [Combinar](combine.md) - [Eliminação de Duplicação](deduplication.md) - [Enriquecimento](enrichment.md) - [Bifurcação](fork.md) - [Reconciliação](reconciliation.md) - [Divisão](split.md) - [Espera](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

A atividade **Wait** é um componente **Flow control** usado para introduzir um atraso entre duas atividades em uma campanha orquestrada. Isso ajuda a garantir que suas atividades de acompanhamento sejam mais cronometradas e relevantes para o engajamento do usuário.

Por exemplo, você pode aguardar alguns dias após um delivery de email para rastrear aberturas e cliques antes de enviar uma mensagem de acompanhamento.

## Configuração{#wait-configuration}

Siga estas etapas para configurar a atividade **Aguardar**:

1. Adicione uma atividade **Wait** à campanha orquestrada.

1. Selecione o tipo de espera que melhor atenda às suas necessidades:

   * **Duração**: especifique um atraso em segundos, minutos, horas ou dias antes de prosseguir para a próxima atividade.

   * **Hora fixa**: Defina uma data e hora específicas após as quais a próxima atividade iniciará.

   ![](../assets/wait_activity.png)

## Exemplo{#wait-example}

O exemplo a seguir ilustra a atividade **Wait** em um caso de uso comum.  Um email com um código promocional é enviado para perfis que comemoram seus aniversários. Após 29 dias, um SMS é enviado para o mesmo grupo como um lembrete de que o código promocional de aniversário está prestes a expirar.

![](../assets/wait-example.png)
