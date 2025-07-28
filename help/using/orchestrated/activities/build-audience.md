---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade de criar público-alvo
description: Saiba como usar a atividade Criar público-alvo em uma campanha orquestrada
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 3959b5fa-0c47-42a5-828f-4d7ca9b7e72d
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 57%

---

# Criar público-alvo {#build-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience"
>title="Atividade Criar público-alvo"
>abstract="A atividade **Criar público-alvo** permite definir o público-alvo que entrará na campanha Orquestrada. Ao enviar mensagens no contexto de uma campanha Orquestrada, o público-alvo da mensagem não é definido na atividade de canal, mas em uma atividade **Criar público-alvo**."

+++ Índice 

| Bem-vindo às campanhas orquestradas | Iniciar sua primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução às campanhas orquestradas](../gs-orchestrated-campaigns.md)<br/><br/>Criar e gerenciar esquemas e conjuntos de dados relacionais:</br> <ul><li>[Introdução a Esquemas e Conjuntos de Dados](../gs-schemas.md)</li><li>[Esquema manual](../manual-schema.md)</li><li>[Esquema de carregamento de arquivo](../file-upload-schema.md)</li><li>[Assimilar dados](../ingest-data.md)</li></ul>[Acessar e gerenciar campanhas orquestradas](../access-manage-orchestrated-campaigns.md) | [Etapas principais para criar uma campanha Orquestrada](../gs-campaign-creation.md)<br/><br/>[Criar e agendar a campanha](../create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](../orchestrate-activities.md)<br/><br/>[Iniciar e monitorar a campanha](../start-monitor-campaigns.md)<br/><br/>[Relatórios](../reporting-campaigns.md) | [Trabalhar com o construtor de regras](../orchestrated-rule-builder.md)<br/><br/>[Criar a sua primeira consulta](../build-query.md)<br/><br/>[Editar expressões](../edit-expressions.md)<br/><br/>[Redirecionamento](../retarget.md) | [Introdução às atividades](about-activities.md)<br/><br/>Atividades:<br/>[Associação](and-join.md) - <b>[Criar público-alvo](build-audience.md)</b> - [Mudar dimensão](change-dimension.md) - [Atividades de canal](channels.md) - [Combinar](combine.md) - [Desduplicação](deduplication.md) - [Enriquecimento](enrichment.md) - [Bifurcação](fork.md) - [Reconciliação](reconciliation.md) - [Salvar público-alvo](save-audience.md) - [Divisão](split.md) - [Aguardar](wait.md) |

{style="table-layout:fixed"}

+++


<br/>

>[!BEGINSHADEBOX]

</br>

O conteúdo desta página não é final e pode estar sujeito a alterações.

>[!ENDSHADEBOX]

Como profissional de marketing, você pode criar segmentos complexos de público-alvo por meio de uma interface intuitiva, permitindo direcionar usuários com base em uma grande variedade de critérios e comportamentos para adaptar as suas campanhas com mais eficiência.

Para isso, use a atividade de direcionamento **[!UICONTROL Criar público-alvo]**. Essa atividade define o público-alvo que entra na campanha Orquestrada. Ao enviar mensagens como parte de uma campanha Orquestrada, o público-alvo é definido na atividade **[!UICONTROL Criar público-alvo]**, não dentro da campanha Orquestrada.

## Configurar a atividade Criar público-alvo {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience_audienceselector"
>title="Público-alvo"
>abstract="Selecione o público-alvo assim como faz ao criar uma nova entrega. "

Siga estas etapas para configurar a atividade **[!UICONTROL Criar público-alvo]**:

1. Adicione uma atividade **[!UICONTROL Criar público-alvo]**.

   ![](../assets/build-audience.png)

1. Defina um **[!UICONTROL Rótulo]**.

1. Configure o seu público-alvo, seguindo as etapas detalhadas nas guias abaixo.

1. Escolha a **[!UICONTROL Dimensão de direcionamento]**. A dimensão de direcionamento permite definir a população-alvo da operação: destinatários, beneficiários(as) de contrato, operadores(as), assinantes, etc. Por padrão, o público-alvo é selecionado entre os destinatários.

1. Clique em **[!UICONTROL Continuar]**.

1. Use o modelador de consultas para definir a sua consulta. [Saiba mais sobre o modelador de consultas nesta seção](../orchestrated-rule-builder.md)

1. Especifique se uma transição de saída deve ser gerada quando o público-alvo estiver vazio.

## Exemplos{#build-audience-examples}

Este é um exemplo de uma campanha Orquestrada com duas atividades **[!UICONTROL Build audience]**. A primeira é direcionada a perfis que têm itens em seus carrinhos, seguida por uma entrega de email. A segunda é direcionada a perfis com uma lista de desejos, seguida por uma entrega de SMS.

![](../assets/build-audience-2.png)
