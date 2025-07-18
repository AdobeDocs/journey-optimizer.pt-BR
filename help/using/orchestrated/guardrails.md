---
solution: Journey Optimizer
product: journey optimizer
title: Medidas de proteção e limitações para campanhas orquestradas
description: Saiba mais sobre as medidas de proteção e limitações das campanhas orquestradas
hide: true
hidefromtoc: true
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 5%

---

# Medidas de proteção e limitações {#guardrails}

+++ Sumário

| Bem-vindo às campanhas orquestradas | Lançar a primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](gs-orchestrated-campaigns.md)<br/><br/>Criar e gerenciar Esquemas e Conjuntos de Dados relacionais:</br> <ul><li>[Introdução a Esquemas e Conjuntos de Dados](gs-schemas.md)</li><li>[Esquema manual](manual-schema.md)</li><li>[Esquema de carregamento de arquivo](file-upload-schema.md)</li><li>[Assimilar dados](ingest-data.md)</li></ul>[Acesse e gerencie campanhas orquestradas](access-manage-orchestrated-campaigns.md)<br/><br/>[Etapas principais para criar uma campanha orquestrada](gs-campaign-creation.md) | [Criar e agendar a campanha](create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](orchestrate-activities.md)<br/><br/>[Iniciar e monitorar a campanha](start-monitor-campaigns.md)<br/><br/>[Relatórios](reporting-campaigns.md) | [Trabalhar com o construtor de regras](orchestrated-rule-builder.md)<br/><br/>[Criar a primeira consulta](build-query.md)<br/><br/>[Editar expressões](edit-expressions.md)<br/><br/>[Redirecionamento](retarget.md) | [Introdução às atividades](activities/about-activities.md)<br/><br/>Atividades:<br/>[And-join](activities/and-join.md) - [Criar público](activities/build-audience.md) - [Alterar dimensão](activities/change-dimension.md) - [Atividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Desduplicação](activities/deduplication.md) - [Enriquecimento](activities/enrichment.md) - [Bifurcação](activities/fork.md) - [Reconciliação](activities/reconciliation.md) - [Salvar público](activities/save-audience.md) - [Divisão](activities/split.md) - [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

## Limitações do fluxo de dados para o conjunto de dados

Cada conjunto de dados na Adobe Experience Platform só pode ser associado a um fluxo de dados ativo por vez. Essa cardinalidade 1:1 é estritamente imposta pela plataforma.

Se você precisar alternar fontes de dados (por exemplo, do Amazon S3 para o Salesforce):

Você deve excluir o fluxo de dados existente conectado ao conjunto de dados.

Em seguida, crie um novo fluxo de dados com a nova origem mapeada para o mesmo conjunto de dados.

Isso garante a assimilação confiável de dados e é essencial ao usar o Change Data Capture (CDC), que depende de uma chave primária definida e de um atributo de controle de versão (por exemplo, modificado pela última vez) para atualizações incrementais.


## Esquemas relacionais / limitações de assimilação de dados

* Número de Esquemas - O número máximo de esquemas relacionais (tabelas no armazenamento de dados relacional) é 200
* Tamanho do esquema relacional - O tamanho máximo do esquema relacional para a orquestração de campanha será de 100 GB.
* Frequência de assimilação de dados - A frequência de assimilação de dados em lote para a orquestração de campanha não deve exceder um a cada quinze minutos.
* Alterações/Atualizações - As atualizações/alterações diárias devem estar abaixo de 20% do total de registros de um determinado esquema relacional
