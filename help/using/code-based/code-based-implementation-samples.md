---
title: Amostras de implementação baseadas em código
description: Esta página mostra amostras do método de implementação para o recurso baseado em código do Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: Developer
level: Experienced
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: e5ae8b4e-7cd2-4a1d-b2c0-8dafd5c4cdfd
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '823'
ht-degree: 7%

---

# Amostras de métodos de implementação baseados em código {#implementation-samples}

>[!BEGINSHADEBOX]

O que há neste guia de documentação:

* [Introdução ao canal baseado em código](get-started-code-based.md)
* [Pré-requisitos baseados em código](code-based-prerequisites.md)
* **[Amostras de implementação baseadas em código](code-based-implementation-samples.md)**
* [Criar experiências baseadas em código](create-code-based.md)

>[!ENDSHADEBOX]

A experiência baseada em código é compatível com qualquer tipo de implementação de cliente. Nesta página, você pode encontrar amostras para cada método de implementação:

* [Lado do cliente](#client-side-implementation)
* [Lado do servidor](#server-side-implementation)
* [Híbrido](#hybrid-implementation)

Você também pode seguir [este link](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"} para encontrar implementações de amostra para diferentes casos de uso de personalização e experimentação. Confira-as e execute-as para entender melhor quais são as etapas de implementação necessárias e como funciona o fluxo de personalização completo.

## Implementação do lado do cliente {#client-side-implementation}

Se você tiver uma implementação no lado do cliente, poderá usar um dos SDKs do cliente da AEP: AEP Web SDK ou AEP Mobile SDK. As etapas abaixo descrevem o processo de busca do conteúdo publicado na borda pelas campanhas de experiência baseadas em código em uma amostra da implementação do SDK da Web e a exibição do conteúdo personalizado.

### Como funciona

1. [SDK da Web](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=pt-BR){target="_blank"} está incluído na página.

1. Você precisa usar o `sendEvent` e especifique o URI de superfície para buscar conteúdo de personalização.

   ```javascript
   alloy("sendEvent", {
   renderDecisions: true,
   personalization: {
       surfaces: ["#sample-json-content"],
   },
   }).then(applyPersonalization("#sample-json-content"));
   ```

1. Os itens de experiência baseados em código devem ser aplicados manualmente pelo código de implementação (usando o [`applyPersonalization`](https://github.com/adobe/alloy-samples/blob/ac83b6927d007dc456caad2c6ce0b324c99c26c9/ajo/personalization-client-side/public/script.js){target="_blank"} para atualizar o DOM com base na decisão.

1. Para campanhas de experiência baseadas em código, os eventos de exibição devem ser enviados manualmente para indicar quando o conteúdo foi exibido. Isso é feito por meio da `sendEvent` comando.

```javascript
function sendDisplayEvent(decision) {
  const { id, scope, scopeDetails = {} } = decision;

  alloy("sendEvent", {

    xdm: {
      eventType: "decisioning.propositionDisplay",
      _experience: {
        decisioning: {
          propositions: [
            {
              id: id,
              scope: scope,
              scopeDetails: scopeDetails,
            },
          ],
        },
      },
    },
  });
}
```

### Principais observações

**Cookies**

Os cookies são usados para manter a identidade do usuário e as informações do cluster. Ao usar uma implementação no lado do cliente, o SDK da Web lida com o armazenamento e envio desses cookies automaticamente durante o ciclo de vida da solicitação.

| Cookie | Propósito | Armazenado por | Enviado por |
| ------------------------ | -------------------------------------------------------------------------- | --------- | ------- |
| kndctr_AdobeOrg_identity | Contém detalhes da identidade do usuário | Web SDK | Web SDK |
| kndctr_AdobeOrg_cluster | Indica qual cluster de borda de experiência deve ser usado para atender a solicitações | Web SDK | Web SDK |

**Solicitar posicionamento**

As solicitações para a API do Adobe Experience Platform são necessárias para obter apresentações e enviar uma notificação de exibição. Ao usar uma implementação no lado do cliente, o SDK da Web faz essas solicitações quando a variável `sendEvent` é usado.

| Solicitação | Feito por |
| ---------------------------------------------- | ----------------------------------- |
| solicitação de interação para obter apresentações | SDK da Web usando o comando sendEvent |
| solicitação de interação para enviar notificações de exibição | SDK da Web usando o comando sendEvent |

**Diagrama de Fluxo**

![](assets/code-based-client-side-implementation.png)

## Implementação do lado do servidor {#server-side-implementation}

Se você tiver uma implementação do lado do servidor, poderá usar uma da API da rede de borda da AEP. As etapas abaixo descrevem o processo de busca do conteúdo publicado na borda pelas campanhas de experiência baseadas em código em uma amostra da implementação da API da rede de borda para uma página da Web e a exibição do conteúdo personalizado.

### Como funciona

1. A página da Web é solicitada e todos os cookies armazenados anteriormente pelo navegador com o prefixo `kndctr_` estão incluídos.
1. Quando a página é solicitada no servidor de aplicativos, um evento é enviado para o [ponto de extremidade de coleção de dados interativa](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html) para buscar conteúdo de personalização. Este aplicativo de amostra usa alguns métodos auxiliares para simplificar a criação e o envio de solicitações para a API (consulte [aepEdgeClient.js](https://github.com/adobe/alloy-samples/blob/ac83b6927d007dc456caad2c6ce0b324c99c26c9/common/aepEdgeClient.js){target="_blank"}). Mas o pedido é simplesmente um `POST` com uma carga que contém um evento e uma consulta. Os cookies (se disponíveis) da etapa anterior estão incluídos com a solicitação na `meta>state>entries` matriz.

   ```javascript
   fetch(
     "https://edge.adobedc.net/ee/v2/interact?dataStreamId=abc&requestId=123",
     {
       headers: {
         accept: "*/*",
         "accept-language": "en-US,en;q=0.9",
         "cache-control": "no-cache",
         "content-type": "text/plain; charset=UTF-8",
         pragma: "no-cache",
         "sec-fetch-dest": "empty",
         "sec-fetch-mode": "cors",
         "sec-fetch-site": "cross-site",
         "sec-gpc": "1",
         "Referrer-Policy": "strict-origin-when-cross-origin",
         Referer: "https://localhost/",
       },
       body: JSON.stringify({
         event: {
           xdm: {
             eventType: "decisioning.propositionFetch",
             web: {
               webPageDetails: {
                 URL: "https://localhost/",
               },
               webReferrer: {
                 URL: "",
               },
             },
             identityMap: {
               FPID: [
                 {
                   id: "xyz",
                   authenticatedState: "ambiguous",
                   primary: true,
                 },
               ],
             },
             timestamp: "2022-06-23T22:21:00.878Z",
           },
           data: {},
         },
         query: {
           identity: {
             fetch: ["ECID"],
           },
           personalization: {
             schemas: [
               "https://ns.adobe.com/personalization/default-content-item",
               "https://ns.adobe.com/personalization/html-content-item",
               "https://ns.adobe.com/personalization/json-content-item",
               "https://ns.adobe.com/personalization/redirect-item",
               "https://ns.adobe.com/personalization/dom-action",
             ],
             surfaces: ["web://localhost/","web://localhost/#sample-json-content"],
           },
         },
         meta: {
           state: {
             domain: "localhost",
             cookiesEnabled: true,
             entries: [
               {
                 key: "kndctr_XXX_AdobeOrg_identity",
                 value: "abc123",
               },
               {
                 key: "kndctr_XXX_AdobeOrg_cluster",
                 value: "or2",
               },
             ],
           },
         },
       }),
       method: "POST",
     }
   ).then((res) => res.json());
   ```

1. A experiência JSON da campanha de experiência baseada em código é lida da resposta e usada ao produzir a resposta HTML.
1. Para campanhas de experiência baseadas em código, os eventos de exibição devem ser enviados manualmente na implementação para indicar quando o conteúdo da campanha foi exibido. Neste exemplo, a notificação é enviada no lado do servidor durante o ciclo de vida da solicitação.

   ```javascript
   function sendDisplayEvent(aepEdgeClient, req, propositions, cookieEntries) {
     const address = getAddress(req);
   
     aepEdgeClient.interact(
       {
         event: {
           xdm: {
             web: {
               webPageDetails: { URL: address },
               webReferrer: { URL: "" },
             },
             timestamp: new Date().toISOString(),
             eventType: "decisioning.propositionDisplay",
             _experience: {
               decisioning: {
                 propositions: propositions.map((proposition) => {
                   const { id, scope, scopeDetails } = proposition;
   
                   return {
                     id,
                     scope,
                     scopeDetails,
                   };
                 }),
               },
             },
           },
         },
         query: { identity: { fetch: ["ECID"] } },
         meta: {
           state: {
             domain: "",
             cookiesEnabled: true,
             entries: [...cookieEntries],
           },
         },
       },
       {
         Referer: address,
       }
     );
   }
   ```

1. Quando a resposta do HTML é retornada, a identidade e os cookies de cluster são definidos na resposta pelo servidor de aplicativos.

### Principais observações

**Cookies**

Os cookies são usados para manter a identidade do usuário e as informações do cluster. Ao usar uma implementação do lado do servidor, o servidor de aplicativos deve lidar com o armazenamento e o envio desses cookies durante o ciclo de vida da solicitação.

| Cookie | Propósito | Armazenado por | Enviado por |
| ------------------------ | -------------------------------------------------------------------------- | ------------------ | ------------------ |
| kndctr_AdobeOrg_identity | Contém detalhes da identidade do usuário | servidor de aplicativos | servidor de aplicativos |
| kndctr_AdobeOrg_cluster | Indica qual cluster de borda de experiência deve ser usado para atender a solicitações | servidor de aplicativos | servidor de aplicativos |

**Solicitar posicionamento**

As solicitações para a API do Adobe Experience Platform são necessárias para obter apresentações e enviar uma notificação de exibição. Ao usar uma implementação no lado do cliente, o SDK da Web faz essas solicitações quando a variável `sendEvent` é usado.

| Solicitação | Feito por |
| ---------------------------------------------- | ------------------------------------------------------------ |
| solicitação de interação para obter apresentações | servidor de aplicativos que chama a API do Adobe Experience Platform |
| solicitação de interação para enviar notificações de exibição | servidor de aplicativos que chama a API do Adobe Experience Platform |

**Diagrama de Fluxo**

![](assets/code-based-server-side-implementation.png)

## Implementação híbrida {#hybrid-implementation}

Se você tiver uma implementação híbrida, verifique os links abaixo.

* Blog da Adobe Tech: [Personalização híbrida no SDK da Web do Adobe Experience Platform](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}
* Documentação do SDK: [Personalização híbrida usando o SDK da Web e a API do servidor de rede de borda](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/hybrid-personalization.html){target="_blank"}
