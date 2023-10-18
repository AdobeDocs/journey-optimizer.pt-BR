---
solution: Journey Optimizer
product: journey optimizer
title: Etapas adicionais para enviar eventos a uma jornada
description: Saiba mais sobre as etapas adicionais para enviar eventos a uma jornada
feature: Journeys, Events
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: etapas, configuração, jornada, eventos, fluxo, API
exl-id: e0144151-6c54-4656-9650-b544d8e7be16
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 5%

---

# Etapas adicionais para enviar eventos {#additional-steps-to-send-events}

Para configurar eventos a serem enviados para o **[!UICONTROL APIs de assimilação de fluxo]** e para serem utilizados em [!DNL Journey Optimizer], é necessário seguir estas etapas:

1. Obtenha o URL de entrada das APIs do Adobe Experience Platform. Saiba mais em [Visão geral das APIs de assimilação de fluxo](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=pt-BR){target="_blank"}.
1. Copie o conteúdo da pré-visualização de carga no **[!UICONTROL Evento]** menu. Saiba mais [nesta página](../event/about-creating.md#define-the-payload-fields).

Em seguida, é necessário configurar o sistema de dados que envia eventos para as APIs de assimilação de streaming usando a carga útil copiada:

1. Configure uma chamada de API POST para o URL das APIs de assimilação de streaming (chamada de entrada).
1. Usar a carga copiada do [!DNL Journey Optimizer] no corpo (&quot;seção de dados&quot;) da chamada da API para as APIs de assimilação de streaming. Veja um exemplo abaixo
1. Determine onde obter todas as variáveis presentes na carga. Exemplo: se o evento deve transmitir o endereço, a carga colada mostrará &quot;address&quot;: &quot;string&quot;. &quot;string&quot; deve ser substituída pela variável que preencherá automaticamente o valor correto, o email da pessoa para a qual enviar uma mensagem. Observe que na pré-visualização de carga, no campo **[!UICONTROL Cabeçalho]** preenchemos automaticamente muitos valores para facilitar o trabalho.
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
            "timestamp": "2018-05-29T00:00:00.000Z",
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

Para facilitar a identificação do local onde colar a parte de &quot;dados&quot;, você pode usar uma ferramenta de visualização JSON, como [Formatador JSON](https://jsonformatter.curiousconcept.com){target="_blank"}.

Para solucionar problemas de APIs de assimilação de fluxo, consulte [Documentação do Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target="_blank"}.
