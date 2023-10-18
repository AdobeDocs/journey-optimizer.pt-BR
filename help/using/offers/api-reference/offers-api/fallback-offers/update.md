---
title: Atualizar uma oferta substituta
description: Uma oferta substituta é enviada aos clientes se eles não estiverem qualificados para outras ofertas
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7ff69887-620f-4bc0-b8ff-5144ff30696c
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 12%

---

# Atualizar uma oferta substituta {#update-fallback-offer}

Você pode modificar ou atualizar uma oferta substituta no seu contêiner fazendo uma solicitação PATCH para o [!DNL Offer Library] API.

Para obter mais informações sobre o Patch JSON, incluindo as operações disponíveis, consulte o [Documentação de patch de JSON](https://jsonpatch.com/).

## Cabeçalhos Accept e Content-Type {#accept-and-content-type-headers}

A tabela a seguir mostra os valores válidos que compõem a variável *Tipo de conteúdo* e *Aceitar* campos no cabeçalho da solicitação:

| Nome do cabeçalho | Valor |
| ----------- | ----- |
| Tipo de conteúdo | `application/json` |

**Formato da API**

```http
PATCH /{ENDPOINT_PATH}/offers/{ID}?offer-type=fallback
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | A ID da entidade que você deseja atualizar. | `fallbackOffer1234` |

**Solicitação**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offers/fallbackOffer1234?offer-type=fallback' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated fallback offer"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated fallback offer description"
    }
]'
```

| Parâmetro | Descrição |
| --------- | ----------- |
| `op` | A chamada de operação usada para definir a ação necessária para atualizar a conexão. As operações incluem: `add`, `replace`, `remove`, `copy` e `test`. |
| `path` | O caminho do parâmetro a ser atualizado. |
| `value` | O novo valor com o qual você deseja atualizar seu parâmetro. |

**Resposta**

Uma resposta bem-sucedida retorna os detalhes atualizados da oferta substituta, incluindo seus `id`.

```json
{
    "id": "{ID}",
    "datasetId": "{DATASET_ID}",
    "sandboxId": "{SANDBOX_ID}",
    "etag": 2,
    "createdDate": "2023-09-07T12:47:43.012Z",
    "lastModifiedDate": "2023-09-07T12:47:43.012Z",
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
