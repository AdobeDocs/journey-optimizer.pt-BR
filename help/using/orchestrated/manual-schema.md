---
solution: Journey Optimizer
product: journey optimizer
title: Etapas de configuração
description: Saiba como criar esquemas relacionais diretamente pela interface do usuário.
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 8c785431-9a00-46b8-ba54-54a10e288141
source-git-commit: 3dc0bf4acc4976ca1c46de46cf6ce4f2097f3721
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 3%

---

# Configurar um esquema relacional manual {#manual-schema}

+++ Sumário

| Bem-vindo às campanhas orquestradas | Lançar a primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](gs-orchestrated-campaigns.md)<br/><br/>Criar e gerenciar Esquemas e Conjuntos de Dados relacionais:</br><ul><li>[Introdução a Esquemas e Conjuntos de Dados](gs-schemas.md)</li><li>[Esquema manual](manual-schema.md)</li><li>[Esquema de carregamento de arquivo](file-upload-schema.md)</li><li>[Assimilar dados](ingest-data.md)</li></ul>[Acesse e gerencie campanhas orquestradas](access-manage-orchestrated-campaigns.md)<br/><br/>[Etapas principais para criar uma campanha orquestrada](gs-campaign-creation.md) | [Criar e agendar a campanha](create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](orchestrate-activities.md)<br/><br/>[Iniciar e monitorar a campanha](start-monitor-campaigns.md)<br/><br/>[Relatórios](reporting-campaigns.md) | [Trabalhar com o construtor de regras](orchestrated-rule-builder.md)<br/><br/>[Criar a primeira consulta](build-query.md)<br/><br/>[Editar expressões](edit-expressions.md)<br/><br/>[Redirecionamento](retarget.md) | [Introdução às atividades](activities/about-activities.md)<br/><br/>Atividades:<br/>[And-join](activities/and-join.md) - [Criar público](activities/build-audience.md) - [Alterar dimensão](activities/change-dimension.md) - [Atividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Desduplicação](activities/deduplication.md) - [Enriquecimento](activities/enrichment.md) - [Bifurcação](activities/fork.md) - [Reconciliação](activities/reconciliation.md) - [Salvar público](activities/save-audience.md) - [Divisão](activities/split.md) - [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

O conteúdo desta página não é final e pode estar sujeito a alterações.

>[!ENDSHADEBOX]

Esquemas relacionais podem ser criados diretamente por meio da interface do usuário, permitindo a configuração detalhada de atributos, chaves primárias, campos de versionamento e relacionamentos.

O exemplo a seguir define manualmente o esquema **Associações de fidelidade** para ilustrar a estrutura necessária para campanhas orquestradas.

1. [Crie um esquema relacional manualmente](#schema) usando a interface do Adobe Experience Platform.

1. [Adicionar atributos](#schema-attributes), como ID de cliente, nível de associação e campos de status.

1. [Vincule seu esquema](#link-schema) a esquemas internos, como Recipients para direcionamento de campanha.

1. [Crie um conjunto de dados](#dataset) com base no seu esquema e habilite-o para uso em campanhas orquestradas.

1. [Assimilar dados](ingest-data.md) em seu conjunto de dados de fontes compatíveis.

## Criar seu esquema {#schema}

Comece criando um novo esquema relacional manualmente no Adobe Experience Platform. Esse processo permite definir a estrutura do schema do zero, incluindo seu nome e comportamento.

1. Faça logon no Adobe Experience Platform.

1. Navegue até o menu **[!UICONTROL Gerenciamento de Dados]** > **[!UICONTROL Esquema]**.

1. Clique em **[!UICONTROL Criar Esquema]**.

1. Selecione **[!UICONTROL Relacional]** como seu **Tipo de esquema**.

   ![](assets/admin_schema_1.png){zoomable="yes"}

1. Escolha **[!UICONTROL Criar manualmente]** para criar o esquema adicionando campos manualmente.

1. Insira seu **[!UICONTROL nome para exibição do esquema]**.

1. Escolha **[!UICONTROL Registro]** como seu **[!UICONTROL Comportamento de esquema]**.

   ![](assets/schema_manual_8.png){zoomable="yes"}

1. Clique em **Concluir** para prosseguir para a criação do esquema.

Agora é possível começar a adicionar atributos ao esquema para definir sua estrutura.

## Adicionar atributos ao esquema {#schema-attributes}

Em seguida, adicione atributos para definir a estrutura do esquema. Esses campos representam os principais pontos de dados usados em campanhas orquestradas, como identificadores de clientes, detalhes de associação e datas de atividade. Defini-los com precisão garante personalização, segmentação e rastreamento confiáveis.

1. Na tela, clique em ![](assets/do-not-localize/Smock_AddCircle_18_N.svg) ao lado do seu **Nome do esquema** para começar a adicionar atributos.

   ![](assets/schema_manual_1.png){zoomable="yes"}

1. Insira seu atributo **[!UICONTROL Nome do campo]**, **[!UICONTROL Nome de exibição]** e **[!UICONTROL Tipo]**.

   Neste exemplo, adicionamos os atributos detalhados na tabela abaixo ao esquema **Associações de fidelidade**.

+++ Exemplos de atributos

   | Nome do atributo | Tipo de dados | Atributos Adicionais |
   |-|-|-|
   | cliente | STRING | Chave primária |
   | nível_de_associação | STRING | Obrigatório |
   | points_balance | INTEIRO | Obrigatório |
   | enrollment_date | DATA | Obrigatório |
   | last_status_change | DATA | Obrigatório |
   | data_expiração | DATA | - |
   | is_ative | BOOLEANO | Obrigatório |
   | última modificação | DATETIME | Obrigatório |

+++

1. Atribua os campos apropriados como a **[!UICONTROL Chave Primária]** e o **[!UICONTROL Descritor de Versão]**.

   A **[!UICONTROL Chave Primária]** garante que cada registro seja identificado exclusivamente, enquanto o **[!UICONTROL Descritor de Versão]** captura atualizações ao longo do tempo, habilitando o Change Data Capture e o espelhamento de dados de suporte.

   ![](assets/schema_manual_2.png){zoomable="yes"}

1. Clique em **[!UICONTROL Salvar]**.

Depois que os atributos forem criados, é necessário vincular o esquema recém-criado a um esquema incorporado.

## Vincular esquemas {#link-schema}

Criar uma relação entre dois esquemas permite enriquecer suas campanhas orquestradas com dados armazenados fora do esquema de perfil primário.

1. Em seu esquema recém-criado, selecione o atributo que deseja usar como link e clique em **[!UICONTROL Adicionar relacionamento]**.

   ![](assets/schema_manual_3.png){zoomable="yes"}

1. Escolha o **[!UICONTROL Esquema de referência]** e o **[!UICONTROL Campo de referência]** para estabelecer a relação com.

   Neste exemplo, o atributo `customer` está vinculado ao esquema `recipients`.

   ![](assets/schema_manual_4.png){zoomable="yes"}

1. Insira um nome de Relacionamento do esquema atual e do esquema de referência.

1. Clique em **[!UICONTROL Aplicar]** depois de configurado.

Depois que a relação for estabelecida, é necessário criar um conjunto de dados com base no esquema.

## Criar um conjunto de dados para o esquema {#dataset}

Depois de definir seu esquema, a próxima etapa é criar um conjunto de dados com base nele. Esse conjunto de dados armazena seus dados assimilados e deve ser ativado para Campanhas orquestradas para torná-lo acessível no Adobe Journey Optimizer. Habilitar essa opção garante que o conjunto de dados seja reconhecido para uso em workflows de orquestração e personalização em tempo real.

1. Navegue até o menu **[!UICONTROL Data Management]** > **[!UICONTROL Datasets]** e clique em **[!UICONTROL Criar conjunto de dados]**.

   ![](assets/schema_manual_5.png){zoomable="yes"}

1. Selecione **[!UICONTROL Criar conjunto de dados do esquema]**.

1. Escolha o esquema criado anteriormente, aqui **Associações de fidelidade**, e clique em **[!UICONTROL Avançar]**.

   ![](assets/schema_manual_6.png){zoomable="yes"}

1. Insira um **[!UICONTROL Nome]** para seu **[!UICONTROL Conjunto de Dados]** e clique em **[!UICONTROL Concluir]**.

1. Habilite a opção **Campanhas orquestradas** para disponibilizar o conjunto de dados para uso em suas campanhas do AJO.

   A ativação pode levar alguns minutos. A assimilação de dados só é possível depois que a opção é totalmente ativada.

   ![](assets/schema_manual_7.png){zoomable="yes"}

Agora é possível começar a assimilar dados no esquema usando a fonte de sua escolha.

➡️ [Saiba como assimilar dados](ingest-data.md)
