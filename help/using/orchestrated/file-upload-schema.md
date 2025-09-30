---
solution: Journey Optimizer
product: journey optimizer
title: Etapas de configuração
description: Saiba como criar um esquema baseado em modelo no Adobe Experience Platform fazendo upload de uma DDL
exl-id: 88eb1438-0fe5-4a19-bfb6-2968a427e9e8
version: Campaign Orchestration
source-git-commit: e189bb6a52691770655a436e45c6788d1011a8ca
workflow-type: tm+mt
source-wordcount: '1080'
ht-degree: 46%

---


# Criar esquemas baseados em modelo usando um arquivo DDL {#file-upload-schema}

Defina o modelo de dados baseado em modelo necessário para campanhas orquestradas, criando esquemas como **Associações de Fidelidade**, **Transações de Fidelidade** e **Recompensas de Fidelidade**. Cada esquema deve incluir uma chave primária, um atributo de controle de versão e relações apropriadas com entidades de referência, como **Destinatários** ou **Marcas**.

Os esquemas podem ser criados manualmente por meio da interface ou importados em massa usando um arquivo DDL.

Esta seção fornece orientação passo a passo sobre como criar um esquema baseado em modelo no Adobe Experience Platform fazendo upload de um arquivo DDL (Data Definition Language). Usar um arquivo DDL permite definir a estrutura do modelo de dados com antecedência, incluindo tabelas, atributos, chaves e relacionamentos.

1. [Carregue um arquivo DDL](#ddl-upload) para criar esquemas baseados em modelo e definir sua estrutura.

1. [Definir relações](#relationships) entre tabelas no modelo de dados.

1. [Vincule esquemas](#link-schema) para conectar seus dados baseados em modelo a entidades de perfil existentes, como Destinatários ou Marcas.

1. [Assimile dados](ingest-data.md) em seu conjunto de dados de fontes compatíveis.

➡️ [Saiba mais sobre esquemas baseados em modelo na documentação do Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/xdm/schema/model-based)

## Fazer upload de um arquivo DDL{#ddl-upload}

Ao fazer upload de um arquivo DDL, você pode definir a estrutura do modelo de dados antecipadamente, incluindo tabelas, atributos, chaves e relacionamentos.

Os uploads de arquivo de esquema baseados em Excel são compatíveis. Baixe o [modelo fornecido](assets/template.zip) para preparar facilmente as definições do esquema.

+++Os seguintes recursos são compatíveis ao criar esquemas baseados em modelo no Adobe Experience Platform

* **ENUMERAÇÃO**\
  Os campos ENUM são suportados na criação de esquema manual e baseado em DDL, permitindo que você defina atributos com um conjunto fixo de valores permitidos.
Exemplo:

  ```
  CREATE TABLE orders (
  order_id     INT NOT NULL,
  product_id   INT NOT NULL,
  order_date   DATE NOT NULL,
  customer_id  INT NOT NULL,
  quantity     INT NOT NULL,
  order_status enum ('PENDING', 'SHIPPED', 'DELIVERED', 'CANCELLED'),
  PRIMARY KEY (order_id, product_id)
  );
  ```

* **Rótulo do esquema para governança de dados**\
  A rotulagem é compatível no nível do campo de esquema para aplicar políticas de governança de dados, como controle de acesso e restrições de uso. Para obter mais detalhes, consulte a [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR).

* **Chave Composta**\
  As chaves primárias compostas são compatíveis com definições de esquema baseadas em modelo, permitindo o uso de vários campos juntos para identificar registros de forma exclusiva.

+++

1. Faça logon no Adobe Experience Platform.

1. Navegue até o menu **Gerenciamento de Dados** > **Esquema**.

1. Clique em **Criar Esquema**.

1. Selecione **[!UICONTROL Baseado em modelo]** como seu **Tipo de esquema**.

   ![](assets/admin_schema_1.png)

1. Selecione **[!UICONTROL Fazer upload de arquivo DDL]** para definir um diagrama de relações de entidades e criar esquemas.

   A estrutura da tabela precisa conter:
   * Pelo menos uma chave primária.
   * Um identificador de versão, como um campo `lastmodified` do tipo `datetime` ou `number`.
   * Para a assimilação do CDC (Change Data Capture), uma coluna especial chamada `_change_request_type` do tipo `String`, que indica o tipo de alteração de dados (por exemplo, inserir, atualizar, excluir) e habilita o processamento incremental.
   * O arquivo DDL não deve definir mais de 200 tabelas.


   >[!IMPORTANT]
   >
   > Qualquer esquema usado para direcionamento deve incluir pelo menos um campo de identidade do tipo `String` com um **namespace de identidade** associado.\
   >Isso garante a compatibilidade com os recursos de definição de metas e resolução de identidade da Adobe Journey Optimizer.

1. Arraste e solte o arquivo DDL, e clique em **[!UICONTROL Próximo]**.

   Observe que o tamanho máximo suportado para um arquivo DDL é 10 MB.

1. Digite o **[!UICONTROL Nome do esquema]**.

1. Configure cada esquema e suas colunas, garantindo que uma chave primária e um descritor de versão sejam especificados.

   Um atributo, como `lastmodified`, deve ser designado como descritor de versão (tipo `datetime`, `long` ou `int`) para garantir que os conjuntos de dados sejam atualizados com os dados mais recentes. Os usuários podem alterar o descritor de versão, que se torna obrigatório depois de definido. Um atributo não pode ser uma chave primária (PK) e um descritor de versão ao mesmo tempo.

   ![](assets/admin_schema_2.png)

1. Marcar um atributo como `identity` e mapeá-lo para um namespace de identidade definido.

1. Renomeie, exclua ou adicione uma descrição a cada tabela.

1. Clique em **[!UICONTROL Concluído]** quando terminar.

Agora, é possível verificar a tabela e as definições de campos na tela. [Saiba mais na seção abaixo](#entities)

## Definir relacionamentos {#relationships}

Você pode especificar relações diretamente no arquivo DDL ao criar seu esquema. Se preferir definir relações fora do arquivo, faça isso na interface seguindo as etapas abaixo.

1. Acesse a visualização da tela do seu modelo de dados e escolha as duas tabelas que deseja vincular

1. Clique no botão ![](assets/do-not-localize/Smock_AddCircle_18_N.svg) ao lado da associação de origem e arraste e guie a seta em direção à associação de público-alvo para estabelecer a conexão.

   >[!NOTE]
   >
   >As chaves compostas terão suporte se forem definidas no arquivo DDL.

   ![](assets/admin_schema_5.png)

1. Preencha o formulário fornecido para definir o vínculo e clique em **Aplicar** depois de configurar.

   ![](assets/admin_schema_3.png)

   **Cardinalidade**:

   * **1-N**: uma ocorrência da tabela de público-alvo pode ter várias ocorrências correspondentes da tabela de destino, mas uma ocorrência da tabela de destino pode ter, no máximo, uma ocorrência correspondente da tabela de origem.

   * **N-1**: uma ocorrência da tabela de destino pode ter várias ocorrências correspondentes da tabela de origem, mas uma ocorrência da tabela de origem pode ter, no máximo, uma ocorrência correspondente da tabela de público-alvo.

   * **1-1**: uma ocorrência da tabela de origem pode ter, no máximo, uma ocorrência correspondente da tabela de público-alvo.

1. Todos os vínculos definidos no modelo de dados são representados como setas na visualização da tela. Clique em uma seta entre duas tabelas para visualizar os detalhes, fazer edições ou remover o vínculo, conforme necessário.

   ![](assets/admin_schema_6.png)

1. Use a barra de ferramentas para personalizar e ajustar a tela.

   ![](assets/toolbar.png)

   * **Aumentar zoom**: amplie a tela para ver mais detalhes do seu modelo de dados com mais clareza.

   * **Diminuir zoom**: reduza o tamanho da tela para obter uma visualização mais ampla do seu modelo de dados.

   * **Ajustar visualização**: ajuste o zoom para ajustar todos os esquemas à área visível.

   * **Filtro**: escolha qual esquema será exibido na tela.

   * **Forçar layout automático**: ordena os esquemas automaticamente para uma melhor organização.

   * **Exibir mapa**: ative uma sobreposição de minimapa para ajudar a navegar mais facilmente por layouts de esquema grandes ou complexos.

1. Clique em **Salvar** quando terminar. Esta ação cria os esquemas e conjuntos de dados associados, e habilita o conjunto de dados para uso em campanhas orquestradas.

1. Clique em **[!UICONTROL Abrir trabalhos]** para monitorar o progresso da tarefa de criação. Esse processo pode levar alguns minutos, dependendo do número de tabelas definidas no arquivo DDL.

   Você também pode acessar seus trabalhos de importação de DDL abrindo a janela **[!UICONTROL Carregar arquivo DDL]** e selecionando **[!UICONTROL Exibir todos os trabalhos de importação de DDL]**.

   ![](assets/admin_schema_4.png)

## Vincular esquemas {#link-schema}

>[!IMPORTANT]
>
> Somente as relações explicitamente definidas no arquivo DDL são reconhecidas pelo sistema. Qualquer relação de entidade que exista fora do arquivo DDL será ignorada e não processada.

Estabeleça uma relação entre o esquema de **Transações de fidelidade** e o esquema de **Destinatários** para associar cada transação ao registro de cliente correto.

1. Navegue até **[!UICONTROL Esquemas]** e abra as **Transações de fidelidade** criadas anteriormente.

1. Clique em **[!UICONTROL Adicionar relacionamento]** nas **[!UICONTROL Propriedades do campo]** do cliente.

   ![](assets/schema_1.png)

1. Selecione **[!UICONTROL De muitos para um]** como o **[!UICONTROL Tipo]** de relação.

1. Vincule ao esquema de **Destinatários** existente.

   ![](assets/schema_2.png)

1. Insira o **[!UICONTROL Nome da relação do esquema atual]** e o **[!UICONTROL Nome da relação do esquema de referência]**.

1. Clique em **[!UICONTROL Aplicar]** para salvar as alterações.

Continue criando um relacionamento entre o esquema de **Recompensas por fidelidade** e o esquema de **Marcas** para associar cada entrada de recompensa à marca apropriada.

![](assets/schema_3.png)
