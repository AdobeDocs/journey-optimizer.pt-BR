---
title: API de decisão em lote
description: Saiba como usar a API de decisão em lote para selecionar as melhores ofertas para perfis segmentados em um escopo de decisão predefinido.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1ed01a6b-5e42-47c8-a436-bdb388f50b4e
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 3%

---


# Delivery de ofertas usando o [!DNL Batch Decisioning] API {#deliver-offers-batch}

O [!DNL Batch Decisioning] A API permite que as organizações usem a funcionalidade do offer decisioning para todos os perfis em um determinado segmento em uma chamada. O conteúdo da oferta para cada perfil no segmento é colocado em um conjunto de dados do Adobe Experience Platform, onde está disponível para fluxos de trabalho em lote personalizados.

Com o [!DNL Batch Decisioning] API, é possível preencher um conjunto de dados com as melhores ofertas para todos os perfis em um segmento do Adobe Experience Platform para escopos de decisão. Por exemplo, uma organização pode querer executar [!DNL Batch Decisioning] para que possam enviar ofertas a um fornecedor de delivery de mensagens. Essas ofertas são então usadas como conteúdo que é enviado para delivery de mensagens em lote para o mesmo segmento de usuários.

Para fazer isso, a organização:

* Execute o [!DNL Batch Decisioning] API, que contém duas solicitações:

   1. A **Solicitação de POST em lote** para iniciar uma carga de trabalho para processar em lote as seleções de ofertas.

   2. A **Solicitação de GET em lote** para obter o status da carga de trabalho em lote.

* Exporte o conjunto de dados para a API do fornecedor do delivery de mensagens.

<!-- (Refer to the [export jobs endpoint documentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/export-jobs.html?lang=en) to learn more about exporting segments.) -->

>[!NOTE]
>
>A decisão em lote também pode ser executada usando a interface do Journey Optimizer. Para obter mais informações, consulte [esta seção](../../batch-delivery.md), que fornece informações sobre pré-requisitos e limitações globais a serem considerados ao usar a decisão em lote.

* **O número de trabalhos em lote em execução por conjunto de dados**: É possível executar até cinco trabalhos em lote por vez, por conjunto de dados. Quaisquer outras solicitações em lote com o mesmo conjunto de dados de saída são adicionadas à fila. Um trabalho em fila é selecionado para o processamento quando o trabalho anterior terminar de ser executado.
* **Limite de frequência**: Um lote é executado do instantâneo do perfil que ocorre uma vez por dia. O [!DNL Batch Decisioning] A API limita a frequência e sempre carrega perfis do instantâneo mais recente.

## Introdução {#getting-started}

Antes de usar essa API, complete as etapas de pré-requisitos a seguir.

### Preparar a decisão {#prepare-decision}

Para preparar uma ou mais decisões, verifique se você criou um conjunto de dados, um segmento e uma decisão. Esses pré-requisitos estão detalhados em [esta seção](../../batch-delivery.md).

### Requisitos da API {#api-requirements}

Todos [!DNL Batch Decisioning] para além dos referidos no [Guia do desenvolvedor da API de gerenciamento de decisões](../getting-started.md):

* `Content-Type`: `application/json`
* `x-request-id`: Uma string exclusiva que identifica a solicitação.
* `x-sandbox-name`: O nome da sandbox.
* `x-sandbox-id`: A ID da sandbox.

## Iniciar um processo em lote {#start-a-batch-process}

Para iniciar uma carga de trabalho para decisões de processo em lote, faça uma solicitação de POST para a `/workloads/decisions` endpoint .

>[!NOTE]
>
>Informações detalhadas sobre o tempo de processamento de trabalhos em lote estão disponíveis em [esta seção](../../batch-delivery.md).

**Formato da API**

```https
POST {ENDPOINT_PATH}/{CONTAINER_ID}/workloads/decisions
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do terminal para APIs do repositório. | `https://platform.adobe.io/data/core/ode` |
| `{CONTAINER_ID}` | O contêiner onde as decisões estão localizadas. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Solicitação**

```shell
curl -X POST 'https://platform.adobe.io/data/core/ode/0948b1c5-fff8-3b76-ba17-909c6b93b5a2/workloads/decisions' \
-H 'x-request-id: f671a589-eb7b-432f-b6b9-23d5b796b4dc' \
-H 'Content-Type: application/json' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-sandbox-id: {SANDBOX_ID}' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-d '{
  "xdm:segmentIds": [
    "609028e4-e66c-4776-b0d9-c782887e2273"
  ],
  "xdm:dataSetId": "6196b4a1a63bd118dafe093c",
  "xdm:propositionRequests": [
        {
            "xdm:activityId": "xcore:offer-activity:1410cdcda196707b",
            "xdm:placementId": "xcore:offer-placement:1410c4117306488a",
            "xdm:itemCount": 1
        }
  ],
  "xdm:includeContent": false
}'
```

| Propriedade | Descrição | Exemplo |
| -------- | ----------- | ------- |
| `xdm:segmentIds` | O valor é uma matriz que contém o identificador exclusivo do segmento. Ela só pode conter um valor. | `609028e4-e66c-4776-b0d9-c782887e2273` |
| `xdm:dataSetId` | O dataSet de saída em que os eventos de decisão podem ser gravados. | `6196b4a1a63bd118dafe093c` |
| `xdm:propositionRequests` | Um invólucro que contém o `placementId` e `activityId` |  |
| `xdm:activityId` | O identificador único da decisão. | `xcore:offer-activity:1410cdcda196707b` |
| `xdm:placementId` | O identificador exclusivo de posicionamento. | `xcore:offer-placement:1410c4117306488a` |
| `xdm:itemCount` | Este é um campo opcional que mostra o número de itens, como opções solicitadas para o escopo de decisão. Por padrão, a API retorna uma opção por escopo, mas você pode solicitar explicitamente mais opções especificando esse campo. É possível solicitar um mínimo de 1 e um máximo de 30 opções por escopo. | `1` |
| `xdm:includeContent` | Este é um campo opcional e é `false` por padrão. If `true`, o conteúdo da oferta é incluído nos eventos de decisão do conjunto de dados. | `false` |

Consulte a [Documentação do Gerenciamento de decisões](../../get-started/starting-offer-decisioning.md) para obter uma visão geral dos principais conceitos e propriedades.

**Resposta**

```json
{
    "@id": "47efef25-4bcf-404f-96e2-67c4f784a1f5",
    "xdm:imsOrgId": "9GTO98D5F@AdobeOrg",
    "xdm:containerId": "0948b1c5-fff8-3b76-ba17-909c6b93b5a2",
    "ode:createDate": 1648078924834,
    "ode:status": "QUEUED"
}
```

| Propriedade | Descrição | Exemplo |
| -------- | ----------- | ------- |
| `@id` | O UUID gerado pelo Offer Decisioning que identifica uma única carga de trabalho. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | A ID da organização. | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | A ID do contêiner. | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | A hora em que a solicitação de carga de trabalho de decisão foi criada. | `1648078924834` |
| `ode:status` | O status da carga de trabalho. | `ode:status: "QUEUED"` |

## Recuperar informações de uma decisão de lote {#retrieve-information-on-a-batch-decision}

Para recuperar informações sobre uma decisão específica, faça uma solicitação GET ao `/workloads/decisions` endpoint ao fornecer o valor da ID da carga de trabalho correspondente para sua decisão.

**Formato da API**

```https
GET  {ENDPOINT_PATH}/{CONTAINER_ID}/workloads/decisions/{WORKLOAD_ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do terminal para APIs do repositório. | `https://platform.adobe.io/data/core/ode` |
| `{CONTAINER_ID}` | O contêiner onde as decisões estão localizadas. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{WORKLOAD_ID}` | O UUID gerado pelo Offer Decisioning que identifica uma única carga de trabalho. | `47efef25-4bcf-404f-96e2-67c4f784a1f5` |

**Solicitação**

```shell
curl -X GET 'https://platform.adobe.io/data/core/ode/0948b1c5-fff8-3b76-ba17-909c6b93b5a2/workloads/decisions/f395ab1f-dfaf-48d4-84c9-199ad6354591' \
-H 'x-request-id: 7832a42a-d4e5-413b-98e8-e49bef056436' \
-H 'Content-Type: application/json' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H'x-sandbox-id: {SANDBOX_ID}' \
-H 'Authorization: Bearer {ACCESS_TOKEN}'
```

**Resposta**

```json
{
    "@id": "f395ab1f-dfaf-48d4-84c9-199ad6354591",
    "xdm:imsOrgId": "{IMS_ORG}",
    "xdm:containerId": "0948b1c5-fff8-3b76-ba17-909c6b93b5a2",
    "ode:createDate": 1648076994405,
    "ode:status": "COMPLETED"
}
```

| Propriedade | Descrição | Exemplo |
| -------- | ----------- | ------- |
| `@id` | O UUID gerado pelo Offer Decisioning que identifica uma única carga de trabalho. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | A ID da organização | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | A ID do contêiner | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | A hora em que a solicitação de Carga de Trabalho de Decisão foi criada. | `1648076994405` |
| `ode:status` | O status da carga de trabalho começa com &quot;FILA&quot; e muda para &quot;PROCESSAMENTO&quot;, &quot;ASSIMILAÇÃO&quot;, &quot;CONCLUÍDO&quot; ou &quot;ERRO&quot;. | `ode:status: "COMPLETED"` |
| `ode:statusDetail` | Isso mostra mais detalhes, como sparkJobId e batchID, se o status for &quot;PROCESSAMENTO&quot; ou &quot;ASSIMILAÇÃO&quot;. Ele mostra os detalhes do erro se o status for &quot;ERRO&quot;. |  |

## Próximas etapas {#next-steps}

Ao seguir este guia de API, você verificou o status da carga de trabalho e as ofertas entregues usando o [!DNL [!DNL Batch Decisioning]] API. Para obter mais informações, consulte o [visão geral sobre o Gerenciamento de decisões](../../get-started/starting-offer-decisioning.md).
