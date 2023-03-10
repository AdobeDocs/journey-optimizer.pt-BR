---
product: experience platform
solution: Experience Platform
title: Configurar captura de eventos
description: Saiba como configurar seu esquema de oferta para capturar eventos
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: f70ba749-f517-4e09-a381-243b21713b48
source-git-commit: b06b545d377fcd1ffe6ed218badeb94c1bb85ef2
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 2%

---

# Configurar coleção de dados {#schema-requirements}

<!--To send in feedback data, you must define how the experience events will be captured.-->

Para obter feedback sobre tipos de evento diferentes dos eventos de decisão, você deve definir o valor correto para cada tipo de evento em um **evento de experiência** que é enviado para o Adobe Experience Platform.

Para cada tipo de evento, verifique se o esquema usado no conjunto de dados tem o **[!UICONTROL Evento de experiência - Interações de apresentação]** grupo de campos associado a ele. [Saiba mais](create-dataset.md)

Abaixo estão os requisitos de esquema que você precisa implementar no seu código JavaScript.

>[!NOTE]
>
>Os eventos de decisão não precisam ser enviados, pois a Gestão de decisão gerará esses eventos automaticamente e os colocará na **[!UICONTROL ODE DecisionEvents]** conjunto de dados<!--to check--> que é gerado automaticamente.

## Rastrear impressões

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

## Rastrear cliques

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

## Rastrear eventos personalizados

Para eventos personalizados, o esquema usado no conjunto de dados também deve ter o **[!UICONTROL Evento de experiência - Interações de apresentação]** grupo de campos associado a ele, mas não há requisito específico no tipo de evento de experiência que deve ser usado para marcar esses eventos.

<!--
## Using a ranking strategy {#using-ranking}

To use the ranking strategy you created above, follow the steps below:

Once a ranking strategy has been created, you can assign it to a placement in a decision. For more on this, see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md).

1. Create a decision.
1. Add a placement.
1. Add a collection.
1. Choose to rank offers by AI ranking (select it from the drop-down list).
1. Click Add ranking.
1. Select the ranking strategy that you created. All the details of the ranking strategy are displayed.
1. Click Next to confirm.
1. Save your decision.

It is now ready to be used in a decision to rank eligible offers for a placement (see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md)).
-->
