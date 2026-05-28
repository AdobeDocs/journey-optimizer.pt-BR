---
title: Atualizar regras de elegibilidade
description: As Regras de elegibilidade permitem definir os candidatos elegíveis com base no que você deseja direcionar, como atributos de perfil e públicos-alvo.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 8d82b4db-2ba8-4692-a63e-9cb3c6c434c3
version: Journey Orchestration
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 162
ht-degree: 9%

---

# Atualizar uma regra de elegibilidade {#update-eligibility-rule}

Você pode modificar ou atualizar uma regra fazendo uma solicitação PUT para a API da biblioteca de ofertas.

Para obter mais informações sobre JSON PUT, incluindo as operações disponíveis, consulte a [documentação oficial sobre JSON PUT](https://jsonpatch.com/).

**Cabeçalhos Aceitar e Tipo de Conteúdo**

A tabela a seguir mostra os valores válidos que compõem os campos Content-Type no cabeçalho da solicitação:

| Nome do cabeçalho | Valor |
| --------- | ----------- |
| Tipo de conteúdo | `application/json` |

**Formato da API**

```http
PUT /{ENDPOINT_PATH}/offer-rules/{ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | A ID da entidade que você deseja atualizar. | `rule1234` |

**Solicitação**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offer-rules/rule1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "[UPDATED] Test Offer Rule DPS",
    "description": "Offer Rule description",
    "exdRule": true,
    "condition": {
        "type": "PQL",
        "format": "pql/text",
        "value": "homeAddress.stateProvince.equals(\"CA\", false) and (select var1 from xEvent where var1.eventType.equals(\"purchase\", true) and (var1.commerce.order.priceTotal = 1000.0 and var1.commerce.order.currencyCode.equals(\"USD\", false)))"
    },
    "definedOn": {
        "": {
            "schema": {
                "altId": "_xdm.context.profile",
                "version": "1"
            },
            "referencePaths": [
                "homeAddress.stateProvince"
            ]
        },
        "xEvent": {
            "schema": {
                "altId": "_xdm.context.experienceevent",
                "version": "1"
            },
            "referencePaths": [
                "eventType",
                "commerce.order.priceTotal",
                "commerce.order.currencyCode"
            ]
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

Uma resposta bem-sucedida retorna os detalhes atualizados da regra de elegibilidade, incluindo a ID.

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
