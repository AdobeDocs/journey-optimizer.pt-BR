---
title: Introdução às APIs de entrega de ofertas
description: Saiba mais sobre as APIs disponíveis para fornecer ofertas personalizadas.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: 91f52af0c2e42556c4456be9b6b0cb84378c2a23
workflow-type: tm+mt
source-wordcount: '624'
ht-degree: 4%

---

# Introdução às APIs de entrega de ofertas {#about-decisioning-apis}

É possível entregar ofertas usando a variável **Decisão** ou o **Edge Decisioning** API. Além disso, a **Decisão em lote** A API permite entregar ofertas a todos os perfis em um determinado público-alvo com uma única chamada. O conteúdo da oferta de cada perfil no público-alvo é colocado em um conjunto de dados do Adobe Experience Platform, onde ele estará disponível para fluxos de trabalho em lote personalizados.

Nesta página, você encontrará informações sobre funcionalidades específicas disponíveis com o **Decisão** e **Edge Decisioning** APIs. Embora ambos permitam que você forneça ofertas aos seus clientes, recomendamos usar o **Edge Decisioning** sempre que possível para casos de uso de entrada e para garantir melhor latência e taxa de transferência na sua plataforma.

Para obter mais informações sobre como trabalhar com as APIs, consulte estas seções:
* [API de decisão](decisioning-api.md)
* [API de decisão do Edge](edge-decisioning-api.md)
* [API de decisão em lote](batch-decisioning-api.md)

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

## Recursos da API do Edge Decisioning {#edge}

**Solicitação única para eventos de experiência e solicitações de decisão**

Com a API do Edge Decisioning, é possível enviar o próprio evento de experiência juntamente com a solicitação de decisão em uma única solicitação, em vez de ter duas solicitações diferentes.

Por exemplo, se um cliente visitar seu site, a solicitação incluirá o evento de experiência (a visita do cliente à página) e obterá uma oferta para preencher a página visitada.

**Armazenamento de dados de contexto no Adobe Experience Platform**

Dados de contexto se referem a dados que você só sabe no momento em que deseja uma oferta de volta. Por exemplo, a cor do artigo comprado, o clima no momento da compra etc.

Ao transmitir dados de contexto com uma solicitação da API do Edge Decisioning, os dados são armazenados no perfil do Adobe Experience Platform, permitindo reutilização futura.

>[!NOTE]
>
>Para que os dados de contexto sejam armazenados, é necessário ter um esquema XDM dedicado configurado.

## Recursos da API de decisão {#decisioning}

As funcionalidades listadas abaixo só estão disponíveis com a API de decisão. Se você precisar usar uma delas para atender aos seus requisitos, use a API de decisão. Caso contrário, recomendamos usar as APIs do Edge Decisioning.

* **Conteúdo e características da oferta**: é possível optar por não retornar o conteúdo e as características de uma oferta usando uma opção dedicada.
* **Metadados da oferta**: habilite uma opção para retornar os metadados de uma oferta.
* **Política de mesclagem**: use em sua solicitação uma política de mesclagem diferente da que está associada à sua sandbox.
* **Eventos de decisão e limite de frequência**: os eventos de decisão de bloco não são contados por nenhum limite de frequência que ocorra.
* **Proposições duplicadas**: ative uma opção para não desduplicar apresentações.
