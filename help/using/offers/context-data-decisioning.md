---
product: experience platform
solution: Experience Platform
title: Dados de contexto e solicitações de decisão
description: Saiba como transmitir dados de contexto em solicitações de decisão.
feature: Decision Management
role: Developer, Data Engineer
level: Experienced
source-git-commit: 9b66f4871d8b539bf0201b2974590672205a3243
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# Dados de contexto e solicitações de decisão {#context-data-decisioning}

Esta seção orienta você sobre a transmissão de dados de contexto nas solicitações de Decisão e seu uso nas regras de qualificação.

>[!BEGINSHADEBOX]

Para ir além, você também pode aproveitar o contexto em **fórmulas de classificação** para aumentar suas ofertas. Exemplos detalhados de fórmulas de classificação aproveitando dados de contexto estão disponíveis em [esta seção](../offers/ranking/create-ranking-formulas.md#context-data).

>[!ENDSHADEBOX]

## Transmitir dados de contexto em solicitações de decisão

Os dados de contexto em solicitações de Decisão são definidos usando a chave: `xdm:ContextData`.

Os atributos dos dados de contexto não são orientados pelo esquema XDM. Você pode transmitir quaisquer dados de contexto em JSON como parte da carga da solicitação de decisão.

Esta é uma amostra de solicitação de decisão com dados de contexto (consulte `xdm:ContextData`):

```
curl --location 'https://platform-stage.adobe.io/data/core/ods/decisions' \
--header 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
--header 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"' \
--header 'Authorization: Bearer eyJhbGciOi....' \
--header 'x-api-key: {{api_key}}' \
--header 'x-gw-ims-org-id: {{ims_org}}' \
--header 'x-sandbox-name: {{sandbox_name}}' \
--header 'x-request-id: {{$guid}}' \
--data-raw '{
    "xdm:propositionRequests": [
        {
            "xdm:activityId": "dps:offer-activity:19978bf95ebfc8fb",
            "xdm:placementId": "dps:offer-placement:199772e1c90d50ac"
        }
    ],
    "xdm:profiles": [
        {
            "xdm:identityMap": {
                "Email": [
                    {
                        "xdm:id": "test@test.com",
                        "primary": true
                    }
                ]
            },
            "xdm:contextData": [
                {
                    "@type": "_xdm.context.additionalParameters;version=1",
                    "xdm:data": {
                        "xdm:channel": "mobile",
                        "xdm:language": "en",
                        "xdm:isThirdParty": true,
                        "xdm:mobileVersion": "3.0.5106",
                        "xdm:mobileVersionMajor": "3",
                        "xdm:mobileVersionMinor": "0",
                        "xdm:mobileVersionPatch": "125",
                        "xdm:deviceType": "iOS",
                        "xdm:features": [
                            "p1000",
                            "p1001"
                        ]
                    }
                }
            ]
        }
    ],
    "xdm:allowDuplicatePropositions": {
        "xdm:acrossActivities": true,
        "xdm:acrossPlacements": true
    },
    "xdm:responseFormat": {
        "xdm:includeContent": true,
        "xdm:includeMetadata": {
            "xdm:activity": [
                "name"
            ],
            "xdm:option": [
                "name"
            ],
            "xdm:placement": [
                "name"
            ]
        }
    }
}'
```

## Usar dados de contexto em regras de elegibilidade

Estes são exemplos ilustrando como usar dados de contexto transmitidos em solicitações de Decisão nas regras de elegibilidade.

* Elegível se os recursos de dados de contexto contiverem um valor específico:

  ```
  select contextData from @{_xdm.context.additionalParameters;version=1} where contextData.features AND (select personetic from contextData.features where personetic.contains("123"))
  ```

* Qualificado se o canal não estiver vazio e for igual a móvel:

  ```
  select contextData from @{_xdm.context.additionalParameters;version=1} where !contextData.channel.isNull() AND contextData.channel!="" AND contextData.channel="mobile"
  ```
