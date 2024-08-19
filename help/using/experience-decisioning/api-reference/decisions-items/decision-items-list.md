---
title: Listar itens de decisão
description: Itens de decisão são ofertas de marketing que podem ser criadas e organizadas em coleções e catálogos.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: eb89bc5205d98a67cd0bb42bebbd9429786e33e7
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 13%

---


# Listar itens de decisão {#list-decision-items}

O Journey Optimizer permite gerar ofertas de marketing, conhecidas como itens de decisão, que você pode criar e organizar em catálogos e coleções centralizados. Eles são compostos de atributos padrão e personalizados projetados para se alinharem com precisão às suas necessidades. Além disso, incorporam restrições de perfil que permitem definir para quem um item de decisão pode ser exibido.

É possível visualizar uma lista de todos os itens de decisão executando uma única solicitação do GET para a API da Biblioteca de ofertas.

**Formato da API**

```http
GET /{ENDPOINT_PATH}/offer-items?{QUERY_PARAMS}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | Parâmetros de consulta opcionais para filtrar os resultados. | `limit=2` |

## Uso de parâmetros de consulta {#using-query-parameters}

Você pode usar parâmetros de consulta para paginar e filtrar resultados ao listar recursos.

### Paginação {#paging}

Os parâmetros de consulta mais comuns para paginação incluem:

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `property` | Um filtro de propriedade opcional: <ul><li>As propriedades são agrupadas por operação AND.</li><li>Os parâmetros podem ser repetidos da seguinte forma: property={PROPERTY_EXPR}[&amp;property={PROPERTY_EXPR2}...] or property={PROPERTY_EXPR1}[,{PROPERTY_EXPR2}...]</li><li>As expressões de propriedade estão no formato `[!]field[op]value`, com `op` em `[==,!=,<=,>=,<,>,~]`, com suporte para expressões regulares.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Classificar os resultados por uma propriedade específica. Adicionar um - antes do nome (orderby=-name) classificará os itens pelo nome em ordem decrescente (Z-A). As expressões de caminho estão no formato de caminhos separados por pontos. Este parâmetro pode ser repetido assim: `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Limitar o número de entidades retornadas. | `limit=5` |

**Solicitação**

```shell
curl -X GET '<https://platform.adobe.io/data/core/dps/offer-items?limit=2>' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-schema-id: {SCHEMA_ID}'
```

**Resposta**

Uma resposta bem-sucedida retorna uma lista de itens de oferta aos quais você tem acesso. O nó `_<imsOrg>` hospeda atributos de itens de decisão personalizados.

```json
{
    "results": [
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
                        "lifecycleStatus": "draft"
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
        },
        {
            "created": "2024-06-04T17:51:52.849Z",
            "modified": "2024-06-28T18:29:27.951Z",
            "etag": 5,
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerItem1234",
            "_experience": {
                "decisioning": {
                    "offeritem": {
                        "frequencyCappingConstraints": [],
                        "fCapConstraintsLastIndex": 0,
                        "lifecycleStatus": "approved"
                    },
                    "decisionitem": {
                        "itemCalendarConstraints": {
                            "endDate": "2030-12-31T08:00:00.000Z",
                            "startDate": "2024-06-01T07:00:00.000Z"
                        },
                        "itemCatalogID": "itemCatalong1234",
                        "itemConstraints": {
                            "profileConstraintType": "none"
                        },
                        "itemDescription": "Offer item description",
                        "itemID": "offerItem1234",
                        "itemLabels": [],
                        "itemName": "Offer Item Two",
                        "itemPriority": 2,
                        "itemTags": []
                    }
                }
            },
            "YOUR_CUSTOM_ATTRIBUTES": {
                "some_field": "some value",
                "some_boolean_field": true
            }
        }
    ],
    "count": 2,
    "total": 844,
    "_links": {
        "self": {
            "href": "/offer-items?orderby=-modified&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/offer-items?orderby=-modified&limit=2&start=2024-06-28T03:44:15.630Z",
            "type": "application/json"
        }
    }
}
```
