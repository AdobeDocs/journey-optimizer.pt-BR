---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Pesquisar uma coleção
description: Coleções são subconjuntos de ofertas com base em condições predefinidas por um profissional de marketing, como a categoria da oferta.
feature: Decision Management, API, Collections
badge: label="Legado" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 723daab2-5590-4c44-acb6-93a77f2e7877
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/FhWiKNwWUr3amFyD3EoZvq1QTJh-tt5tK6qYYzNplTY
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 20%

---

# Pesquisar uma coleção {#look-up-collection}

>[!TIP]
>
>O serviço de Decisão, o novo recurso de tomada de decisão do [!DNL Adobe Journey Optimizer], agora está disponível por meio da experiência baseada em código e dos canais de email. [Saiba mais](../../../../experience-decisioning/gs-experience-decisioning.md)


Coleções são subconjuntos de ofertas com base em condições predefinidas por um profissional de marketing, como a categoria da oferta.

Você pode pesquisar coleções específicas fazendo uma solicitação GET para a API [!DNL Offer Library] que inclui a coleção `id` no caminho da solicitação.

**Formato da API**

```http
GET /{ENDPOINT_PATH}/offer-collections/{ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | A ID da entidade que você deseja pesquisar. | `offerCollection1234` |

**Solicitação**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-collections/offerCollection1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna os detalhes da coleção, incluindo informações sobre sua coleção exclusiva `id`.

```json
{
        "created": "2022-09-16T18:59:23.063+00:00",
    "modified": "2022-09-16T18:59:23.063+00:00",
    "etag": 1,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.4"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "offerCollection1234",
    "name": "Test Collection with tags",
    "filterType": "any-tags",
    "ids": [
        "tag1234"
    ],
    "labels": [
        "core/C5",
        "custom/myLabel"
    ]
}
```
