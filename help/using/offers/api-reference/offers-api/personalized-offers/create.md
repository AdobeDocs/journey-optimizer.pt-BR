---
title: Criar ofertas personalizadas
description: Uma oferta personalizada é uma mensagem de marketing personalizável com base em regras e restrições de elegibilidade.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 97dc9af3-ca31-4512-aad2-f959dfc9ad0b
source-git-commit: bdb7b6373cb9f5a64a74a8503f46adb3fd226f77
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 10%

---

# Criar uma oferta personalizada {#create-personalized-offer}

Uma oferta personalizada é uma mensagem de marketing personalizável com base em regras e restrições de elegibilidade.

Você pode criar uma oferta personalizada fazendo uma solicitação de POST para a [!DNL Offer Library] API, enquanto fornece a ID do contêiner.

## Aceitar e digitar cabeçalhos de tipo de conteúdo {#accept-and-content-type-headers}

A tabela a seguir mostra os valores válidos que compõem a variável *Tipo de conteúdo* e *Aceitar* campos no cabeçalho da solicitação:

| Nome do cabeçalho | Valor |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Tipo de conteúdo | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"` |

**Formato da API**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do terminal para APIs do repositório. | `https://platform.adobe.io/data/core/xcore/` |
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
            "xdm:startDate": "2020-10-01T16:00:00Z",
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

Uma resposta bem-sucedida retorna informações sobre a oferta personalizada recém-criada, incluindo sua ID de instância exclusiva e seu posicionamento `@id`. Você pode usar a ID da instância em etapas posteriores para atualizar ou excluir sua oferta personalizada.

```json
{
    "instanceId": "0f4bc230-13df-11eb-bc55-c11be7252432",
    "@id": "xcore:personalized-offer:124e181c8b0d7878",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-21T20:50:32.018624Z",
    "repo:lastModifiedDate": "2020-10-21T20:50:32.018624Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```

## Limitações {#limitations}

Atualmente, as representações de oferta e algumas restrições de oferta não são compatíveis com o dispositivo móvel [!DNL Experience Edge] fluxos de trabalho, por exemplo `Capping`. O `Capping` O valor do campo especifica o número de vezes que uma oferta pode ser apresentada em todos os usuários. Para obter mais detalhes, consulte [Documentação de regras e restrições de qualificação de oferta](../../../offer-library/creating-personalized-offers.md).