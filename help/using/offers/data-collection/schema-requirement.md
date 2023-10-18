---
product: experience platform
solution: Experience Platform
title: Configurar captura de eventos
description: Saiba como configurar seu esquema de oferta para capturar eventos
feature: Ranking, Datasets, Decision Management
role: Developer, Data Engineer
level: Experienced
exl-id: f70ba749-f517-4e09-a381-243b21713b48
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 5%

---

# Configurar a coleção de dados {#schema-requirements}

Para obter feedback sobre tipos de evento diferentes dos eventos de decisão, você deve definir o valor correto para cada tipo de evento em um **evento de experiência** que é enviado para o Adobe Experience Platform.

>[!CAUTION]
>
>Para cada tipo de evento, verifique se o esquema usado no conjunto de dados tem o **[!UICONTROL Evento de experiência - Interações de apresentação]** grupo de campos associado a ele. [Saiba mais](create-dataset.md)

Abaixo estão os requisitos de esquema que você precisa implementar no seu código JavaScript.

>[!NOTE]
>
>Os eventos de decisão não precisam ser enviados, pois a Gestão de decisão gerará esses eventos automaticamente e os colocará na **[!UICONTROL ODE DecisionEvents]** conjunto de dados<!--to check--> que é gerado automaticamente.

## Rastrear impressões {#track-impressions}

Verifique se o tipo e a origem do evento são os seguintes:

**Tipo de evento de experiência:** `decisioning.propositionDisplay`
**Fonte:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) ou assimilação em lote
+++**Carga de exemplo:**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2020-09-26T15:52:25+00:00",
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
**Fonte:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) ou assimilação em lote
+++**Carga de exemplo:**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2020-09-26T15:52:25+00:00",
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

Para eventos personalizados, o esquema usado no conjunto de dados também deve ter o **[!UICONTROL Evento de experiência - Interações de apresentação]** grupo de campos associado a ele, mas não há requisito específico no tipo de evento de experiência que deve ser usado para marcar esses eventos.

>[!NOTE]
>
>Para contabilizar os eventos personalizados no [limite de frequência](../offer-library/add-constraints.md#capping), é necessário conectar o evento de experiência aos endpoints do Adobe Experience Platform, enviando-o para um desses dois endpoints de coleta de dados do Edge:
>
>* POST /ee/v2/interaction
>* POST /ee/v2/collect
>
>Se você estiver usando a variável [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=pt-BR){target="_blank"} or [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"}, a conexão é feita automaticamente.
