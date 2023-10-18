---
title: Pesquisar uma decisão
description: Uma decisão contém a lógica que informa a seleção de uma oferta.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 99159704-fa39-47ff-b445-0cd6b325007d
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 4%

---

# Pesquisar uma decisão {#look-up-decision}

Você pode pesquisar decisões específicas fazendo uma solicitação GET para a [!DNL Offer Library] API que inclui as decisões `@id` ou o nome da decisão no caminho da solicitação.

**Formato da API**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_ACTIVITIES}&{QUERY_PARAMS}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs do repositório. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | O contêiner onde as decisões estão localizadas. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_ACTIVITIES}` | Define o esquema associado às decisões. | `https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5` |
| `id` | Uma string usada para corresponder ao `@id` propriedade das entidades. A string é exatamente igual. Os parâmetros `id` e `name` não podem ser usados juntos. | `xcore:offer-activity:124527ab00b2ebbc` |
| `name` | Uma sequência de caracteres usada para corresponder à propriedade xdm:name das entidades. A string é exatamente igual, com maiúsculas e minúsculas, mas caracteres curinga podem ser usados. Os parâmetros &quot;id&quot; e &quot;name&quot; não podem ser usados juntos | `LBAR` |

**Solicitação**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5&id=xcore:offer-activity:124527ab00b2ebbc' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna os detalhes do posicionamento, incluindo informações sobre ID do container, ID da instância e, decisão exclusiva `@id`.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5",
    "requestTime": "2020-10-19T19:50:08.047489Z",
    "_embedded": {
        "results": [
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
                "_score": 0,
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
        "total": 1,
        "count": 1
            },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5&id=xcore:offer-activity:124527ab00b2ebbc",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
            }   
        }
}
```
