---
title: Listar posicionamentos de exd
description: Os posicionamentos de Exd consistem em coleções associadas a restrições e métodos de classificação para determinar ofertas.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 8fa34ebb7c853f9af5b3f58574374a3acb641dd9
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 5%

---

# Listar posicionamentos de exd {#list-exd-placements}

Você pode visualizar uma lista de todas as disposições de exd executando uma única solicitação do GET para a API da Biblioteca de ofertas.

**Formato da API**

```http
GET /{ENDPOINT_PATH}/exd-placements?{QUERY_PARAMS}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps` |

## Uso de parâmetros de consulta {#using-query-parameters}

Você pode usar parâmetros de consulta para paginar e filtrar resultados ao listar recursos. Você pode filtrar por status, canal e channelConfiguration.

### Paginação {#paging}

Os parâmetros de consulta mais comuns para paginação incluem:

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `property` | Um filtro de propriedade opcional: <ul><li>As propriedades são agrupadas por operação AND.</li><li>Os parâmetros podem ser repetidos da seguinte forma: property={PROPERTY_EXPR}[&amp;property={PROPERTY_EXPR2}...] or property={PROPERTY_EXPR1}[,{PROPERTY_EXPR2}...]</li><li>As expressões de propriedade estão no formato `[!]field[op]value`, com `op` em `[==,!=,<=,>=,<,>,~]`, com suporte para expressões regulares.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Classificar os resultados por uma propriedade específica. Adicionar um - antes do nome (orderby=-name) classificará os itens pelo nome em ordem decrescente (Z-A). As expressões de caminho estão no formato de caminhos separados por pontos. Este parâmetro pode ser repetido assim: `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Limitar o número de entidades retornadas. | `limit=5` |

**Solicitação**

```shell
curl --location --request GET 'https://platform-stage.adobe.io/data/core/dps/exd-placements' \
--header 'Content-Type: application/json' \
--header 'x-gw-ims-org-id: {IMS_ORG}' \
--header 'x-sandbox-name: {SANDBOX_NAME}' \
--header 'x-api-key: {API_KEY}' \
--header 'Authorization: Bearer {ACCESS_TOKEN}' \
--data '{"query":"","variables":{}}'
```

**Resposta**

Uma resposta bem-sucedida retorna uma lista de disposições de Exd às quais você tem acesso.

```json
{
    "results": [
        {
            "created": "2024-11-14T23:30:29.820Z",
            "modified": "2024-11-14T23:30:29.820Z",
            "etag": 1,
            "schemas": [
                "exd-placement"
            ],
            "createdBy": "14D546EA60B67E540A494010@658557135fa10b860a494019",
            "lastModifiedBy": "14D546EA60B67E540A494010@658557135fa10b860a494019",
            "id": "dps:exd-placement:19c61da45ed96159",
            "name": "testing-alfa",
            "description": "atest",
            "tags": [
                "35801d6b-6371-449d-9083-d895fc120569"
            ],
            "channel": "https://ns.adobe.com/xdm/channel-types/email",
            "channelConfiguration": "fb8e9621-a5e8-485f-9f3f-d040c601ebc4",
            "status": "active"
        },
        {
            "created": "2024-10-22T00:18:17.997Z",
            "modified": "2024-10-22T05:04:15.315Z",
            "etag": 2,
            "schemas": [
                ""
            ],
            "createdBy": "71486D7B5F4011980A494030@AdobeID",
            "lastModifiedBy": "71486D7B5F4011980A494030@AdobeID",
            "id": "dps::19a7426d533db126",
            "name": "Test Exd Placement capacitor",
            "description": "Wooden system",
            "status": "archived"
        }
    ],
    "count": 2,
    "total": 2,
    "_links": {
        "self": {
            "href": "/exd-placements?orderby=-modified&limit=50",
            "type": "application/json"
        }
    }
}
```
