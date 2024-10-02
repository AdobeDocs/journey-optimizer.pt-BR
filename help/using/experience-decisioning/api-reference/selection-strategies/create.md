---
title: Criar uma estratégia de seleção
description: As estratégias de seleção consistem em coleções associadas a restrições e métodos de classificação para determinar ofertas.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 0e35c77b-6741-4c32-b012-36fc3a8b6d7a
source-git-commit: 7bfbb88c2817d18b7897a7fe1657ebf11be6eb58
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 8%

---

# Criar uma estratégia de seleção {#create-selection-strategy}

Você pode criar uma estratégia de seleção fazendo uma solicitação POST para a API da biblioteca de ofertas.

**Formato da API**

```http
POST /{ENDPOINT_PATH}/selection-strategies 
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps` |

**Solicitação**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/selection-strategies' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{    
    "name": "Selection Strategy One",
    "description": "Selection Strategy",
    "rank": {
        "priority": 1,
        "order": {
            "orderEvaluationType": "static"
        }
    },
    "profileConstraint": {
        "profileConstraintType": "eligibilityRule",
        "eligibilityRule": "offerRule1234"
    },
    "optionSelection": {
        "filter": "itemCollection1234",
    }
}'
```

**Resposta**

Uma resposta bem-sucedida retorna os detalhes da estratégia de seleção recém-criada, incluindo a id. Você pode usar a id em etapas posteriores para atualizar ou excluir sua estratégia de seleção.

```json
{
    "etag": 1,
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
