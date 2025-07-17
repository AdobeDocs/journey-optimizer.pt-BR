---
solution: Journey Optimizer
product: journey optimizer
title: Use a atividade Wait em campanhas orquestradas
description: Saiba como usar a atividade de espera em campanhas orquestradas
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 12%

---

# Aguardar {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="Atividade aguardar"
>abstract="A atividade **Aguardar** é usada para atrasar a transição de uma atividade para outra."


+++ Sumário

| Bem-vindo às campanhas orquestradas | Lançar a primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](../gs-orchestrated-campaigns.md)<br/><br/>Criar e gerenciar Esquemas e Conjuntos de Dados relacionais:</br> <ul><li>[Introdução a Esquemas e Conjuntos de Dados](../gs-schemas.md)</li><li>[Esquema manual](../manual-schema.md)</li><li>[Esquema de carregamento de arquivo](../file-upload-schema.md)</li><li>[Assimilar dados](../ingest-data.md)</li></ul>[Acessar e gerenciar campanhas orquestradas](../access-manage-orchestrated-campaigns.md) | [Etapas principais para criar uma campanha orquestrada](../gs-campaign-creation.md)<br/><br/>[Criar e agendar a campanha](../create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](../orchestrate-activities.md)<br/><br/>[Iniciar e monitorar a campanha](../start-monitor-campaigns.md)<br/><br/>[Relatórios](../reporting-campaigns.md) | [Trabalhar com o construtor de regras](../orchestrated-rule-builder.md)<br/><br/>[Criar a primeira consulta](../build-query.md)<br/><br/>[Editar expressões](../edit-expressions.md)<br/><br/>[Redirecionamento](../retarget.md) | [Introdução às atividades](about-activities.md)<br/><br/>Atividades:<br/>[And-join](and-join.md) - [Criar público](build-audience.md) - [Alterar dimensão](change-dimension.md) - [Atividades de canal](channels.md) - [Combinar](combine.md) - [Desduplicação](deduplication.md) - [Enriquecimento](enrichment.md) - [Bifurcação](fork.md) - [Reconciliação](reconciliation.md) - [Salvar público](save-audience.md) - [Divisão](split.md) - <b>[Espera](wait.md)</b> |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

O conteúdo desta página não é final e pode estar sujeito a alterações.

>[!ENDSHADEBOX]

A atividade **[!UICONTROL Wait]** é um componente **[!UICONTROL Flow control]** usado para introduzir um atraso entre duas atividades em uma campanha orquestrada. Isso ajuda a garantir que suas atividades de acompanhamento sejam mais cronometradas e relevantes para o engajamento do usuário.

Por exemplo, você pode aguardar alguns dias após um delivery de email para rastrear aberturas e cliques antes de enviar uma mensagem de acompanhamento.

## Configuração{#wait-configuration}

Siga estas etapas para configurar a atividade **[!UICONTROL Aguardar]**:

1. Adicione uma atividade **[!UICONTROL Wait]** à campanha orquestrada.

1. Selecione o tipo de espera que melhor atenda às suas necessidades:

   * **[!UICONTROL Duração]**: especifique um atraso em segundos, minutos, horas ou dias antes de prosseguir para a próxima atividade.

   * **[!UICONTROL Hora fixa]**: Defina uma data e hora específicas após as quais a próxima atividade iniciará.

   ![](../assets/wait_activity.png)

## Exemplo{#wait-example}

O exemplo a seguir ilustra a atividade **[!UICONTROL Wait]** em um caso de uso comum.  Um email com um código promocional é enviado para perfis que comemoram seus aniversários. Após 29 dias, um SMS é enviado para o mesmo grupo como um lembrete de que o código promocional de aniversário está prestes a expirar.

![](../assets/wait-example.png)
