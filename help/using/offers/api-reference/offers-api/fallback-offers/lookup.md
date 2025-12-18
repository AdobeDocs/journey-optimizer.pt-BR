---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: pesquisar ofertas substitutas
description: Uma oferta substituta é enviada aos clientes se eles não estiverem qualificados para outras ofertas
feature: Decision Management, API
badge: label="Legado" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 8f1fa116-30d2-4732-8973-bbce0dc66dec
version: Journey Orchestration
source-git-commit: 0b6d41fad9715985ec6418cdda27760f977bbc47
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 23%

---

# Pesquisar ofertas substitutas {#look-up-fallback-offers}

>[!TIP]
>
>O serviço de Decisão, o novo recurso de tomada de decisão do [!DNL Adobe Journey Optimizer], agora está disponível por meio da experiência baseada em código e dos canais de email. [Saiba mais](../../../../experience-decisioning/gs-experience-decisioning.md)


Você pode pesquisar ofertas substitutas específicas fazendo uma solicitação GET para a API [!DNL Offer Library] que inclui a ID da oferta substituta no caminho da solicitação.

**Formato da API**

```http
GET /{ENDPOINT_PATH}/offers/{ID}?offer-type=fallback
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | A ID da entidade que você deseja pesquisar. | `fallbackOffer1234` |

**Solicitação**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offers/fallbackOffer1234?offer-type=fallback' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna os detalhes da oferta substituta, incluindo informações sobre a oferta substituta e a id exclusiva da oferta substituta.

```json
{
    "created": "2023-06-08T14:04:41.011+00:00",
    "modified": "2023-06-08T14:04:41.011+00:00",
    "etag": 1,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.8"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "fallbackOffer1234",
    "name": "Fallback Offer Web",
    "description": "Fallback Offer Web Description",
    "status": "draft",
    "representations": [
        {
            "channel": "https://ns.adobe.com/xdm/channel-types/web",
            "placement": "offerPlacement1234",
            "components": [
                {
                    "type": "imagelink",
                    "format": "image/png",
                    "deliveryURL": "https://mysite.com"
                }
            ]
        }
    ]
}
```
