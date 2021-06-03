---
title: Ofertas de entrega
description: O Gerenciamento de decisões é uma coleção de serviços e programas de interface do usuário que permite aos profissionais de marketing criar e fornecer experiências de ofertas personalizadas para o usuário final em canais e aplicativos usando lógica de negócios e regras de decisão.
source-git-commit: 741fe2b614e3ded57c4a7ecd9b7333bdd99ab359
workflow-type: tm+mt
source-wordcount: '945'
ht-degree: 2%

---

# Fornecer ofertas usando a API de decisões

Com o Gerenciamento de decisões, você pode criar e fornecer experiências de ofertas personalizadas para o usuário final, em canais e aplicativos, usando a lógica de negócios e as regras de decisão. Uma oferta é uma mensagem de marketing que pode ter regras associadas a ela que especificam quem está qualificado para ver a oferta.

Você pode criar e entregar ofertas fazendo uma solicitação de POST para a API [!DNL Decisions].

Este tutorial requer uma compreensão funcional das APIs, especificamente em relação ao Gerenciamento de decisões. Para obter mais informações, consulte o [Guia do desenvolvedor da API de Gerenciamento de Decisão](../getting-started.md). Este tutorial também exige que você tenha uma ID de posicionamento exclusiva e um valor de ID de decisão disponíveis. Se você não adquiriu esses valores, consulte os tutoriais para [criar uma disposição](../offers-api/placements/create.md) e [criar uma decisão](../activities-api/activities/create.md).

![](../../../assets/do-not-localize/how-to-video.png) [Descubra este recurso no vídeo](#video)

## Aceitar e digitar cabeçalhos de tipo de conteúdo

A tabela a seguir mostra os valores válidos que compõem os campos *Content-Type* e *Accept* no cabeçalho da solicitação:

| Nome do cabeçalho | Valor |
| ----------- | ----- |
| Accept | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"` |
| Tipo de conteúdo | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"` |

**Formato da API**

```https
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/decisions
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do terminal para APIs do repositório. | `https://platform.adobe.io/data/core/ode/` |
| `{CONTAINER_ID}` | O contêiner onde as decisões estão localizadas. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Solicitação**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/ode/e0bd8463-0913-4ca1-bd84-6309134ca1f6/decisions' \
  -H 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
  -H 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0'
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
  -d '{
        "xdm:propositionRequests": [
            {
              "xdm:placementId": "xcore:offer-placement:ffed0456",
              "xdm:activityId": "xcore:offer-activity:ffed0123",
              "xdm:itemCount": 2
            },
            {
              "xdm:placementId": "xcore:offer-placement:ffed0012",
              "xdm:activityId": "xcore:offer-activity:fffc0789"
            }
        ],
        "xdm:profiles": [
            {
              "xdm:identityMap": {
                "SWCUSTID": [
                {
                    "xdm:id": "123@abc.com"
                }
                ]
            },
            "xdm:decisionRequestId": "0AA00002-0000-1337-c0de-c0fefec0fefe"
            }
        ],
        "xdm:allowDuplicatePropositions": {
            "xdm:acrossActivities": true,
            "xdm:acrossPlacements": true
        },
        "xdm:mergePolicy": {
            "xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"
        },
        "xdm:responseFormat": {
            "xdm:includeContent": true,
            "xdm:includeMetadata": {
            "xdm:activity": [
                "name"
            ],
            "xdm:option": [
                "name"
            ],
            "xdm:placement": [
                "name"
            ]
            }
        }
      }'
```

| Propriedade | Descrição | Exemplo |
| -------- | ----------- | ------- |
| `xdm:propositionRequests` | Esse objeto contém os identificadores de posicionamento e decisão. |
| `xdm:propositionRequests.xdm:placementId` | O identificador exclusivo de posicionamento. | `"xdm:placementId": "xcore:offer-placement:ffed0456"` |
| `xdm:propositionRequests.xdm:activityId` | O identificador de decisão único. | `"xdm:activityId": "xcore:offer-activity:ffed0123"` |
| `xdm:itemCount` | O número de ofertas a serem retornadas. O número máximo é 30. | `"xdm:itemCount": 2` |
| `xdm:profiles` | Esse objeto contém informações sobre o perfil para o qual a decisão é solicitada. Para uma solicitação de API, isso conterá um perfil. |
| `xdm:profiles.xdm:identityMap` | Esse objeto contém um conjunto de identidades de usuário final com base no código de integração do namespace da identidade. O mapa de identidade pode ter mais de uma identidade de cada namespace. Para obter mais informações sobre namespaces, consulte a [Visão geral do namespace de identidade](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html). | `Email: [{"xdm:id": "123@abc.com"}]` |
| `xdm:profiles.xdm:decisionRequestId` | A ID gerada pelo cliente que pode ser usada para identificar exclusivamente uma solicitação de decisão de perfil. Essa ID é repetida na resposta e não influencia o resultado da decisão. | `"xdm:decisionRequestId": "0AA00002-0000-1337-c0de-c0fefec0fefe"` |
| `xdm:allowDuplicatePropositions` | Esse objeto é a estrutura de controle das regras de eliminação de duplicação. Consiste em uma série de sinalizadores que indicam se a mesma opção pode ser proposta em uma determinada dimensão. Um sinalizador definido como true significa que as duplicatas são permitidas e não devem ser removidas na categoria indicada pelo sinalizador. Um sinalizador definido como falso significa que o mecanismo de decisão não deve fazer a mesma apresentação na dimensão e, em vez disso, escolher a próxima melhor opção para uma das subdecisões. |
| `xdm:allowDuplicatePropositions.xdm:acrossActivities` | Se definido como verdadeiro, várias decisões podem receber a mesma opção. | `"xdm:acrossActivities": true` |
| `xdm:allowDuplicatePropositions.xdm:acrossPlacements` | Se definido como verdadeiro, várias disposições podem receber a mesma opção. | `"xdm:acrossPlacements": true` |
| `xdm:mergePolicy.xdm:id` | Identifica a política de mesclagem pela qual os dados retornados pelo serviço de acesso ao perfil devem ser controlados. Se um não for especificado na solicitação, o Gerenciamento de decisões não passará por nenhum serviço de acesso a perfis; caso contrário, passará a id fornecida pelo chamador. | `"xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"` |
| `xdm:responseFormat` | Um conjunto de sinalizadores que formata o conteúdo de resposta. |
| `xdm:responseFormat.xdm:includeContent` | Um valor booleano que, se definido como `true`, inclui conteúdo para a resposta. | `"xdm:includeContent": true` |
| `xdm:responseFormat.xdm:includeMetadata` | Um objeto usado para especificar quais metadados adicionais são retornados. Se essa propriedade não for incluída, então `xdm:id` e `repo:etag` serão retornadas por padrão. | `name` |
| `xdm:responseFormat.xdm:activity` | Esse sinalizador identifica as informações de metadados específicas retornadas para `xdm:activity`. | `name` |
| `xdm:responseFormat.xdm:option` | Esse sinalizador identifica as informações de metadados específicas retornadas para `xdm:option`. | `name`, `characteristics` |
| `xdm:responseFormat.xdm:placement` | Esse sinalizador identifica as informações de metadados específicas retornadas para `xdm:placement`. | `name`, `channel`, `componentType` |

**Resposta**

Uma resposta bem-sucedida retorna informações sobre sua proposta, incluindo seu `xdm:propositionId` exclusivo.

```json
{
  "xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8",
  "xdm:propositions": [
    {
      "xdm:activity": {
        "xdm:id": "xcore:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "xcore:placement:ffed0456",
        "repo:etag": 1
      },
      "xdm:options": [
        {
          "xdm:id": "xcore:personalized-option:ccc0111",
          "repo:etag": 3,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>some html</html>"
        },
        {
          "xdm:id": "xcore:personalized-option:ccc0222",
          "repo:etag": 5,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>hello, world</html>",
          "xdm:score": 45.65
        }
      ]
    },
    {
      "xdm:activity": {
        "xdm:id": "xcore:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "xcore:placement:ffed0789",
        "repo:etag": 2
      },
      "xdm:fallback": {
        "xdm:id": "xcore:fallback:ccc0222",
        "repo:etag": 5,
        "@type": "https://ns.adobe.com/experience/decisioning/content-component-imagelink",
        "dc:format": "image/png",
        "xdm:deliveryURL": "https://cdn.adobe.com/content/1445323-1134331.png",
        "xdm:content": "https://www.adobe.com/index2.html"
      }
    }
  ],
  "ode:createDate": 1566497582038
}
```

| Propriedade | Descrição | Exemplo |
| -------- | ----------- | ------- |
| `xdm:propositionId` | O identificador exclusivo da entidade de proposta associado a um evento de decisão XDM. | `"xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8"` |
| `xdm:propositions` | Esse objeto contém uma única apresentação de decisão. Várias opções podem ser retornadas para a decisão. Se nenhuma opção for encontrada, a oferta de fallback da decisão será retornada. As apresentações de decisão única sempre incluem uma propriedade `options` ou uma propriedade `fallback`. Quando presente, a propriedade `options` não pode estar vazia. |
| `xdm:propositions.xdm:activity` | Esse objeto contém o identificador exclusivo de uma decisão. | `"xdm:id": "xcore:activity:ffed0123"` |
| `xdm:propositions.xdm:placement` | Esse objeto contém o identificador exclusivo para uma disposição da oferta. | `"xdm:id": "xcore:placement:ffed0456"` |
| `xdm:propositions.xdm:options` | Esse objeto contém uma única opção, incluindo seu identificador exclusivo. Se estiver presente, esse objeto não poderá estar vazio. | `xdm:id": "xcore:personalized-option:ccc0111` |
| `xdm:propositions.xdm:options.@type` | Define o tipo do componente. `@type` atua como contrato de processamento para o cliente. Quando a experiência for montada, o compositor procurará os componentes que têm um tipo específico. | `https://ns.adobe.com/experience/offer-management/content-component-imagelink` |
| `xdm:propositions.xdm:content` | O formato do conteúdo da resposta. | O conteúdo da resposta pode ser: `text`, `html block` ou `image link` |
| `xdm:score` | A pontuação de uma opção que é calculada como resultado de uma função de classificação associada à opção ou à decisão. Esse campo será retornado pela API se uma função de classificação estiver envolvida na determinação da pontuação de uma oferta durante a classificação. | `"xdm:score": 45.65` |
| `xdm:propositions.xdm:fallback` | Esse objeto contém uma única oferta de fallback, incluindo seu identificador exclusivo. | `"xdm:id": "xcore:fallback:ccc0222"` |
| `xdm:propositions.xdm:fallback.dc:format` | A manifestação física ou digital do recurso. Normalmente, o formato deve incluir o tipo de mídia do recurso. O formato pode ser usado para determinar o software, hardware ou outro equipamento necessário para exibir ou operar o recurso. É recomendável selecionar um valor de um vocabulário controlado, por exemplo, a lista de [Tipos de Mídia da Internet](http://www.iana.org/assignments/media-types/) definindo formatos de mídia de computador. | `"dc:format": "image/png"` ou `"image/jpeg"` |
| `xdm:propositions.xdm:fallback.xdm:deliveryURL` | Um URL opcional para ler o ativo de uma rede de entrega de conteúdo ou ponto de extremidade de serviço. Esse URL é usado para acessar o ativo publicamente de um agente do usuário. | `https://d37yhxrr0p3l3l.cloudfront.net/0fd0f090-a148-11ea-89e3-f1f2ad52f7e8/urn:aaid:sc:US:a68c86a6-9295-4940-a083-11916b665500/0/40d78a12-f8b6-3f07-8e67-7cb8ae2cc7ec` |
| `ode:createDate` | A hora em que a mensagem de resposta da decisão foi criada. Isso é representado como uma época. | `"ode:createDate": 1566497582038` |

## Tutorial em vídeo {#video}

O vídeo a seguir é destinado a auxiliar a compreensão dos componentes do Gerenciamento de decisões.

>[!NOTE]
>
>Este vídeo se aplica ao serviço de aplicativo do Offer Decisioning criado no Adobe Experience Platform. No entanto, fornece orientação genérica para usar a Oferta no contexto do Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329919/?quality=12)

## Próximas etapas

Seguindo este guia de API, você criou e entregou ofertas usando a API [!DNL Decisions]. Para obter mais informações, consulte a [visão geral sobre o Gerenciamento de decisões](../../../offers/get-started/starting-offer-decisioning.md).
