---
title: Fornecer ofertas usando a API do Edge Decisioning
description: O SDK da Web da Adobe Experience Platform permite recuperar e renderizar ofertas personalizadas que você criou usando APIs ou a Biblioteca de ofertas.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 4e2dc0d6-4610-4a2f-8388-bc58182b227f
source-git-commit: 79d3bd42c208d38aaebce742e70b247106c21587
workflow-type: tm+mt
source-wordcount: '1049'
ht-degree: 2%

---

# Fornecer ofertas usando a API do Edge Decisioning {#edge-decisioning-api}

## Introdução e pré-requisitos {#edge-overview-and-prerequisites}

O [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview) é uma biblioteca JavaScript do lado do cliente que permite que os clientes da Adobe Experience Cloud interajam com os vários serviços no Experience Cloud por meio da Experience Platform Edge Network.

O Experience Platform Web SDK oferece suporte à consulta de soluções de personalização no Adobe, incluindo o Gerenciamento de decisões, permitindo recuperar e renderizar ofertas personalizadas que você criou usando APIs ou a Biblioteca de ofertas. Para obter instruções mais detalhadas, consulte a documentação em [criação de uma oferta](../../get-started/starting-offer-decisioning.md).

Há duas maneiras de implementar o Offer Decisioning com a variável [SDK da Web da plataforma](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview). Uma maneira é voltada para desenvolvedores e requer conhecimento de sites e programação. Outra maneira é usar a interface do usuário do Adobe Experience Platform para configurar ofertas que exigem apenas um pequeno script para ser referenciado no cabeçalho da página HTML.

Consulte a documentação em [offer decisioning](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/offer-decisioning/offer-decisioning-overview.html?lang=en#enabling-offer-decisioning) para obter mais informações sobre como fornecer ofertas personalizadas usando o SDK da Web da plataforma.

>[!NOTE]
>
>O uso do Gerenciamento de decisões no Adobe Experience Platform Web SDK está disponível no momento com acesso antecipado a usuários selecionados. Essa funcionalidade não está disponível para todas as organizações.

## SDK da Web da Adobe Experience Platform {#aep-web-sdk}

O SDK da Web da plataforma substitui os seguintes SDKs:

* Visitor.js
* AppMeasurement.js
* AT.js
* DIL.js

O SDK não combinou essas bibliotecas e é uma nova implementação desde o início. Para usá-lo, primeiro siga estas etapas:

1. Certifique-se de que sua organização tenha as permissões apropriadas para usar o SDK e tenha configurado as permissões corretamente.

   <!-- For more detailed instructions, refer to the documentation on using the [Adobe Experience Platform Web SDK](). -->

1. [Configurar o fluxo de dados](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/datastreams.html?lang=en) na guia Coleta de dados em sua conta na Adobe Experience Cloud.

1. Instale o SDK. Existem vários métodos para isso, que são abordados no [Instalar a página do SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en). Esta página continuará com cada método de implementação diferente.

Para usar o SDK, você deve ter um [schema](../../../start/get-started-schemas.md) e [datastream](../../../start/get-started-datasets.md) definido.

<!-- ****TODO - Configure schema**** -->

Para personalizar ofertas, você deve configurar separadamente sua personalização/perfis.

<!-- Refer to the [doc](www.link.com) for detailed instructions.  -->

Para configurar o SDK para Offer Decisioning, siga uma das duas etapas abaixo:

## Opção 1 - Instalar a extensão de tag e a implementação usando o Launch

Essa opção é mais fácil de usar para pessoas que podem ter menos experiência em codificação.

1. [Criar uma propriedade de tag](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html?lang=en)

1. [Adicionar o código incorporado](https://experienceleague.adobe.com/docs/core-services-learn/implementing-in-websites-with-launch/configure-launch/launch-add-embed.html?lang=en)

1. Instale e configure a extensão SDK da Web da plataforma com o Datastream criado selecionando a configuração na lista suspensa &quot;Datastream&quot;. Consulte a documentação em [extensões](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html?lang=en).

   ![SDK da Web da Adobe Experience Platform](../../assets/installed-catalog-web-sdk.png)

   ![Configurar extensão](../../assets/configure-sdk-extension.png)

1. Crie o [Elementos de dados](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/data-elements.html?lang=en). No mínimo, você deve criar um Mapa de identidade do SDK da Web da plataforma e um elemento de dados do Objeto XDM do SDK da Web da plataforma.

   ![Mapa de identidade](../../assets/sdk-identity-map.png)

   ![Objeto XDM](../../assets/xdm-object.png)

1. Crie seu [Regras](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/rules.html?lang=en):

   Adicione uma ação Enviar evento do SDK da Web da plataforma e adicione os escopos de decisão relevantes à configuração dessa ação

   ![Renderizar oferta](../../assets/rule-render-offer.png)

   ![Solicitar oferta](../../assets/rule-request-offer.png)

1. [Criar e publicar](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en) uma biblioteca contendo todas as regras, elementos de dados e extensões relevantes que você configurou.

## Opção 2: implementar manualmente usando a versão independente pré-criada

Estas são as etapas necessárias para usar o Offer Decisioning usando a instalação independente pré-criada do SDK da Web. Este guia pressupõe que esta seja a primeira vez que você implementa o SDK, de modo que todas as etapas podem não se aplicar a você. Este guia também assume alguma experiência de desenvolvimento.

Inclua o seguinte trecho do JavaScript da Opção 2: A versão independente pré-criada em [esta página](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en) no `<head>` da sua página do HTML.

```
javascript
    <script>
        !function(n,o){o.forEach(function(o){n[o]||((n.__alloyNS=n.__alloyNS||
        []).push(o),n[o]=function(){var u=arguments;return new Promise(
        function(i,l){n[o].q.push([i,l,u])})},n[o].q=[])})}
        (window,["alloy"]);
    </script>
    <script src="https://cdn1.adoberesources.net/alloy/2.6.4/alloy.js" async></script>
```

Você precisará de duas IDs da sua conta do Adobe para configurar o SDK - sua edgeConfigId e sua orgId. O edgeConfigId é o mesmo da ID do conjunto de dados, que você deve ter configurado nos Pré-requisitos.

Para encontrar a ID edgeConfigID/datastream, vá para Coleta de dados e selecione o Datastream. Para encontrar o orgId, acesse o seu perfil.

Configure o SDK em JavaScript seguindo as instruções desta página. Você sempre usará edgeConfigId e orgId na função de configuração. A documentação também descreve quais parâmetros opcionais existem para sua configuração. Sua configuração final pode acabar parecendo algo assim:

```
javascript
    alloy("configure", {
        "edgeConfigId": "12345678-0ABC-DEF-GHIJ-KLMNOPQRSTUV",                            
        "orgId":"ABCDEFGHIJKLMNOPQRSTUVW@AdobeOrg",
        "debugEnabled": true,
        "edgeDomain": "edge.adobedc.net",
        "clickCollectionEnabled": true,
        "idMigrationEnabled": true,
        "thirdPartyCookiesEnabled": true,
        "defaultConsent":"in"  
    });
```

Instale a extensão do Chrome do Debugger para usar com a depuração. Isso pode ser encontrado aqui: <https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob>

Em seguida, faça logon em sua conta no depurador da . Em seguida, acesse Logs e verifique se você está conectado ao espaço de trabalho correto. Agora, copie a versão codificada da base64 do escopo de decisão da sua oferta.

Ao editar seu site, inclua o script com a configuração e o `sendEvent` para enviar o escopo de decisão para o Adobe.

**Exemplo**:

```
javascript
    alloy("sendEvent", {
        "decisionScopes": 
        [
        "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTXXXXXXXXXX"
        ]
    });
```

Consulte o exemplo a seguir para saber como lidar com a resposta:

```
javascript
    alloy("sendEvent", {
        "decisionScopes":
        [
        "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTXXXXXXXXXX"
        ]
    }).then(function(result) {
        Object.entries(result).forEach(([key, value]) => {
            console.log(key, value);
        });
    });
```

Você pode usar o depurador para verificar se você se conectou com êxito à rede Edge.

>[!NOTE]
>
>Caso não esteja vendo uma conexão com a borda nos logs, talvez seja necessário desativar o bloqueador de anúncios.

Consulte como você criou a oferta e a formatação usada. Com base nos critérios cumpridos na decisão, uma oferta será retornada a você contendo as informações especificadas ao criá-la na Adobe Experience Platform.

Neste exemplo, o JSON a ser retornado é:

```
json
{
   "name":"ABC Test",
   "description":"This is a test offer", 
   "link":"https://sampletesting.online/",
   "image":"https://sample-demo-URL.png"
}
```

Lide com o objeto de resposta e analise os dados necessários. Como você pode enviar vários escopos de decisão em um `sendEvent` , sua resposta pode ser um pouco diferente.

```
json
    {
        "id": "abrxgl843d913",
        "scope": "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTVlNWRmOSJ9",
        "items": 
        [
            {
                "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                "etag": "1",
                "schema": "https://ns.adobe.com/experience/offer-management/content-component-json",
                "data": {
                    "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                    "format": "application/json",
                    "language": [
                        "en-us"
                    ],
                    "content": "{\"name\":\"ABC Test\",\"description\":\"This is a test offer\", \"link\":\"https://sampletesting.online/\",\"image\":\"https://sample-demo-URL.png\"}"
                }
            }
        ]
    }
]
}
```

```
json
{
    "propositions": 
    [
    {
        "renderAttempted": false,
        "id": "e15ecb09-993e-4b66-93d8-0a4c77e3d913",
        "scope": "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTVlNWRmOSJ9",
        "items": 
        [
            {
                "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                "etag": "1",
                "schema": "https://ns.adobe.com/experience/offer-management/content-component-json",
                "data": {
                    "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                    "format": "application/json",
                    "language": [
                        "en-us"
                    ],
                    "content": "{\"name\":\"Claire Hubacek Test\",\"description\":\"This is a test offer\", \"link\":\"https://sampletesting.online/\",\"image\":\"https://sample-demo-URL.png\"}"
                }
            }
        ]
    }
    ]
}
```

Neste exemplo, o caminho necessário para lidar e usar os detalhes específicos da oferta na página da Web era: `result['decisions'][0]['items'][0]['data']['content']`

Para definir as variáveis JS:

```
javascript
const offer = JSON.parse(result['decisions'][0]['items'][0]['data']['content']);

let offerURL = offer['link'];
let offerDescription = offer['description'];
let offerImageURL = offer['image'];

document.getElementById("offerDescription").innerHTML = offerDescription;
document.getElementById('offerImage').src = offerImageURL;
```

## Limitações

No momento, algumas restrições de oferta não são compatíveis com os fluxos de trabalho da borda da experiência móvel, por exemplo, Limitação. O valor do campo Limitação especifica o número de vezes que uma oferta pode ser apresentada em todos os usuários. Para obter mais detalhes, consulte [Adicionar restrições a uma oferta](../../offer-library/add-constraints.md#capping).
