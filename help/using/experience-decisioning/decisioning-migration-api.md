---
title: API de migração de decisão
description: Saiba como usar a API do serviço de migração do Decisioning para migrar objetos de Gestão de decisões entre sandboxes com resolução de dependência automatizada e suporte de reversão.
feature: Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 3ec084ca-af9e-4b5e-b66f-ec390328a9d6
source-git-commit: 7b1b79e9263aa2512cf69cb130f322a1558eecff
workflow-type: tm+mt
source-wordcount: '1154'
ht-degree: 4%

---

# API de migração de decisão {#decisioning-migration-api}

A API do serviço de migração de decisão permite migrar objetos de Gestão de decisões de uma sandbox para outra. O processo de migração é executado como fluxos de trabalho assíncronos que incluem análise de dependência, execução e recursos opcionais de reversão.

Essa API permite fazer a transição perfeita do conteúdo de decisão entre ambientes (por exemplo, do desenvolvimento ao preparo ou do preparo à produção), mantendo a integridade e os relacionamentos dos dados.

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

Antes de executar uma migração, verifique se a sandbox de destino está configurada corretamente:

* **Atributos** - Verifique se os atributos de perfil e os atributos de contexto necessários existem na sandbox de destino ou prepare mapeamentos para eles.
* **Segmentos** - Verifique se os segmentos necessários existem na sandbox de destino ou planeje mapeá-los usando namespace e ID.
* **Conjunto de dados** - Identifique um nome de conjunto de dados a ser usado para a migração (`dependency.datasetName`).
* **Sequência de dados** - Decida se a migração deve criar uma sequência de dados (`createDataStream`).

Para obter mais informações sobre o gerenciamento de sandboxes, consulte [Usar e atribuir sandboxes](../administration/sandboxes.md).

## Noções básicas sobre API {#api-basics}

### URLs base {#base-urls}

Use os seguintes URLs base, dependendo do seu ambiente:

* **Produção**: `https://decisioning-migration.adobe.io`
* **Estágios**: `https://decisioning-migration-stage.adobe.io`

### Autenticação {#authentication}

Todas as solicitações de API exigem os seguintes cabeçalhos:

* `Authorization: Bearer <IMS_ACCESS_TOKEN>`
* `x-gw-ims-org-id: <IMS_ORG_ID>`
* `Content-Type: application/json`

Para obter instruções detalhadas sobre como configurar a autenticação, consulte o [guia de autenticação do Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}.

### Modelo de fluxo de trabalho {#workflow-model}

Cada chamada de API cria ou recupera um recurso de workflow. Workflows são operações assíncronas que controlam o progresso e os resultados de tarefas de migração.

Um workflow tem as seguintes propriedades:

* `id` - Identificador de fluxo de trabalho exclusivo (UUID)
* `status` - Status atual do fluxo de trabalho: `New`, `Running`, `Completed` ou `Failed`
* `result` - Saída de fluxo de trabalho quando concluído (inclui resultados e avisos de migração)
* `errors` - Detalhes de erros estruturados quando com falha
* `_etag` - Identificador de versão usado para operações de exclusão (somente usuários do serviço)
* `_links.self` - URL do fluxo de trabalho para recuperar o status

## Fluxo de trabalho de migração {#migration-workflow}

O processo de migração consiste em duas etapas principais: analisar dependências e executar a migração. Siga estas etapas para garantir uma migração bem-sucedida.

### Etapa 1: Analisar dependências {#analyze-dependencies}

Antes de migrar, use o fluxo de trabalho de dependência para identificar o que precisa ser mapeado da Gestão de decisões para a Decisão na sandbox de destino. Essa análise ajuda a entender as relações entre objetos e preparar os mapeamentos necessários.

#### Criar um fluxo de trabalho de dependência {#create-dependency-workflow}

Use a chamada de API a seguir para criar um fluxo de trabalho de análise de dependência.

**Formato da API**

```http
POST /workflows/generate-dependencies
```

**Dependência em nível de sandbox (recomendada primeiro)**

Comece com uma análise em nível de sandbox para obter uma visualização completa de todas as dependências:

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

**Dependência no nível da oferta**

Para analisar dependências somente para ofertas específicas, defina `requestLevel: "offer"` e forneça uma matriz `offersList` com as IDs de oferta que você deseja analisar.

**Dependência de nível de decisão**

Para analisar dependências somente para decisões específicas, defina `requestLevel: "decision"` e forneça uma matriz `decisionsList` com as IDs de decisão que você deseja analisar.

#### Verificar status do fluxo de trabalho de dependência {#poll-dependency-status}

Consulte o fluxo de trabalho de dependência para verificar quando a análise é concluída.

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

Quando o campo `status` mostra `Completed`, a análise de dependência está pronta. Use a saída do fluxo de trabalho para criar os mapeamentos de dependência de migração:

* **profileAttributes** - Mapeia atributos de perfil de origem para atributos de perfil de destino
* **contextAttributes** - Mapeia atributos de contexto de origem para atributos de contexto de destino
* **segmentos** - Mapeia chaves de segmento de origem para identificadores de segmento de destino (`{namespace, id}`)
* **datasetName** - Especifica o nome do conjunto de dados de destino para a migração

### Etapa 2: Executar a migração {#execute-migration}

Depois de analisar as dependências e preparar os mapeamentos, você pode executar a migração.

#### Criar um fluxo de trabalho de migração {#create-migration-workflow}

Use os mapeamentos de dependência da Etapa 1 para configurar e executar a migração.

**Formato da API**

```http
POST /workflows/migration
```

**Migração no nível da sandbox**

Para migrar todos os objetos de decisão de uma sandbox para outra:

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

**Migração no nível da oferta**

Para migrar somente ofertas específicas, use `requestLevel: "offer"` e adicione uma matriz `offersList`:

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

## Limpeza do fluxo de trabalho {#cleanup}

Os recursos de fluxo de trabalho podem ser excluídos somente por usuários do serviço. As operações de exclusão exigem um cabeçalho `If-Match` com o valor `_etag` do fluxo de trabalho.

**Operações de exclusão disponíveis:**

* `DELETE /workflows/generate-dependencies/{id}`
* `DELETE /workflows/migration/{id}`
* `DELETE /workflows/rollback/{id}`

>[!NOTE]
>
>A exclusão de fluxo de trabalho só está disponível para contas de serviço com permissões apropriadas. Se precisar excluir um recurso de fluxo de trabalho, entre em contato com o administrador do sistema.

## Tópicos relacionados {#related-topics}

* [Migrar da Gestão de decisões para a Decisão](migrate-to-decisioning.md) - Entenda os benefícios e recursos da migração para a Decisão
* [Introdução ao serviço de decisão](gs-experience-decisioning.md)
* [Medidas de proteção e limitações da decisão](decisioning-guardrails.md)
* [Introdução às APIs de tomada de decisão](api-reference/getting-started.md)
