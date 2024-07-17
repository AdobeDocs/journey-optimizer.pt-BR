---
title: Atualizar ofertas personalizadas
description: Uma oferta personalizada é uma mensagem de marketing personalizável baseada em regras de elegibilidade e restrições.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 9d8f2df6-aa04-4e66-8555-d51c2e409063
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 10%

---

# Atualizar uma oferta personalizada {#update-personalized-offer}

Você pode modificar ou atualizar uma oferta personalizada fazendo uma solicitação PATCH para a API [!DNL Offer Library]

Para obter mais informações sobre o Patch JSON, incluindo as operações disponíveis, consulte a [documentação oficial do Patch JSON](https://jsonpatch.com/).

## Cabeçalhos Accept e Content-Type {#accept-and-content-type-headers}

A tabela a seguir mostra os valores válidos que compõem o campo *Content-Type* no cabeçalho da solicitação:

| Nome do cabeçalho | Valor |
| ----------- | ----- |
| Tipo de conteúdo | `application/json` |

**Formato da API**

```http
PATCH /{ENDPOINT_PATH}/offers/{ID}?offer-type=personalized
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | A ID da entidade que você deseja atualizar. | `personalizedOffer1234` |

**Solicitação**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offers/personalizedOffer1234?offer-type=personalized' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated personalized offer"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated personalized offer description"
    }
]'
```

| Parâmetro | Descrição |
| --------- | ----------- |
| `op` | A chamada de operação usada para definir a ação necessária para atualizar a conexão. As operações incluem: `add`, `replace`, `remove`, `copy` e `test`. |
| `path` | O caminho do parâmetro a ser atualizado. |
| `value` | O novo valor com o qual você deseja atualizar seu parâmetro. |

**Resposta**

Uma resposta bem-sucedida retorna os detalhes atualizados do posicionamento, incluindo a ID do posicionamento.

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
