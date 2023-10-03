---
title: Listar ofertas substitutas
description: Uma oferta substituta é enviada aos clientes se eles não estiverem qualificados para outras ofertas
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: dd95c040-d905-4f5a-8cc5-58e39082e57e
source-git-commit: 54b92b19f2e3a6afa6557ffeff0d971a4c411510
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 6%

---

# Listar ofertas substitutas {#list-fallback-offers}

Uma oferta substituta é enviada aos clientes se eles não estiverem qualificados para outras ofertas. As etapas para criar uma oferta substituta consistem na criação de uma ou várias representações, como ao criar uma oferta.

Você pode exibir uma lista de todas as ofertas substitutas em um contêiner executando uma única solicitação GET para [!DNL Offer Library] API.

**Formato da API**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_FALLBACK_OFFER}&{QUERY_PARAMS}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs do repositório. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | O container onde as ofertas substitutas estão localizadas. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_FALLBACK_OFFER}` | Define o esquema associado às ofertas substitutas. | `https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1` |
| `{QUERY_PARAMS}` | Parâmetros de consulta opcionais para filtrar os resultados. | `limit=1` |

**Solicitação**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1&limit=1' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
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
| `q` | Uma sequência de consulta opcional a ser pesquisada nos campos selecionados. A sequência de consulta deve estar em minúsculas e pode estar entre aspas duplas para impedir que seja tokenizada e para evitar caracteres especiais. Os caracteres `+ - = && \|\| > < ! ( ) { } [ ] ^ \" ~ * ? : \ /` têm significado especial e devem ser evitadas com uma barra invertida ao serem exibidas na sequência de consulta. | `default` |
| `qop` | Aplica o operador AND ou OR a valores no parâmetro de sequência de consulta q. | `AND` / `OR` |
| `field` | Lista opcional de campos aos quais limitar a pesquisa. Esse parâmetro pode ser repetido da seguinte maneira: field=field1[,campo=campo2,...] e (expressões de caminho estão no formato de caminhos separados por pontos, como _instance.xdm:name) | `_instance.xdm:name` |
| `orderBy` | Classificar os resultados por uma propriedade específica. Adicionar um `-` antes do título (`orderby=-title`) classificará os itens por título em ordem decrescente (Z-A). | `-repo:createdDate` |
| `limit` | Limite o número de ofertas substitutas retornadas. | `limit=5` |

**Resposta**

Uma resposta bem-sucedida retorna uma lista de ofertas substitutas que estão presentes no container ao qual você tem acesso.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1",
    "requestTime": "2020-10-22T07:12:30.923768Z",
    "_embedded": {
      "results": [
        {
                "instanceId": "053bc610-f8f9-11ea-ad6e-775ad2c9b1a1",
            "schemas": [
                    "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.5"
            ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 3,
                "repo:createdDate": "2020-09-17T15:18:20.657299Z",
                "repo:lastModifiedDate": "2020-10-02T02:34:48.034583Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:name": "F1: Web fallback ",
                    "xdm:representations": [
                {
                            "xdm:components": [
                        {
                                    "xdm:content": "aaa",
                                    "@type": "https://ns.adobe.com/experience/offer-management/content-component-json",
                                    "dc:format": "application/json",
                                    "repo:name": "aa"
                        }
                            ],
                            "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                            "xdm:placement": "xcore:offer-placement:122201b2150d98c2"
        },
        {
                            "xdm:components": [
                                {
                                    "xdm:content": "bb",
                                    "@type": "https://ns.adobe.com/experience/offer-management/content-component-html",
                                    "dc:format": "text/html",
                                    "repo:name": "bb"
                                }
            ],
                            "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                            "xdm:placement": "xcore:offer-placement:122201c34354a2b4"
                        },
                {
                            "xdm:components": [
                        {
                                    "xdm:deliveryURL": "https://mysite.com",
                                    "@type": "https://ns.adobe.com/experience/offer-management/content-component-imagelink",
                                    "dc:format": "image/png",
                                    "repo:name": "ll"
                        }
                            ],
                            "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                            "xdm:placement": "xcore:offer-placement:122207eddb05205a"
                }
            ],
                    "xdm:status": "approved",
                    "xdm:tags": [],
                    "@id": "xcore:fallback-offer:122206064e0d98df"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.5#053bc610-f8f9-11ea-ad6e-775ad2c9b1a1",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/053bc610-f8f9-11ea-ad6e-775ad2c9b1a1",
                        "@type": "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.5"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
        }
    ],
        "total": 5,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1&limit=1",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        },
        "next": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?start=053bc610-f8f9-11ea-ad6e-775ad2c9b1a1&orderby=instanceId&schema=https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1&limit=1",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
