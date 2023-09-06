---
title: Listar decisões
description: Uma decisão contém a lógica que informa a seleção de uma oferta.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 123ed057-e15f-4110-9fc6-df0e9cb5b038
source-git-commit: 3568e86015ee7b2ec59a7fa95e042449fb5a0693
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 8%

---

# Listar decisões {#list-decisions}

Uma decisão contém a lógica que informa a seleção de uma oferta.

Você pode exibir uma lista de todas as decisões executando uma única solicitação GET para o [!DNL Offer Library] API.

**Formato da API**

```http
GET /{ENDPOINT_PATH}/offer-decisions?{QUERY_PARAMS}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | Parâmetros de consulta opcionais para filtrar os resultados. | `limit=2` |

**Solicitação**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-decisions?limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

## Uso de parâmetros de consulta {#using-query-parameters}

Você pode usar parâmetros de consulta para paginar e filtrar resultados ao listar recursos.

### Paginação {#paging}

Os parâmetros de consulta mais comuns para paginação incluem:

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `property` | Um filtro de propriedade opcional: <br> <ul> - As propriedades são agrupadas por operação AND. <br><br> - Os parâmetros podem ser repetidos da seguinte maneira: property=<property-expr>[&amp;propriedade=<property-expr2>..] ou property=<property-expr1>[,<property-expr2>..] <br><br> - As expressões de propriedade estão no formato [!]campo[op]valor, com op em [==,!=,&lt;=,>=,&lt;,>,~], suportando expressões regulares | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Classificar os resultados por uma propriedade específica. Adicionar um - antes do nome (orderby=-name) classificará os itens pelo nome em ordem decrescente (Z-A). As expressões de caminho estão no formato de caminhos separados por pontos. Esse parâmetro pode ser repetido da seguinte maneira: `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Limitar o número de entidades retornadas. | `limit=5` |

**Resposta**

Uma resposta bem-sucedida retorna uma lista de decisões às quais você tem acesso.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5",
    "requestTime": "2020-10-21T22:38:32.838180Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "286f6f80-026b-11eb-9439-ad36e372cbf1",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 5,
                "repo:createdDate": "2020-09-29T15:48:02.808677Z",
                "repo:lastModifiedDate": "2020-10-15T15:49:26.673560Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:fallback": "xcore:fallback-offer:1233160780eaa2ef",
                    "xdm:name": "A2: Cross Channel Activity",
                    "xdm:endDate": "2020-10-09T07:00:00.000Z",
                    "xdm:startDate": "2020-09-29T07:00:00.000Z",
                    "xdm:status": "live",
                    "xdm:criteria": [
                        {
                            "xdm:placements": [
                                "xcore:offer-placement:122204529514a2c0"
                            ],
                            "xdm:optionSelection": {
                                "xdm:filter": "xcore:offer-filter:122a120f234dac7f"
                            }
                        },
                        {
                            "xdm:placements": [
                                "xcore:offer-placement:122201b2150d98c2"
                            ],
                            "xdm:optionSelection": {
                                "xdm:filter": "xcore:offer-filter:1222058c3f0d98de"
                            }
                        }
                    ],
                    "@id": "xcore:offer-activity:12317fe6aeec9330"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5#286f6f80-026b-11eb-9439-ad36e372cbf1",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/286f6f80-026b-11eb-9439-ad36e372cbf1",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            },
            {
                "instanceId": "4e0206d0-0e6a-11eb-884a-c1a1104e3d7d",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2020-10-14T22:12:10.300775Z",
                "repo:lastModifiedDate": "2020-10-14T22:12:10.300775Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:fallback": "xcore:fallback-offer:1233160780eaa2ef",
                    "xdm:name": "LBAR",
                    "xdm:endDate": "2021-02-28T08:00:00.000Z",
                    "xdm:startDate": "2020-10-14T07:00:00.000Z",
                    "xdm:status": "live",
                    "xdm:criteria": [
                        {
                            "xdm:placements": [
                                "xcore:offer-placement:122204529514a2c0"
                            ],
                            "xdm:optionSelection": {
                                "xdm:filter": "xcore:offer-filter:122a120f234dac7f"
                            }
                        }
                    ],
                    "@id": "xcore:offer-activity:124527ab00b2ebbc"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5#4e0206d0-0e6a-11eb-884a-c1a1104e3d7d",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/4e0206d0-0e6a-11eb-884a-c1a1104e3d7d",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            }
        ],
        "total": 7,
        "count": 2
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        },
        "next": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?start=4e0206d0-0e6a-11eb-884a-c1a1104e3d7d&orderby=instanceId&schema=https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
