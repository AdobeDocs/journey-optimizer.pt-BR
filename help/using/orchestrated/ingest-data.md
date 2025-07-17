---
solution: Journey Optimizer
product: journey optimizer
title: Etapas de configuração
description: Saiba como trazer dados para a Adobe Experience Platform de fontes compatíveis, como SFTP, armazenamento na nuvem ou bancos de dados.
badge: label="Alfa"
hide: true
hidefromtoc: true
source-git-commit: 25120dd71159d0233783ac4c189f528ff2c93ae3
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 7%

---

# Assimilar dados {#ingest-data}

+++ Sumário

| Bem-vindo às campanhas orquestradas | Lançar a primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](gs-orchestrated-campaigns.md)<br/><br/>Criar e gerenciar esquemas e conjuntos de dados relacionais</br> <ul><li>[Esquema manual](manual-schema.md)</li><li>[Esquema de carregamento de arquivo](file-upload-schema.md)</li><li>[Assimilar dados](ingest-data.md)</li></ul>[Acesse e gerencie campanhas orquestradas](access-manage-orchestrated-campaigns.md)<br/><br/>[Etapas principais para criar uma campanha orquestrada](gs-campaign-creation.md) | [Criar e agendar a campanha](create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](orchestrate-activities.md)<br/><br/>[Iniciar e monitorar a campanha](start-monitor-campaigns.md)<br/><br/>[Relatórios](reporting-campaigns.md) | [Trabalhar com o construtor de regras](orchestrated-rule-builder.md)<br/><br/>[Criar a primeira consulta](build-query.md)<br/><br/>[Editar expressões](edit-expressions.md)<br/><br/>[Redirecionamento](retarget.md) | [Introdução às atividades](activities/about-activities.md)<br/><br/>Atividades:<br/>[And-join](activities/and-join.md) - [Criar público](activities/build-audience.md) - [Alterar dimensão](activities/change-dimension.md) - [Atividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Desduplicação](activities/deduplication.md) - [Enriquecimento](activities/enrichment.md) - [Bifurcação](activities/fork.md) - [Reconciliação](activities/reconciliation.md) - [Salvar público](activities/save-audience.md) - [Divisão](activities/split.md) - [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

O conteúdo desta página não é final e pode estar sujeito a alterações.

>[!ENDSHADEBOX]

O Adobe Experience Platform permite que os dados sejam assimilados de fontes externas e, ao mesmo tempo, fornece a capacidade de estruturar, rotular e aprimorar os dados recebidos usando os serviços da Experience Platform. Você pode assimilar dados de várias fontes, como aplicativos Adobe, armazenamentos baseados na nuvem, bancos de dados e muitas outras.

## Com armazenamento na nuvem {#ingest}

<!--
>[!IMPORTANT]
>
>Each dataset in Adobe Experience Platform supports only one active dataflow at a time. For detailed setup guidance on how to switch data sources, refer to this [section](#cdc-ingestion).
-->

Você pode configurar um fluxo de dados para assimilar dados de uma origem do Amazon S3 na Adobe Experience Platform. Depois de configurado, o fluxo de dados permite a assimilação automatizada e programada de dados estruturados e oferece suporte a atualizações em tempo real.

1. No menu **[!UICONTROL Conexões]**, acesse o menu **[!UICONTROL Fontes]**.

1. Selecione a categoria **[!UICONTROL Armazenamento na nuvem]**, depois o Amazon S3 e clique em **[!UICONTROL Adicionar dados]**.

   ![](assets/admin_sources_1.png)

1. Conectar sua Conta S3:

   * Com uma conta existente

   * Com uma nova conta

   [Saiba mais na documentação do Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3#connect)

   ![](assets/admin_sources_2.png)

1. Escolha o **[!UICONTROL Formato dos dados]**, **[!UICONTROL Delimitador]** e **[!UICONTROL Tipo de compactação]** da pasta.

1. Navegue pela origem S3 conectada até localizar as duas pastas criadas anteriormente, ou seja, **recompensas de fidelidade** e **transações de fidelidade**.

1. Selecione a pasta que contém seus dados.

   Selecionar uma pasta garante que todos os arquivos atuais e futuros com a mesma estrutura sejam processados automaticamente. A seleção de um único arquivo, no entanto, requer o upload manual de cada novo incremento de dados.

   ![](assets/S3_config_2.png)

1. Escolha o **[!UICONTROL Formato dos dados]**, **[!UICONTROL Delimitador]** e **[!UICONTROL Tipo de compactação]** da pasta. Verifique a precisão dos dados de amostra e clique em **[!UICONTROL Avançar]**.

   ![](assets/S3_config_1.png)

1. Marque **[!UICONTROL Habilitar captura de dados de alteração]** para selecionar entre conjuntos de dados mapeados para esquemas relacionais e que tenham uma chave primária e um descritor de versão definidos.

1. Selecione o [Conjunto de Dados criado anteriormente](#entities) e clique em **[!UICONTROL Avançar]**.

   ![](assets/S3_config_3.png)

1. Na janela **[!UICONTROL Mapping]**, verifique se cada atributo de arquivo de origem está mapeado corretamente com os campos correspondentes no esquema de destino.

   Clique em **[!UICONTROL Avançar]** depois de concluído.

   ![](assets/S3_config_4.png)

1. Configure o fluxo de dados **[!UICONTROL Agendar]** com base na frequência desejada.

1. Clique em **[!UICONTROL Concluir]** para criar o fluxo de dados. Ele será executado automaticamente de acordo com o agendamento definido.

1. No menu **[!UICONTROL Conexões]**, selecione **[!UICONTROL Fontes]** e acesse a guia **[!UICONTROL Fluxos de Dados]** para rastrear a execução do fluxo, revisar registros assimilados e solucionar quaisquer erros.

   ![](assets/S3_config_5.png)

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