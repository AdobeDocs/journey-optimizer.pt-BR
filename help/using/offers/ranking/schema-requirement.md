---
product: experience platform
solution: Experience Platform
title: Configurar captura de eventos
description: Saiba como configurar o schema de ofertas para capturar eventos
feature: Ranking Formulas
role: User
level: Intermediate
source-git-commit: 12b01cb9de84399e5ede987866609acc10b64c5f
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# Configurar captura de eventos {#schema-requirements}

Nesse ponto, você deve ter:

* criou o modelo de IA,
* definiu qual tipo de evento você deseja capturar - oferta exibida (impressão) e/ou oferta clicada (conversão),
* e em qual conjunto de dados você deseja coletar os dados do evento.

Agora, cada vez que uma oferta é exibida e/ou clicada, você deseja que o evento correspondente seja capturado automaticamente pela variável **[!UICONTROL Experience Event - Proposition Interactions]** grupo de campos que usa a variável [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html#what-is-adobe-experience-platform-web-sdk%3F){target=&quot;_blank&quot;} ou SDK do Mobile.

Para poder enviar tipos de evento (oferta exibida ou oferta clicada), você deve definir o valor correto para cada tipo de evento em um evento de experiência enviado para o Adobe Experience Platform. Abaixo estão os requisitos de esquema que você precisa implementar no código JavaScript:

### Cenário exibido da oferta

**Tipo de evento:** `decisioning.propositionDisplay`
**Fonte:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) ou a ingestão por lotes
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
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id - taken from experience event for “nextBestOffer”
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id - taken from experience event for “nextBestOffer”
        }
    ]
}
```

+++

### Cenário de oferta clicada

**Tipo de evento:** `decisioning.propositionInteract`
**Fonte:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) ou a ingestão por lotes
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

