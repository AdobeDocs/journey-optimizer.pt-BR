---
title: Pesquisar um qualificador de coleção
description: Os qualificadores de coleção permitem organizar e classificar melhor suas ofertas.
feature: Offers, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: e2d1f093-c1b8-4c4c-a20f-4bd7c2ea5269
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 4%

---

# Pesquisar um qualificador de coleção {#look-up-tag}

Você pode pesquisar qualificadores de coleção específicos (anteriormente conhecidos como &quot;tags&quot;) fazendo uma solicitação GET para o [!DNL Offer Library] API que inclui o qualificador de coleção `@id` ou o nome do qualificador de coleção no caminho da solicitação.

**Formato da API**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_TAG}&{QUERY_PARAMS}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs do repositório. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | O contêiner onde os qualificadores de coleta estão localizados. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_TAG}` | Define o esquema associado aos qualificadores da coleção. | `https://ns.adobe.com/experience/offer-management/tag;version=0.1` |
| `id` | Uma string usada para corresponder ao `@id` propriedade das entidades. A string é exatamente igual. Os parâmetros `id` e `name` não podem ser usados juntos. | `xcore:tag:124e147572cd7866` |
| `name` | Uma sequência de caracteres usada para corresponder à propriedade xdm:name das entidades. A string é exatamente igual, com maiúsculas e minúsculas, mas caracteres curinga podem ser usados. Os parâmetros `id` e `name` não podem ser usados juntos | `Holiday sales and promotions` |

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

Uma resposta bem-sucedida retorna os detalhes do qualificador de coleta, incluindo informações sobre ID do contêiner, ID da instância e qualificador de coleta exclusivo `@id`.

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
