---
title: Listar de regras de decisão
description: As regras de decisão são restrições adicionadas a uma oferta personalizada e aplicadas a um perfil para determinar a elegibilidade.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: c4c3e415-bc57-45db-b27f-4a5e9fc1f02c
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 8%

---

# Listar de regras de decisão {#list-decision-rules}

As regras de decisão são restrições adicionadas a uma oferta personalizada e aplicadas a um perfil para determinar a elegibilidade. Você pode exibir uma lista de regras de decisão existentes em um contêiner executando uma única solicitação GET para a API [!DNL Offer Library].

**Formato da API**

```http
GET /{ENDPOINT_PATH}/offer-rules?{QUERY_PARAMS}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | Parâmetros de consulta opcionais para filtrar os resultados. | `limit=2` |

## Uso de parâmetros de consulta {#using-query-parameters}

Você pode usar parâmetros de consulta para paginar e filtrar resultados ao listar recursos.

### Paginação {#paging}

Os parâmetros de consulta mais comuns para paginação incluem:

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `property` | Um filtro de propriedade opcional: <ul><li>As propriedades são agrupadas por operação AND.</li><li>Os parâmetros podem ser repetidos da seguinte forma: property={PROPERTY_EXPR}[&amp;property={PROPERTY_EXPR2}...] or property={PROPERTY_EXPR1}[,{PROPERTY_EXPR2}...]</li><li>As expressões de propriedade estão no formato `[!]field[op]value`, com `op` em `[==,!=,<=,>=,<,>,~]`, com suporte para expressões regulares.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Classificar os resultados por uma propriedade específica. Adicionar um - antes do nome (orderby=-name) classificará os itens pelo nome em ordem decrescente (Z-A). As expressões de caminho estão no formato de caminhos separados por pontos. Este parâmetro pode ser repetido assim: `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Limitar o número de entidades retornadas. | `limit=5` |

**Solicitação**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-rules?limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna uma lista de regras de decisão às quais você tem acesso.

```json
{
     "results": [
        {
            "created": "2022-09-16T18:59:53.651+00:00",
            "modified": "2022-09-16T18:59:53.651+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerRule1234",
            "name": "Californians with one or more purchases greater than $1000",
            "condition": {
                "type": "PQL",
                "format": "pql/text",
                "value": "homeAddress.stateProvince.equals(\"CA\", false) and (select var1 from xEvent where var1.eventType.equals(\"purchase\", true) and (var1.commerce.order.priceTotal = 1000.0 and var1.commerce.order.currencyCode.equals(\"USD\", false)))"
                 }
        },
        {
            "created": "2023-03-06T15:11:42.178+00:00",
            "modified": "2023-03-06T15:11:42.178+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerRule5678",
            "name": "People born after 1981",
            "description": "Persons with the birth date after 1981",
            "condition": {
                "type": "PQL",
                "format": "pql/text",
                "value": "person.birthDate occurs after date(1981, 1, 1)"
            }
        }
    ],
    "count": 2,
    "total": 25,
    "_links": {
        "self": {
            "href": "/offer-rules?href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/offer-rules?href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
