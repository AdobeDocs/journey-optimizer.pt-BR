---
title: Listar inserções
description: Posicionamentos são contêineres usados para exibir suas ofertas.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 36030ffe-eb7a-4487-914d-84ccb0a6bf6e
source-git-commit: ccc3ad2b186a64b9859a5cc529fe0aefa736fc00
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 12%

---

# Listar inserções {#list-placements}

Posicionamentos são contêineres usados para exibir suas ofertas. Uma disposição ajuda a garantir que o conteúdo de oferta correto seja exibido no local certo na mensagem. Ao adicionar conteúdo a uma oferta, você será solicitado a selecionar uma disposição na qual o conteúdo possa ser exibido.

Você pode exibir uma lista de todos os posicionamentos em um contêiner executando uma única solicitação GET para [!DNL Offer Library] API.

**Formato da API**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_PLACEMENT}&{QUERY_PARAMS}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs do repositório. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | O container onde os posicionamentos estão localizados. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `SCHEMA_PLACEMENT}` | Define o esquema associado a disposições. | `https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4` |
| `{QUERY_PARAMS}` | Parâmetros de consulta opcionais para filtrar os resultados. | `limit=2` |

## Uso de parâmetros de consulta {#using-query-parameters}

Você pode usar parâmetros de consulta para paginar e filtrar resultados ao listar recursos.

### Paginação {#paging}

Os parâmetros de consulta mais comuns para paginação incluem:

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `q` | Uma sequência de consulta opcional a ser pesquisada nos campos selecionados. A sequência de consulta deve estar em minúsculas e pode estar entre aspas duplas para impedir que seja tokenizada e para evitar caracteres especiais. Os caracteres `+ - = && \|\| > < ! ( ) { } [ ] ^ \" ~ * ? : \ /` têm significado especial e devem ser evitadas com uma barra invertida ao serem exibidas na sequência de consulta. | JSON do site |
| `qop` | Aplica o operador AND ou OR a valores no parâmetro de sequência de consulta q. | `AND` / `OR` |
| `field` | Lista opcional de campos aos quais limitar a pesquisa. Esse parâmetro pode ser repetido da seguinte maneira: field=field1[,campo=campo2,...] e (expressões de caminho estão no formato de caminhos separados por pontos, como _instance.xdm:name) | `_instance.xdm:name` |
| `orderBy` | Classificar os resultados por uma propriedade específica. Adicionar um `-` antes do título (`orderby=-title`) classificará os itens por título em ordem decrescente (Z-A). | `-repo:createdDate` |
| `limit` | Limitar o número de posicionamentos retornados. | `limit=5` |

**Solicitação**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4&limit=2' \
  -H 'Accept: *,application/json' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna uma lista de disposições presentes no contêiner ao qual você tem acesso.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4",
    "requestTime": "2020-10-21T19:48:51.843067Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "0feb6a80-0f32-11eb-8110-e17787c335b5",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 2,
                "repo:createdDate": "2020-10-15T22:02:05.480449Z",
                "repo:lastModifiedDate": "2020-10-15T22:13:00.278175Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:name": "New placement name",
                    "xdm:componentType": "https://ns.adobe.com/experience/offer-management/content-component-html",
                    "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                    "xdm:description": "Updated placement description",
                    "@id": "xcore:offer-placement:12466ef35fc5baa0"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4#0feb6a80-0f32-11eb-8110-e17787c335b5",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0feb6a80-0f32-11eb-8110-e17787c335b5",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
                    }
                }
            },
            {
                "instanceId": "269192b0-f8f2-11ea-8723-916b9fbadc53",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2020-09-17T14:29:10.107121Z",
                "repo:lastModifiedDate": "2020-09-17T14:29:10.107121Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:componentType": "https://ns.adobe.com/experience/offer-management/content-component-html",
                    "xdm:name": "demo placement",
                    "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                    "@id": "xcore:offer-placement:1221fac4e7340521"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4#269192b0-f8f2-11ea-8723-916b9fbadc53",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/269192b0-f8f2-11ea-8723-916b9fbadc53",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            }
        ],
        "total": 17,
        "count": 2
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        },
        "next": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?start=269192b0-f8f2-11ea-8723-916b9fbadc53&orderby=instanceId&schema=https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
