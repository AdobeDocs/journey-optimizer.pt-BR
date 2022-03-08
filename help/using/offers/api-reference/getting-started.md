---
title: Introdução
description: Saiba como começar a usar a API da Biblioteca de ofertas para executar operações-chave usando o Mecanismo de gerenciamento de decisões.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 6%

---

# Guia do desenvolvedor da API de gerenciamento de decisões {#decision-management-api-developer-guide}

Este guia do desenvolvedor fornece etapas para ajudá-lo a começar a usar o [!DNL Offer Library] API. O guia fornece exemplos de chamadas de API para executar operações principais usando o Mecanismo de gerenciamento de decisões.

➡️ [Descubra este recurso no vídeo](#video)

## Pré-requisitos {#prerequisites}

Este guia requer uma compreensão funcional dos seguintes componentes do Adobe Experience Platform:

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target=&quot;_blank&quot;}: O quadro normalizado pelo qual [!DNL Experience Platform] organiza os dados de experiência do cliente.
   * [Noções básicas da composição do schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=pt-BR){target=&quot;_blank&quot;}: Saiba mais sobre os componentes básicos dos esquemas XDM.
* [Gerenciamento de decisões](../../../using/offers/get-started/starting-offer-decisioning.md): Explica os conceitos e os componentes usados para o Experience Decisioning em geral e para o Offer decisioning em particular. Ilustra as estratégias usadas para escolher a melhor opção para apresentar durante a experiência de um cliente.
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html){target=&quot;_blank&quot;}: O PQL é um idioma avançado para gravar expressões em instâncias do XDM. O PQL é usado para definir regras de decisão.

## Lendo exemplos de chamadas de API {#reading-sample-api-calls}

Este guia fornece exemplos de chamadas de API para demonstrar como formatar suas solicitações do . Isso inclui caminhos, cabeçalhos necessários e cargas de solicitação formatadas corretamente. O JSON de exemplo retornado nas respostas da API também é fornecido. Para obter informações sobre as convenções usadas na documentação para chamadas de API de exemplo, consulte a seção sobre [como ler exemplos de chamadas de API](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request){target=&quot;_blank&quot;} no [!DNL Experience Platform] guia de solução de problemas.

## Coletar valores para cabeçalhos necessários {#gather-values-for-required-headers}

Para fazer chamadas para [!DNL Platform] As APIs devem ser concluídas primeiro [tutorial de autenticação](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html){target=&quot;_blank&quot;}. A conclusão do tutorial de autenticação fornece os valores para cada um dos cabeçalhos necessários em todos [!DNL Experience Platform] Chamadas de API, conforme mostrado abaixo:

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`

Todas as solicitações que contêm uma carga útil (POST, PUT, PATCH) exigem um cabeçalho adicional:

* `Content-Type: application/json`

## Gerenciar acesso a um contêiner {#manage-access-to-container}

Um contêiner é um mecanismo de isolamento para manter diferentes preocupações separadas. A ID do contêiner é o primeiro elemento de caminho para todas as APIs do repositório. Todos os objetos de decisão residem em um contêiner.

Um administrador pode agrupar principais, recursos e permissões de acesso semelhantes em perfis. Isso reduz a carga administrativa e é compatível com [Adobe Admin Console](https://adminconsole.adobe.com/). Você deve ser um administrador de produto do Adobe Experience Platform em sua organização para criar perfis e atribuir usuários a eles. É suficiente criar perfis de produto que correspondam a determinadas permissões em uma única etapa e, em seguida, simplesmente adicionar usuários a esses perfis. Os perfis atuam como grupos aos quais foram concedidas permissões e cada usuário real ou técnico nesse grupo herda essas permissões.

Com determinados privilégios de administrador, você pode conceder ou retirar permissões aos usuários por meio do [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;}. Para obter mais informações, consulte o [Visão geral do controle de acesso](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=pt-BR){target=&quot;_blank&quot;}.

### Listar contêineres acessíveis para usuários e integrações {#list-containers-accessible-to-users-and-integrations}

**Formato da API**

```http
GET /{ENDPOINT_PATH}?product={PRODUCT_CONTEXT}&property={PROPERTY}==decisioning
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do terminal para APIs do repositório. | `https://platform.adobe.io/data/core/xcore/` |
| `{PRODUCT_CONTEXT}` | Filtra a lista de contêineres por sua associação aos contextos de produto. | `acp` |
| `{PROPERTY}` | Filtra o tipo de contêiner retornado. | `_instance.containerType==decisioning` |

**Solicitação**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/?product=acp&property=_instance.containerType==decisioning' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Resposta**

Uma resposta bem-sucedida retorna informações sobre contêineres de gerenciamento de decisões. Isso inclui uma `instanceId` , cujo valor é a ID do contêiner.

```json
{
    "_embedded": {
        "https://ns.adobe.com/experience/xcore/container": [
            {
                "instanceId": "{INSTANCE_ID}",
                "schemas": [
                    "https://ns.adobe.com/experience/xcore/container;version=0.5"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 2,
                "repo:createdDate": "2020-09-16T07:54:28.319959Z",
                "repo:lastModifiedDate": "2020-09-16T07:54:32.098139Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "containerType": "decisioning",
                    "repo:name": "{REPO_NAME}",
                    "dataCenter": "{DATA_CENTER}",
                    "parentName": "{PARENT_NAME}",
                    "parentId": "{PARENT_ID}"
                },
                "_links": {
                    "self": {
                        "href": "/containers/{INSTANCE_ID}"
                    }
                }
            }
        ]
    },
    "_links": {
        "self": {
            "href": "/?product=acp&property=_instance.containerType==decisioning",
            "@type": "https://ns.adobe.com/experience/xcore/hal/home"
        }
    }
}
```

## Próximas etapas {#next-steps}

Este documento cobria os pré-requisitos necessários para fazer chamadas para o [!DNL Offer Library] API, incluindo a aquisição da ID do contêiner. Agora você pode prosseguir para as chamadas de exemplo fornecidas neste guia do desenvolvedor e seguir com suas instruções.

## Tutorial em vídeo {#video}

O vídeo a seguir é destinado a auxiliar a compreensão dos componentes do Gerenciamento de decisões.

>[!NOTE]
>
>Este vídeo se aplica ao serviço de aplicativo do Offer Decisioning criado no Adobe Experience Platform. No entanto, fornece orientação genérica para usar a Oferta no contexto do Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)
