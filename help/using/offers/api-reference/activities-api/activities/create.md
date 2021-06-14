---
title: Criar decisões
description: Uma decisão contém a lógica que informa a seleção de uma oferta.
feature: Ofertas
topic: Integrações
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 12%

---

# Criar uma decisão

Você pode criar uma decisão (anteriormente conhecida como atividade de oferta) fazendo uma solicitação de POST para a API [!DNL Offer Library], fornecendo a ID do contêiner.

## Aceitar e digitar cabeçalhos de tipo de conteúdo

A tabela a seguir mostra os valores válidos que compõem os campos *Content-Type* e *Accept* no cabeçalho da solicitação:

| Nome do cabeçalho | Valor |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Tipo de conteúdo | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"` |

**Formato da API**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do terminal para APIs do repositório. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | O contêiner onde as decisões estão localizadas. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Solicitação**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
        "xdm:name": "Activity 1",
        "xdm:startDate": "2020-10-01T16:00:00Z",
        "xdm:endDate": "2021-12-13T16:00:00Z",
        "xdm:status": "live",
        "xdm:criteria": [
            {
                "xdm:placements": [
                    "xcore:offer-placement:122204529514a2c0"
                ],
                "xdm:optionSelection": {
                    "xdm:filter": "xcore:offer-filter:122a120f234dac7f"
                }
            }
        ],
        "xdm:fallback": "xcore:fallback-offer:1233160780eaa2ef"
    }'
```

**Resposta**

Uma resposta bem-sucedida retorna informações sobre a decisão recém-criada, incluindo a ID de instância exclusiva e o posicionamento `@id`. Você pode usar a ID da instância em etapas posteriores para atualizar ou excluir sua decisão.

```json
{
    "instanceId": "f88c9be0-1245-11eb-8622-b77b60702882",
    "@id": "xcore:offer-activity:124b79dc3ce2d720",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-19T20:02:09.694067Z",
    "repo:lastModifiedDate": "2020-10-19T20:02:09.694067Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
