---
title: Listar qualificadores de coleção
description: Os qualificadores de coleção permitem organizar e classificar melhor suas ofertas.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 6156689d9e5d7abedcd612389c5e332c695601f0
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 6%

---


# Listar qualificadores de coleção {#list-tags}

Os qualificadores de coleção (anteriormente conhecidos como &quot;tags&quot;) permitem organizar e classificar melhor suas ofertas. Por exemplo, você pode rotular as ofertas de Black Friday com o qualificador de coleção &quot;Black Friday&quot;. Em seguida, você pode usar a funcionalidade de pesquisa na Biblioteca de ofertas para localizar facilmente todas as ofertas com esse qualificador de coleção.

Qualificadores de coleção também podem ser usados para agrupar ofertas em coleções. Para obter mais informações, consulte o tutorial em [criação de coleções](../../../../offer-library/creating-collections.md).

Você pode exibir uma lista de todos os qualificadores de coleta executando uma única solicitação GET para a [!DNL Offer Library] API.

**Formato da API**

```http
GET /{ENDPOINT_PATH}/tags?{QUERY_PARAMS}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps` |

**Solicitação**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/tags?limit=2' \
-H 'Accept: *,application/json' \
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
| `property` | Um filtro de propriedade opcional: <ul><li>As propriedades são agrupadas por operação AND.</li><li>Os parâmetros podem ser repetidos da seguinte maneira: property={PROPERTY_EXPR}[&amp;propriedade={PROPERTY_EXPR2}..] ou property={PROPERTY_EXPR1}[,{PROPERTY_EXPR2}..]</li><li>As expressões de propriedade estão no formato `[!]field[op]value`, com `op` in `[==,!=,<=,>=,<,>,~]`, que suporta expressões regulares.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Classificar os resultados por uma propriedade específica. Adicionar um - antes do nome (orderby=-name) classificará os itens pelo nome em ordem decrescente (Z-A). As expressões de caminho estão no formato de caminhos separados por pontos. Esse parâmetro pode ser repetido da seguinte maneira: `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Limitar o número de entidades retornadas. | `limit=5` |

**Resposta**

Uma resposta bem-sucedida retorna uma lista de qualificadores de coleção presentes.

```json
{
    "results": [
        {
            "created": "2022-09-16T19:00:02.070+00:00",
            "modified": "2022-09-16T19:00:02.070+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "tag1234",
            "name": "Sneakers"
        },
        {
            "created": "2022-09-16T19:55:02.168+00:00",
            "modified": "2022-09-16T19:55:02.168+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "tag5678",
            "name": "Black Friday"
        }
    ],
    "count": 2,
    "total": 5,
    "_links": {
        "self": {
            "href": "/tags?href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/tags?href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
