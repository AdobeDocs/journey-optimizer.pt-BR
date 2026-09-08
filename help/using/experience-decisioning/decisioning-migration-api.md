---
title: API de migração de decisão
description: Saiba como usar a API do serviço de migração do Decisioning para migrar objetos de Gestão de decisões entre sandboxes com resolução de dependência automatizada e suporte de reversão.
feature: Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 3ec084ca-af9e-4b5e-b66f-ec390328a9d6
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
  - id: a984631b-2bae-4860-9b15-69c41a799dcb
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: bf147566ac63bce11f4413a2450b55d436f01d7a
workflow-type: tm+mt
source-wordcount: 3211
ht-degree: 3%

---

# API de migração de decisão {#decisioning-migration-api}

>[!BEGINSHADEBOX]

**Nesta página:** use a API do Serviço de Migração de Decisão para mover objetos de Gerenciamento de decisão entre sandboxes com análise de dependência automatizada e suporte de reversão, para que você possa fazer a transição de conteúdo de decisão entre ambientes, preservando a integridade dos dados.

>[!ENDSHADEBOX]

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

Antes de executar uma migração, verifique se a sandbox de destino está configurada corretamente:

* **Atributos** - Verifique se os atributos de perfil e os atributos de contexto necessários existem na sandbox de destino ou prepare mapeamentos para eles.
* **Segmentos** - Verifique se os segmentos necessários existem na sandbox de destino ou planeje mapeá-los usando namespace e ID.
* **Conjunto de dados** - Identifique um nome de conjunto de dados a ser usado para a migração (`dependency.datasetName`).
* **Sequência de dados** - Decida se a migração deve criar uma sequência de dados (`createDataStream`).

Para obter mais informações sobre o gerenciamento de sandboxes, consulte [Usar e atribuir sandboxes](../administration/sandboxes.md).

>[!NOTE]
>
>A sandbox de destino pode ser igual à sandbox de origem. O processo de migração trata desse cenário e garante a integridade dos dados, independentemente de os objetos serem migrados na mesma sandbox ou para uma diferente.

### Pré-requisitos de migração entre sandboxes {#cross-sandbox-prerequisites}

Quando a sandbox de origem ≠ sandbox de destino, os seguintes itens são necessários:

* **Atributos de Perfil** - Deve existir na sandbox de destino ou ter mapeamentos predefinidos
* **IDs de segmento** - Deve ser pré-criado na sandbox de destino com mapeamentos de ID antigos e novos
* **Mapeamento de Identidade** - Deve ser configurado para resolução de identidade consistente

## Noções básicas sobre API {#api-basics}

### URL base {#base-url}

Use o seguinte URL base:

* **Produção**: `https://decisioning-migration.adobe.io`

### Autenticação {#authentication}

Todas as solicitações de API exigem os seguintes cabeçalhos:

* `Authorization: Bearer <IMS_ACCESS_TOKEN>`
* `x-gw-ims-org-id: <IMS_ORG_ID>`
* `Content-Type: application/json`

Para obter instruções detalhadas sobre como configurar a autenticação, consulte o [guia de autenticação do Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}.

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
  --url "https://decisioning-migration.adobe.io/workflows/generate-dependencies?request-level=sandbox" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "Content-Type: application/json" \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" }
  }'
```

**Dependência no nível da oferta**

Para analisar dependências somente para ofertas específicas, chame o mesmo ponto de extremidade com `request-level=offer` na cadeia de caracteres de consulta e forneça uma matriz `offersList` no corpo com as IDs de oferta que você deseja analisar.

**Dependência de nível de decisão**

Para analisar dependências somente para decisões específicas, use `request-level=decision` na cadeia de caracteres de consulta e forneça uma matriz `decisionsList` no corpo com as IDs de decisão que você deseja analisar.

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
* **segmentos** - Mapeia cada chave de segmento de origem para um identificador de segmento de destino (`{namespace, id}`)
* **datasetName** - O conjunto de dados de Evento de Experiência de destino usado para a migração. Ele deve ser anexado a um fluxo de dados habilitado para chamadas do Journey Optimizer Edge (Web SDK); seu esquema é usado para adicionar os atributos de contexto migrados.

Você fornece esses mapeamentos no objeto `dependency` da solicitação de migração na Etapa 2.

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
  --url 'https://decisioning-migration.adobe.io/workflows/migration?request-level=sandbox' \
  --header 'Authorization: Bearer <IMS_ACCESS_TOKEN>' \
  --header 'Content-Type: application/json' \
  --header 'x-gw-ims-org-id: <IMS_ORG_ID>' \
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
    }
  }'
```

**Migração no nível da oferta**

Para migrar somente ofertas específicas, use `request-level=offer` na cadeia de caracteres de consulta e adicione uma matriz `offersList` ao corpo:

```json
"offersList": ["offer-id-1", "offer-id-2"]
```

**Migração de nível de decisão**

Para migrar apenas decisões específicas, use `request-level=decision` na cadeia de caracteres de consulta e adicione uma matriz `decisionsList` ao corpo:

```json
"decisionsList": ["decision-id-1", "decision-id-2"]
```

**Solicitar campos**

* **nível de solicitação** (consulta) - Escopo de migração: `sandbox`, `offer` ou `decision`.
* **imsOrgId** (obrigatório) - Sua ID da Organização IMS.
* **sourceSandboxDetails.sandboxName** (obrigatório) - sandbox da Source que contém as entidades de gerenciamento de decisão.
* **targetSandboxDetails.sandboxName** (obrigatório) - Sandbox de destino onde as entidades de decisão são criadas.
* **dependency.datasetName** (obrigatório) - Conjunto de dados Evento de Experiência de Destino. Ele deve ser anexado a um fluxo de dados habilitado para chamadas do Journey Optimizer Edge (Web SDK); seu esquema é usado para adicionar os atributos de contexto migrados.
* **createDataStream** - `true` cria uma nova sequência de dados habilitada para Journey Optimizer; `false` reutiliza a já anexada ao conjunto de dados em `dependency.datasetName`.
* **dependency.profileAttributes** - Mapa de origem → atributos de perfil de destino.
* **dependency.contextAttributes** - Mapa de origem → atributos de contexto de destino.
* **dependency.segments** - Mapa da chave do segmento de origem → segmento de destino (`{namespace, id}`).
* **offersList[]** / **DecisionsList[]** - As IDs de oferta ou decisão a serem migradas; necessárias quando `request-level` for `offer` ou `decision`, respectivamente.

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

Cada fluxo de trabalho (dependência, migração e reversão) retorna os mesmos campos de recurso:

* **id** - Identificador de fluxo de trabalho (UUID); sondar seu status com o `GET /{id}` correspondente.
* **status** - Estado do ciclo de vida: `New`, `Running`, `Completed` ou `Failed`.
* **resultado** - Presente em `Completed`; a saída do fluxo de trabalho (por exemplo, mapeamentos de objetos migrados e avisos).
* **erros[]** - Presente em `Failed`; detalhes de erros estruturados (consulte também `result.error`).
* **_links.self** - URL do recurso de fluxo de trabalho.

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

## Escopo e cobertura da migração {#migration-scope}

Compreender o escopo da migração ajuda a planejar e validar a transição da Gestão de decisões para a Decisão. Esta seção descreve o que é abordado pelo processo de migração e o que requer ação manual.

### Dentro do escopo: o que é coberto {#in-scope}

A API de migração lida com os seguintes itens e recursos:

* **Casos de uso** - Somente casos de uso de decisão de entrada/Edge estão no escopo. A migração de canal de email de saída ou de OD no Journey Optimizer é compatível, mas requer atualizações manuais.
* **Campanhas de experiência baseadas em código** - Criadas automaticamente durante a migração, uma campanha por escopo de decisão migrado na sandbox de destino.
* **Configuração/superfície de canal** - Configurações/superfícies de canal criadas por posicionamento de Gestão de decisão, garantindo o roteamento adequado de respostas de decisão.
* **Tipos de conteúdo da oferta** - As ofertas são migradas somente se o tipo de conteúdo for JSON ou Text. Outros tipos de conteúdo exigem recriação manual.
* **Características da oferta** - Preservadas no grupo de campos `offer_item_custom_attributes` no esquema &quot;Itens de oferta personalizados - Experience Decisioning&quot;, mantendo metadados personalizados.
* **Atributos de contexto** - Adicionados ao esquema Evento de experiência no grupo de campos `custom_context_attributes` para rastreamento e personalização.
* **Escopos de decisão** - Um escopo de decisão do gerenciamento de decisão mapeia para uma estratégia de seleção + uma política de decisão + uma campanha no Decisioning, garantindo a hierarquia de entidade adequada.
* **Regras de qualificação somente API** - As regras de elegibilidade criadas somente por API (não na interface do usuário da Gestão de decisões) são migradas e permanecem somente API no Decisioning. As regras criadas pela interface do usuário também são migradas.

### Fora do escopo: o que não é coberto ou requer ação manual {#out-of-scope}

Os seguintes itens exigem ação manual ou não são suportados pelas ferramentas de migração:

* **Posicionamentos de decisão** - Nenhum posicionamento é criado pela ferramenta de migração. Você deve criá-los manualmente na Decisão antes ou depois da migração com base na sua arquitetura.
* **Limite de nível de posicionamento** - O limite de frequência de nível de posicionamento não é migrado.
* **Conteúdo de oferta não-JSON/Text** - Ofertas com tipos de conteúdo diferentes de JSON ou Text (por exemplo, HTML, imagens) NÃO são migradas e exigem recriação manual no Decisioning.
* **Atributos e segmentos de perfil** - Atributos de perfil e associações de segmento NUNCA são criados ou editados por ferramentas de migração. Eles já devem existir na sandbox de destino antes de executar a migração.
* **Mapeamento de ID de segmento** - As IDs de segmento devem ser pré-criadas na sandbox de destino. Você deve fornecer um mapeamento de ID antigo → novo na solicitação da API de migração para a resolução do segmento.
* **Alterações no código de coleta de dados** - As alterações no código de rastreamento de eventos do lado do cliente e do lado do servidor NÃO são automatizadas. Sua equipe de implementação deve atualizar a coleção de eventos para usar os formatos de solicitação/resposta e os esquemas de evento de decisão do Decisioning.

## Referência de mapeamento de entidade {#entity-mapping}

Ao migrar da Gestão de decisões para o Decisioning, as entidades são mapeadas de acordo com a tabela a seguir. Os mapeamentos incluem as entidades Decisioning principais e entidades associadas adicionais criadas ou usadas durante a migração.

### Gestão de decisões para Mapeamento de entidades de decisão

| Entidade de Gestão de Decisões | Entidade de decisão | Entidades Adicionais |
|-----------|--------------|-------------------|
| Decisão | Estratégia de seleção | Coleção de Itens, Regra de Elegibilidade, Fórmula de Classificação |
| | Política de decisão | Contagem de Itens, Estratégias de Seleção, Item da Oferta de Fallback |
| | Campanha de experiência baseada em código | Política de decisão, conteúdo, configuração de canal, fragmentos do Journey Optimizer |
| Posicionamento | Configuração de canais | — |
| Coleção | Coleção de itens | Tags unificadas, itens de oferta |
| Qualificador de Coleção | Tags unificadas | — |
| Regra | Regra de decisão | — |
| Fórmula de Classificação | Fórmula de classificação de decisão | — |
| Oferta | Item de oferta | Regra de elegibilidade, Fragmentos do Journey Optimizer, Tags unificadas, Limite de frequência |
| | Esquema de item de oferta | — |
| | Fragmentos do Journey Optimizer | — |

### Convenções de nomenclatura

O processo de migração aplica convenções de nomenclatura usando o prefixo `ExD_` para garantir a consistência e evitar conflitos de nomenclatura.

| Objeto do Source | Gerenciamento de decisão Padrão de nome | Padrão de nome de decisão |
|---------------|-----------------|-------------------|
| Oferta | `<offerName>` | `ExD_<offerName>` |
| Regra de elegibilidade | `<ruleName>` | `ExD_<ruleName>` |
| Fórmula de Classificação | `<formulaName>` | `ExD_<formulaName>` |
| Coleção | `<collectionName>` | `ExD_<collectionName>_<placementName>` |
| Decisão → Estratégia de seleção | `<decisionName>` | `ExD_<decisionName>_selection_strategy_<index>` |
| Decisão → Política de decisão | `<decisionName>` | `ExD_<decisionName>_<placementName>` |
| Fragmento do Journey Optimizer | `<offerName>` | `ExD_<offerName>_<placementName>_<index>` |
| Posicionamento → Superfície | `<placementName>` | `ExD_<placementName>` *(espaços/pontos convertidos em sublinhados)* |
| Tag unificada | `<sourceName>, <targetName>` | `ExDMigration_<sourceName>_<targetName>` |
| Campanha CBE | `<decisionName>, <placementName>` | `Campaign for <decisionName> : <placementName>` |

### Atributos Adicionais

| Atributo do Source | Local de destino |
|-----------------|-----------------|
| Atributos de oferta | campo &quot;migratedofferattributes&quot; no esquema de item de oferta personalizada |
| Atributos de contexto | campo &quot;migratedcontextattributes&quot; no esquema anexado ao conjunto de dados fornecido durante a migração |

## Modelo de solicitação e resposta {#request-response-model}

Ao migrar da Gestão de decisões para o Decisioning, o código do aplicativo deve ser atualizado para usar os novos formatos de solicitação e resposta. Ambos os sistemas usam o endpoint do Edge Network, mas com estruturas de carga e nomes de campo diferentes.

### Solicitação Edge do Gerenciamento de decisão (Atual) {#dm-request}

A solicitação atual do Edge de Gestão de decisão segue esta estrutura:

**Ponto de extremidade:**

```
POST https://edge.adobedc.net/ee/v2/interact
```

**Cabeçalhos:**
&#x200B;- `Authorization: Bearer <IMS_ACCESS_TOKEN>`
&#x200B;- `x-api-key: <API_KEY>` (do Developer Console)
&#x200B;- `x-gw-ims-org-id: <IMS_ORG_ID>` (formato: `{ORG_ID}@AdobeOrg`)
&#x200B;- `x-request-id: <UNIQUE_REQUEST_ID>` (para rastreamento e desduplicação)
&#x200B;- `Content-Type: application/vnd.adobe.xdm+json; schema="…/decision-request;version=1.0"`
&#x200B;- `Accept: application/vnd.adobe.xdm+json; schema="…/decision-response;version=1.0"`
&#x200B;- `x-sandbox-name: <SANDBOX_NAME>` (por exemplo, prod, dev)

**Solicitar Parâmetros de Corpo:**
&#x200B;- `xdm:dryRun` (verdadeiro/falso) - Testar solicitações sem poluir relatórios
&#x200B;- `xdm:propositionRequests[]` - Matriz de solicitações de decisão:
  &#x200B;- `activityId` - Identificador de atividade de decisão
  &#x200B;- `placementId` - Identificador de posicionamento
  &#x200B;- `itemCount` - Número máximo de ofertas a serem retornadas
&#x200B;- `xdm:profiles[].xdm:identityMap` - Mapeamento de identidade (email, ECID etc.)
&#x200B;- `xdm:validateContextData` - Sinalizador de validação de dados de contexto restrito
&#x200B;- `xdm:responseFormat.xdm:includeContent` - Incluir conteúdo real vs. somente IDs

**Exemplo de corpo de solicitação:**

```json
{
  "xdm": {
    "dryRun": false,
    "propositionRequests": [
      { "activityId": "<ACTIVITY_ID>", "placementId": "<PLACEMENT_ID>", "itemCount": 3 }
    ],
    "profiles": [
      { "identityMap": { "ECID": [ { "id": "<ECID>", "primary": true } ] } }
    ],
    "validateContextData": true,
    "responseFormat": { "includeContent": true }
  }
}
```

>[!NOTE]
>Para obter a referência completa de solicitação/resposta do Gerenciamento de decisão (OD), consulte [API de decisão do Edge](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/decisioning/offer-decisioning/api-reference/offer-delivery-api/edge-decisioning-api) (a variante Web SDK/Edge, que usa `decisionScopes` codificado em base64 carregando `activityId` e `placementId`).

### Solicitação Edge de decisão (após a migração) {#decisioning-request}

Após a migração, use o formato de solicitação de Decisão por meio do mesmo endpoint do Edge Network.

**Ponto de extremidade:**

```
POST https://edge.adobedc.net/ee/v2/interact
```

**Campos-chave de solicitação:**
&#x200B;- `query.identity.fetch` - Matriz de tipos de identidade para resolver (por exemplo, `["ECID"]`)
&#x200B;- `event.xdm.environment.type` - Tipo de ambiente: `"browser"`, `"app"` ou `"server"`
&#x200B;- `event.xdm.environment.browserDetails` - Metadados do navegador (`viewportWidth`, `viewportHeight`, `userAgent`)
&#x200B;- `event.xdm.identityMap` - Mesmo mapeamento de identidade da Gestão de decisões
&#x200B;- `event.xdm.timestamp` - Carimbo de data/hora ISO 8601
&#x200B;- `query.personalization.surfaces` - Matriz de superfícies de destino (por exemplo, `["web://site.com/homepage"]`) — substitui `decisionScope`
&#x200B;- `query.personalization.schemas` - Esquemas de conteúdo a serem retornados (por exemplo, `["json-content-item", "html-content-item"]`)
&#x200B;- `data.__adobe.ajo.allowDuplicateDecisionItems` - Controle de desduplicação (o padrão é `true`; defina `false` para que um item que se qualifique para várias superfícies seja retornado apenas uma vez, com as outras superfícies recebendo um item de fallback/vazio). Substitui o Gerenciamento de decisão `allowDuplicatePropositions`.
&#x200B;- `data.__adobe.ajo.dryRun` - Sinalizador de teste; suprime eventos de feedback para contadores de relatório e limite. Substitui o Gerenciamento de decisão `xdm:dryRun`. Remover antes da produção.

**Exemplo de corpo de solicitação (lado do servidor):**

```json
{
  "events": [
    {
      "query": {
        "identity": { "fetch": ["ECID"] },
        "personalization": {
          "surfaces": ["web://my-web/IP_NLI_HP_GET_LOAN_WIDGET"],
          "schemas": [
            "https://ns.adobe.com/personalization/json-content-item",
            "https://ns.adobe.com/personalization/html-content-item"
          ]
        }
      },
      "xdm": {
        "eventType": "decisioning.propositionFetch",
        "environment": {
          "type": "browser",
          "browserDetails": { "viewportWidth": 1280, "viewportHeight": 900, "userAgent": "<USER_AGENT>" }
        },
        "identityMap": {
          "ECID": [ { "id": "<ECID>", "authenticatedState": "ambiguous", "primary": true } ]
        },
        "timestamp": "2025-09-08T12:00:00.000Z"
      },
      "data": {
        "__adobe": { "ajo": { "allowDuplicateDecisionItems": false } }
      }
    }
  ],
  "meta": {
    "state": {
      "domain": "my-web",
      "cookiesEnabled": true,
      "entries": [
        { "key": "kndctr_<ORG>_AdobeOrg_identity", "value": "<identity-cookie>" },
        { "key": "kndctr_<ORG>_AdobeOrg_cluster", "value": "<cluster-cookie>" }
      ]
    }
  }
}
```

>[!NOTE]
>Para obter a referência completa do Journey Optimizer Decisioning Web SDK / Edge, consulte [Experiência baseada em código: implementações de decisão](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/code-based-experience/configure-code-based-channel/code-based-decisioning-implementations).

### Decisão da resposta do Edge {#decisioning-response}

A resposta de Decisão contém vários identificadores organizados por tipo de preocupação: `personalization:decisions` (as ofertas), `locationHint:result` e `state:store` (os cookies a serem mantidos).

**Estrutura de Resposta:**

```json
{
  "requestId": "<REQUEST_ID>",
  "handle": [
    {
      "type": "personalization:decisions",
      "eventIndex": 0,
      "payload": [
        {
          "id": "103ae599-e6d8-4631-baf3-51dd8c6ed4c1",
          "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
          "scopeDetails": {
            "decisionProvider": "AJO",
            "correlationID": "<CORRELATION_ID>",
            "characteristics": {
              "eventToken": "<base64 message-level event token>",
              "subPropositions": "<base64-encoded array of decision items>"
            },
            "rank": 1,
            "activity": {
              "id": "<campaignId>#<actionId>",
              "priority": 0,
              "matchedSurfaces": ["web://my-web/IP_NLI_HP_GET_LOAN_WIDGET"]
            }
          },
          "items": [
            {
              "id": "36646bab-af1b-44c6-b632-bbfb9c357919",
              "schema": "https://ns.adobe.com/personalization/json-content-item",
              "data": { "content": "{ ...offer JSON... }" }
            }
          ]
        }
      ]
    },
    {
      "type": "locationHint:result",
      "payload": [
        { "scope": "EdgeNetwork", "hint": "ind1", "ttlSeconds": 1800 }
      ]
    },
    {
      "type": "state:store",
      "payload": [
        { "key": "kndctr_<ORG>_AdobeOrg_cluster", "value": "<cluster-cookie>", "maxAge": 1800 },
        { "key": "kndctr_<ORG>_AdobeOrg_identity", "value": "<identity-cookie>", "maxAge": 34128000 }
      ]
    }
  ]
}
```

**Campos-chave de resposta:**
&#x200B;- `handle[].type` - Tipo de identificador (`personalization:decisions`, `locationHint:result`, `state:store`)
&#x200B;- `payload[].id` - ID exclusiva da instância da proposta — eco de volta na exibição/interagir com eventos
&#x200B;- `payload[].scope` - URI de superfície para o qual a proposta foi resolvida
&#x200B;- `payload[].scopeDetails.decisionProvider` - Confirma que o mecanismo é `AJO`
&#x200B;- `payload[].scopeDetails.correlationID` - Vincula a instância de decisão ao evento de serviço
&#x200B;- `payload[].scopeDetails.rank` / `payload[].scopeDetails.activity` - Classificação e metadados de campanha/ação para a proposta
&#x200B;- `payload[].scopeDetails.characteristics.eventToken` - Token de rastreamento em nível de mensagem
&#x200B;- `payload[].scopeDetails.characteristics.subPropositions` - Matriz **codificada na Base64 dos itens de decisão**; cada item carrega seu próprio item `token`. Estes tokens por item são o que você passa no `propositionAction.tokens` em eventos de exibição/interação
&#x200B;- `payload[].items[].schema` / `payload[].items[].data.content` - Esquema de conteúdo e conteúdo real da oferta (JSON/HTML) para renderizar
&#x200B;- `state:store` carga - A identidade e os cookies de cluster para persistir e encaminhar em solicitações subsequentes (lado do servidor)

A cadeia de caracteres `characteristics.subPropositions` base64-decodifica para a matriz de itens servidos, cada um com seu item por item `token`:

```json
[
  {
    "id": "1ae75277-8832-4c23-bbbc-09f01cfe6c8b",
    "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
    "scopeDetails": { "decisionProvider": "EXD", "correlationID": "<CORRELATION_ID>-0", "rank": 1 },
    "items": [
      { "id": "dps:<schema>:1be64ff83a612488", "name": "ExD_Personal Loan Offer", "score": 997.0, "token": "CLaefQnVLcLbCtzEXV3Jeg" },
      { "id": "dps:<schema>:1be6516838e1248c", "name": "ExD_Home Loan Offer",     "score": 995.0, "token": "ALlB5KV1B0e+CpHoahi7Ew" },
      { "id": "dps:<schema>:1be650da3cd06e98", "name": "ExD_Auto Loan Offer",     "score": 994.0, "token": "koJTRQcwFkR92AqbZ88ytQ" },
      { "id": "dps:<schema>:1be65612d5a1248d", "name": "ExD_Fallback Offer",      "itemSelection": { "selectionDetail": { "selectionType": "fallback" } }, "token": "GHo4ow7h6iCzBOhYR1+6jg" }
    ]
  }
]
```

## Padrões de implementação {#implementation-patterns}

O Decisioning suporta três abordagens de implementação:

### Implementação Do Lado Do Cliente (Web SDK/SDK Móvel) {#client-side}

O Web SDK ou Mobile SDK lida com todas as solicitações e com o gerenciamento de cookies automaticamente. O SDK armazena e encaminha cookies de identidade e de cluster com cada solicitação.

**Tratamento de cookies:** Automático — o Web SDK gerencia cookies `kndctr_<OrgId>_identity` e `kndctr_<OrgId>_cluster`.

### Implementação do lado do servidor (API do Edge Network) {#server-side}

O servidor de aplicativos faz o POST diretamente no Edge Network e deve gerenciar manualmente o encaminhamento de cookies. O servidor extrai os cookies do navegador das solicitações recebidas e os encaminha para a Edge Network por meio de `meta.state.entries[]` e retorna os cookies na resposta.

**Tratamento de cookies:** Manual — o servidor de aplicativos deve extrair cookies da solicitação do navegador, encaminhar para o Edge Network no corpo da solicitação e definir como resposta. Os cookies devem ser explicitamente encaminhados em `meta.state.entries` para consistência de identidade.

### Implementação híbrida {#hybrid}

Combina a renderização do lado do servidor (carregamento inicial da página) com a SDK do lado do cliente (interações subsequentes). O servidor renderiza o conteúdo inicial por meio do Edge Network e, em seguida, o Web SDK assume o controle das solicitações de personalização subsequentes.

**Tratamento de cookies:** misto — o lado do servidor requer o encaminhamento manual de cookies para o Edge Network; o lado do cliente é manipulado automaticamente pelo Web SDK. Verifique se os tokens de identidade da renderização do lado do servidor estão disponíveis para o SDK do lado do cliente para resolução de identidade consistente.

## Rastreamento de eventos e coleta de dados {#event-tracking}

Para atribuir corretamente os resultados da decisão, ativar o limite de frequência e a otimização de classificação baseada em IA de energia, você deve implementar o rastreamento de eventos usando o schema de eventos Decisioning.

### Campos de evento obrigatórios {#event-fields}

`eventType` e `_experience.decisioning.propositionEventType` são obrigatórios. Se um deles estiver ausente, o contador de exibição/interação correspondente não será incrementado.

* **`eventType`** - Especifica a categoria do evento:
  &#x200B;- `decisioning.propositionDisplay` — Evento de impressão (oferta mostrada ao usuário)
  &#x200B;- `decisioning.propositionInteract` — Evento de interação (usuário clicou ou engajou com a oferta)

* **`_experience.decisioning.propositionEventType`** - Sinaliza o subtipo de evento. Incluir **exatamente uma** chave de tipo de evento definida como `1` (cada valor é `1` ou `0`; não defina vários tipos de evento como `1` no mesmo objeto):
  &#x200B;- `{ "display": 1 }` — Evento de impressão
  &#x200B;- `{ "interact": 1 }` — Evento de interação
  &#x200B;- Se todos os `display`/`interact`/`dismiss` forem `0` — ou `eventType` tiver qualquer valor diferente de `decisioning.proposition<Display|Interact|Dismiss>` — o evento será tratado como um **evento personalizado**.

* **`_experience.decisioning.propositionAction.tokens[]`** - Token(s) por item identificando quais itens servidos incrementam contadores para:
  &#x200B;- Copie o `token` de cada item da matriz decodificada `subPropositions` — **não** `scopeDetails.characteristics.eventToken`, que é um token diferente em nível de mensagem.
  &#x200B;- Envie o token exatamente como recebido, sem modificações.
  &#x200B;- **Interagir eventos:** forneça **exatamente um** token (o item clicado).
  &#x200B;- **Exibir eventos:** opcional(is) — fornecer token(s) para incrementar itens específicos ou **omitir** `tokens` para incrementar o contador para **todos** itens em `subPropositions`.

* **`_experience.decisioning.propositions[]`** - Ecoar de volta a(s) proposta(s) apresentada(s), incluindo `id`, `scope` e `scopeDetails` completa da resposta (que carrega `characteristics.subPropositions` e requer `decisionProvider`). Não é necessário criar uma matriz `items[]` explícita.

### Requisitos do esquema {#schema-requirements}

Associe o grupo de campos Decisão ao esquema do conjunto de dados do evento antes da migração:

1. No Experience Platform, abra o esquema do conjunto de dados do evento
2. Adicionar o grupo de campos `Experience Event - Proposition Details`
3. Verifique se os seguintes campos estão mapeados:
   &#x200B;- `_experience.decisioning.*` campos
   &#x200B;- `_experience.decisioning.propositionAction.tokens`
   &#x200B;- `_experience.decisioning.propositionEventType`

### Tratamento do token de rastreamento {#tracking-token}

O token de rastreamento deve ser manipulado de acordo com estes requisitos:

* **O token por item direciona os contadores** — os valores em `propositionAction.tokens` são `token` de cada item servido a partir de `subPropositions`, não o `characteristics.eventToken` de nível de mensagem.
* **Interagir eventos** — forneça exatamente um token (o item clicado).
* **Exibir eventos** — os tokens são opcionais; omita para incrementar todos os itens em `subPropositions` ou forneça tokens específicos para incrementar apenas esses itens.
* **Não modificar o token** — transmitir o valor exatamente como recebido; não codificar, analisar ou alterá-lo.

## Exemplos de eventos de decisão {#event-examples}

Cada exemplo ecoa a proposta apresentada (incluindo seu `scopeDetails`, que carrega `characteristics.subPropositions`) e define `eventType` e `propositionEventType`. Os contadores são incrementados em relação aos itens em `subPropositions`; `propositionAction.tokens` seleciona quais itens.

### Eventos de exibição

Exibir eventos notifica a Decisão quando uma oferta é exibida a um usuário. Forneça os tokens dos itens mostrados ou omita `tokens` para incrementar o contador de exibição para todos os itens em `subPropositions`:

```json
{
  "header": {
    "imsOrgId": "YOUR_ORG_ID",
    "sandboxId": "sandbox-id",
    "sandboxName": "sandbox-name",
    "source": { "name": "ajo-inbound" }
  },
  "body": {
    "xdmEntity": {
      "identityMap": {
        "ECID": [ { "id": "ecid-123", "primary": true } ]
      },
      "eventType": "decisioning.propositionDisplay",
      "_experience": {
        "decisioning": {
          "propositionEventType": { "display": 1 },
          "propositionAction": {
            "id": "b96f842b-5dd9-4c55-9dae-647d96250028",
            "tokens": ["CLaefQnVLcLbCtzEXV3Jeg", "ALlB5KV1B0e+CpHoahi7Ew"]
          },
          "propositions": [
            {
              "id": "103ae599-e6d8-4631-baf3-51dd8c6ed4c1",
              "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
              "scopeDetails": {
                "decisionProvider": "AJO",
                "characteristics": {
                  "eventToken": "<base64 eventToken from response>",
                  "subPropositions": "<base64 subPropositions from response>"
                }
              }
            }
          ]
        }
      }
    }
  }
}
```

### Interagir (clicar) eventos

Os eventos do Interact rastreiam quando um usuário clica ou se envolve com uma oferta exibida. Você **deve** fornecer **exatamente um** token identificando o item clicado:

```json
{
  "header": {
    "imsOrgId": "YOUR_ORG_ID",
    "sandboxId": "sandbox-id",
    "sandboxName": "sandbox-name",
    "source": { "name": "ajo-inbound" }
  },
  "body": {
    "xdmEntity": {
      "identityMap": {
        "ECID": [ { "id": "ecid-123", "primary": true } ]
      },
      "eventType": "decisioning.propositionInteract",
      "_experience": {
        "decisioning": {
          "propositionEventType": { "interact": 1 },
          "propositionAction": {
            "id": "b96f842b-5dd9-4c55-9dae-647d96250028",
            "tokens": ["CLaefQnVLcLbCtzEXV3Jeg"]
          },
          "propositions": [
            {
              "id": "103ae599-e6d8-4631-baf3-51dd8c6ed4c1",
              "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
              "scopeDetails": {
                "decisionProvider": "AJO",
                "characteristics": {
                  "eventToken": "<base64 eventToken from response>",
                  "subPropositions": "<base64 subPropositions from response>"
                }
              }
            }
          ]
        }
      }
    }
  }
}
```

### Eventos personalizados

Um evento personalizado usa um `eventType` definido pelo cliente (qualquer valor diferente de `decisioning.proposition<Display|Interact|Dismiss>`) e define todos os `display`/`interact`/`dismiss` como `0` em `propositionEventType` (classificado como `OTHER`). Eventos personalizados são decodificados como eventos de exibição (filtragem de vários tokens) em relação a `subPropositions` e avaliados por meio do PQL configurado:

```json
{
  "header": {
    "imsOrgId": "YOUR_ORG_ID",
    "sandboxId": "sandbox-id",
    "sandboxName": "sandbox-name",
    "originalTimestamp": 1700000
  },
  "body": {
    "xdmEntity": {
      "identityMap": {
        "ECID": [ { "id": "ecid-123", "primary": true } ]
      },
      "eventType": "add-to-cart",
      "_experience": {
        "decisioning": {
          "propositionEventType": { "display": 0, "interact": 0, "dismiss": 0 },
          "propositionAction": {
            "id": "b96f842b-5dd9-4c55-9dae-647d96250028",
            "tokens": ["CLaefQnVLcLbCtzEXV3Jeg"]
          },
          "propositions": [
            {
              "id": "103ae599-e6d8-4631-baf3-51dd8c6ed4c1",
              "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
              "scopeDetails": {
                "decisionProvider": "AJO",
                "characteristics": {
                  "eventToken": "<base64 eventToken from response>",
                  "subPropositions": "<base64 subPropositions from response>"
                }
              }
            }
          ]
        }
      }
    }
  }
}
```

Esses eventos permitem limitação de frequência, relatórios prontos para uso e otimização de classificação orientada por IA no Decisioning. Para enviar eventos de apresentação com o Web SDK, consulte [Experiência baseada em código: implementações de decisão](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/code-based-experience/configure-code-based-channel/code-based-decisioning-implementations).

## Processo de migração completo {#migration-process}

1. Validar pré-requisitos — Verifique se a sandbox de destino está preparada e se todas as dependências de pré-requisitos estão identificadas e prontas antes de iniciar a migração (atributos de perfil, IDs de segmento, mapeamento de ID).

1. Chamar a API de migração — Execute a API de migração para migrar objetos do Gestão de decisões para o Decisioning usando seus pré-requisitos e mapeamentos preparados.

1. Geração de entidades de decisão de rascunho — A ferramenta cria Campanhas, Políticas de decisão, Estratégias de seleção, Itens de oferta etc. no estado de rascunho por mapeamento de entidade. Revise todos os objetos de Decisão gerados na sandbox de destino. Validar nomes, tipos de entidade e referências estão corretos. Nada é voltado para o cliente ainda, o Gerenciamento de decisões continua atendendo o tráfego direto.

1. Atualizar código do cliente e do servidor — Implemente as alterações de código necessárias para usar os novos formatos de solicitação/resposta do Decisioning e implemente o rastreamento de eventos com os campos obrigatórios.

1. Ativar e transferir — Ative os objetos de decisão (estratégias, políticas, campanhas, superfícies) e afaste o tráfego do Gerenciamento de decisão em sua própria linha do tempo.

## Tópicos relacionados {#related-topics}

* [Migrar da Gestão de decisões para a Decisão](migrate-to-decisioning.md) - Entenda os benefícios e recursos da migração para a Decisão
* [Introdução ao serviço de decisão](gs-experience-decisioning.md)
* [Medidas de proteção e limitações da decisão](decisioning-guardrails.md)
* [Introdução às APIs de tomada de decisão](api-reference/getting-started.md)