---
title: Utilização do Adobe Journey Optimizer com o Experience Platform Web SDK
description: Saiba como renderizar conteúdo personalizado com o Experience Platform Web SDK usando o Adobe Journey Optimizer
feature: Web Channel
topic: Content Management
role: Developer
level: Intermediate
keywords: ajo;ajo web;adobe jornada otimizer;renderDecisions;superfícies;decisões;propostas;escopo;esquema
source-git-commit: 2ab7c7b767f2f04cb4519d203d92f7f7d4611540
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 2%

---

# Usando [!DNL Adobe Journey Optimizer] com [!DNL Experience Platform Web SDK]

O [!DNL Adobe Experience Platform] [!DNL Web SDK] pode entregar e renderizar experiências personalizadas gerenciadas no [!DNL Adobe Journey Optimizer] para o canal da Web. Você pode usar um editor de WYSIWYG, o [!DNL Adobe Journey Optimizer] [Canal da Web](get-started-web.md), ou uma interface não visual, o [Canal de Experiência baseado em Código](../code-based/get-started-code-based.md) para criar, ativar e entregar suas campanhas do [!DNL Journey Optimizer Web] e experiências de personalização.

## Terminologia {#terminology}

**[!UICONTROL Superfície]**: uma superfície da Web é uma página da Web ou um local em uma página identificada por um URI onde o conteúdo de experiência [!DNL Adobe Journey Optimizer] será entregue.

**[!UICONTROL Propositions]**: em [!DNL Adobe Journey Optimizer], as propostas estão correlacionadas à experiência selecionada em um [!DNL Journey Optimizer Campaign].

## Habilitando [!DNL Adobe Journey Optimizer] {#enable-ajo}

Para começar a usar o [!DNL Adobe Journey Optimizer], siga as etapas abaixo.

1. Passe pelos [pré-requisitos](web-prerequisites.md), especificamente:
   * Configurar [!DNL Adobe Experience Cloud Visual Editing Helper].
   * Habilitar [!DNL Adobe Journey Optimizer] na sua [sequência de dados](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html?lang=pt-BR){target="_blank"}.
   * Habilite a opção [!UICONTROL Política de Mesclagem Ativa-na-Edge].

1. Adicione a opção `renderDecisions` aos seus eventos. Defina `renderDecisions` como `true` para renderização automática das propostas de conteúdo do Journey Optimizer entregues nas superfícies da sua página da Web.

   ```javascript
   alloy("sendEvent", {
       ...,
       "renderDecisions": true
   })
   ```

1. Como opção, especifique superfícies adicionais em seus eventos. Por padrão, o Web SDK gerará automaticamente a superfície da Web da página da Web atual e a incluirá na solicitação ao Edge Network. Se necessário, superfícies adicionais podem ser incluídas na solicitação especificando-as na opção `personalization.surfaces` do comando `sendEvent` ou na configuração da Extensão Web SDK correspondente **[!UICONTROL Superfícies]** [[!UICONTROL Ação Enviar evento]](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/action-types.html?lang=pt-BR#send-event){target="_blank"}.

   ```javascript
   alloy("sendEvent", {
       ...
       "personalization": {
           "surfaces": [ "web://my.site.com/about.html", "web://my.site.com/contact.html" ]
       }
   })
   ```

   ![extensão-adicionar-superfície](assets/extension-add-surface.png)

   Superfícies de evento estão incluídas no campo de solicitação `query.personalization.surfaces`:

   ```json
   {
   "events": [
       {
           "query": {
               "personalization": {
               "schemas": [
                   ...
               ],
               "decisionScopes": [
                   "__view__"
               ],
               "surfaces": [
                   "web://ajostage.weebly.com/"
               ]
               }
           },
           ...
       }
   ]
   }
   ```

1. Semelhante a outros recursos de personalização, você pode adicionar um **[trecho pré-ocultação](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/manage-flicker.html?lang=pt-BR){target="_blank"}** para ocultar apenas determinadas partes da página enquanto busca experiências.

## Renderização de conteúdo personalizado {#rendering-personalized-content}

Consulte a [documentação do Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/rendering-personalization-content.html?lang=pt-BR){target="_blank"} para obter mais informações sobre renderização de conteúdo personalizado.

As propostas Adobe Journey Optimizer para superfícies da web são processadas de maneira semelhante às `__view__` propostas de escopo de decisão. Especificamente, quando a opção `renderDecisions` estiver definida como `true` no comando `sendEvent`, eles serão renderizados automaticamente pelo Web SDK.

Exemplo de proposta de conteúdo do Journey Optimizer:

```json
{
    "scope": "web://ajostage.weebly.com/",
    "scopeDetails": {
        "correlationID": "ccfaf19c-6360-4aea-b464-0cf924db5da7",
        "characteristics": {
            "eventToken": "eyJtZXNzYWdlRXhlY3V0aW9uIjp7Im1lc3NhZ2VFeGVjdXRpb25JRCI6ImEzNDYxYTMzLTc5MjktNGQyNS1hNmMxLTVkYzM2YWY1NzRmMyIsIm1lc3NhZ2VJRCI6ImNjZmFmMTljLTYzNjAtNGFlYS1iNDY0LTBjZjkyNGRiNWRhNyIsIm1lc3NhZ2VUeXBlIjoibWFya2V0aW5nIiwiY2FtcGFpZ25JRCI6IjEzN2JmMzllLWM1ODgtNGI1My1iODQxLTJiMWZiZDYxM2JkYiIsImNhbXBhaWduVmVyc2lvbklEIjoiMTA1NzY1MmEtZWYwNS00YjE3LWExMmUtY2FlOTQyOTFhMWFjIiwiY2FtcGFpZ25BY3Rpb25JRCI6ImViNTlmODQ4LTk5ZDYtNGE1OC05YmU4LTk4MjIxODU0NmYzNiIsIm1lc3NhZ2VQdWJsaWNhdGlvbklEIjoiYzg2NzFjZmItNDdjYS00YTVjLTg4Y2YtNzYwZDFlZjU1MzQyIn0sIm1lc3NhZ2VQcm9maWxlIjp7ImNoYW5uZWwiOnsiX2lkIjoiaHR0cHM6Ly9ucy5hZG9iZS5jb20veGRtL2NoYW5uZWxzL3dlYiIsIl90eXBlIjoiaHR0cHM6Ly9ucy5hZG9iZS5jb20veGRtL2NoYW5uZWwtdHlwZXMvd2ViIn0sIm1lc3NhZ2VQcm9maWxlSUQiOiI2YTViY2I3ZC02MmYxLTQ5NDItODRkMC02MzE5ZjM5Zjk1ZGUifX0="
        },
        "decisionProvider": "AJO",
        "activity": {
            "id": "137bf39e-c588-4b53-b841-2b1fbd613bdb#eb59f848-99d6-4a58-9be8-982218546f36"
        }
    },
    "id": "002321c0-dff5-4153-b171-a9dfb70b9750",
    "items": [
        {
            "schema": "https://ns.adobe.com/personalization/dom-action",
            "data": {
                "uiData": {
                    "tagType": "Text",
                    "actionType": "changed"
                },
                "content": "Welcome AJO!",
                "prehidingSelector": "#wsite-content > DIV:nth-of-type(2) > DIV:nth-of-type(1) > DIV:nth-of-type(1) > DIV:nth-of-type(1) > DIV:nth-of-type(1) > DIV:nth-of-type(3) > FONT:nth-of-type(1) > SPAN:nth-of-type(1)",
                "type": "setHtml",
                "selector": "#wsite-content > DIV.wsite-section-wrap:eq(1) > DIV.wsite-section:eq(0) > DIV.wsite-section-content:eq(0) > DIV.container:eq(0) > DIV.wsite-section-elements:eq(0) > DIV.paragraph:eq(0) > FONT:nth-of-type(1) > SPAN:nth-of-type(1)"
            },
            "id": "0a522f66-9e6a-4ded-b1d0-e9167f103290"
        }
    ]
}
```

## Depuração {#debugging}

Para depurar implementações de personalização do Adobe Journey Optimizer, use a [Depuração do Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/debugging.html){target="_blank"}. [!DNL Adobe Journey Optimizer] rastreamentos de depuração estão disponíveis ao solucionar problemas usando [[!DNL Adobe Experience Platform Assurance]](https://developer.adobe.com/client-sdks/documentation/platform-assurance/). Verifique se há eventos com o prefixo `AJO:`.

![assurance-ajo-trace](assets/assurance-ajo-trace.png)
