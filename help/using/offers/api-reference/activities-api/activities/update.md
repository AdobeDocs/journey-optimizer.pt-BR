---
title: Atualizar decisões
description: Uma decisão contém a lógica que informa a seleção de uma oferta.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 6%

---

# Atualizar uma decisão

Você pode modificar ou atualizar uma decisão em seu contêiner fazendo uma solicitação de PATCH para a API [!DNL Offer Library].

Para obter mais informações sobre o Patch JSON, incluindo operações disponíveis, consulte a [documentação oficial do Patch JSON](http://jsonpatch.com/).

## Aceitar e digitar cabeçalhos de tipo de conteúdo

A tabela a seguir mostra os valores válidos que compõem os campos *Content-Type* e *Accept* no cabeçalho da solicitação:

| Nome do cabeçalho | Valor |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Tipo de conteúdo | `application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"` |

**Formato da API**

```http
PATCH /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do terminal para APIs do repositório. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | O contêiner onde as decisões estão localizadas. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | O ID da instância da decisão. | `f88c9be0-1245-11eb-8622-b77b60702882` |

**Solicitação**

```shell
curl -X PATCH \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/f88c9be0-1245-11eb-8622-b77b60702882' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '[
        {
            "op": "replace",
            "path": "/_instance/xdm:name",
            "value": "Example Activity Name"
        }
    ]'
```

| Parâmetro | Descrição |
| --------- | ----------- |
| `op` | A chamada de operação usada para definir a ação necessária para atualizar a conexão. As operações incluem: `add`, `replace` e `remove`. |
| `path` | O caminho do parâmetro a ser atualizado. |
| `value` | O novo valor com o qual você deseja atualizar seu parâmetro. |

**Resposta**

Uma resposta bem-sucedida retorna os detalhes atualizados da decisão, incluindo a ID de instância exclusiva e a decisão `@id`.

```json
{
    "instanceId": "f88c9be0-1245-11eb-8622-b77b60702882",
    "@id": "xcore:offer-activity:124b79dc3ce2d720",
    "repo:etag": 2,
    "repo:createdDate": "2020-10-19T20:02:09.694067Z",
    "repo:lastModifiedDate": "2020-10-19T21:28:24.284719Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
