---
title: Criar uma oferta substituta
description: Uma oferta substituta é enviada aos clientes se eles não estiverem qualificados para outras ofertas
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1a9c074a-187a-45b1-9ad0-378aeef0d03d
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 13%

---

# Criar uma oferta substituta {#create-fallback-offer}

Você pode criar uma oferta substituta fazendo uma solicitação POST para a API [!DNL Offer Library] e, ao mesmo tempo, fornecendo sua ID de container.

## Cabeçalhos Accept e Content-Type {#accept-and-content-type-headers}

A tabela a seguir mostra os valores válidos que compõem os campos *Content-Type* e *Accept* no cabeçalho da solicitação:

| Nome do cabeçalho | Valor |
| ----------- | ----- |
| Aceitar | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Tipo de conteúdo | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1"` |

**Formato da API**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs do repositório. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | O container onde as ofertas substitutas estão localizadas. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Solicitação**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
        "xdm:status": "approved",
        "xdm:name": "Fallback for sales",
        "xdm:representations": [
            {
                "xdm:components": [
                    {
                        "dc:language": [
                            "en"
                        ],
                        "@type": "https://ns.adobe.com/experience/offer-management/content-component-html",
                        "dc:format": "text/html"
                    }
                ],
                "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                "xdm:placement": "xcore:offer-placement:124e0be5699743d3"
            }
        ]
}'
```

**Resposta**

Uma resposta bem-sucedida retorna informações sobre a oferta substituta recém-criada, incluindo sua ID de instância exclusiva e o posicionamento `@id`. Você pode usar a ID de instância em etapas posteriores para atualizar ou excluir sua oferta substituta. Você pode usar sua oferta exclusiva de fallback `@id` em um tutorial posterior para criar uma decisão.


```json
{
    "instanceId": "b3966680-13ec-11eb-9c20-8323709cfc65",
    "@id": "xcore:fallback-offer:124e2e764b1ac1b9",
    "repo:etag": 1,
    "repo:createdDate": "2023-10-21T22:28:11.111732Z",
    "repo:lastModifiedDate": "2023-10-21T22:28:11.111732Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
