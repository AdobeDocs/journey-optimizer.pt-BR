---
title: SDK da Web de configuração de cartões de conteúdo
description: Configurar o suporte a cartões de conteúdo no SDK da Web
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="Disponibilidade limitada" type="Informative"
hide: true
hidefromtoc: true
source-git-commit: 8a902298bbbac5689b4f84266dd9c9027e45fad5
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 3%

---

# Configurar o suporte a cartões de conteúdo no SDK da Web {#content-card-configuration-sdk}

>[!AVAILABILITY]
>
>Atualmente, os cartões de conteúdo estão disponíveis apenas para algumas organizações (disponibilidade limitada). Para obter acesso, entre em contato com seu representante da Adobe.

Este exemplo mostra como recuperar Cartões de conteúdo do Adobe Journey Optimizer (AJO) usando o Adobe Experience Platform. Com o [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/home), o conteúdo de personalização é obtido e renderizado totalmente no lado do cliente.

Após o carregamento inicial, a página exibe seu estado padrão. No entanto, se você interagir com os botões **Depositar Fundos** ou **Compartilhar em redes sociais**, serão exibidos cartões de conteúdo adicionais. Esses cartões são acionados pelas condições do lado do cliente, garantindo que sejam exibidos somente quando ações específicas forem executadas.

![](assets/content-card-web-1.png)

## Execução da amostra {#run-sample}

Pré-requisito: você precisa instalar o nó e o npm. [Consulte esta documentação](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)

1. Configurar certificados SSL locais para HTTPS. Esses exemplos exigem certificados SSL assinados localmente para veicular conteúdo em HTTPS:

   1. Instalar o `mkcert` no computador.

   1. Após a instalação, execute o `mkcert -install` para instalar o certificado `mkcert root`.

1. Clonar o repositório no computador local.

1. Abra um terminal e navegue até a pasta do exemplo.

1. Instale as dependências necessárias executando `npm install`.

1. Inicie o aplicativo executando `npm start`.

1. Abra seu navegador da Web e vá para `https://localhost`.

## Como funciona {#setup}

1. Inclua e configure o [SDK da Web](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/home) na página usando as configurações do arquivo `.env` na pasta de exemplo.

   ```
   <script src="https://cdn1.adoberesources.net/alloy/2.18.0/alloy.min.js" async></script>
   alloy("configure", {
       defaultConsent: "in",
       edgeDomain: "{{edgeDomain}}",
       edgeConfigId: "{{edgeConfigId}}",
       orgId:"{{orgId}}",
       debugEnabled: false,
       personalizationStorageEnabled: true,
       thirdPartyCookiesEnabled: false
   });
   ```

1. Use o comando `sendEvent` para buscar conteúdo personalizado.

   ```
   alloy("sendEvent", {
       renderDecisions: true,
       personalization: {
           surfaces: ["web://alloy-samples.adobe.com/#content-cards-sample"],
       },
   });
   ```

1. Inscreva-se em cartões de conteúdo para uma superfície específica usando o comando `subscribeRulesetItems`. Sempre que os conjuntos de regras forem avaliados, manipule o objeto resultante no retorno de chamada, que conterá `propositions` com os dados do cartão de conteúdo.

   ```
   const contentCardManager = createContentCardManager("content-cards");
   
   alloy("subscribeRulesetItems", {
       surfaces: ["web://alloy-samples.adobe.com/#content-cards-sample"],
       schemas: ["https://ns.adobe.com/personalization/message/content-card"],
       callback: (result, collectEvent) => {
           const { propositions = [] } = result;
           contentCardManager.refresh(propositions, collectEvent);
       },
   });
   ```

1. Gerencie a renderização de cartões de conteúdo e envie eventos `interact` e `display` usando o objeto `contentCardsManager` encontrado em `script.js`. Extraia, classifique e processe cartões de conteúdo das apresentações recebidas.

   ```
   const createContentCard = (proposition, item) => {
       const { data = {}, id } = item;
       const {
           content = {},
           meta = {},
           publishedDate,
           qualifiedDate,
           displayedDate,
       } = data;
   
       return {
           id,
           ...content,
           meta,
           qualifiedDate,
           displayedDate,
           publishedDate,
           getProposition: () => proposition,
       };
   };
   
   const extractContentCards = (propositions) =>
       propositions
           .reduce((allItems, proposition) => {
           const { items = [] } = proposition;
   
           return [
               ...allItems,
               ...items.map((item) => createContentCard(proposition, item)),
           ];
       }, [])
       .sort(
           (a, b) =>
               b.qualifiedDate - a.qualifiedDate || b.publishedDate - a.publishedDate
       );
   
   const contentCards = extractContentCards(propositions);
   ```

1. Renderize os cartões de conteúdo com base nos detalhes definidos para cada campanha. Cada cartão inclui um `title`, `body`, `imageUrl` e outros valores de dados personalizados.

   ```
   const renderContentCards = () => {
       const contentCardsContainer = document.getElementById(containerElementId);
       contentCardsContainer.addEventListener("click", handleContentCardClick);
   
       let contents = "";
   
       contentCards.forEach((card) => {
           const { id, title, body, imageUrl, meta = {} } = card;
           const { buttonLabel = "" } = meta;
   
           contents += `
               <div class="col">
                   <div data-id="${id}" class="card h-100">
                       <img src="${imageUrl}" class="card-img-top" alt="...">
                       <div class="card-body d-flex flex-column">
                           <h5 class="card-title">${title}</h5>
                           <p class="card-text">${body}</p>
                           <a href="#" class="mt-auto btn btn-primary">${buttonLabel}</a>
                       </div>
                   </div>
                </div>
            `;
       });
   
       contentCardsContainer.innerHTML = contents;
       collectEvent(
           "display",
           contentCards.map((card) => card.getProposition())
        );
   };
   ```

1. Quando o retorno de chamada `subscribeRulesetItems` é invocado, uma função de conveniência chamada `collectEvent` também é fornecida. Essa função é usada para enviar eventos do Experience Edge para rastrear interações, exibições e outras ações do usuário. Neste exemplo, collectEvent rastreia quando um cartão de conteúdo é clicado. Além disso, se o botão no cartão de conteúdo for clicado, o navegador será direcionado para o `actionUrl` especificado pela campanha.

   ```
   const handleContentCardClick = (evt) => {
       const cardEl = evt.target.closest(".card");
   
       if (!cardEl) {
           return;
       }
   
       const isAnchor = evt.target.nodeName === "A";
       const card = contentCards.find((card) => card.id === cardEl.dataset.id);
   
       if (!card) {
           return;
       }
   
       collectEvent("interact", [card.getProposition()]);
   
       if (isAnchor) {
           evt.preventDefault();
           evt.stopImmediatePropagation();
           const { actionUrl } = card;
           if (actionUrl && actionUrl.length > 0) {
               window.location.href = actionUrl;
           }
       }
   };
   ```

## Principais observações {#key-observations}

### personalizationStorageEnabled

A opção `personalizationStorageEnabled` está definida como `true` no comando `configure`. Isso garante que os cartões de conteúdo qualificados anteriormente sejam armazenados e continuem sendo exibidos nas sessões do usuário.

### Acionadores

Os cartões de conteúdo são compatíveis com acionadores personalizados avaliados no lado do cliente. Quando uma regra de acionador é atendida, cartões de conteúdo adicionais são exibidos. Este exemplo usa quatro campanhas diferentes, uma para cada cartão de conteúdo, todas compartilhando a mesma superfície: `web://alloy-samples.adobe.com/#content-cards-sample`. A tabela abaixo descreve as regras de acionador para cada campanha e como satisfazê-las.

<table>
    <tr>
        <th>Regra de acionamento</th>
        <th>Cartão</th>
        <th>Como cumprir a regra de acionador</th>
    </tr>
    <tr>
        <td>None</td>
        <td><img src="assets/content-card-web-2.png"></td>
        <td>comando sendEvent. Nenhuma regra do lado do cliente a ser atendida.</td>
    </tr>
    <tr>
        <td>None</td>
        <td><img src="assets/content-card-web-3.png"></td>
        <td>comando sendEvent. Nenhuma regra do lado do cliente a ser atendida.</td>
    </tr>
    <tr>
        <td><img src="assets/content-card-web-4.png"></td>
        <td><img src="assets/content-card-web-5.png"></td>
        <td><img src="assets/content-card-web-6.png"></td>
    </tr>
    <tr>
        <td><img src="assets/content-card-web-7.png"></td>
        <td><img src="assets/content-card-web-8.png"></td>
        <td><img src="assets/content-card-web-9.png"></td>
    </tr>
</table>

O comando `evaluateRulesets` é acionado ao clicar nos botões &quot;Depositar Fundos&quot; e &quot;Compartilhar em redes sociais&quot;. Cada botão especifica o `decisionContext` relevante para cumprir as regras definidas para as respectivas campanhas.

```
document.getElementById("action-button-1").addEventListener("click", () => {
    alloy("evaluateRulesets", {
        renderDecisions: true,
        personalization: {
            decisionContext: {
                action: "deposit-funds",
            },
        },
    });
});

document.getElementById("action-button-2").addEventListener("click", () => {
    alloy("evaluateRulesets", {
        renderDecisions: true,
        personalization: {
            decisionContext: {
                action: "social-media",
            },
        },
    });
});
```
