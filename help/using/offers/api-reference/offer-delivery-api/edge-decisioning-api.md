---
title: Fornecer ofertas usando a API do Edge Decisioning
description: O Adobe Experience Platform Web SDK permite recuperar e renderizar ofertas personalizadas que você criou usando APIs ou a Biblioteca de ofertas.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 4e2dc0d6-4610-4a2f-8388-bc58182b227f
source-git-commit: 64e225cdc8615e51655ef550866b67ca249a7572
workflow-type: tm+mt
source-wordcount: '889'
ht-degree: 1%

---

# Fornecer ofertas usando a API do Edge Decisioning {#edge-decisioning-api}

## Introdução e pré-requisitos {#edge-overview-and-prerequisites}

A [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=pt-BR#video-overview) é uma biblioteca JavaScript do lado do cliente que permite aos clientes da Adobe Experience Cloud interagir com os vários serviços na Experience Cloud por meio da Experience Platform Edge Network.

O Experience Platform Web SDK é compatível com a consulta de soluções de personalização na Adobe, incluindo a Gestão de decisões, permitindo recuperar e renderizar ofertas personalizadas que você criou usando APIs ou a Biblioteca de ofertas. Para obter instruções mais detalhadas, consulte a documentação sobre [criação de uma oferta](../../get-started/starting-offer-decisioning.md).

Há duas maneiras de implementar a gestão de decisões com o [Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=pt-BR#video-overview). Uma maneira é voltada para desenvolvedores e requer conhecimento de sites e programação. Outra maneira é usar a interface do usuário do Adobe Experience Platform para configurar ofertas que exigem apenas uma pequena referência de script no cabeçalho da página do HTML.

Consulte a documentação do Adobe Experience Platform em [gestão de decisões](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/offer-decisioning/offer-decisioning-overview.html?lang=pt-BR#enabling-offer-decisioning) para obter mais informações sobre como fornecer ofertas personalizadas usando o Adobe Experience Platform Web SDK.

## SDK da Web da Adobe Experience Platform {#aep-web-sdk}

O Platform Web SDK substitui os seguintes SDKs:

* Visitor.js
* AppMeasurement.js
* AT.js
* DIL.js

A SDK não combinou essas bibliotecas e é uma nova implementação do zero. Para usá-lo, primeiro siga estas etapas:

1. Verifique se sua organização tem as permissões apropriadas para usar o SDK e se você configurou as permissões corretamente.

   <!-- For more detailed instructions, refer to the documentation on using the [Adobe Experience Platform Web SDK](). -->

1. [Configure sua sequência de dados](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/datastreams.html?lang=pt-BR) na guia Coleção de dados da sua conta no Adobe Experience Cloud.

1. Instale o SDK. Há vários métodos para fazer isso, que são abordados na [página Instalar o SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=pt-BR). Esta página continuará com cada método diferente de implementação.

Para usar o SDK, você deve ter um [esquema](../../../data/get-started-schemas.md) e uma [sequência de dados](../../../data/get-started-datasets.md) definidos.

<!-- ****TODO - Configure schema**** -->

Para personalizar ofertas, você deve configurar separadamente seus perfis/personalizações.

<!-- Refer to the [doc](www.link.com) for detailed instructions.  -->

Para configurar a SDK para a gestão de decisões, siga uma das duas etapas abaixo:

## Opção 1 - Instalar a extensão e a implementação da tag usando o Launch

Essa opção é mais fácil de usar para pessoas que podem ter menos experiência em codificação.

1. [Criar uma propriedade de marca](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html?lang=pt-BR)

1. [Adicionar o código de inserção](https://experienceleague.adobe.com/docs/core-services-learn/implementing-in-websites-with-launch/configure-launch/launch-add-embed.html?lang=pt-BR)

1. Instale e configure a extensão Adobe Experience Platform Web SDK com a sequência de dados criada selecionando a configuração na lista suspensa &quot;Sequência de dados&quot;. Consulte a documentação em [extensões](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html?lang=pt-BR).

   ![SDK da Web da Adobe Experience Platform](../../assets/installed-catalog-web-sdk.png)

   ![Configurar Extensão](../../assets/configure-sdk-extension.png)

1. Crie os [Elementos de Dados](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/data-elements.html?lang=pt-BR) necessários. No mínimo, você deve criar um Mapa de identidade do Platform Web SDK e um elemento de dados do objeto XDM do Platform Web SDK.

   ![Mapa de identidade](../../assets/sdk-identity-map.png)

   ![Objeto XDM](../../assets/xdm-object.png)

1. Crie suas [Regras](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/rules.html?lang=pt-BR):

   Adicione uma ação Enviar evento do Platform Web SDK e adicione os escopos de decisão relevantes à configuração dessa ação

   ![Renderizar oferta](../../assets/rule-render-offer.png)

   ![Solicitar oferta](../../assets/rule-request-offer.png)

1. [Crie e publique](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=pt-BR) uma biblioteca contendo todas as Regras, Elementos de Dados e Extensões relevantes que você configurou.

## Opção 2 - Implementação manual usando a versão independente pré-criada

Estas são as etapas necessárias para usar a gestão de decisões usando a instalação independente pré-criada do Web SDK. Este guia supõe que esta é a primeira vez que você implementa o SDK, portanto, nem todas as etapas se aplicam a você. Este guia também pressupõe alguma experiência de desenvolvimento.

Inclua o seguinte trecho JavaScript da Opção 2: A Versão Autônoma Pré-Compilada nesta [página](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=pt-BR) na seção `<head>` da sua página do HTML.

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

Você precisará de duas IDs na sua conta do Adobe para definir a configuração do SDK: a edgeConfigId e a orgId. O edgeConfigId é o mesmo que a ID do Datastream, que você deve ter configurado nos Pré-requisitos.

Para encontrar sua edgeConfigID/ID do fluxo de dados, vá para Coleção de dados e selecione seu fluxo de dados. Para encontrar sua orgId, acesse seu perfil.

Configure o SDK no JavaScript seguindo as instruções nesta página. Você sempre usará edgeConfigId e orgId na função de configuração. A documentação também descreve quais parâmetros opcionais existem para sua configuração. Sua configuração final pode acabar ficando mais ou menos assim:

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

Instale a extensão Chrome do Debugger para usar com a depuração. Isso pode ser encontrado aqui: <https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob>

Em seguida, faça logon na conta do no depurador. Em seguida, acesse Logs e verifique se você está conectado ao espaço de trabalho correto. Agora, copie da sua oferta a versão codificada em base64 do escopo de decisão.

Ao editar o site, inclua o script com a configuração e a função `sendEvent` para enviar o escopo de decisão para a Adobe.

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

Consulte o seguinte para obter um exemplo de como lidar com a resposta:

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

Você pode usar o depurador para verificar se se conectou com êxito à rede do Edge.

>[!NOTE]
>
>Se você não estiver vendo uma conexão com a borda do nos logs, talvez precise desativar o bloqueador de anúncios.

Consulte como você criou a oferta e a formatação usada. Com base nos critérios atendidos na decisão, uma oferta será retornada para você contendo as informações especificadas ao criá-la no Adobe Experience Platform.

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

Manipule o objeto de resposta e analise os dados necessários. Como você pode enviar vários escopos de decisão em uma chamada `sendEvent`, sua resposta pode ser um pouco diferente.

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

Neste exemplo, o caminho necessário para manipular e usar os detalhes específicos da oferta na página da Web foi: `result['decisions'][0]['items'][0]['data']['content']`

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

<!--## Limitations

Some offer constraints are currently not supported with the mobile Experience Edge workflows, for example Capping. The Capping field value specifies the number of times an offer can be presented across all users. For more details, see [Add constraints to an offer](../../offer-library/add-constraints.md#capping).-->
