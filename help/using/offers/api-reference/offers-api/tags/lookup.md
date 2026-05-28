---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Pesquisar um qualificador de coleção
description: Os qualificadores de coleção permitem organizar e classificar melhor suas ofertas.
feature: Decision Management, API
badge: label="Legado" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: e2d1f093-c1b8-4c4c-a20f-4bd7c2ea5269
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/0WZUQu9VYFAdMn0t5WVzBxc94a7DcEN2zjqXIMbLg8k
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 117
ht-degree: 22%

---

# Pesquisar um qualificador de coleção {#look-up-tag}

>[!TIP]
>
>O serviço de Decisão, o novo recurso de tomada de decisão do [!DNL Adobe Journey Optimizer], agora está disponível por meio da experiência baseada em código e dos canais de email. [Saiba mais](../../../../experience-decisioning/gs-experience-decisioning.md)


Você pode pesquisar qualificadores de coleção específicos (anteriormente conhecidos como &quot;tags&quot;) fazendo uma solicitação GET para a API da Biblioteca de ofertas que inclui a ID do qualificador de coleção no caminho da solicitação.

**Formato da API**

```http
GET /{ENDPOINT_PATH}/tags/{ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps/` |
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

Uma resposta bem-sucedida retorna os detalhes do qualificador de coleção, incluindo informações sobre ID de contêiner, ID de instância e qualificador de coleção exclusivo `@id`.

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
