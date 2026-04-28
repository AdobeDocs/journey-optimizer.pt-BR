---
title: API de migração de decisão
description: Saiba como usar a API do serviço de migração do Decisioning para migrar objetos de Gestão de decisões entre sandboxes com resolução de dependência automatizada e suporte de reversão.
feature: Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 3ec084ca-af9e-4b5e-b66f-ec390328a9d6
source-git-commit: 1ee6f9d74b83ca2b9c2cc0336af0f23a42f4da4f
workflow-type: tm+mt
source-wordcount: '1143'
ht-degree: 4%

---

# API de migração de decisão {#decisioning-migration-api}

A API do serviço de migração de decisão permite migrar objetos de Gestão de decisões de uma sandbox para outra. O processo de migração é executado como fluxos de trabalho assíncronos que incluem análise de dependência, execução e recursos opcionais de reversão.

Essa API permite fazer a transição perfeita do conteúdo de decisão entre ambientes <!--(e.g., from development to staging, or staging to production) -->, mantendo a integridade dos dados e as relações.

Para saber mais sobre os benefícios e recursos do Decisioning em comparação ao Gerenciamento de decisão, consulte [esta página](migrate-to-decisioning.md).

## Recursos {#capabilities}

A API do Serviço de migração do Decisioning fornece os seguintes recursos:

* **Análise de dependência** - Identifique todas as dependências necessárias entre as sandboxes de origem e destino, incluindo atributos, segmentos e requisitos do conjunto de dados.
* **Escopo de migração flexível** - Execute migrações em nível de sandbox, oferta ou decisão de acordo com suas necessidades.
* **Suporte à reversão** - Reverter uma migração concluída se forem descobertos problemas durante a validação.

## Pré-requisitos {#prerequisites}

### Permissões necessárias {#permissions}

Para usar a API de migração, você precisa das permissões apropriadas nas sandboxes de origem e destino:

**Sandbox do Source** - Acesso de leitura a objetos de Gestão de decisões

**Sandbox do Target** - Criar e editar o acesso a objetos do Decisioning

As permissões típicas incluem:

* Gerenciar/Exibir decisão
* Gerenciar/Exibir Decisões
* Gerenciar ofertas
* Gerenciar estratégias de classificação
* Gerenciar campanhas (se estiver migrando artefatos relacionados à campanha)
* Gerenciar/exibir fluxos de dados (se estiver criando um fluxo de dados)
* Gerenciar / Exibir esquemas

>[!NOTE]
>
>Saiba como atribuir permissões de decisão em [esta seção](gs-experience-decisioning.md#steps). Para obter a lista completa de permissões, consulte a página [Permissões internas](../administration/ootb-permissions.md#ootb-permissions).

### Preparar sua sandbox de destino {#target-sandbox-preparation}

Before running a migration, ensure your target sandbox is properly configured:

* **Attributes** - Verify that required profile attributes and context attributes exist in the target sandbox, or prepare mappings for them.
* **Segments** - Ensure required segments exist in the target sandbox, or plan to map them using namespace and ID.
* **Dataset** - Identify a dataset name to use for the migration (`dependency.datasetName`).
* **Datastream** - Decide whether the migration should create a datastream (`createDataStream`).

For more information about sandbox management, refer to [Use and assign sandboxes](../administration/sandboxes.md).

## Noções básicas sobre API {#api-basics}

### URL base {#base-url}

Use the following base URL:

* **Production**: `https://decisioning-migration.adobe.io`
  <!--* **Staging**: `https://decisioning-migration-stage.adobe.io`-->

### Autenticação {#authentication}

All API requests require the following headers:

* `Authorization: Bearer <IMS_ACCESS_TOKEN>`
* `x-gw-ims-org-id: <IMS_ORG_ID>`
* `Content-Type: application/json`

For detailed instructions on setting up authentication, refer to the [Journey Optimizer authentication guide](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}.

### Workflow model {#workflow-model}

Each API call creates or retrieves a workflow resource. Workflows are asynchronous operations that track the progress and results of migration tasks.

A workflow has the following properties:

* `id` - Unique workflow identifier (UUID)
* `status` - Current workflow status: `New`, `Running`, `Completed`, or `Failed`
* `result` - Workflow output when completed (includes migration results and warnings)
* `errors` - Structured error details when failed
* `_links.self` - Workflow URL for retrieving status
  <!--* `_etag` - Version identifier used for delete operations (service users only)-->

## Migration workflow {#migration-workflow}

The migration process consists of two main steps: analyzing dependencies and executing the migration. Follow these steps to ensure a successful migration.

### Step 1: Analyze dependencies {#analyze-dependencies}

Before migrating, use the dependency workflow to identify what needs to be mapped from Decision management to Decisioning in your target sandbox. This analysis helps you understand the relationships between objects and prepare the necessary mappings.

#### Create a dependency workflow {#create-dependency-workflow}

Use the following API call to create a dependency analysis workflow.

**Formato da API**

```http
POST /workflows/generate-dependencies
```

**Sandbox-level dependency (recommended first)**

Start with a sandbox-level analysis to get a complete view of all dependencies:

```shell
curl --request POST \
  --url "https://decisioning-migration.adobe.io/workflows/generate-dependencies" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "Content-Type: application/json" \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" },
    "requestLevel": "sandbox"
  }'
```

**Offer-level dependency**

To analyze dependencies for specific offers only, set `requestLevel: "offer"` and provide an `offersList` array with the offer IDs you want to analyze.

**Decision-level dependency**

To analyze dependencies for specific decisions only, set `requestLevel: "decision"` and provide a `decisionsList` array with the decision IDs you want to analyze.

#### Check dependency workflow status {#poll-dependency-status}

Poll the dependency workflow to check when the analysis is complete.

**Formato da API**

```http
GET /workflows/generate-dependencies/{id}
```

**Solicitação**

```shell
curl --request GET \
  --url "https://decisioning-migration.adobe.io/workflows/generate-dependencies/<WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>"
```

When the `status` field shows `Completed`, the dependency analysis is ready. Use the workflow output to build your migration dependency mappings:

* **profileAttributes** - Maps source profile attributes to target profile attributes
* **contextAttributes** - Maps source context attributes to target context attributes
* **segments** - Maps source segment keys to target segment identifiers (`{namespace, id}`)
* **datasetName** - Specifies the target dataset name for the migration

### Step 2: Execute the migration {#execute-migration}

Once you have analyzed the dependencies and prepared your mappings, you can execute the migration.

#### Create a migration workflow {#create-migration-workflow}

Use the dependency mappings from Step 1 to configure and execute your migration.

**Formato da API**

```http
POST /workflows/migration
```

**Sandbox-level migration**

To migrate all decisioning objects from one sandbox to another:

```shell
curl --request POST \
  --url "https://decisioning-migration.adobe.io/workflows/migration" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "Content-Type: application/json" \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" },
    "createDataStream": true,
    "dependency": {
      "profileAttributes": {
        "sourceAttr1": "targetAttr1"
      },
      "segments": {
        "sourceSegmentKey1": {
          "namespace": "<TARGET_SEGMENT_NAMESPACE>",
          "id": "<TARGET_SEGMENT_ID>"
        }
      },
      "contextAttributes": {
        "sourceCtx1": "targetCtx1"
      },
      "datasetName": "<TARGET_DATASET_NAME>"
    },
    "requestLevel": "sandbox"
  }'
```

**Offer-level migration**

To migrate specific offers only, use `requestLevel: "offer"` and add an `offersList` array:

```json
"offersList": ["offer-id-1", "offer-id-2"]
```

**Migração de nível de decisão**

Para migrar apenas decisões específicas, use `requestLevel: "decision"` e adicione uma matriz `decisionsList`:

```json
"decisionsList": ["decision-id-1", "decision-id-2"]
```

#### Monitorar status da migração {#poll-migration-status}

Consulte o fluxo de trabalho de migração para acompanhar seu progresso.

**Formato da API**

```http
GET /workflows/migration/{id}
```

**Solicitação**

```shell
curl --request GET \
  --url "https://decisioning-migration.adobe.io/workflows/migration/<WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>"
```

**Resultados da migração**

Quando o campo `status` mostra `Completed`, a migração foi bem-sucedida. O fluxo de trabalho `result` inclui:
* Mapeamentos de objetos migrados
* Qualquer aviso encontrado durante a migração

Quando o campo `status` mostrar `Failed`, revise a matriz `errors[]` e o campo `result.error` para obter detalhes sobre o que deu errado.

## Validar sua migração {#validate-migration}

Depois que a migração for concluída com êxito, verifique se todos os objetos foram migrados corretamente.

### Lista de verificação de validação {#validation-checklist}

1. **Segmentos** - Verifique se todos os segmentos referenciados são resolvidos corretamente na sandbox de destino de acordo com seus mapeamentos.
2. **Atributos** - Confirme se todos os atributos de perfil e de contexto existem na sandbox de destino e estão mapeados corretamente.
3. **Objetos de decisão** - Revise os objetos migrados na interface do usuário do Journey Optimizer:
   * Ofertas (itens de decisão)
   * Regras de elegibilidade
   * Fórmulas de classificação
   * Estratégias de seleção
   * Políticas de decisão
4. **Teste de sequência de dados** - Se uma sequência de dados tiver sido criada, teste a entrega em tempo de execução usando a API Edge Interact.

### Exemplo {#test-runtime-delivery}

Se a migração criou um fluxo de dados, você pode testar a entrega de ofertas usando o seguinte exemplo:

```shell
curl --request POST \
  --url "https://edge.adobedc.net/ee/or2/v1/interact?configId=<DATASTREAM_ID>" \
  --header "Content-Type: application/json" \
  --header "x-request-id: <uuid>" \
  --data '{ "events": [ ... ] }'
```

## Reverter uma migração {#rollback}

Se você descobrir problemas durante a validação, poderá reverter uma migração concluída para restaurar a sandbox de destino ao seu estado anterior.

### Criar um fluxo de trabalho de reversão {#create-rollback-workflow}

Inicie uma reversão criando um fluxo de trabalho de reversão que faça referência à migração que você deseja reverter.

**Formato da API**

```http
POST /workflows/rollback
```

**Solicitação**

```shell
curl --request POST \
  --url "https://decisioning-migration.adobe.io/workflows/rollback" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "Content-Type: application/json" \
  --data '{ "rollbackWorkflowId": "<MIGRATION_WORKFLOW_ID>" }'
```

Substitua `<MIGRATION_WORKFLOW_ID>` pela ID do fluxo de trabalho de migração que você deseja reverter.

### Monitorar status de reversão {#poll-rollback-status}

Consulte o workflow de reversão para acompanhar seu progresso.

**Formato da API**

```http
GET /workflows/rollback/{rollbackWorkflowId}
```

**Solicitação**

```shell
curl --request GET \
  --url "https://decisioning-migration.adobe.io/workflows/rollback/<ROLLBACK_WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>"
```

## Lidar com fluxos de trabalho simultâneos {#handle-concurrency}

A API de migração permite que apenas um fluxo de trabalho seja executado por vez por organização. Se você tentar criar um novo fluxo de trabalho enquanto outro estiver em andamento, você receberá uma resposta de erro **409 Conflito** (&quot;Um fluxo de trabalho já está em andamento...&quot;).

Nesse caso, aguarde a conclusão do workflow em andamento ou recupere a ID do workflow e sonde seu status. Quando o fluxo de trabalho atual for concluído, você poderá criar um novo.

## Referência de mapeamento de entidade {#entity-mapping}

Ao migrar da Gestão de decisões para o Decisioning, as entidades são mapeadas da seguinte maneira:

| Gestão de decisões | Tomada de decisão |
|-------------------|-------------|
| Oferta | Item de decisão |
| Coleção de ofertas | Coleção de itens |
| Regra de elegibilidade | Regra de elegibilidade |
| Fórmula de classificação | Fórmula de classificação |
| Decisão | Estratégia de seleção + política de decisão |
| Campaign | Campanha *(somente conteúdo básico)* |
| Posicionamento | Superfície + Configuração de canal |
| Tag | Tag unificada |
| Atributos de oferta | Campo `migratedofferattributes` no esquema de item de oferta personalizado |
| Atributos de contexto | Campo `migratedcontextattributes` no esquema anexado ao conjunto de dados fornecido durante a migração |

## Limpeza do fluxo de trabalho {#cleanup}

<!--
Workflow resources can be deleted by service users only. Delete operations require an `If-Match` header with the workflow's `_etag` value.

**Available delete operations:**

* `DELETE /workflows/generate-dependencies/{id}`
* `DELETE /workflows/migration/{id}`
* `DELETE /workflows/rollback/{id}`
-->

A exclusão de fluxo de trabalho não está disponível publicamente. Se precisar excluir um recurso de fluxo de trabalho, entre em contato com o administrador do sistema.

## Tópicos relacionados {#related-topics}

* [Migrar da Gestão de decisões para a Decisão](migrate-to-decisioning.md) - Entenda os benefícios e recursos da migração para a Decisão
* [Introdução ao serviço de decisão](gs-experience-decisioning.md)
* [Medidas de proteção e limitações da decisão](decisioning-guardrails.md)
* [Introdução às APIs de tomada de decisão](api-reference/getting-started.md)
