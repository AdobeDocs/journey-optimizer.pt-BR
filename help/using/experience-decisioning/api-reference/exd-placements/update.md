---
title: Atualizar posicionamento exd
description: O posicionamento estendido consiste em coleções associadas a restrições e métodos de classificação para determinar ofertas.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
version: Journey Orchestration
exl-id: 74e090e1-4dbe-484b-a482-ef43e082e7b1
TQID: https://experienceleague.adobe.com/6RpNeMQUn2qEfAzQ-Q7f7PgBRJCLqp7WnsoKx0xr12s
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 151
ht-degree: 7%

---

# Atualizar uma inserção de saída {#update-exd-placement}

Você pode modificar ou atualizar um posicionamento fazendo uma solicitação PUT para a API da Biblioteca de ofertas.

Para obter mais informações sobre o JSON PUT, incluindo as operações disponíveis, consulte a documentação oficial do JSON PUT.

**Cabeçalhos Aceitar e Tipo de Conteúdo**

A tabela a seguir mostra os valores válidos que compõem os campos Content-Type no cabeçalho da solicitação:

| Parâmetro | Descrição |
| --------- | ----------- |
| Tipo de conteúdo | `application/json` |

**Formato da API**

```http
PUT /{ENDPOINT_PATH}/exd-placements/{ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs de persistência. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | A ID da entidade que você deseja atualizar. | `placement1234` |

**Solicitação**

```shell
curl --location --request PUT 'https://platform-stage.adobe.io/data/core/dps/exd-placements/dps:exd-placement:19aca09b0a456e57' \
--H 'Content-Type: application/json' \
--H 'x-gw-ims-org-id: {IMS_ORG}' \
--H 'x-sandbox-name: {SANDBOX_NAME}' \
--H 'x-api-key: {API_KEY}' \
--H 'Authorization: Bearer {ACCESS_TOKEN}' \
--X '{
  "id":"dps:exd-placement:19aca09b0a456e57",
  "description": "Keyboard application",
  "status":"archived"
}'
```

| Parâmetro | Descrição |
| --------- | ----------- |
| `value` | O novo valor com o qual você deseja atualizar seu parâmetro. |
| `path` | O caminho do parâmetro a ser atualizado. |
| `op` | A chamada de operação usada para definir a ação necessária para atualizar a conexão. As operações incluem: `add`, `replace`, `remove`, `copy` e `test`. |

**Resposta**

Uma resposta bem-sucedida retorna os detalhes atualizados do posicionamento de extensão, incluindo a ID.

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
