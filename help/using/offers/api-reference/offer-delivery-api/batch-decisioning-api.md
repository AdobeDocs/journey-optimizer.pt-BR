---
title: API de decisão em lote
description: Saiba como usar a API de decisão em lote para selecionar as melhores ofertas para perfis de públicos-alvo em um escopo de decisão predefinido.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1ed01a6b-5e42-47c8-a436-bdb388f50b4e
source-git-commit: d2451bbaf9830ce3d928e71a609627c23a7566fa
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 4%

---


# Entregar ofertas usando a API [!DNL Batch Decisioning] {#deliver-offers-batch}

A API [!DNL Batch Decisioning] permite que as organizações usem a funcionalidade de decisão para todos os perfis em um determinado público-alvo através de uma única chamada. O conteúdo da oferta de cada perfil no público-alvo é colocado em um conjunto de dados do Adobe Experience Platform, onde ele estará disponível para fluxos de trabalho em lote personalizados.

Com a API [!DNL Batch Decisioning], você pode preencher um conjunto de dados com as melhores ofertas para todos os perfis em um público-alvo da Adobe Experience Platform para escopos de decisão. Por exemplo, uma organização pode querer executar [!DNL Batch Decisioning] para enviar ofertas a um fornecedor de entrega de mensagens. Essas ofertas são usadas como conteúdo enviado para entrega de mensagens em lote para o mesmo público-alvo de usuários.

Para fazer isso, a organização deve:

* Execute a API [!DNL Batch Decisioning], que contém duas solicitações:

   1. Uma **Solicitação POST de lote** para iniciar uma carga de trabalho para processar em lote as seleções de ofertas.

   2. Uma **Solicitação de GET em lote** para obter o status da carga de trabalho em lote.

* Exportar o conjunto de dados para a API do fornecedor de delivery de mensagens.

<!-- (Refer to the [export jobs endpoint documentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/export-jobs.html?lang=pt-BR) to learn more about exporting audiences.) -->

>[!NOTE]
>
>A decisão em lote também pode ser executada usando a interface do Journey Optimizer. Para obter mais informações, consulte [esta seção](../../batch-delivery.md), que fornece informações sobre os pré-requisitos e limitações globais que devem ser considerados ao usar a decisão em lote.

* **O número de trabalhos em lotes em execução por conjunto de dados**: até cinco trabalhos em lotes podem ser executados de cada vez, por conjunto de dados. Quaisquer outras solicitações em lote com o mesmo conjunto de dados de saída são adicionadas à fila. Uma tarefa em fila será processada assim que a tarefa anterior terminar de ser executada.
* **Limite de frequência**: um lote é executado fora do instantâneo de perfil que ocorre uma vez por dia. A API [!DNL Batch Decisioning] limita a frequência e sempre carrega perfis do instantâneo mais recente.

## Introdução {#getting-started}

Antes de usar essa API, verifique se você concluiu as seguintes etapas de pré-requisitos.

### Preparar a decisão {#prepare-decision}

Para preparar uma ou mais decisões, verifique se você criou um conjunto de dados, um público-alvo e uma decisão. Esses pré-requisitos estão detalhados em [esta seção](../../batch-delivery.md).

### Requisitos da API {#api-requirements}

Todas as solicitações [!DNL Batch Decisioning] exigem os seguintes cabeçalhos, além dos mencionados no [Guia do desenvolvedor da API de Gestão de Decisões](../getting-started.md):

* `Content-Type`: `application/json`
* `x-request-id`: uma cadeia de caracteres exclusiva que identifica a solicitação.
* `x-sandbox-name`: O nome da sandbox.

## Iniciar um processo em lote {#start-a-batch-process}

Para iniciar uma carga de trabalho para tomar decisões de processo em lote, faça uma solicitação POST para o ponto de extremidade `/workloads/decisions`.

>[!NOTE]
>
>Informações detalhadas sobre o tempo de processamento dos trabalhos em lotes estão disponíveis em [esta seção](../../batch-delivery.md).

**Formato da API**

```https
POST {ENDPOINT_PATH}/workloads/decisions
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs do repositório. | `https://platform.adobe.io/data/core/dwm` |

**Solicitação**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dwm/workloads/decisions' \
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
| `xdm:activityId` | O identificador exclusivo da decisão. |
| `xdm:dataSetId` | O dataSet de saída no qual os eventos de decisão podem ser gravados. | `6196b4a1a63bd118dafe093c` |
| `xdm:enrichedAudience` | Adicione esse parâmetro e defina-o como &quot;true&quot; se você estiver direcionando um público-alvo de CSV | `true` |
| `xdm:includeContent` | Este é um campo opcional e é `false` por padrão. Se `true`, o conteúdo da oferta será incluído nos eventos de decisão do conjunto de dados. | `false` |
| `xdm:itemCount` | Este campo é opcional e mostra o número de itens, como opções solicitadas para o escopo da decisão. Por padrão, a API retorna uma opção por escopo, mas você pode solicitar mais opções explicitamente especificando esse campo. É possível solicitar no mínimo 1 e no máximo 30 opções por escopo. | `1` | `xcore:offer-activity:1410cdcda196707b` |
| `xdm:placementId` | O identificador de posicionamento exclusivo. | `xcore:offer-placement:1410c4117306488a` |
| `xdm:propositionRequests` | Um invólucro que contém o `placementId` e `activityId` |
| `xdm:segmentIds` | O valor é uma matriz que contém o identificador exclusivo do público-alvo. Ele só pode conter um valor. | `609028e4-e66c-4776-b0d9-c782887e2273` |

Consulte a [documentação do Gerenciamento de decisões](../../get-started/starting-offer-decisioning.md) para obter uma visão geral dos principais conceitos e propriedades.

**Resposta**

```json
{
    "@id": "47efef25-4bcf-404f-96e2-67c4f784a1f5",
    "xdm:imsOrgId": "9GTO98D5F@AdobeOrg",
    "ode:createDate": 1648078924834,
    "ode:status": "QUEUED"
}
```

| Propriedade | Descrição | Exemplo |
| -------- | ----------- | ------- |
| `@id` | A UUID gerada pela gestão de decisões que identifica uma única carga de trabalho. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | A ID da organização. | `9GTO98D5F@AdobeOrg` |
| `ode:createDate` | A hora em que a solicitação de carga de trabalho de decisão foi criada. | `1648078924834` |
| `ode:status` | O status da carga de trabalho. | `ode:status: "QUEUED"` |

## Recuperar informações sobre uma decisão em lote {#retrieve-information-on-a-batch-decision}

Para recuperar informações sobre uma decisão específica, faça uma solicitação GET para o ponto de extremidade `/workloads/decisions` enquanto fornece o valor da ID da carga de trabalho correspondente para a sua decisão.

**Formato da API**

```https
GET {ENDPOINT_PATH}/workloads/decisions/{WORKLOAD_ID}
```

| Parâmetro | Descrição | Exemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | O caminho do endpoint para APIs do repositório. | `https://platform.adobe.io/data/core/dwm` |
| `{WORKLOAD_ID}` | A UUID gerada pela gestão de decisões que identifica uma única carga de trabalho. | `47efef25-4bcf-404f-96e2-67c4f784a1f5` |

**Solicitação**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dwm/workloads/decisions/f395ab1f-dfaf-48d4-84c9-199ad6354591' \
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
    "ode:createDate": 1648076994405,
    "ode:status": "COMPLETED"
}
```

| Propriedade | Descrição | Exemplo |
| -------- | ----------- | ------- |
| `@id` | A UUID gerada pela gestão de decisões que identifica uma única carga de trabalho. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | A ID da organização | `9GTO98D5F@AdobeOrg` |
| `ode:createDate` | A hora em que a solicitação de Carga de trabalho de decisão foi criada. | `1648076994405` |
| `ode:status` | O status da carga de trabalho começa com &quot;EM FILA&quot; e muda para &quot;PROCESSING&quot;, &quot;INGESTING&quot;, &quot;COMPLETED&quot; ou &quot;ERROR&quot;. | `ode:status: "COMPLETED"` |
| `ode:statusDetail` | Ela mostra mais detalhes, como sparkJobId e batchID, se o status for &quot;PROCESSING&quot; ou &quot;INGESTING&quot;. Ele mostra os detalhes do erro se o status for &quot;ERRO&quot;. |  |

## Próximas etapas {#next-steps}

Ao seguir este guia de API, você verificou o status da carga de trabalho e entregou ofertas usando a API [!DNL [!DNL Batch Decisioning]]. Para obter mais informações, consulte a [visão geral sobre a Gestão de Decisões](../../get-started/starting-offer-decisioning.md).