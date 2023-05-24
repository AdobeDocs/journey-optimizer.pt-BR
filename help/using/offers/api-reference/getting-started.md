---
title: Introdução
description: Saiba como começar a usar a API da Biblioteca de ofertas para executar operações importantes usando o mecanismo de decisão.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: e7431d1b69e460471b01439c9bd2577fd69944ed
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 6%

---

# Guia do desenvolvedor da API de Gestão de decisões {#decision-management-api-developer-guide}

Este guia do desenvolvedor fornece etapas para ajudar você a começar a usar o [!DNL Offer Library] API. O guia fornece chamadas de API de amostra para executar operações importantes usando o mecanismo de decisão.

➡️ [Saiba mais sobre os componentes da Gestão de decisões neste vídeo](#video)

## Pré-requisitos {#prerequisites}

Este guia requer uma compreensão funcional dos seguintes componentes do Adobe Experience Platform:

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target="_blank"}: o quadro normalizado pelo qual [!DNL Experience Platform] organiza os dados de experiência do cliente.
   * [Noções básicas da composição do esquema](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=pt-BR){target="_blank"}: saiba mais sobre os blocos de construção básicos de esquemas XDM.
* [Gerenciamento de decisão](../../../using/offers/get-started/starting-offer-decisioning.md): explica os conceitos e componentes usados no Experience Decisioning em geral e na gestão de decisões em particular. Ilustra as estratégias usadas para escolher a melhor opção a ser apresentada durante a experiência de um cliente.
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html){target="_blank"}: o PQL é uma linguagem avançada para gravar expressões em instâncias XDM. O PQL é usado para definir regras de decisão.

## Leitura de chamadas de API de amostra {#reading-sample-api-calls}

Este guia fornece exemplos de chamadas de API para demonstrar como formatar suas solicitações. Isso inclui caminhos, cabeçalhos necessários e cargas de solicitação formatadas corretamente. O exemplo de JSON retornado nas respostas da API também é fornecido. Para obter informações sobre as convenções usadas na documentação para chamadas de API de exemplo, consulte a seção sobre [como ler chamadas de API de exemplo](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request){target="_blank"} no [!DNL Experience Platform] guia de solução de problemas.

## Coletar valores para cabeçalhos obrigatórios {#gather-values-for-required-headers}

Para fazer chamadas para [!DNL Adobe Experience Platform] APIs, primeiro conclua o [tutorial de autenticação](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html){target="_blank"}. Concluir o tutorial de autenticação fornece os valores para cada um dos cabeçalhos necessários em todos os [!DNL Experience Platform] Chamadas de API, conforme mostrado abaixo:

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`

Todas as solicitações que contêm uma carga (POST, PUT, PATCH) exigem um cabeçalho adicional:

* `Content-Type: application/json`

## Gerenciar acesso a um container {#manage-access-to-container}

Um container é um mecanismo de isolamento destinado a manter diferentes problemas separados. A ID do container é o primeiro elemento de caminho para todas as APIs do repositório. Todos os objetos de decisão residem em um container.

Um administrador pode agrupar entidades principais, recursos e permissões de acesso semelhantes em perfis. Isso reduz a carga de gerenciamento e é compatível com [Adobe Admin Console](https://adminconsole.adobe.com/). Você deve ser um administrador de produto do Adobe Experience Platform em sua organização para criar perfis e atribuir usuários a eles. Basta criar perfis de produto que correspondam a determinadas permissões em uma única etapa e, em seguida, simplesmente adicionar usuários a esses perfis. Os perfis atuam como grupos aos quais foram concedidas permissões e cada usuário real ou usuário técnico nesse grupo herda essas permissões.

Dados os privilégios de administrador, você pode conceder ou retirar permissões aos usuários por meio do [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"}. For more information, see the [Access control overview](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=pt-BR){target="_blank"}.

### Contêineres de lista acessíveis a usuários e integrações {#list-containers-accessible-to-users-and-integrations}

**Formato da API**

```http
GET /{ENDPOINT_PATH}?product={PRODUCT_CONTEXT}&property={PROPERTY}==decisioning
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs do repositório. | `https://platform.adobe.io/data/core/xcore/` |
| `{PRODUCT_CONTEXT}` | Filtra a lista de contêineres por sua associação aos contextos do produto. | `acp` |
| `{PROPERTY}` | Filtra o tipo de container retornado. | `_instance.containerType==decisioning` |

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

Uma resposta bem-sucedida retorna informações sobre contêineres de gestão de decisões. Isso inclui uma `instanceId` atributo, cujo valor é a ID do container.

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

Este documento cobriu os conhecimentos necessários para fazer chamadas para o [!DNL Offer Library] API, incluindo a aquisição da ID do container. Agora você pode prosseguir para as chamadas de amostra fornecidas neste guia do desenvolvedor e seguir junto com as instruções.
<!--
>[!NOTE]
>
> The In-app messaging channel in Adobe Journey Optimizer uses decision management objects. If your organization uses the in-app messaging channel, then API list requests for objects will include objects created by the in-app messaging service and can be ignored for decision management use cases. Objects created for in-app messages will have `createdBy = “Mobile_Sheliak”`.
-->

## Vídeo explicativo {#video}

O vídeo a seguir é destinado a apoiar a compreensão dos componentes da Gestão de decisões.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)

