---
title: Listar regras de qualificação
description: As Regras de elegibilidade permitem definir os candidatos elegíveis com base no que você deseja direcionar, como atributos de perfil e públicos-alvo.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 8fa34ebb7c853f9af5b3f58574374a3acb641dd9
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 5%

---

# Listar regras de qualificação {#list-eligibilit-rules}

Uma regra de elegibilidade consiste em uma expressão de regra do PQL que define como ela deve definir a elegibilidade.

É possível exibir uma lista de todas as regras de qualificação executando uma única solicitação do GET para a API da Biblioteca de ofertas.

**Formato da API**

```http
GET /{ENDPOINT_PATH}/offer-rules?{QUERY_PARAMS}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | exdRule | `property=exdRule%3D%3Dtrue` |

## Uso de parâmetros de consulta {#using-query-parameters}

Você pode usar parâmetros de consulta para paginar e filtrar resultados ao listar recursos.

### Paginação {#paging}

Os parâmetros de consulta mais comuns para paginação incluem:

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `property` | Um filtro de propriedade opcional: <ul><li>As propriedades são agrupadas por operação AND.</li><li>Os parâmetros podem ser repetidos da seguinte forma: property={PROPERTY_EXPR}[&amp;property={PROPERTY_EXPR2}...] or property={PROPERTY_EXPR1}[,{PROPERTY_EXPR2}...]</li><li>As expressões de propriedade estão no formato `[ !]field[op]value`, com `op` em `[==,!=,<=,>=,<,>,~]`, com suporte para expressões regulares.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Classificar os resultados por uma propriedade específica. Adicionar um - antes do nome (orderby=-name) classificará os itens pelo nome em ordem decrescente (Z-A). As expressões de caminho estão no formato de caminhos separados por pontos. Este parâmetro pode ser repetido assim: `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Limitar o número de entidades retornadas. | `limit=5` |

**Solicitação**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-rules?property=exdRule%3D%3Dtrue&limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna uma lista de regras de qualificação às quais você tem acesso.

```json
{
    "results": [
        {
            "created": "2024-10-28T01:18:08.506Z",
            "modified": "2024-10-28T01:18:08.506Z",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/eligibility-rule"
            ],
            "createdBy": "3254197F65569E890A49422F@658557135fa10b860a494019",
            "lastModifiedBy": "3254197F65569E890A49422F@658557135fa10b860a494019",
            "id": "dps:eligibility-rule:19af09a9ae45a8d3",
            "name": "dasdsa",
            "description": "",
            "exdRule": true,
            "condition": {
                "type": "PQL",
                "format": "pql/text",
                "value": "personalEmail.address.equals(\"youz@adobe.com\", false)"
            },
            "segmentModel": {
                "lifecycleState": "published",
                "expression": {
                    "isValid": true,
                    "logicalOperator": "and",
                    "profileAttributesContainer": {
                        "exclude": false,
                        "items": [
                            {
                                "comparisonType": "equals",
                                "component": {
                                    "id": "profile.personalEmail.address",
                                    "__entity__": true,
                                    "type": "Sz"
                                },
                                "isCaseSensitive": false,
                                "isPlaceholder": false,
                                "originalLocation": [],
                                "value": [
                                    "youz@adobe.com"
                                ],
                                "itemType": "segmentRule"
                            }
                        ],
                        "logicalOperator": "and",
                        "itemType": "segmentContainer"
                    },
                    "xEventAttributesContainer": {
                        "exclude": false,
                        "items": [],
                        "logicalOperator": "then",
                        "itemType": "eventTypeCardContainer"
                    },
                    "itemType": "segmentDefinition"
                },
                "isMissingAnsibleModel": false,
                "relationalExpression": false,
                "deprecated": {
                    "status": false,
                    "reason": ""
                },
                "description": "",
                "evaluationInfo": {
                    "batch": {
                        "enabled": true
                    },
                    "continuous": {
                        "enabled": false
                    },
                    "synchronous": {
                        "enabled": false
                    }
                },
                "labels": [],
                "tags": [],
                "canHaveFolder": true,
                "mergePolicyId": "24526dbe-d615-4d41-9ebb-fd7f2b3dcdc2",
                "name": "dasdsa",
                "namespace": "ups"
            }
        },
        {
            "created": "2024-10-27T04:01:29.343Z",
            "modified": "2024-10-27T04:33:44.781Z",
            "etag": 2,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/eligibility-rule"
            ],
            "createdBy": "3254197F65569E890A49422F@658557135fa10b860a494019",
            "lastModifiedBy": "3254197F65569E890A49422F@658557135fa10b860a494019",
            "id": "dps:eligibility-rule:19ade575cf95e584",
            "name": "nick test pes",
            "description": "dasdsad",
            "exdRule": true,
            "condition": {
                "type": "PQL",
                "format": "pql/text",
                "value": "personalEmail.address.equals(\"youz@adobe.com\", false)"
            },
            "segmentModel": {
                "lifecycleState": "published",
                "expression": {
                    "isValid": true,
                    "logicalOperator": "and",
                    "profileAttributesContainer": {
                        "exclude": false,
                        "items": [
                            {
                                "comparisonType": "equals",
                                "component": {
                                    "id": "profile.personalEmail.address",
                                    "__entity__": true,
                                    "type": "Sz"
                                },
                                "isCaseSensitive": false,
                                "isPlaceholder": false,
                                "originalLocation": [],
                                "value": [
                                    "youz@adobe.com"
                                ],
                                "itemType": "segmentRule"
                            }
                        ],
                        "logicalOperator": "and",
                        "itemType": "segmentContainer"
                    },
                    "xEventAttributesContainer": {
                        "exclude": false,
                        "items": [],
                        "logicalOperator": "then",
                        "itemType": "eventTypeCardContainer"
                    },
                    "itemType": "segmentDefinition"
                },
                "isMissingAnsibleModel": false,
                "relationalExpression": false,
                "deprecated": {
                    "status": false,
                    "reason": ""
                },
                "description": "dasdsad",
                "evaluationInfo": {
                    "batch": {
                        "enabled": true
                    },
                    "continuous": {
                        "enabled": false
                    },
                    "synchronous": {
                        "enabled": false
                    }
                },
                "labels": [],
                "tags": [],
                "canHaveFolder": true,
                "mergePolicyId": "24526dbe-d615-4d41-9ebb-fd7f2b3dcdc2",
                "name": "nick test pes",
                "namespace": "ups",
                "estimates": [
                    {
                        "previewId": "MDpTQU1QTEVfUkVJTklUOmJiNjI0MmZkLWUyOGQtNDY0Ni05ZWJjLTc1YmU5NGQ0YjY1Nzow",
                        "addressabilityText": "Of total",
                        "color": "#12805c",
                        "estimateData": {
                            "previewId": "MDpTQU1QTEVfUkVJTklUOmJiNjI0MmZkLWUyOGQtNDY0Ni05ZWJjLTc1YmU5NGQ0YjY1Nzow",
                            "estimatedSize": 0,
                            "totalRows": 62088,
                            "percent": 0,
                            "standardError": 0,
                            "confidenceInterval": "95%",
                            "state": "RESULT_READY",
                            "profilesReadSoFar": 62088,
                            "numRowsToRead": 62088
                        },
                        "state": "RESULT_READY"
                    }
                ]
            }
        }
    ],
    "count": 2,
    "total": 229,
    "_links": {
        "self": {
            "href": "/offer-rules?orderby=-modified&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/offer-rules?orderby=-modified&limit=2&start=2024-10-27T01:24:51.785Z",
            "type": "application/json"
        }
    }
}
```
