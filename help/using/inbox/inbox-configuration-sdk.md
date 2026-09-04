---
title: Configurar o suporte à caixa de entrada no Web SDK
description: Saiba como criar uma caixa de entrada de mensagem persistente no Adobe Journey Optimizer usando campanhas de Cartão de conteúdo e Caixa de entrada com o Adobe Experience Platform Web SDK.
feature: Content Cards
topic: Content Management
role: Developer
level: Experienced
source-git-commit: 1ee6fd3ed3523635ea7dbe46dbae0e2403246818
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 1%

---

# Configurar o suporte à caixa de entrada no SDK da web {#inbox-configuration-sdk}

>[!BEGINSHADEBOX]

**Nesta página:** configure e execute um exemplo que combine uma campanha de Cartão de Conteúdo e uma campanha de Caixa de Entrada com o Adobe Experience Platform Web SDK, para que você possa enviar uma caixa de entrada de notificação persistente no seu site.

>[!ENDSHADEBOX]

Uma caixa de entrada de mensagem é uma caixa de entrada de notificação persistente orientada por duas campanhas do Adobe Journey Optimizer que têm a mesma superfície como alvo:

* Uma **campanha de Cartão de Conteúdo**, que entrega itens de notificação individuais para a caixa de entrada.
* Uma **Campanha da Caixa de entrada**, que fornece configurações como título, cópia de estado vazio e layout.


## Configurar o Adobe Journey Optimizer {#ajo-setup}

Antes de implementar o Web SDK, configure a sequência de dados, os canais e as campanhas no Journey Optimizer que fornecem conteúdo à caixa de entrada.

1. Configure um **datastream** configurado com o **Adobe Experience Platform** como um serviço, com o **Journey Optimizer** habilitado e um **conjunto de dados de eventos** selecionado.

1. Crie duas configurações de canal que compartilhem a mesma superfície: um canal de **Cartões de Conteúdo** e um canal de **Caixa de Entrada**. [Saiba como configurar um canal de cartão de conteúdo](../content-card/content-card-configuration.md) e [saiba como configurar um canal de Caixa de Entrada](inbox-configuration.md).

   Defina a **URL da Página** e o **Local na página** de ambos os canais para a superfície que você definiu nos pré-requisitos. Este local deve corresponder à superfície que você consulta no código do Web SDK.

1. [Crie uma campanha de Cartão de Conteúdo](../content-card/create-content-card.md) que use o canal de Cartões de Conteúdo para sua configuração de cartão de conteúdo.

   Para mensagens que devem ser entregues com base nas ações do usuário na página da Web, habilite **Regras de entrega adicionais** na ação relevante e defina as condições de evento e valor que determinam quando a mensagem será exibida. Repita isso para cada tipo de notificação que a caixa de entrada deve receber.

1. [Crie uma campanha da Caixa de Entrada](inbox-create.md) que use o canal da Caixa de Entrada. Essa campanha entrega os metadados que configuram o próprio shell da caixa de entrada.

   Combine as configurações de público-alvo e agendamento da campanha Caixa de entrada com a campanha Cartão de conteúdo para que ambos estejam ativos para os mesmos usuários ao mesmo tempo.

1. Ative ambas as campanhas.

## Implementar o Web SDK {#web-sdk-implementation}

A caixa de entrada depende de dois comandos do Web SDK:

* `subscribeRulesetItems` registra um retorno de chamada que é executado sempre que as propostas qualificadas para exibição são alteradas.

* `sendEvent` busca essas apresentações. Você pode enviar eventos adicionais posteriormente para atualizar quais mensagens se qualificam para exibição.

1. Defina o cartão de conteúdo, os esquemas da caixa de entrada e a superfície que corresponde à configuração do canal do AJO:

   ```javascript
   const CONTENT_CARD_SCHEMA = "https://ns.adobe.com/personalization/message/content-card";
   const INBOX_SCHEMA        = "https://ns.adobe.com/personalization/message/inbox";
   const SURFACE             = "web://your-site.example/#message-inbox";
   ```

1. Configure o Web SDK com seu fluxo de dados:

   ```javascript
   alloy("configure", {
     datastreamId: "YOUR_DATASTREAM_ID",
     orgId: "YOUR_ORG_ID@AdobeOrg",
     defaultConsent: "in", // May not be usable in your implementation, but should be used for testing
     personalizationStorageEnabled: true,
   })
   ```

1. Assine itens do conjunto de regras para sua superfície e seus esquemas e forneça um retorno de chamada que lide com as propostas de cartão de conteúdo à medida que elas são alteradas:

   ```javascript
   alloy("subscribeRulesetItems", {
     surfaces: [SURFACE],
     schemas: [CONTENT_CARD_SCHEMA, INBOX_SCHEMA],
     callback: (result, collectEvent) => {
       const { propositions = [] } = result;
       const notifications = propositions
         .filter((p) => p.items?.[0]?.schema === CONTENT_CARD_SCHEMA)
         .map((proposition) => {
           const content = proposition.items[0]?.data?.content ?? {};
           return {
             id: proposition.scopeDetails.activity.id,
             title: content.title?.content ?? content.title ?? "",
             description: content.body?.content ?? content.body ?? "",
             proposition,
           };
         });
       renderNotifications(notifications, collectEvent);
     },
   });
   ```

1. Conforme os usuários interagem com seu aplicativo, envie eventos para atualizar quais apresentações de cartão de conteúdo devem ser exibidas:

   ```javascript
   alloy("sendEvent", {
     renderDecisions: true,
     personalization: { surfaces: [SURFACE] },
   });
   ```

1. Use a função `collectEvent` fornecida pelo retorno de chamada `subscribeRulesetItems` para relatar interações de volta para o AJO. Isso mantém os relatórios da campanha precisos:

   ```javascript
   // When a notification is displayed in the detail view:
   collectEvent("display", [notification.proposition]);
   
   // When a user clicks or interacts with a notification:
   collectEvent("interact", [notification.proposition]);
   
   // When a user dismisses a notification without reading it:
   collectEvent("dismiss", [notification.proposition]);
   
   // When a user deletes a notification:
   collectEvent("interact", [notification.proposition]);
   collectEvent("delete",   [notification.proposition]);
   ```

1. Para cartões com regras de entrega adicionais, por exemplo `action = deposit-funds`, chame `evaluateRulesets` com o `decisionContext` correspondente para acioná-los, já que eles não aparecem somente em `sendEvent`:

   ```javascript
   alloy("evaluateRulesets", {
     renderDecisions: true,
     personalization: {
       decisionContext: { action: "deposit-funds" },
     },
   });
   ```

   O retorno de chamada `subscribeRulesetItems` é executado novamente com todos os cartões recém-qualificados incluídos junto com os existentes.

1. Instale as dependências e inicie o servidor de exemplo:

   ```bash
   npm install
   npm start
   ```

1. Abra `https://localhost` no navegador.

1. Atualize a constante `datastreamId`, `orgId` e `SURFACE` em `src/app/page.js` para apontar para seu ambiente AJO antes de testar.

{{$include /help/_includes/do-not-localize/inbox/ai-augmented-inbox-configuration-sdk.md}}
