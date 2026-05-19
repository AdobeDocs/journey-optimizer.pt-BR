---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Configurar captura de eventos
description: Saiba como configurar seu esquema de oferta para capturar eventos
badge: label="Legado" type="Informative"
feature: Ranking, Datasets, Decision Management
role: Developer
level: Experienced
exl-id: f70ba749-f517-4e09-a381-243b21713b48
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/DhaXO7sS2zR9iewgoQjrN5ptYNpYSt97e-hflU2iq7c
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2:
  - id: e08599ea-8888-4294-ba74-3ba0a7762a46
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: acc16deb-1d7f-4ec9-9ce3-6cdf355afde6
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 307
ht-degree: 10%

---

# Configurar coleção de dados {#schema-requirements}

>[!TIP]
>
>O serviço de Decisão, o novo recurso de tomada de decisão do [!DNL Adobe Journey Optimizer], agora está disponível por meio da experiência baseada em código e dos canais de email. [Saiba mais](../../experience-decisioning/gs-experience-decisioning.md)

Para poder obter feedback sobre tipos de evento que não sejam eventos de decisão, você deve definir o valor correto para cada tipo de evento em um **evento de experiência** enviado para o Adobe Experience Platform.

>[!CAUTION]
>
>Para cada tipo de evento, verifique se o esquema usado no conjunto de dados tem o grupo de campos **[!UICONTROL Evento de experiência - Interações de apresentação]** associado a ele. [Saiba mais](create-dataset.md)

Abaixo estão os requisitos de esquema que você precisa implementar no código JavaScript.

>[!NOTE]
>
>Os eventos de decisão não precisam ser enviados, pois o Gerenciamento de decisão gerará esses eventos automaticamente e os colocará no **conjunto de dados <!--to check--> de DecisionEvents&rbrack;** gerados automaticamente.

## Rastrear impressões {#track-impressions}

Verifique se o tipo e a origem do evento são os seguintes:

**Tipo de evento de experiência:** `decisioning.propositionDisplay`
**Source:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) ou assimilação em lote
+++**Carga de exemplo:**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2023-09-26T15:52:25+00:00",
    "xdm:eventType": "decisioning.propositionDisplay",
    "https://ns.adobe.com/experience/decisioning/propositions":
    [
        {
            "xdm:items":
            [
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee4",
                },
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee5",
                }
            ],
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id - taken from experience event for "nextBestOffer"
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id - taken from experience event for "nextBestOffer"
        }
    ]
}
```

+++

## Rastrear cliques {#track-clicks}

Verifique se o tipo e a origem do evento são os seguintes:

**Tipo de evento de experiência:** `decisioning.propositionInteract`
**Source:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) ou assimilação em lote
+++**Carga de exemplo:**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2023-09-26T15:52:25+00:00",
    "xdm:eventType": "decisioning.propositionInteract",
    "https://ns.adobe.com/experience/decisioning/propositions":
    [
        {
            "xdm:items":
            [
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee4"
                },
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee5"
                },
            ],
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id
        }
    ]
}
```

+++

## Rastrear eventos personalizados {#track-custom-events}

Para eventos personalizados, o esquema usado no conjunto de dados também deve ter o grupo de campos **[!UICONTROL Evento de experiência - Interações de apresentação]** associado a ele, mas não há requisito específico no tipo de evento de experiência que deve ser usado para marcar esses eventos.

>[!NOTE]
>
>Para contabilizar seus eventos personalizados no [limite de frequência](../offer-library/add-constraints.md#capping), é necessário conectar o evento de experiência aos pontos de extremidade do Adobe Experience Platform, enviando-o para um destes dois pontos de extremidade de coleta de dados do Edge:
>
>* POST /ee/v2/interage
>* POST /ee/v2/collect
>
>Se você estiver usando a [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=pt-BR){target="_blank"} ou a [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"}, a conexão será feita automaticamente.
