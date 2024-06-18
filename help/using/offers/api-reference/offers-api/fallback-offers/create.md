---
title: Criar uma oferta substituta
description: Uma oferta substituta é enviada aos clientes se eles não estiverem qualificados para outras ofertas
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 156d6c71-d8fd-4631-ae0c-44452d664dde
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 15%

---

# Criar uma oferta substituta {#create-fallback-offer}

Você pode criar uma oferta substituta fazendo uma solicitação POST para o [!DNL Offer Library] API.

## Cabeçalhos Accept e Content-Type {#accept-and-content-type-headers}

A tabela a seguir mostra os valores válidos que compõem a variável *Tipo de conteúdo* no cabeçalho da solicitação:

| Nome do cabeçalho | Valor |
| ----------- | ----- |
| Tipo de conteúdo | `application/json` |

**Formato da API**

```http
POST /{ENDPOINT_PATH}/offers/{ID}?offer-type=fallback
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps/` |

**Solicitação**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/offers?offer-type=fallback' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "Test Fallback Offer DPS",
    "description": "Fallback Offer description",
    "status": "approved",
    "selectionConstraint": {
        "startDate": "2022-06-10T00:30:00.000+00:00",
        "endDate": "2032-06-06T23:29:21.402+00:00",
        "profileConstraintType": "none"
    },
    "representations": [
        {
            "components": [
                {
                    "deliveryURL": "https://mysite.com",
                    "type": "imagelink",
                    "format": "image/png"
                }
            ],
            "channel": "https://ns.adobe.com/xdm/channel-types/web",
            "placement": "offerPlacement1234"
        }
    ],
    "rank": {
        "priority": 1
    }
}'
```

**Resposta**

Uma resposta bem-sucedida retorna informações sobre a oferta substituta recém-criada, incluindo sua oferta substituta exclusiva `id`. Você pode usar o `id` em etapas posteriores, para atualizar ou excluir sua oferta substituta ou para criar uma decisão em um tutorial posterior.


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
