---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Listar qualificadores de coleção
description: Os qualificadores de coleção permitem organizar e classificar melhor suas ofertas.
feature: Decision Management, API
badge: label="Legado" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 8cee44ed-5569-416c-b463-e75fb20d4c9c
version: Journey Orchestration
source-git-commit: 0b6d41fad9715985ec6418cdda27760f977bbc47
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 13%

---


# Listar qualificadores de coleção {#list-tags}

>[!TIP]
>
>O serviço de Decisão, o novo recurso de tomada de decisão do [!DNL Adobe Journey Optimizer], agora está disponível por meio da experiência baseada em código e dos canais de email. [Saiba mais](../../../../experience-decisioning/gs-experience-decisioning.md)


Os qualificadores de coleção (anteriormente conhecidos como &quot;tags&quot;) permitem organizar e classificar melhor suas ofertas. Por exemplo, você pode rotular as ofertas de Black Friday com o qualificador de coleção &quot;Black Friday&quot;. Em seguida, você pode usar a funcionalidade de pesquisa na Biblioteca de ofertas para localizar facilmente todas as ofertas com esse qualificador de coleção.

Qualificadores de coleção também podem ser usados para agrupar ofertas em coleções.

Você pode exibir uma lista de todos os qualificadores de coleção em um contêiner executando uma única solicitação do GET para a API da Biblioteca de ofertas.

**Formato da API**

```http
GET /{ENDPOINT_PATH}/tags?{QUERY_PARAMS}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | Parâmetros de consulta opcionais para filtrar os resultados. | `limit=2` |

## Paginação {#paging}

Os parâmetros de consulta mais comuns para paginação incluem:

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `property` | Um filtro de propriedade opcional: <ul><li>As propriedades são agrupadas por operação AND.</li><li>Os parâmetros podem ser repetidos da seguinte forma: property={PROPERTY_EXPR}[&amp;property={PROPERTY_EXPR2}...] or property={PROPERTY_EXPR1}[,{PROPERTY_EXPR2}...]</li><li>As expressões de propriedade estão no formato `[ !]field[op]value`, com `op` em `[==,!=,<=,>=,<,>,~]`, com suporte para expressões regulares.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Classificar os resultados por uma propriedade específica. Adicionar um - antes do nome (orderby=-name) classificará os itens pelo nome em ordem decrescente (Z-A). As expressões de caminho estão no formato de caminhos separados por pontos. Este parâmetro pode ser repetido assim: `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Limitar o número de posicionamentos retornados. | `limit=5` |

**Solicitação**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/tags?limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna uma lista de qualificadores de coleção que estão presentes no contêiner ao qual você tem acesso.

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
