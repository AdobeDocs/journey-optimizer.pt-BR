---
title: Entregar ofertas
description: A Gestão de decisões é uma coleção de serviços e programas de interface do usuário que permite aos profissionais de marketing criar e fornecer experiências de oferta personalizadas para o usuário final em canais e aplicativos usando lógica de negócios e regras de decisão.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 692d0aae-6fa1-40b8-a35f-9845d78317a3
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '1058'
ht-degree: 5%

---

# Entregar ofertas usando a API de decisão {#decisioning-api}

Com a Gestão de decisões, você pode criar e fornecer experiências de oferta personalizada de usuários finais, em canais e aplicativos usando lógica de negócios e regras de decisão. Uma oferta é uma mensagem de marketing que pode ter regras associadas que especificam quem está qualificado para ver a oferta.

Você pode criar e entregar ofertas fazendo uma solicitação POST à [!DNL Decisioning] API.

Este tutorial requer uma compreensão funcional das APIs, especificamente no que diz respeito à Gestão de decisões. Para obter mais informações, consulte [Guia do desenvolvedor da API de Gestão de decisões](../getting-started.md). Este tutorial também requer que você tenha uma ID de posicionamento exclusiva e um valor de ID de decisão disponíveis. Se você não adquiriu esses valores, consulte os tutoriais do [criação de uma inserção](../offers-api/placements/create.md) e [criação de uma decisão](../activities-api/activities/create.md).

➡️  [Descubra este recurso no vídeo](#video)

## Cabeçalhos Accept e Content-Type {#accept-and-content-type-headers}

A tabela a seguir mostra os valores válidos que compõem a variável *Tipo de conteúdo* e *Aceitar* campos no cabeçalho da solicitação:

| Nome do cabeçalho | Valor |
| ----------- | ----- |
| Accept | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"` |
| Tipo de conteúdo | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"` |

## solicitação de API {#request}

### Formato da API

```https
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/decisions
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs do repositório. | `https://platform.adobe.io/data/core/ode/` |
| `{CONTAINER_ID}` | O contêiner onde as decisões estão localizadas. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

### Solicitação

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/ode/e0bd8463-0913-4ca1-bd84-6309134ca1f6/decisions' \
  -H 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
  -H 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"'
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
            "xdm:decisionRequestId": "0AA00002-0000-1224-c0de-cjf98Csj43"
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
| `xdm:propositionRequests.xdm:placementId` | O identificador de posicionamento exclusivo. | `"xdm:placementId": "xcore:offer-placement:ffed0456"` |
| `xdm:propositionRequests.xdm:activityId` | O identificador de decisão exclusivo. | `"xdm:activityId": "xcore:offer-activity:ffed0123"` |
| `xdm:itemCount` | O número de ofertas a serem retornadas. O número máximo é 30. | `"xdm:itemCount": 2` |
| `xdm:profiles` | Esse objeto mantém informações sobre o perfil para o qual a decisão é solicitada. Para uma solicitação de API, ela conterá um perfil. |
| `xdm:profiles.xdm:identityMap` | Esse objeto mantém um conjunto de identidades de usuário final com base no código de integração de namespace da identidade. O mapa de identidade pode conter mais de uma identidade de cada namespace. Para obter mais informações sobre namespaces, consulte [esta página](../../../audience/get-started-identity.md). | `Email: [{"xdm:id": "123@abc.com"}]` |
| `xdm:profiles.xdm:decisionRequestId` | A ID gerada pelo cliente que pode ser usada para identificar exclusivamente uma solicitação de decisão de perfil. Essa ID é retomada na resposta do e não influencia o resultado da decisão. | `"xdm:decisionRequestId": "0AA00002-0000-1224-c0de-cjf98Csj43"` |
| `xdm:allowDuplicatePropositions` | Esse objeto controla a estrutura das regras de desduplicação. Consiste em uma série de sinalizadores que indicam se a mesma opção pode ser proposta através de uma determinada dimensão. Um sinalizador definido como verdadeiro significa que duplicatas são permitidas e não devem ser removidas na categoria indicada pelo sinalizador. Um sinalizador definido como falso significa que o mecanismo de decisão não deve fazer a mesma proposta na dimensão e, em vez disso, escolher a próxima melhor opção para uma das subdecisões. |
| `xdm:allowDuplicatePropositions.xdm:acrossActivities` | Se definido como verdadeiro, várias decisões podem receber a mesma opção. | `"xdm:acrossActivities": true` |
| `xdm:allowDuplicatePropositions.xdm:acrossPlacements` | Se definido como verdadeiro, vários posicionamentos podem receber a mesma opção. | `"xdm:acrossPlacements": true` |
| `xdm:mergePolicy.xdm:id` | Identifica a política de mesclagem pela qual controlar os dados retornados pelo serviço de acesso ao perfil. Se um não for especificado na solicitação, a Gestão de decisões não transmitirá nenhum serviço de acesso de perfil, caso contrário, transmitirá a ID fornecida pelo chamador. | `"xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"` |
| `xdm:responseFormat` | Um conjunto de sinalizadores que formata o conteúdo da resposta. |
| `xdm:responseFormat.xdm:includeContent` | Um valor booleano que, se definido como `true`, inclui conteúdo na resposta. | `"xdm:includeContent": true` |
| `xdm:responseFormat.xdm:includeMetadata` | Um objeto usado para especificar quais metadados adicionais são retornados. Se essa propriedade não for incluída, `xdm:id` e `repo:etag` são retornados por padrão. | `name` |
| `xdm:responseFormat.xdm:activity` | Esse sinalizador identifica as informações de metadados específicas retornadas para `xdm:activity`. | `name` |
| `xdm:responseFormat.xdm:option` | Esse sinalizador identifica as informações de metadados específicas retornadas para `xdm:option`. | `name`, `characteristics` |
| `xdm:responseFormat.xdm:placement` | Esse sinalizador identifica as informações de metadados específicas retornadas para `xdm:placement`. | `name`, `channel`, `componentType` |

### Resposta

Uma resposta bem-sucedida retorna informações sobre sua proposta, incluindo suas `xdm:propositionId`.

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
| `xdm:propositionId` | O identificador exclusivo da entidade de proposta associada a um XDM DecisionEvent. | `"xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8"` |
| `xdm:propositions` | Esse objeto contém uma única apresentação de decisão. Várias opções podem ser retornadas para a decisão. Se nenhuma opção for encontrada, a oferta de fallback da decisão será retornada. As propostas de decisão únicas sempre incluem um `options` propriedade ou um `fallback` propriedade. Quando presente, a variável `options` a propriedade não pode estar vazia. |
| `xdm:propositions.xdm:activity` | Este objeto contém o identificador exclusivo de uma decisão. | `"xdm:id": "xcore:activity:ffed0123"` |
| `xdm:propositions.xdm:placement` | Este objeto contém o identificador exclusivo para uma disposição de oferta. | `"xdm:id": "xcore:placement:ffed0456"` |
| `xdm:propositions.xdm:options` | Este objeto contém uma única opção, incluindo seu identificador exclusivo. Se presente, esse objeto não pode estar vazio. | `xdm:id": "xcore:personalized-option:ccc0111` |
| `xdm:propositions.xdm:options.@type` | Define o tipo do componente. `@type` atua como o contrato de processamento do cliente. Quando a experiência for montada, o compositor procurará os componentes que tenham um tipo específico. | `https://ns.adobe.com/experience/offer-management/content-component-imagelink` |
| `xdm:propositions.xdm:content` | O formato do conteúdo da resposta. | O conteúdo da resposta pode ser: `text`, `html block`ou `image link` |
| `xdm:score` | A pontuação de uma opção que é calculada como resultado de uma função de classificação associada à opção ou à decisão. Esse campo será retornado pela API se uma função de classificação estiver envolvida na determinação da pontuação de uma oferta durante a classificação. | `"xdm:score": 45.65` |
| `xdm:propositions.xdm:fallback` | Esse objeto contém uma única oferta substituta, incluindo seu identificador exclusivo. | `"xdm:id": "xcore:fallback:ccc0222"` |
| `xdm:propositions.xdm:fallback.dc:format` | A manifestação física ou digital do recurso. Normalmente, o formato deve incluir o tipo de mídia do recurso. O formato pode ser usado para determinar o software, hardware ou outro equipamento necessário para exibir ou operar o recurso. É recomendável selecionar um valor de um vocabulário controlado, por exemplo, a lista de [Tipos de mídia da Internet](https://www.iana.org/assignments/media-types/) definindo formatos de mídia de computador. | `"dc:format": "image/png"` ou `"image/jpeg"` |
| `xdm:propositions.xdm:fallback.xdm:deliveryURL` | Um URL opcional para ler o ativo de uma rede de entrega de conteúdo ou ponto de extremidade de serviço. Esse URL é usado para acessar o ativo publicamente de um agente do usuário. | `https://d37yhxrr0p3l3l.cloudfront.net/0fd0f090-a148-11ea-89e3-f1f2ad52f7e8/urn:aaid:sc:US:a68c86a6-9295-4940-a083-11916b665500/0/40d78a12-f8b6-3f07-8e67-7cb8ae2cc7ec` |
| `ode:createDate` | A hora em que a mensagem de resposta de decisão foi criada. Isso é representado como época. | `"ode:createDate": 1566497582038` |

**Códigos de resposta**

A tabela abaixo lista todos os códigos que podem ser retornados na resposta:

| Código | Descrição |
|  ---  |  ---  |
| 200 | Sucesso. A decisão foi tomada para determinadas atividades |
| 400 | Parâmetro de solicitação inválido. A solicitação não pode ser entendida pelo servidor devido à sintaxe malformada. |
| 403 | Proibido, permissões insuficientes. |
| 422 | Entidade não processável. A sintaxe da solicitação está correta, no entanto, devido a erros semânticos, ela não pode ser processada. |
| 429 | Muitas solicitações. O usuário enviou muitas solicitações em um determinado período. |
| 500 | Erro interno do servidor. O servidor encontrou uma condição inesperada que o impediu de atender à solicitação. |
| 503 | Serviço indisponível devido à sobrecarga do servidor. No momento, o servidor não pode lidar com a solicitação devido a uma sobrecarga temporária. |

## Tutorial em vídeo {#video}

O vídeo a seguir é destinado a apoiar a compreensão dos componentes da Gestão de decisões.

>[!NOTE]
>
>Este vídeo se aplica ao serviço de aplicativos do Offer Decisioning criado na Adobe Experience Platform. No entanto, fornece orientação genérica para usar a Oferta no contexto do Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329919/?quality=12)

## Próximas etapas {#next-steps}

Ao seguir este guia de API, você criou e entregou ofertas usando o [!DNL Decisions] API. Para obter mais informações, consulte [visão geral do Gerenciamento de decisão](../../../offers/get-started/starting-offer-decisioning.md).
