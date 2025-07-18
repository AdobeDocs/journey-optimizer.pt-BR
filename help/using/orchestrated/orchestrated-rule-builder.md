---
solution: Journey Optimizer
product: journey optimizer
title: Trabalhar com o construtor de regras
description: Saiba como criar regras para suas campanhas orquestradas
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: fb7a0eb2-b2ff-49fa-af1f-f1c10f219b00
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 9%

---


# Trabalhar com o construtor de regras {#orchestrated-rule-builder}

+++ Sumário

| Bem-vindo às campanhas orquestradas | Lançar a primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](gs-orchestrated-campaigns.md)<br/><br/>Criar e gerenciar Esquemas e Conjuntos de Dados relacionais:</br> <ul><li>[Introdução a Esquemas e Conjuntos de Dados](gs-schemas.md)</li><li>[Esquema manual](manual-schema.md)</li><li>[Esquema de carregamento de arquivo](file-upload-schema.md)</li><li>[Assimilar dados](ingest-data.md)</li></ul>[Acesse e gerencie campanhas orquestradas](access-manage-orchestrated-campaigns.md)<br/><br/>[Etapas principais para criar uma campanha orquestrada](gs-campaign-creation.md) | [Criar e agendar a campanha](create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](orchestrate-activities.md)<br/><br/>[Iniciar e monitorar a campanha](start-monitor-campaigns.md)<br/><br/>[Relatórios](reporting-campaigns.md) | <b>[Trabalhar com o construtor de regras](orchestrated-rule-builder.md)</b><br/><br/>[Criar a primeira consulta](build-query.md)<br/><br/>[Editar expressões](edit-expressions.md)<br/><br/>[Redirecionamento](retarget.md) | [Introdução às atividades](activities/about-activities.md)<br/><br/>Atividades:<br/>[And-join](activities/and-join.md) - [Criar público](activities/build-audience.md) - [Alterar dimensão](activities/change-dimension.md) - [Atividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Desduplicação](activities/deduplication.md) - [Enriquecimento](activities/enrichment.md) - [Bifurcação](activities/fork.md) - [Reconciliação](activities/reconciliation.md) - [Salvar público](activities/save-audience.md) - [Divisão](activities/split.md) - [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

O conteúdo desta página não é final e pode estar sujeito a alterações.

>[!ENDSHADEBOX]

As campanhas orquestradas vêm com um construtor de regras que simplifica o processo de filtragem do banco de dados com base em vários critérios. O construtor de regras gerencia consultas muito complexas e longas com eficiência, oferecendo flexibilidade e precisão aprimoradas.

Ele também oferece suporte a filtros predefinidos em condições, permitindo que você refine as consultas com facilidade enquanto usa expressões e operadores avançados para estratégias abrangentes de direcionamento e segmentação de público.

## Acessar o construtor de regras

O modelador de consultas está disponível em todo contexto onde é preciso definir regras para filtrar dados.

| Uso | Exemplo |
|  ---  |  ---  |
| **Criar públicos-alvo**: especifique a população que deseja direcionar em suas campanhas orquestradas usando uma atividade **[!UICONTROL Criar público-alvo]** e crie facilmente novos públicos-alvo adaptados às suas necessidades. [Saiba como criar públicos-alvo](../orchestrated/activities/build-audience.md) | ![Imagem mostrando como acessar a interface de criação de público-alvo](assets/query-access-audience.png){width="200" align="center" zoomable="yes"} |
| **Criar condição na tela de campanha**: aplique regras na tela de campanha usando uma atividade **[!UICONTROL Split]** para alinhar-se aos seus requisitos específicos. [Saiba como usar uma atividade de Split](../orchestrated/activities/split.md) | ![Imagem mostrando como acessar opções de personalização de fluxo de trabalho](assets/query-access-split.png){width="200" align="center" zoomable="yes"} |
| **Criar filtros avançados**: crie regras para filtrar os dados exibidos em listas, como logs de fluxo de trabalho ou dimensões de direcionamento. | ![Imagem mostrando como personalizar filtros de lista](assets/query-access-advanced-filters.png){width="200" align="center" zoomable="yes"} |

## Interface do construtor de regras {#interface}

O construtor de regras fornece uma tela central onde você cria sua consulta e um painel de propriedades que fornece informações sobre a regra.

![Imagem mostrando a interface do construtor de regras](assets/rule-builder-interface.png)

* A **tela central** é onde você adiciona e combina os diferentes componentes para criar sua regra. [Saiba como criar uma regra](../orchestrated/build-query.md)

* O painel **[!UICONTROL Propriedades da regra]** fornece informações sobre a regra. Ele permite executar várias operações para verificar a regra e garantir que ela atenda às suas necessidades.

  Este painel é exibido ao criar uma consulta para criar um público-alvo. [Saiba como verificar e validar sua consulta](build-query.md#check-and-validate-your-query)
