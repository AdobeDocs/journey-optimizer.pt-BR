---
title: Atualizar fórmulas de classificação
description: As fórmulas de classificação permitem definir as funções de pontuação, que são usadas para classificar itens.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 8fa34ebb7c853f9af5b3f58574374a3acb641dd9
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 7%

---

# Atualizar uma fórmula de classificação {#update-ranking-formula}

Você pode modificar ou atualizar uma fórmula de classificação fazendo uma solicitação PUT para a API da biblioteca de ofertas.

Para obter mais informações sobre o JSON PUT, incluindo as operações disponíveis, consulte a [documentação oficial do JSON PUT](http://jsonpatch.com/).

**Cabeçalhos Aceitar e Tipo de Conteúdo**

A tabela a seguir mostra os valores válidos que compõem os campos Content-Type no cabeçalho da solicitação:

| Nome do cabeçalho | Valor |
| --------- | ----------- |
| Tipo de conteúdo | `application/json` |

**Formato da API**

```http
PUT /{ENDPOINT_PATH}/ranking-formulas/{ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | A ID da entidade que você deseja atualizar. | `rankingFormula1234` |

**Solicitação**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/ranking-formulas/rankingFormula1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "[UPDATED] Test Ranking Function DPS",
    "description": "Ranking  function description",
    "isPure": true,
    "exdFunction": true,
    "returnType": {
        "type": "integer"
    },
    "expression": {
        "type": "PQL",
        "format": "pql/text",
        "value": "if(offer.rank.priority.isNotNull(), offer.rank.priority, 0) * if(offer.tags.intersects(boosted.tags), 2, 1)"
    },
    "definedOn": {
        "offer": {
            "schema": {
                "altId": "_experience.offer-management.personalized-offer",
                "version": "0"
            }
        },
        "boosted": {
            "schema": {
                "altId": "_xdm.context.foo",
                "version": "0"
            }
        }
    }
}'
```

| Parâmetro | Descrição |
| --------- | ----------- |
| `value` | O novo valor com o qual você deseja atualizar seu parâmetro. |
| `path` | O caminho do parâmetro a ser atualizado. |
| `op` | A chamada de operação usada para definir a ação necessária para atualizar a conexão. As operações incluem: `add`, `replace`, `remove`, `copy` e `test`. |

**Resposta**

Uma resposta bem-sucedida retorna os detalhes atualizados da fórmula de classificação, incluindo a ID.

```json
{
    "etag": 2,
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "{ID}",
    "sandboxId": "{SANDBOX_ID}",
    "createdDate": "2023-05-31T15:09:11.771Z",
    "lastModifiedDate": "2023-05-31T15:09:11.771Z",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
