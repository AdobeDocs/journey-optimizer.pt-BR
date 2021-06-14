---
title: Pesquisar uma tag
description: Tags permitem organizar e classificar melhor suas ofertas.
feature: Ofertas
topic: Integrações
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 4%

---

# Pesquisar uma tag

Você pode pesquisar tags específicas fazendo uma solicitação GET para a API [!DNL Offer Library] que inclui a tag `@id` ou o nome da tag no caminho da solicitação.

**Formato da API**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_TAG}&{QUERY_PARAMS}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do terminal para APIs do repositório. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | O contêiner onde as tags estão localizadas. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_TAG}` | Define o schema associado às tags. | `https://ns.adobe.com/experience/offer-management/tag;version=0.1` |
| `id` | Uma string usada para corresponder à propriedade `@id` das entidades. A sequência de caracteres corresponde exatamente. Os parâmetros `id` e `name` não podem ser usados juntos. | `xcore:tag:124e147572cd7866` |
| `name` | Uma string usada para corresponder à propriedade xdm:name das entidades. A string é correspondida exatamente com maiúsculas, mas caracteres curingas podem ser usados. Os parâmetros `id` e `name` não podem ser usados juntos | `Holiday sales and promotions` |

**Solicitação**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/tag;version=0.1&name=Holiday%20sales%20and%20promotions' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema='\''https://ns.adobe.com/experience/xcore/hal/results'\''' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
```

**Resposta**

Uma resposta bem-sucedida retorna os detalhes da tag , incluindo informações sobre a ID do contêiner, a ID da instância e a tag exclusiva `@id`.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/tag;version=0.1",
    "requestTime": "2020-10-21T20:35:28.233975Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "d48fd160-13dc-11eb-bc55-c11be7252432",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2020-10-21T20:34:34.486296Z",
                "repo:lastModifiedDate": "2020-10-21T20:34:34.486296Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_score": 0,
                "_instance": {
                    "xdm:name": "Holiday sales and promotions",
                    "@id": "xcore:tag:124e147572cd7866"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/tag;version=0.1#d48fd160-13dc-11eb-bc55-c11be7252432",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/d48fd160-13dc-11eb-bc55-c11be7252432",
                        "@type": "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
                    }
                }
            }
        ],
        "total": 1,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/tag;version=0.1&name=Holiday%20sales%20and%20promotions",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
