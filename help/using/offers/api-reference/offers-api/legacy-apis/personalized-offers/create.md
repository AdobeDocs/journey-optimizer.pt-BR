---
title: Criar uma oferta personalizada
description: Uma oferta personalizada é uma mensagem de marketing personalizável baseada em regras de elegibilidade e restrições.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 234bee17-c830-4bc0-b258-182804df4cb3
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 11%

---

# Criar uma oferta personalizada {#create-personalized-offer}

Uma oferta personalizada é uma mensagem de marketing personalizável baseada em regras de elegibilidade e restrições.

Você pode criar uma oferta personalizada fazendo uma solicitação POST para a API [!DNL Offer Library] e, ao mesmo tempo, fornecendo sua ID de contêiner.

## Cabeçalhos Accept e Content-Type {#accept-and-content-type-headers}

A tabela a seguir mostra os valores válidos que compõem os campos *Content-Type* e *Accept* no cabeçalho da solicitação:

| Nome do cabeçalho | Valor |
| ----------- | ----- |
| Aceitar | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Tipo de conteúdo | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"` |

**Formato da API**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs do repositório. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | O container onde as ofertas personalizadas estão localizadas. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Solicitação**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
        "xdm:name": "Sale offer",
        "xdm:status": "draft",
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
                "xdm:placement": "xcore:offer-placement:124e0be5699743d3"
        }
    ],
        "xdm:selectionConstraint": {
            "xdm:startDate": "2023-10-01T16:00:00Z",
            "xdm:endDate": "2021-12-13T16:00:00Z",
            "xdm:eligibilityRule": "xcore:eligibility-rule:124e0faf5b8ee89b"
        },
        "xdm:rank": {
            "xdm:priority": 1
    },
        "xdm:cappingConstraint": {
            "xdm:globalCap": 150
    },
        "xdm:tags": [
            "xcore:tag:124e147572cd7866"
    ]
}'
```

**Resposta**

Uma resposta bem-sucedida retorna informações sobre a oferta personalizada recém-criada, incluindo sua ID de instância exclusiva e o posicionamento `@id`. Você pode usar a ID de instância em etapas posteriores para atualizar ou excluir sua oferta personalizada.

```json
{
    "instanceId": "0f4bc230-13df-11eb-bc55-c11be7252432",
    "@id": "xcore:personalized-offer:124e181c8b0d7878",
    "repo:etag": 1,
    "repo:createdDate": "2023-10-21T20:50:32.018624Z",
    "repo:lastModifiedDate": "2023-10-21T20:50:32.018624Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```

## Limitações {#limitations}

Atualmente, as representações de oferta e algumas restrições de oferta não são compatíveis com os fluxos de trabalho móveis [!DNL Experience Edge], por exemplo `Capping`. O valor do campo `Capping` especifica o número de vezes que uma oferta pode ser apresentada entre todos os usuários. Para obter mais detalhes, consulte [Documentação de regras e restrições de qualificação da oferta](../../../../offer-library/creating-personalized-offers.md).
