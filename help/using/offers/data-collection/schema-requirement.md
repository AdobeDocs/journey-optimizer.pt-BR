---
product: experience platform
solution: Experience Platform
title: Configurar captura de eventos
description: Saiba como configurar seu esquema de oferta para capturar eventos
feature: Ranking, Datasets, Decision Management
role: Developer, Data Engineer
level: Experienced
exl-id: f70ba749-f517-4e09-a381-243b21713b48
source-git-commit: 3b0931a532cc85b316718d590c2e5e78471be890
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 1%

---

# Configurar coleção de dados {#schema-requirements}

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
>Se você estiver usando a [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=pt-BR){target="_blank"} ou a [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html?lang=pt-BR){target="_blank"}, a conexão será feita automaticamente.
