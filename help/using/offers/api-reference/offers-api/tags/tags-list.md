---
title: Listar qualificadores de coleção
description: Os qualificadores de coleção permitem organizar e classificar melhor suas ofertas.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 8cee44ed-5569-416c-b463-e75fb20d4c9c
source-git-commit: adcf2c1b83f80110c926e06fa931167c411c8d91
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 5%

---


# Listar qualificadores de coleção {#list-tags}

Os qualificadores de coleção (anteriormente conhecidos como &quot;tags&quot;) permitem organizar e classificar melhor suas ofertas. Por exemplo, você pode rotular as ofertas de Black Friday com o qualificador de coleção &quot;Black Friday&quot;. Em seguida, você pode usar a funcionalidade de pesquisa na Biblioteca de ofertas para localizar facilmente todas as ofertas com esse qualificador de coleção.

Qualificadores de coleção também podem ser usados para agrupar ofertas em coleções. Para obter mais informações, consulte o tutorial em [criação de coleções](../../../offer-library/creating-collections.md)

Você pode exibir uma lista de todos os qualificadores de coleta em um contêiner executando uma única solicitação GET para a [!DNL Offer Library] API.

**Formato da API**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_TAG}&{QUERY_PARAMS}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs do repositório. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | O contêiner onde os qualificadores de coleta estão localizados. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_TAG}` | Define o esquema associado aos qualificadores da coleção. | `https://ns.adobe.com/experience/offer-management/tag;version=0.1` |
| `{QUERY_PARAMS}` | Parâmetros de consulta opcionais para filtrar os resultados. | `limit=2` |

**Solicitação**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/tag;version=0.1&limit=2' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `q` | Uma sequência de consulta opcional a ser pesquisada nos campos selecionados. A sequência de consulta deve estar em minúsculas e pode estar entre aspas duplas para impedir que seja tokenizada e para evitar caracteres especiais. Os caracteres `+ - = && \|\| > < ! ( ) { } [ ] ^ \" ~ * ? : \ /` têm significado especial e devem ser evitadas com uma barra invertida ao serem exibidas na sequência de consulta. | JSON do site |
| `qop` | Aplica o operador AND ou OR a valores no parâmetro de sequência de consulta q. | `AND` / `OR` |
| `field` | Lista opcional de campos aos quais limitar a pesquisa. Esse parâmetro pode ser repetido da seguinte maneira: field=field1[,campo=campo2,...] e (expressões de caminho estão no formato de caminhos separados por pontos, como _instance.xdm:name) | `_instance.xdm:name` |
| `orderBy` | Classificar os resultados por uma propriedade específica. Adicionar um `-` antes do título (`orderby=-title`) classificará os itens por título em ordem decrescente (Z-A). | `-repo:createdDate` |
| `limit` | Limite o número de qualificadores de coleção retornados. | `limit=5` |

**Resposta**

Uma resposta bem-sucedida retorna uma lista de qualificadores de coleção que estão presentes no contêiner ao qual você tem acesso.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/tag;version=0.1",
    "requestTime": "2020-10-21T20:28:21.521267Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "0adf2ef0-0f6e-11eb-b3be-9b775f952952",
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
            ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 2,
                "repo:createdDate": "2020-10-16T05:11:26.815213Z",
                "repo:lastModifiedDate": "2020-10-16T22:20:20.190006Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:name": "Sneakers",
                    "@id": "xcore:tag:1246d138ec8cca1f"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/tag;version=0.1#0adf2ef0-0f6e-11eb-b3be-9b775f952952",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0adf2ef0-0f6e-11eb-b3be-9b775f952952",
                        "@type": "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
                    }
                }
        },
        {
                "instanceId": "149e0de0-ff5f-11ea-b017-f98866426d43",
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
            ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2020-09-25T18:44:02.109748Z",
                "repo:lastModifiedDate": "2020-09-25T18:44:02.109748Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:name": "retirement",
                    "@id": "xcore:tag:122c81d2804e69e3"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/tag;version=0.1#149e0de0-ff5f-11ea-b017-f98866426d43",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/149e0de0-ff5f-11ea-b017-f98866426d43",
                        "@type": "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
        }
    ],
        "total": 11,
        "count": 2
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/tag;version=0.1&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        },
        "next": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?start=149e0de0-ff5f-11ea-b017-f98866426d43&orderby=instanceId&schema=https://ns.adobe.com/experience/offer-management/tag;version=0.1&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
