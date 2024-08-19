---
title: Pesquisar um item de decisão
description: Itens de decisão são ofertas de marketing que podem ser criadas e organizadas em coleções e catálogos.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: eb89bc5205d98a67cd0bb42bebbd9429786e33e7
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 8%

---


# Pesquisar um item de decisão {#lookup-decision-items}

Para pesquisar itens de decisão específicos, faça uma solicitação GET à API da biblioteca de ofertas que inclua a ID no caminho da solicitação.

**Formato da API**

```http
GET /{ENDPOINT_PATH}/offer-items/{ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | A ID da entidade que você deseja pesquisar. | `offerItem1234` |

**Solicitação**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-items/offerItem1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-schema-id: {SCHEMA_ID}'
```

**Resposta**

Uma resposta bem-sucedida retorna os detalhes do item de decisão.

```json
{
    "created": "2024-06-10T16:00:34.014Z",
    "modified": "2024-07-09T22:59:21.507Z",
    "etag": 1,
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "offerItem5678",
    "_experience": {
        "decisioning": {
            "offeritem": {
                "fCapConstraintsLastIndex": 0,
                "lifecycleStatus": "approved"
            },
            "decisionitem": {
                "itemCalendarConstraints": {
                    "endDate": "2030-12-31T08:00:00.000Z",
                    "startDate": "2024-06-10T04:00:00.000Z"
                },
                "itemCatalogID": "itemCatalong1234",
                "itemConstraints": {
                    "eligibilityRule": "rule1234",
                    "profileConstraintType": "eligibilityRule"
                },
                "itemDescription": "Offer item description",
                "itemID": "offerItem5678",
                "itemLabels": [],
                "itemName": "Offer Item One",
                "itemPriority": 1,
                "itemTags": []
            }
        }
    },
    "_<imsOrg>": {
        "some_field": "some value"
    }
}
```
