---
title: Pesquisar um qualificador de coleção
description: Os qualificadores de coleção permitem organizar e classificar melhor suas ofertas.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: f31e6a17-c99a-4db9-a301-426a1f0bcc92
source-git-commit: d312410ce2a91d3084d99e3caceb53ce4ada87b8
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 7%

---

# Pesquisar um qualificador de coleção {#look-up-tag}

Você pode pesquisar qualificadores de coleção específicos (anteriormente conhecidos como &quot;tags&quot;) fazendo uma solicitação GET para o [!DNL Offer Library] API que inclui o qualificador de coleção `id` no caminho da solicitação.

**Formato da API**

```http
GET /{ENDPOINT_PATH}/tags/{ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs do repositório. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | A ID da entidade que você deseja pesquisar. | `tag1234` |

**Solicitação**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/tags/tag1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna os detalhes do qualificador de coleta, incluindo informações sobre seu qualificador de coleta exclusivo `id`.

```json
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
}
```
