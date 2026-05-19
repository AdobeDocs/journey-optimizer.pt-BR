---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Pesquisar um qualificador de coleção
description: Os qualificadores de coleção permitem organizar e classificar melhor suas ofertas.
feature: Decision Management, API
badge: label="Herdados" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: f31e6a17-c99a-4db9-a301-426a1f0bcc92
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/w6XntRXFGM5FsYNK2-wJNZNdzJvqc7kmDZbvrkQWKj8
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2:
  - id: ed0d8d0e-04b9-4326-be72-a0fbca265377
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 109
ht-degree: 0%

---

# Pesquisar um qualificador de coleção {#look-up-tag}

>[!TIP]
>
>A decisão, o novo recurso de decisão do [!DNL Adobe Journey Optimizer], agora está disponível por meio da experiência baseada em código e canais de email! [Saiba mais](../../../../../experience-decisioning/gs-experience-decisioning.md)


Você pode pesquisar qualificadores de coleção específicos (anteriormente conhecidos como &quot;tags&quot;) fazendo uma solicitação GET para a API [!DNL Offer Library] que inclui o qualificador de coleção `id` no caminho da solicitação.

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

Uma resposta bem-sucedida retorna os detalhes do qualificador de coleção, incluindo informações sobre o qualificador de coleção exclusivo `id`.

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
