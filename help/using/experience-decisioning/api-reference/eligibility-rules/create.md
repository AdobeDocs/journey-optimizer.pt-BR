---
title: Criar uma regra de elegibilidade
description: As Regras de elegibilidade permitem definir os candidatos elegíveis com base no que você deseja direcionar, como atributos de perfil e públicos-alvo.
feature: API, Collections, Decisioning
role: Developer
level: Experienced
exl-id: 39c6e82e-c1b1-4dda-a941-3db6324cef37
version: Journey Orchestration
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 93712df16d9a3df94fd31cb8bc4da9762691d1ef
workflow-type: tm+mt
source-wordcount: 89
ht-degree: 7%

---

# Criar uma regra de elegibilidade {#create-eligibility-rule}

É possível criar uma regra de elegibilidade fazendo uma solicitação POST para a API da biblioteca de ofertas.

**Formato da API**

```http
POST /{ENDPOINT_PATH}/offer-rules 
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps` |

**Solicitação**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/offer-rules' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '
{
    "name": "test dule",
    "description": "xxxxxx",
    "exdRule": true,
    "condition": {
        "type": "PQL",
        "format": "pql/text",
        "value": "inSegment(\"849807b6-0a76-4895-96d9-89996477f23b\") and billingAddress.city.equals(\"san jose\", false)"
    }
}'
```

**Resposta**

Uma resposta bem-sucedida retorna os detalhes da regra de elegibilidade recém-criada, incluindo a ID. Você pode usar a id em etapas posteriores para atualizar ou excluir sua regra de elegibilidade.

```json
{
    "etag": 1,
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
