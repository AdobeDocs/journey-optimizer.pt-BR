---
solution: Journey Optimizer
product: journey optimizer
title: Etapas de configuração
description: Saiba como trazer dados para a Adobe Experience Platform de fontes compatíveis, como SFTP, armazenamento na nuvem ou bancos de dados.
exl-id: 7f1e7985-b68e-43d6-9c8f-fea2469f8af9
version: Campaign Orchestration
source-git-commit: 059670c143595b9cacdf7e82a8a5c3efda78f30b
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 21%

---


# Assimilar dados {#ingest-data}

>[!IMPORTANT]
>
>Para alterar a fonte de dados de um conjunto de dados, primeiro exclua o fluxo de dados existente, antes de criar um novo que faça referência ao mesmo conjunto de dados e à nova fonte.
>
>O Adobe Experience Platform impõe uma relação rigorosa um para um entre os fluxos de dados e conjuntos de dados. Isso permite manter a sincronização entre a origem e o conjunto de dados para uma assimilação incremental precisa.

A Adobe Experience Platform permite a assimilação de dados de fontes externas, além de permitir estruturar, rotular e aprimorar os dados recebidos por meio dos serviços da Experience Platform. Você pode assimilar dados de várias fontes, como aplicativos Adobe, armazenamentos baseados na nuvem, bancos de dados e muitas outras.

Um conjunto de dados é uma construção de armazenamento e gerenciamento para uma coleção de dados, normalmente uma tabela, que contém um esquema (colunas) e campos (linhas). Os dados assimilados com sucesso na Experience Platform são armazenados no data lake como conjuntos de dados.

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

## Diretrizes para a higiene de dados do esquema relacional {#cdc}

Para conjuntos de dados habilitados com a **[!UICONTROL captura de dados de alteração]**, todas as alterações de dados, incluindo exclusões, são automaticamente espelhadas do sistema de origem para a Adobe Experience Platform.

Como as Campanhas do Adobe Journey Optimizer exigem que todos os conjuntos de dados integrados sejam habilitados com a **[!UICONTROL captura de dados de alteração]**, é responsabilidade do cliente gerenciar as exclusões na origem. Qualquer registro excluído do sistema de origem será removido automaticamente do conjunto de dados correspondente no Adobe Experience Platform.

Para excluir registros por meio da assimilação baseada em arquivo, o arquivo de dados do cliente deve marcar o registro usando um valor `D` no campo `Change Request Type`. Isso indica que o registro deve ser excluído no Adobe Experience Platform, espelhando o sistema de origem.

Se o cliente quiser excluir registros somente do Adobe Experience Platform sem afetar os dados de origem originais, as seguintes opções estarão disponíveis:

* **Tabela de Proxy ou Limpa para Replicação de captura de dados de Alteração**

  O cliente pode criar um proxy ou uma tabela de origem limpa para controlar quais registros são replicados no Adobe Experience Platform. As exclusões podem ser gerenciadas seletivamente nessa tabela intermediária.

* **Exclusão via Data Distiller**

  Se licenciado, o **Data Distiller** poderá ser usado para oferecer suporte a operações de exclusão diretamente no Adobe Experience Platform, independentemente do sistema de origem.

  [Saiba mais sobre o Data Distiller](https://experienceleague.adobe.com/pt-br/docs/experience-platform/query/data-distiller/overview)

## Configurar um fluxo de dados

Este exemplo demonstra como configurar um fluxo de dados que assimila dados estruturados na Adobe Experience Platform. O fluxo de dados configurado suporta assimilação automatizada e agendada e permite atualizações em tempo real.

1. No menu **[!UICONTROL Conexões]**, acesse o menu **[!UICONTROL Fontes]**.

1. Escolha sua origem de acordo com as [Fontes com Suporte para campanhas Orquestradas](#supported).

   ![](assets/admin_sources_1.png)

1. Conecte seu Armazenamento na nuvem ou a conta do Google Cloud Storage se você escolher fontes baseadas em nuvem.

   ![](assets/admin_sources_2.png)

1. Escolha os dados que serão assimilados na Adobe Experience Platform.

   ![](assets/S3_config_1.png)

1. Na página **[!UICONTROL Detalhes do conjunto de dados]**, marque **[!UICONTROL Habilitar captura de dados de alteração]** para exibir somente conjuntos de dados mapeados para esquemas relacionais e incluir uma chave primária e um descritor de versão.

[Saiba mais sobre diretrizes para a higiene de dados de esquemas relacionais](#cdc)

   >[!IMPORTANT]
   >
   > Somente para **fontes baseadas em arquivo**, cada linha do arquivo de dados deve incluir uma coluna `_change_request_type` com valores `U` (substituição) ou `D` (exclusão). Sem essa coluna, o sistema não reconhecerá os dados como suporte ao controle de alterações e o botão Campanha orquestrada não será exibido, impedindo que o conjunto de dados seja selecionado para direcionamento.

   ![](assets/S3_config_6.png)

1. Selecione o Conjunto de Dados criado anteriormente e clique em **[!UICONTROL Avançar]**.

   ![](assets/S3_config_3.png)

1. Se você estiver usando apenas fontes baseadas em arquivo, na janela **[!UICONTROL Selecionar dados]**, carregue os arquivos locais e visualize sua estrutura e conteúdo.

   Observe que o tamanho máximo suportado é 100 MB.

1. Na janela **[!UICONTROL Mapping]**, verifique se cada atributo de arquivo de origem está mapeado corretamente com os campos correspondentes no esquema de destino. [Saiba mais sobre dimensões de direcionamento](target-dimension.md).

   Clique em **[!UICONTROL Próximo]** quando terminar.

   ![](assets/S3_config_4.png)

1. Configure o fluxo de dados de **[!UICONTROL Agendar]** com base na frequência desejada.

1. Clique em **[!UICONTROL Concluir]** para criar o fluxo de dados. Ele será executado automaticamente de acordo com a programação definida.

1. No menu **[!UICONTROL Conexões]**, selecione **[!UICONTROL Fontes]** e acesse a guia **[!UICONTROL Fluxos de dados]** para rastrear a execução do fluxo, revisar registros assimilados e solucionar quaisquer erros.

   ![](assets/S3_config_5.png)


