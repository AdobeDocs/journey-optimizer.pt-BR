---
title: Listar inserções
description: Posicionamentos são contêineres usados para exibir suas ofertas.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 36030ffe-eb7a-4487-914d-84ccb0a6bf6e
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 16%

---

# Listar inserções {#list-placements}

Posicionamentos são contêineres usados para exibir suas ofertas. Uma disposição ajuda a garantir que o conteúdo de oferta correto seja exibido no local certo na mensagem. Ao adicionar conteúdo a uma oferta, você será solicitado a selecionar uma disposição na qual o conteúdo possa ser exibido.

Você pode exibir uma lista de todos os posicionamentos executando uma única solicitação GET para a API [!DNL Offer Library].

**Formato da API**

```http
GET /{ENDPOINT_PATH}/placements?{QUERY_PARAMS}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs do repositório. | `https://platform.adobe.io/data/core/dps` |

## Uso de parâmetros de consulta {#using-query-parameters}

Você pode usar parâmetros de consulta para paginar e filtrar resultados ao listar recursos.

### Paginação {#paging}

Os parâmetros de consulta mais comuns para paginação incluem:

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `property` | Um filtro de propriedade opcional: <ul><li>As propriedades são agrupadas por operação AND.</li><li>Os parâmetros podem ser repetidos da seguinte forma: property={PROPERTY_EXPR}[&amp;property={PROPERTY_EXPR2}...] or property={PROPERTY_EXPR1}[,{PROPERTY_EXPR2}...]</li><li>As expressões de propriedade estão no formato `[!]field[op]value`, com `op` em `[==,!=,<=,>=,<,>,~]`, com suporte para expressões regulares.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Classificar os resultados por uma propriedade específica. Adicionar um - antes do nome (orderby=-name) classificará os itens pelo nome em ordem decrescente (Z-A). As expressões de caminho estão no formato de caminhos separados por pontos. Este parâmetro pode ser repetido assim: `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |

**Solicitação**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/placements?limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna uma lista de disposições presentes e aquelas às quais você tem acesso.

```json
{
    "results": [
        {
            "created": "2023-05-15T11:22:50.031+00:00",
            "modified": "2023-05-15T11:22:50.031+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.5"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerPlacement5678",
            "name": "Placement one",
            "description": "Placement description",
            "componentType": "html",
            "channel": "https://ns.adobe.com/xdm/channel-types/web",
            "itemCount": 1,
            "allowDuplicatePlacements": false,
            "returnContent": false,
            "returnMetaData": {
                "decisionName": true,
                "offerName": true,
                "offerAttributes": true,
                "offerPriority": true,
                "placementName": true,
                "channelType": true,
                "contentType": true
            }
        },
        {
            "created": "2023-05-19T08:29:15.875+00:00",
            "modified": "2023-05-19T08:29:15.875+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.5"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerPlacement1234",
            "name": "Placement two",
            "description": "Placement description",
            "componentType": "html",
            "channel": "https://ns.adobe.com/xdm/channel-types/email",
            "itemCount": 1,
            "allowDuplicatePlacements": false,
            "returnContent": false,
            "returnMetaData": {
                "decisionName": true,
                "offerName": true,
                "offerAttributes": true,
                "offerPriority": true,
                "placementName": true,
                "channelType": true,
                "contentType": true
            }
        }
    ],
    "count": 2,
    "total": 4,
    "_links": {
        "self": {
            "href": "/placements?href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/placements?href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
