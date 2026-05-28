---
title: Atualizar um item de decisão
description: Itens de decisão são ofertas de marketing que podem ser criadas e organizadas em coleções e catálogos.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: b924b7d0-bbed-409e-8173-0685fc41d7de
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/5hMZmGEl--fCOFYxhy-wRRFh4JG7o-CHWDMKfA7rD78
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 138
ht-degree: 6%

---

# Atualizar um item de decisão {#update-decision-items}

Você pode modificar ou atualizar um item de decisão fazendo uma solicitação PATCH para a API da biblioteca de ofertas.

Para obter mais informações sobre o Patch JSON, incluindo as operações disponíveis, consulte a [documentação oficial do Patch JSON](https://jsonpatch.com/).

**Formato da API**

```http
PATCH /{ENDPOINT_PATH}/offer-items/{ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | A ID da entidade que você deseja atualizar. | `offerItem1234` |

**Solicitação**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offer-items/offerItem1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-schema-id: {SCHEMA_ID}' \
-d '[
    {
        "op": "replace",
        "path": "/_experience/decisioning/decisionitem/itemName",
        "value": "Updated offer item"
    },
    {
        "op": "replace",
        "path": "/_experience/decisioning/decisionitem/itemDescription",
        "value": "Updated offer item description"
    }
]'
```

| Parâmetro | Descrição |
| --------- | ----------- |
| `value` | O novo valor com o qual você deseja atualizar seu parâmetro. |
| `path` | O caminho do parâmetro a ser atualizado. |
| `op` | O tipo de operação a ser executada. As operações incluem: `add`, `replace`, `remove`, `copy` e `test`. |

**Resposta**

Uma resposta bem-sucedida retorna os detalhes do item atualizado, incluindo a id. Você pode usar a id em etapas posteriores para atualizar ou excluir o item de decisão.

```json
{
    "etag": 2,
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "{ID}",
    "sandboxId": "{SANDBOX_ID}",
    "createdDate": "2023-05-31T15:09:11.771Z",
    "lastModifiedDate": "2023-05-31T15:09:11.771Z",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
