---
solution: Journey Optimizer
product: Journey Optimizer
title: Configurar captura de eventos
description: Saiba como configurar seu esquema de oferta para capturar eventos
feature: Ranking, Datasets, Decision Management
role: Developer
level: Experienced
exl-id: ce3a2c33-c15b-436f-90b1-7373d7b2b1ca
version: Journey Orchestration
source-git-commit: 5de16a8f69089e49484104bbae109df111cbf1ed
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 1%

---

# Configurar coleção de dados {#schema-requirements}

Para poder obter feedback sobre tipos de evento que não sejam eventos de decisão, você deve definir o valor correto para cada tipo de evento em um **evento de experiência** enviado para o Adobe Experience Platform.

>[!CAUTION]
>
>Para cada tipo de evento, verifique se o esquema usado no conjunto de dados tem o grupo de campos **[!UICONTROL Evento de experiência - Interações de apresentação]** associado a ele. <!--[Learn more](create-dataset.md)-->

Abaixo estão os requisitos de esquema que você precisa implementar no código JavaScript.

## Rastrear impressões {#track-impressions}

Verifique se os seguintes campos estão configurados corretamente:

**Tipo de evento de experiência:** `decisioning.propositionDisplay`

**propositionEventType:** `_experience.decisioning.propositionEventType.display`

**Source:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) ou assimilação em lote

+++**Carga de exemplo:**

```json
{
  "_experience": {
    "decisioning": {
      "propositionEventType": {
        "display": 1
      },
      "proposition": [
        {
          "items": [
            {
              "itemSelection": {
                "rankingDetail": {
                  "algorithmID": "RANDOM",
                  "strategyID": "1YYKhS4MImWqIBrpudMIf4",
                  "trafficType": "random",
                  "step": "aiModel"
                },
                "selectionDetail": {
                  "selectionType": "selectionStrategy",
                  "strategyName": "not a real selection strategy",
                  "strategyID": "dps:selection-strategy:1b630b32da42125a",
                  "version": "35a6b5b1-62ff-4a4b-94cd-96852a59d89a"
                }
              },
              "name": "not a real offer",
              "id": "dps:14c7468e7f6271ff8023748a1146d11f05f77b7fc1368081:1b630a7d8d9f2g4j",
              "score": 0.9765416360350985
            }
          ],
          "scopeDetails": {
            "decisionPolicy": {
              "id": "01c3ad3d-6d41-4013-a88f-5a4975579179"
            },
            "decisionProvider": "EXD",
            "placement": {
              "id": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test"
            },
            "correlationID": "28ca161e-552c-464e-dh37-bc38d4ce944b-0"
          },
          "scope": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test",
          "id": "86fb8f37-0498-4533-9dab-c206690c1f67"
        }
      ],
      "exdRequestID": "edb61199-ef92-46c8-adc5-f622df5b9078"
    }
  },
  "eventType": "decisioning.propositionDisplay",
  "_id": "04b5384e-c09c-4df8-b6f0-7c476a51b219",
  "timestamp": "2025-10-07T20:22:00Z"
}
```

+++

## Rastrear cliques {#track-clicks}

Verifique se os seguintes campos estão configurados corretamente:

**Tipo de evento de experiência:** `decisioning.propositionInteract`

**propositionEventType:** `_experience.decisioning.propositionEventType.interact`

**Source:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) ou assimilação em lote

Cada oferta em uma proposta inclui um token de rastreamento, que é um identificador exclusivo gerado pelo Adobe. Esse token deve ser transmitido exatamente como recebido, sem alteração, no evento de clique ou impressão correspondente. Os tokens de rastreamento correspondentes garantem que o Adobe possa associar precisamente a ação do usuário à decisão de oferta correta, permitindo a geração de relatórios downstream e a otimização baseada em IA.

+++**Carga de exemplo:**

```json
{
  "_experience": {
    "decisioning": {
      "propositionEventType": {
        "interact": 1
      },
      "propositionAction": {
        "tokens": [
          "Vx9fwWXmp6/kyYRVOUZWEQ"
        ]
      },
      "proposition": [
        {
          "items": [
            {
              "itemSelection": {
                "rankingDetail": {
                  "algorithmID": "RANDOM",
                  "strategyID": "1YYKhS4MImWqIBrpudMIf4",
                  "trafficType": "random",
                  "step": "aiModel"
                },
                "selectionDetail": {
                  "selectionType": "selectionStrategy",
                  "strategyName": "not a real selection strategy",
                  "strategyID": "dps:selection-strategy:1b630b32da42125a",
                  "version": "35a6b5b1-62ff-4a4b-94cd-96852a59d89a"
                }
              },
              "name": "not a real offer",
              "id": "dps:14c7468e7f6271ff8023748a1146d11f05f77b7fc1368081:1b630a7d8d9f2g4j",
              "score": 0.9765416360350985
            }
          ],
          "scopeDetails": {
            "decisionPolicy": {
              "id": "01c3ad3d-6d41-4013-a88f-5a4975579179"
            },
            "decisionProvider": "EXD",
            "placement": {
              "id": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test"
            },
            "correlationID": "28ca161e-552c-464e-dh37-bc38d4ce944b-0"
          },
          "scope": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test",
          "id": "86fb8f37-0498-4533-9dab-c206690c1f67"
        }
      ],
      "exdRequestID": "edb61199-ef92-46c8-adc5-f622df5b9078"
    }
  },
  "eventType": "decisioning.propositionInteract",
  "_id": "04b5384e-c09c-4df8-b6f0-7c476a51b765",
  "timestamp": "2025-10-07T20:50:00Z"
}
```

+++

## Rastrear eventos personalizados {#track-custom-events}

Para eventos personalizados, o esquema usado no conjunto de dados também deve ter o grupo de campos **[!UICONTROL Evento de experiência - Interações de apresentação]** associado a ele, mas não há requisito específico no tipo de evento de experiência que deve ser usado para marcar esses eventos.

<!--

>[!NOTE]
>
>To have your custom events accounted for in [capping](../items.md#capping), you need to connect the experience event to Adobe Experience Platform endpoints by sending it to either one of these two Edge data collection endpoints:
>
>* POST /ee/v2/interact
>* POST /ee/v2/collect
>
>If you are using the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=pt-BR){target="_blank"} or [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html?lang=pt-BR){target="_blank"}, the connection is made automatically.-->

