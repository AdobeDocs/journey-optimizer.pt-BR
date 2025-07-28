---
solution: Journey Optimizer
product: journey optimizer
title: Etapas de configuração
description: Saiba como criar um esquema relacional no Adobe Experience Platform fazendo upload de uma DDL
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 327597f6-8a53-42dc-966a-baae49b58bb3
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 25%

---

# Introdução a esquemas e conjuntos de dados{#gs-schemas}

+++ Índice 

| Bem-vindo às campanhas orquestradas | Iniciar sua primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução às campanhas orquestradas](gs-orchestrated-campaigns.md)<br/><br/>Criar e gerenciar esquemas e conjuntos de dados relacionais:</br> <ul><li>[Introdução a Esquemas e Conjuntos de Dados](gs-schemas.md)</li><li>[Esquema manual](manual-schema.md)</li><li>[Esquema de carregamento de arquivo](file-upload-schema.md)</li><li>[Assimilar dados](ingest-data.md)</li></ul>[Acesse e gerencie campanhas orquestradas](access-manage-orchestrated-campaigns.md)<br/><br/>[Etapas principais para criar uma campanha orquestrada](gs-campaign-creation.md) | [Criar e programar a campanha](create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](orchestrate-activities.md)<br/><br/>[Iniciar e monitorar a campanha](start-monitor-campaigns.md)<br/><br/>[Geração de relatórios](reporting-campaigns.md) | [Trabalhar com o construtor de regras](orchestrated-rule-builder.md)<br/><br/>[Criar a sua primeira consulta](build-query.md)<br/><br/>[Editar expressões](edit-expressions.md)<br/><br/>[Redirecionamento](retarget.md) | [Introdução às atividades](activities/about-activities.md)<br/><br/>Atividades:<br/>[Associação](activities/and-join.md) - [Criar público-alvo](activities/build-audience.md) - [Mudar dimensão](activities/change-dimension.md) - [Atividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Desduplicação](activities/deduplication.md) - [Enriquecimento](activities/enrichment.md) - [Bifurcação](activities/fork.md) - [Reconciliação](activities/reconciliation.md) - [Salvar público-alvo](activities/save-audience.md) - [Divisão](activities/split.md) - [Aguardar](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

O conteúdo desta página não é final e pode estar sujeito a alterações.

>[!ENDSHADEBOX]

Este guia orienta você pelo processo de criação de um esquema relacional, configuração de um conjunto de dados para campanhas orquestradas e assimilação de dados.

![](assets/do-not-localize/schema_admin.png)

1. Criar [esquema relacional manualmente](manual-schema.md) ou [usando um arquivo DDL](file-upload-schema.md)

   Defina a estrutura do modelo de dados, incluindo tabelas, atributos e relações. Opte por criar o esquema manualmente na interface do usuário ou fazer upload de um arquivo DDL para uma configuração mais rápida.

1. [Vincular esquema](file-upload-schema.md)

   Estabeleça relacionamentos entre seus esquemas para garantir a consistência dos dados e habilitar consultas entre entidades. Por exemplo, vincule transações de fidelidade a recipients ou recompensas a marcas.

1. [Assimilar dados](ingest-data.md)

   Traga dados para a Adobe Experience Platform a partir de fontes compatíveis, como SFTP, armazenamento na nuvem ou bancos de dados.

