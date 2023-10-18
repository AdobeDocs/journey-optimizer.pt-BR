---
title: Atualizar coleções
description: Coleções são subconjuntos de ofertas com base em condições predefinidas por um profissional de marketing, como a categoria da oferta.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7d766f0a-4fcb-434a-bbfd-e18ade71ae56
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 9%

---

# Atualizar uma coleção {#update-collection}

Você pode modificar ou atualizar uma coleção fazendo uma solicitação PATCH para o [!DNL Offer Library] API

Para obter mais informações sobre o Patch JSON, incluindo as operações disponíveis, consulte o [Documentação de patch de JSON](https://jsonpatch.com/).

## Cabeçalhos Accept e Content-Type {#accept-and-content-type-headers}

A tabela a seguir mostra os valores válidos que compõem a variável *Tipo de conteúdo* no cabeçalho da solicitação:

| Nome do cabeçalho | Valor |
| ----------- | ----- |
| Tipo de conteúdo | `application/json` |

**Formato da API**

```http
PATCH /{ENDPOINT_PATH}/offer-collections/{ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | A ID da entidade que você deseja atualizar. | `offerCollection1234` |

**Solicitação**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offer-collections/offerCollection1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated offer collection"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated offer collection description"
    }
]'
```

| Parâmetro | Descrição |
| --------- | ----------- |
| `op` | A chamada de operação usada para definir a ação necessária para atualizar a conexão. As operações incluem: `add`, `replace`, `remove`, `copy` e `test`. |
| `path` | O caminho do parâmetro a ser atualizado. |
| `value` | O novo valor com o qual você deseja atualizar seu parâmetro. |

**Resposta**

Uma resposta bem-sucedida retorna os detalhes atualizados da coleção, incluindo sua coleção exclusiva `id`.

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
