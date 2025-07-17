---
solution: Journey Optimizer
product: journey optimizer
title: Etapas de configuração
description: Saiba como criar um esquema relacional no Adobe Experience Platform fazendo upload de uma DDL
badge: label="Alfa"
hide: true
hidefromtoc: true
source-git-commit: 25120dd71159d0233783ac4c189f528ff2c93ae3
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 5%

---

# Introdução a esquemas e relatórios associados {#file-upload-schema}

+++ Sumário

| Bem-vindo às campanhas orquestradas | Lançar a primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](gs-orchestrated-campaigns.md)<br/><br/>Criar e gerenciar Esquemas e Conjuntos de Dados relacionais:</br> <ul><li>[Esquema manual](manual-schema.md)</li><li>[Esquema de carregamento de arquivo](file-upload-schema.md)</li><li>[Assimilar dados](ingest-data.md)</li></ul>[Acesse e gerencie campanhas orquestradas](access-manage-orchestrated-campaigns.md)<br/><br/>[Etapas principais para criar uma campanha orquestrada](gs-campaign-creation.md) | [Criar e agendar a campanha](create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](orchestrate-activities.md)<br/><br/>[Iniciar e monitorar a campanha](start-monitor-campaigns.md)<br/><br/>[Relatórios](reporting-campaigns.md) | [Trabalhar com o construtor de regras](orchestrated-rule-builder.md)<br/><br/>[Criar a primeira consulta](build-query.md)<br/><br/>[Editar expressões](edit-expressions.md)<br/><br/>[Redirecionamento](retarget.md) | [Introdução às atividades](activities/about-activities.md)<br/><br/>Atividades:<br/>[And-join](activities/and-join.md) - [Criar público](activities/build-audience.md) - [Alterar dimensão](activities/change-dimension.md) - [Atividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Desduplicação](activities/deduplication.md) - [Enriquecimento](activities/enrichment.md) - [Bifurcação](activities/fork.md) - [Reconciliação](activities/reconciliation.md) - [Salvar público](activities/save-audience.md) - [Divisão](activities/split.md) - [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

O conteúdo desta página não é final e pode estar sujeito a alterações.

>[!ENDSHADEBOX]

Este guia o orienta pelo processo de criação de um esquema relacional, configuração de um conjunto de dados para campanhas orquestradas, assimilação de dados por meio de uma fonte S3 e consulta dos dados assimilados na plataforma AP.

Neste exemplo, a configuração inclui a integração de duas entidades principais, **Transações de Fidelidade** e **Recompensas de Fidelidade**, e os vincula às entidades principais existentes **Destinatários** e **Marcas**.

![](assets/do-not-localize/schema_admin.png)

1. [Criar Esquema relacional e Conjunto de Dados associado](#schema)

   Defina o modelo de dados relacionais para campanhas orquestradas, incluindo as entidades **Associações de Fidelidade**, **Transações de Fidelidade** e **Recompensas de Fidelidade**, juntamente com as chaves e os atributos de controle de versão necessários.

1. [Esquema de link](#link-schema)

   Vincule a entidade **Transações de Fidelidade** a **Destinatários** e **Recompensas de Fidelidade** a **Marcas** para criar um modelo de dados conectado que ofereça suporte a jornadas personalizadas de clientes.

1. [Dados de assimilação](#ingest)

   Traga dados para a Adobe Experience Platform de fontes compatíveis, como SFTP, armazenamento na nuvem ou bancos de dados.


<!--### Setting Up Change data capture ingestion {#cdc-ingestion}

If you need to change the data source, you must delete the existing dataflow and create a new one pointing to the same dataset with the new source.

When using Change Data Capture (CDC), it is essential that the source and dataset remain in sync to ensure accurate incremental updates. Follow the steps below:

1. **Schema Requirements**
   - Your schema must include:
     - A **primary key** (e.g., `transaction_id`)
     - A **versioning field** (e.g., `lastmodified` or an incrementing `version_id`)
   - Enable the dataset for **Orchestrated Campaigns** if needed.

2. **CDC Dataflow Setup**
   - During dataflow creation, after choosing your source and files:
     - **Enable the CDC option**
     - Select your CDC-ready dataset
     - Confirm field mappings (especially version field)

3. **Keep Source and Target in Sync**
   - The source system must consistently update the version field so the platform can detect changes accurately.

Once set up, the platform will automatically ingest **only changed or new records** each time the flow runs.
-->
