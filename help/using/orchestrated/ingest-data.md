---
solution: Journey Optimizer
product: journey optimizer
title: Etapas de configuração
description: Saiba como trazer dados para a Adobe Experience Platform de fontes compatíveis, como SFTP, armazenamento na nuvem ou bancos de dados.
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 7f1e7985-b68e-43d6-9c8f-fea2469f8af9
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 36%

---

# Assimilar dados {#ingest-data}

+++ Índice 

| Bem-vindo às campanhas orquestradas | Iniciar sua primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução às campanhas orquestradas](gs-orchestrated-campaigns.md)<br/><br/>Criar e gerenciar esquemas e conjuntos de dados relacionais</br> <ul><li>[Introdução a Esquemas e Conjuntos de Dados](gs-schemas.md)</li><li>[Esquema manual](manual-schema.md)</li><li>[Esquema de carregamento de arquivo](file-upload-schema.md)</li><li>[Assimilar dados](ingest-data.md)</li></ul>[Acesse e gerencie campanhas orquestradas](access-manage-orchestrated-campaigns.md)<br/><br/>[Etapas principais para criar uma campanha orquestrada](gs-campaign-creation.md) | [Criar e programar a campanha](create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](orchestrate-activities.md)<br/><br/>[Iniciar e monitorar a campanha](start-monitor-campaigns.md)<br/><br/>[Geração de relatórios](reporting-campaigns.md) | [Trabalhar com o construtor de regras](orchestrated-rule-builder.md)<br/><br/>[Criar a sua primeira consulta](build-query.md)<br/><br/>[Editar expressões](edit-expressions.md)<br/><br/>[Redirecionamento](retarget.md) | [Introdução às atividades](activities/about-activities.md)<br/><br/>Atividades:<br/>[Associação](activities/and-join.md) - [Criar público-alvo](activities/build-audience.md) - [Mudar dimensão](activities/change-dimension.md) - [Atividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Desduplicação](activities/deduplication.md) - [Enriquecimento](activities/enrichment.md) - [Bifurcação](activities/fork.md) - [Reconciliação](activities/reconciliation.md) - [Salvar público-alvo](activities/save-audience.md) - [Divisão](activities/split.md) - [Aguardar](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

O conteúdo desta página não é final e pode estar sujeito a alterações.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>Para alterar a fonte de dados de um conjunto de dados, primeiro exclua o fluxo de dados existente, antes de criar um novo que faça referência ao mesmo conjunto de dados e à nova fonte.
>
>O Adobe Experience Platform impõe uma relação rigorosa um para um entre os fluxos de dados e conjuntos de dados. Isso permite manter a sincronização entre a origem e o conjunto de dados para uma assimilação incremental precisa.

A Adobe Experience Platform permite a assimilação de dados de fontes externas, além de permitir estruturar, rotular e aprimorar os dados recebidos por meio dos serviços da Experience Platform. Você pode assimilar dados de várias fontes, como aplicativos Adobe, armazenamentos baseados na nuvem, bancos de dados e muitas outras.

## Fontes compatíveis para campanhas orquestradas {#supported}

As seguintes origens são compatíveis com o uso de campanhas orquestradas:

<table>
  <thead>
    <tr>
      <th>Tipo</th>
      <th>Fonte</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="3">Armazenamento na nuvem</td>
      <td><a href="https://experienceleague.adobe.com/pt-br/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/s3">Amazon S3</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/pt-br/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/google-cloud-storage">Google Cloud Storage</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/pt-br/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/sftp">SFTP</a></td>
    </tr>
      <td rowspan="4">Data Warehouses da nuvem</td>
      <td><a href="https://experienceleague.adobe.com/pt-br/docs/experience-platform/sources/ui-tutorials/create/databases/snowflake">Snowflake</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/pt-br/docs/experience-platform/sources/ui-tutorials/create/databases/bigquery">Google BigQuery</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/pt-br/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/data-landing-zone">Data Landing Zone<a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/pt-br/docs/experience-platform/sources/ui-tutorials/create/databases/databricks">Azure Databricks</a></td>
    </tr>
    <tr>
      <td rowspan="3">Uploads baseados em arquivo</td>
      <td><a href="https://experienceleague.adobe.com/pt-br/docs/experience-platform/sources/ui-tutorials/create/local-system/local-file-upload">Upload de arquivo local<a></td>
    </tr>

</tbody>
</table>

## Configurar um fluxo de dados

Este exemplo demonstra como configurar um fluxo de dados que assimila dados estruturados na Adobe Experience Platform. O fluxo de dados configurado suporta assimilação automatizada e agendada e permite atualizações em tempo real.

1. No menu **[!UICONTROL Conexões]**, acesse o menu **[!UICONTROL Fontes]**.

1. Escolha sua origem de acordo com as [Fontes com Suporte para campanhas Orquestradas](#supported).

   ![](assets/admin_sources_1.png)

1. Conecte seu Armazenamento na nuvem ou a conta do Google Cloud Storage se você escolher fontes baseadas em nuvem.

   ![](assets/admin_sources_2.png)

1. Escolha os dados que deseja assimilar na Adobe Experience Platform.

   ![](assets/S3_config_1.png)

1. Na página **[!UICONTROL Detalhes do conjunto de dados]**, marque **[!UICONTROL Habilitar captura de dados de alteração]** para exibir somente conjuntos de dados mapeados para esquemas relacionais e incluir uma chave primária e um descritor de versão.

   >[!IMPORTANT]
   >
   > Somente para **fontes baseadas em arquivo**, cada linha do arquivo de dados deve incluir uma coluna `_change_request_type` com valores `U` (substituição) ou `D` (exclusão). Sem essa coluna, o sistema não reconhecerá os dados como suporte ao controle de alterações e o botão Campanha orquestrada não será exibido, impedindo que o conjunto de dados seja selecionado para direcionamento.

   ![](assets/S3_config_6.png)

1. Selecione o Conjunto de Dados criado anteriormente e clique em **[!UICONTROL Avançar]**.

   ![](assets/S3_config_3.png)

1. Se você estiver usando apenas fontes baseadas em arquivo, na janela **[!UICONTROL Selecionar dados]**, carregue os arquivos locais e visualize sua estrutura e conteúdo.

   Observe que o tamanho máximo suportado é 100 MB.

1. Na janela **[!UICONTROL Mapeamento]**, verifique se cada atributo de arquivo de origem está mapeado corretamente com os campos correspondentes no esquema de público-alvo.

   Clique em **[!UICONTROL Próximo]** quando terminar.

   ![](assets/S3_config_4.png)

1. Configure o fluxo de dados de **[!UICONTROL Agendar]** com base na frequência desejada.

1. Clique em **[!UICONTROL Concluir]** para criar o fluxo de dados. Ele será executado automaticamente de acordo com a programação definida.

1. No menu **[!UICONTROL Conexões]**, selecione **[!UICONTROL Fontes]** e acesse a guia **[!UICONTROL Fluxos de dados]** para rastrear a execução do fluxo, revisar registros assimilados e solucionar quaisquer erros.

   ![](assets/S3_config_5.png)

