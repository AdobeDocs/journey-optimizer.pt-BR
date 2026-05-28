---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Pesquisar uma regra de decisão
description: As regras de decisão são restrições adicionadas a uma oferta personalizada e aplicadas a um perfil para determinar a elegibilidade.
feature: Decision Management, API
badge: label="Legado" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 3099736d-7109-4c94-aea6-053a9b885278
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/7uHa13tFd6FkFhDVXb5fOciNNH25pxA3PwJVTi7RUOs
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 183
ht-degree: 14%

---

# Pesquisar uma regra de decisão {#lookup-decision-rule}

>[!TIP]
>
>O serviço de Decisão, o novo recurso de tomada de decisão do [!DNL Adobe Journey Optimizer], agora está disponível por meio da experiência baseada em código e dos canais de email. [Saiba mais](../../../../../experience-decisioning/gs-experience-decisioning.md)


Você pode pesquisar uma regra de decisão específica fazendo uma solicitação GET para a API [!DNL Offer Library] que inclui a regra de decisão `@id` ou o nome da regra de decisão no caminho da solicitação.

**Formato da API**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_ELIGIBILITY_RULE}&{QUERY_PARAMS}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs do repositório. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | O contêiner onde as regras de decisão estão localizadas. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_ELIGIBILITY_RULE}` | Define o esquema associado às regras de decisão. | `https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3` |
| `id` | Uma cadeia de caracteres usada para corresponder à propriedade `@id` das entidades. A string é exatamente igual. Os parâmetros `id` e `name` não podem ser usados juntos. | `xcore:eligibility-rule:124e0faf5b8ee89b` |
| `name` | Uma cadeia de caracteres usada para corresponder à propriedade xdm:name das entidades. A string é exatamente igual, com maiúsculas e minúsculas, mas caracteres curinga podem ser usados. Os parâmetros `id` e `name` não podem ser usados juntos | `Sales rule` |

**Solicitação**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3&name=Sales%20rule' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna os detalhes da regra de decisão específica pesquisada, incluindo informações sobre sua regra de decisão exclusiva `id`.

```json
  {
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3",
    "requestTime": "2023-10-21T20:14:08.153670Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "eaa5af90-13d9-11eb-9472-194dee6dc381",
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"
    ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2023-10-21T20:13:43.048666Z",
                "repo:lastModifiedDate": "2023-10-21T20:13:43.048666Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_score": 0,
                "_instance": {
                    "xdm:name": "Sales rule",
                    "description": "Decisioning rule for sales",
                    "xdm:definedOn": {
                        "profile": {
                            "xdm:schema": {
                                "$ref": "https://ns.adobe.com/xdm/context/profile_union",
                                "version": "1"
                            },
                            "xdm:referencePaths": [
                                "person.name.firstName"
                            ]
                        }
                    },
    "condition": {
                        "format": "pql/text",
        "type": "PQL",
                        "value": "profile.person.name.firstName.equals(\"Joe\", false)"
                    },
                    "@id": "xcore:eligibility-rule:124e0faf5b8ee89b"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3#eaa5af90-13d9-11eb-9472-194dee6dc381",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/eaa5af90-13d9-11eb-9472-194dee6dc381",
                        "@type": "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"
                    }
                }
            }
        ],
        "total": 1,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3&name=Sales%20rule",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
            }
}
```
