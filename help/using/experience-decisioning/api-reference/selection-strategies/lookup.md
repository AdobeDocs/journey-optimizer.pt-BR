---
title: Pesquisar uma estratégia de seleção
description: As estratégias de seleção consistem em coleções associadas a restrições e métodos de classificação para determinar ofertas.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: db590963-b45b-4844-ac12-775cc955b03e
source-git-commit: 7bfbb88c2817d18b7897a7fe1657ebf11be6eb58
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 8%

---

# Pesquisar uma estratégia de seleção {#list-selection-strategy}

Você pode pesquisar uma estratégia de seleção específica fazendo uma solicitação GET para a API da biblioteca de ofertas que inclui a id no caminho da solicitação.

**Formato da API**

```http
GET /{ENDPOINT_PATH}/selection-strategies/{ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | A ID da entidade que você deseja pesquisar. | `selectionStrategy1234` |

**Solicitação**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/selection-strategies/selectionStrategy1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna os detalhes da estratégia de seleção.

```json
{
    "created": "2024-02-08T03:01:50.924Z",
    "modified": "2024-02-16T23:03:03.019Z",
    "etag": 4,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/selection-strategy;version=0.2"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "selectionStrategy1234",
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
}
```
