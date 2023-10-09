---
title: Criar uma coleção
description: Coleções são subconjuntos de ofertas com base em condições predefinidas por um profissional de marketing, como a categoria da oferta.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: ea79add2-1ea7-4c5c-ba67-f99d10975c4f
source-git-commit: d312410ce2a91d3084d99e3caceb53ce4ada87b8
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 10%

---

# Criar uma coleção {#create-collection}

Coleções são subconjuntos de ofertas com base em condições predefinidas por um profissional de marketing, como a categoria da oferta.

Você pode criar uma coleção fazendo uma solicitação POST para a [!DNL Offer Library] ao fornecer a ID do contêiner.

## Cabeçalhos Accept e Content-Type {#accept-and-content-type-headers}

A tabela a seguir mostra os valores válidos que compõem a variável *Tipo de conteúdo* e *Aceitar* campos no cabeçalho da solicitação:

| Nome do cabeçalho | Valor |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Tipo de conteúdo | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1"` |

**Formato da API**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs do repositório. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | O container onde as coleções estão localizadas. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Solicitação**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
        "xdm:name": "Offer Collection 1",
        "xdm:filterType": "anyTags",
        "xdm:ids": [
            "xcore:tag:124e147572cd7866"
        ]
    }'
```

**Resposta**

Uma resposta bem-sucedida retorna informações sobre a coleção recém-criada, incluindo a ID de instância exclusiva e o posicionamento `@id`. Você pode usar a ID de instância em etapas posteriores para atualizar ou excluir sua coleção. Você pode usar sua coleção exclusiva `@id` em um tutorial posterior para criar uma decisão.

```json
{
   "@id": "xcore:offer-filter:124e3594ce8b4930",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-21T22:59:17.345797Z",
    "repo:lastModifiedDate": "2020-10-21T22:59:17.345797Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
