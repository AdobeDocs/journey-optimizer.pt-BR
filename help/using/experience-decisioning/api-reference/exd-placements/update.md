---
title: Atualizar posicionamento exd
description: O posicionamento estendido consiste em coleções associadas a restrições e métodos de classificação para determinar ofertas.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 8fa34ebb7c853f9af5b3f58574374a3acb641dd9
workflow-type: tm+mt
source-wordcount: '148'
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
