---
solution: Journey Optimizer
product: journey optimizer
title: Etapas adicionais para enviar eventos a uma jornada
description: Saiba mais sobre as etapas adicionais para enviar eventos a uma jornada
feature: Journeys, Events
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: etapas, configuração, jornada, eventos, fluxo, API
exl-id: e0144151-6c54-4656-9650-b544d8e7be16
TQID: https://experienceleague.adobe.com/SiUXmerz2D-TYmIEXvaYk4usjRq67Y0v7V7sGVN-4vo
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 318
ht-degree: 5%

---

# Etapas adicionais para enviar eventos {#additional-steps-to-send-events}

Para configurar eventos a serem enviados para **[!UICONTROL APIs de assimilação de streaming]** e para serem usados em [!DNL Journey Optimizer], é necessário seguir estas etapas:

1. Obtenha o URL de entrada das APIs do Adobe Experience Platform. Saiba mais em [Visão geral das APIs de assimilação de streaming](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=pt-BR){target="_blank"}.
1. Copie a carga da visualização de carga no menu **[!UICONTROL Evento]**. Saiba mais [nesta página](../event/about-creating.md#define-the-payload-fields).

>[!IMPORTANT]
>
>Para obter os requisitos e as limitações do evento (transmissão, Serviço de consulta, assimilação em lote), consulte [medidas de proteção de Jornada - Eventos](../start/guardrails.md#events-g).

Em seguida, é necessário configurar o sistema de dados que envia eventos para as APIs de assimilação de streaming usando a carga útil copiada:

1. Configure uma chamada de API POST para o URL das APIs de assimilação de streaming (chamada de entrada).
1. Use a carga copiada de [!DNL Journey Optimizer] no corpo (&quot;seção de dados&quot;) da chamada da API para as APIs de assimilação de fluxo. Veja um exemplo abaixo
1. Determine onde obter todas as variáveis presentes na carga. Exemplo: se o evento deve transmitir o endereço, a carga colada mostrará &quot;address&quot;: &quot;string&quot;. &quot;string&quot; deve ser substituída pela variável que preencherá automaticamente o valor correto, o email da pessoa para a qual enviar uma mensagem. Observe que na pré-visualização de carga, na seção **[!UICONTROL Cabeçalho]**, preenchemos automaticamente muitos valores esperados para facilitar seu trabalho.
1. Selecione &quot;application/json&quot; como um tipo de corpo.
1. Passe a ID da organização no cabeçalho usando a chave &quot;x-gw-ims-org-id&quot;. No valor, use a ID da organização (&quot;XXX@AdobeOrg&quot;).

Este é um exemplo de um evento de APIs de assimilação de fluxo:

```
{
    "header": {
        "msgType": "xdmEntityCreate",
        "msgId": "c25585b9-252e-431d-b562-e73da70c04e7",
        "msgVersion": "1.0",
        "xactionId": "f5995abe-c49d-4848-9577-a7a4fc2996fb",
        "datasetId": "string - required if you want the data to land in a specific dataset - not mandatory",
        "imsOrgId": "XXX@AdobeOrg",
        "schemaRef": {
            "id": "XXX",
            "contentType": "application/vnd.adobe.xed-full+json;version=1"
        },
        "source": {
            "name": "Journeys"
        }
    },
    "body": {
        "xdmMeta": {
            "schemaRef": {
                "id": "XXX",
                "contentType": "application/vnd.adobe.xed-full+json;version=1"
            }
        },
        "xdmEntity": {
            "_instance_name": {
                "person": {
                    "firstName": "string",
                    "lastName": "string",
                    "gender": "string",
                    "birthYear": 10,
                    "emailAddress": "string"
                }
            },
            "identityMap": {
                "Email": [
                {
                    "id": "string"
                    }
                ]
            },
            "_id": "string",
            "timestamp": "2023-05-29T00:00:00.000Z",
            "_experience": {
                "campaign": {
                    "orchestration": {
                    "eventID": "XXX"
                    }
                }
            }
        }
    }
}
```

Para facilitar a identificação do local onde colar a parte de &quot;dados&quot;, você pode usar uma ferramenta de visualização JSON, como o [formatador JSON](https://jsonformatter.curiousconcept.com){target="_blank"}.

Para solucionar problemas de APIs de assimilação de fluxo, consulte a [documentação do Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target="_blank"}.
