---
solution: Journey Optimizer
product: journey optimizer
title: Medidas de proteção e limitações para campanhas orquestradas
description: Saiba mais sobre as medidas de proteção e limitações das campanhas orquestradas
hide: true
hidefromtoc: true
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 10%

---

# Medidas de proteção e limitações {#guardrails}

+++ Índice 

| Bem-vindo às campanhas orquestradas | Iniciar sua primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução às campanhas orquestradas](gs-orchestrated-campaigns.md)<br/><br/>Criar e gerenciar esquemas e conjuntos de dados relacionais:</br> <ul><li>[Introdução a Esquemas e Conjuntos de Dados](gs-schemas.md)</li><li>[Esquema manual](manual-schema.md)</li><li>[Esquema de carregamento de arquivo](file-upload-schema.md)</li><li>[Assimilar dados](ingest-data.md)</li></ul>[Acesse e gerencie campanhas orquestradas](access-manage-orchestrated-campaigns.md)<br/><br/>[Etapas principais para criar uma campanha orquestrada](gs-campaign-creation.md) | [Criar e programar a campanha](create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](orchestrate-activities.md)<br/><br/>[Iniciar e monitorar a campanha](start-monitor-campaigns.md)<br/><br/>[Geração de relatórios](reporting-campaigns.md) | [Trabalhar com o construtor de regras](orchestrated-rule-builder.md)<br/><br/>[Criar a sua primeira consulta](build-query.md)<br/><br/>[Editar expressões](edit-expressions.md)<br/><br/>[Redirecionamento](retarget.md) | [Introdução às atividades](activities/about-activities.md)<br/><br/>Atividades:<br/>[Associação](activities/and-join.md) - [Criar público-alvo](activities/build-audience.md) - [Mudar dimensão](activities/change-dimension.md) - [Atividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Desduplicação](activities/deduplication.md) - [Enriquecimento](activities/enrichment.md) - [Bifurcação](activities/fork.md) - [Reconciliação](activities/reconciliation.md) - [Salvar público-alvo](activities/save-audience.md) - [Divisão](activities/split.md) - [Aguardar](activities/wait.md) |

{style="table-layout:fixed"}

+++

## Limitações do fluxo de dados para o conjunto de dados

Cada conjunto de dados na Adobe Experience Platform só pode ser associado a um fluxo de dados ativo por vez. Essa cardinalidade 1:1 é estritamente imposta pela plataforma.

Se você precisar alternar fontes de dados (por exemplo, do Amazon S3 para o Salesforce):

Você deve excluir o fluxo de dados existente conectado ao conjunto de dados.

Em seguida, crie um novo fluxo de dados com a nova origem mapeada para o mesmo conjunto de dados.

Isso garante a assimilação confiável de dados e é essencial ao usar o Change Data Capture (CDC), que depende de uma chave primária definida e de um atributo de controle de versão (por exemplo, modificado pela última vez) para atualizações incrementais.


## Esquemas relacionais / limitações de assimilação de dados

* Até 200 esquemas relacionais (tabelas) são suportados no armazenamento de dados relacional.

* O tamanho total de um esquema relacional usado para a Orquestração de campanha não deve exceder 100 GB.

* A assimilação em lote para a Orquestração de campanha não deve ocorrer com mais frequência do que uma vez a cada 15 minutos.

* As alterações diárias em um esquema relacional devem permanecer abaixo de 20% da contagem total de registros.

## Modelagem de dados

* O descritor de versão é obrigatório em todos os esquemas, incluindo tabelas de fatos.

* Uma chave primária é necessária para cada tabela.

* O table_name atribuído durante a criação do conjunto de dados é usado na interface do usuário de segmentação e nos recursos de personalização.

  Esse nome é permanente e não pode ser alterado após a criação.

* Os grupos de campos não são aceitos no momento.

## Ingestão de dados

* É necessária a assimilação de perfil + dados relacionais.

* Um campo de tipo de alteração é necessário para assimilação baseada em arquivo, enquanto o log de tabela deve ser ativado para assimilação no Cloud DB. Isso é necessário para a Captura de dados de alteração (CDC).

* A latência da assimilação à disponibilidade dos dados no Snowflake varia de 15 minutos a 2 horas, dependendo do volume de dados, da simultaneidade e do tipo de operações (as inserções são mais rápidas que as atualizações).

* O monitoramento de dados no Snowflake está em desenvolvimento; atualmente, não há confirmação nativa para a assimilação bem-sucedida.

* Não há suporte para atualizações diretas no Snowflake ou no conjunto de dados. Todas as alterações devem fluir pelas fontes CDC.

  O serviço de consulta é somente leitura.

* ETL não é compatível — os clientes devem fornecer dados no formato necessário.

* Atualizações parciais não são permitidas. Cada linha deve ser fornecida como um registro completo.

* A assimilação depende do Serviço de consulta e do Data Distiller.

## Segmentação

* A LOV (Lista de Valores) e as listas discriminadas estão disponíveis no momento.

* Públicos salvos são listas estáticas, seu conteúdo reflete os dados disponíveis no momento em que a campanha é executada.

* Anexar a um público-alvo salvo não é suportado. As atualizações exigem uma substituição completa.

* Os públicos devem consistir somente em atributos escalares; não há suporte para mapas e matrizes.

* A segmentação suporta principalmente dados relacionais. Embora a combinação com dados de perfil seja permitida, trazer grandes conjuntos de dados de perfil pode afetar o desempenho. Para evitar isso:

* As medidas de proteção estão em vigor, como limitar o número de atributos de perfil selecionados em lote ou públicos de transmissão.

* Os públicos-alvo de leitura não são armazenados em cache — cada execução de campanha aciona uma leitura completa.

  A otimização é necessária para públicos-alvo grandes ou complexos.