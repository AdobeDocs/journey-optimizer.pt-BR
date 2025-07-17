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
source-wordcount: '827'
ht-degree: 1%

---

# Upload de arquivo {#file-upload-schema}

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

Defina o modelo de dados relacionais necessário para campanhas orquestradas, criando esquemas como **Associações de Fidelidade**, **Transações de Fidelidade** e **Recompensas de Fidelidade**. Cada esquema deve incluir uma chave primária, um atributo de controle de versão e relações apropriadas com entidades de referência como **Destinatários** ou **Marcas**.

Os esquemas podem ser criados manualmente por meio da interface ou importados em massa usando um arquivo DDL.

Esta seção fornece orientação passo a passo sobre como criar um esquema relacional no Adobe Experience Platform fazendo upload de um arquivo DDL (Data Definition Language). Usar um arquivo DDL permite definir a estrutura do modelo de dados antecipadamente, incluindo tabelas, atributos, chaves e relacionamentos.

## Fazer upload de um arquivo DDL{#ddl-upload}

Ao fazer upload de um arquivo DDL, você pode definir a estrutura do modelo de dados antecipadamente, incluindo tabelas, atributos, chaves e relacionamentos.

1. Faça logon no Adobe Experience Platform.

1. Navegue até **Gerenciamento de Dados** > **Esquema**.

1. Clique em **Criar esquema**.

1. Você será solicitado a selecionar entre dois tipos de esquema:

   * **Padrão**
   * **Relational**, usado especificamente para campanhas orquestradas

   ![](assets/admin_schema_1.png)

1. Selecione **Carregar arquivo DDL** para definir um diagrama de relação de entidade e criar esquemas.

   A estrutura da tabela deve conter:
   * Pelo menos uma chave primária
   * Um identificador de versão, como um campo `lastmodified` do tipo `datetime` ou `number`.

1. Arraste e solte seu arquivo DDL e clique em **[!UICONTROL Próximo]**.

1. Digite seu **[!UICONTROL Nome do esquema]**.

1. Configure cada esquema e suas colunas, garantindo que uma chave primária seja especificada.

   Um atributo, como `lastmodified`, deve ser designado como descritor de versão. Este atributo, normalmente do tipo `datetime`, `long` ou `int`, é essencial para processos de assimilação para garantir que o conjunto de dados seja atualizado com a versão de dados mais recente.

   ![](assets/admin_schema_2.png)

1. Clique em **[!UICONTROL Concluído]** depois de concluído.

Agora é possível verificar a tabela e as definições de campo na tela. [Saiba mais na seção abaixo](#entities)

## Definir relacionamentos {#relationships}

Para definir conexões lógicas entre tabelas no esquema, siga as etapas abaixo.

1. Acesse a visualização da tela do modelo de dados e escolha as duas tabelas que deseja vincular

1. Clique no botão ![](assets/do-not-localize/Smock_AddCircle_18_N.svg) ao lado do Source Join e arraste e guie a seta em direção ao Target Join para estabelecer a conexão.

   ![](assets/admin_schema_5.png)

1. Preencha o formulário fornecido para definir o link e clique em **Aplicar** depois de configurado.

   ![](assets/admin_schema_3.png)

   **Cardinalidade**:

   * **1-N**: uma ocorrência da tabela de origem pode ter várias ocorrências correspondentes da tabela de destino, mas uma ocorrência da tabela de destino pode ter no máximo uma ocorrência correspondente da tabela de origem.

   * **N-1**: uma ocorrência da tabela de destino pode ter várias ocorrências correspondentes da tabela de origem, mas uma ocorrência da tabela de origem pode ter no máximo uma ocorrência correspondente da tabela de destino.

   * **1-1**: uma ocorrência da tabela de origem pode ter no máximo uma ocorrência correspondente da tabela de destino.

1. Todos os links definidos no modelo de dados são representados como setas na exibição da tela. Clique em uma seta entre duas tabelas para exibir detalhes, fazer edições ou remover o link, conforme necessário.

   ![](assets/admin_schema_6.png)

1. Use a barra de ferramentas para personalizar e ajustar a tela.

   ![](assets/toolbar.png)

   * **Ampliar**: aumente a tela para ver mais detalhes do seu modelo de dados com mais clareza.

   * **Reduzir**: reduza o tamanho da tela para obter uma exibição mais ampla do seu modelo de dados.

   * **Ajustar exibição**: ajuste o zoom para ajustar todos os esquemas dentro da área visível.

   * **Filtro**: escolha o esquema a ser exibido na tela.

   * **Forçar layout automático**: Organiza esquemas automaticamente para uma melhor organização.

   * **Exibir mapa**: alternar uma sobreposição de minimapa para ajudar a navegar mais facilmente por layouts de esquema grandes ou complexos.

1. Clique em **Salvar** depois de concluído. Essa ação cria os esquemas e conjuntos de dados associados e habilita o conjunto de dados para uso em Campanhas orquestradas.

1. Clique em **[!UICONTROL Abrir trabalhos]** para monitorar o progresso do trabalho de criação. Esse processo pode levar alguns minutos, dependendo do número de tabelas definidas no arquivo DDL.

   ![](assets/admin_schema_4.png)

## Esquema de link {#link-schema}

Estabeleça uma relação entre o esquema **transações de fidelidade** e o esquema **Destinatários** para associar cada transação ao registro de cliente correto.

1. Navegue até **[!UICONTROL Esquemas]** e abra as **transações de fidelidade** criadas anteriormente.

1. Clique em **[!UICONTROL Adicionar relacionamento]** nas **[!UICONTROL Propriedades do campo]** do cliente.

   ![](assets/schema_1.png)

1. Selecione **[!UICONTROL De muitos para um]** como o **[!UICONTROL Tipo]** de relação.

1. Link para o esquema existente **Recipients**.

   ![](assets/schema_2.png)

1. Insira um **[!UICONTROL Nome do relacionamento do esquema atual]** e **[!UICONTROL Nome do relacionamento do esquema de referência]**.

1. Clique em **[!UICONTROL Aplicar]** para salvar as alterações.

Continue criando uma relação entre o esquema **recompensas de fidelidade** e o esquema **Marcas** para associar cada entrada de recompensa à marca apropriada.

![](assets/schema_3.png)

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