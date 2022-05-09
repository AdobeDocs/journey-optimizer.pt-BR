---
title: Etapas adicionais para enviar eventos para uma jornada
description: Saiba mais sobre as etapas adicionais para enviar eventos a uma jornada
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: e0144151-6c54-4656-9650-b544d8e7be16
source-git-commit: 79d3bd42c208d38aaebce742e70b247106c21587
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 5%

---

# Etapas adicionais para enviar eventos {#additional-steps-to-send-events}

Para configurar eventos a serem enviados para **[!UICONTROL Streaming Ingestion APIs]** e a utilizar em [!DNL Journey Optimizer], siga estas etapas:

1. Obtenha o URL de entrada das APIs do Adobe Experience Platform. Saiba mais em [Visão geral de APIs de assimilação de fluxo](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=pt-BR){target=&quot;_blank&quot;}.
1. Copie a carga da pré-visualização de carga no **[!UICONTROL Event]** menu. Saiba mais [nesta página](../event/about-creating.md#define-the-payload-fields).

Em seguida, é necessário configurar o sistema de dados que envia eventos para as APIs de assimilação de streaming usando a carga útil copiada:

1. Configure uma chamada POST API para o URL das APIs de assimilação de fluxo (chamada de entrada).
1. Usar a carga copiada de [!DNL Journey Optimizer] no corpo (&quot;seção de dados&quot;) da chamada da API para APIs de assimilação de fluxo. Veja abaixo um exemplo
1. Determine onde obter todas as variáveis presentes na carga útil. Exemplo: se o evento tiver que transmitir o endereço, a carga colada mostrará &quot;endereço&quot;: &quot;string&quot;. &quot;string&quot; deve ser substituída pela variável que preencherá automaticamente o valor correto, o email da pessoa para a qual enviar uma mensagem. Observe que, na pré-visualização de carga, no **[!UICONTROL Header]** , preenchemos automaticamente muitos valores esperados para facilitar seu trabalho.
1. Selecione &quot;application/json&quot; como um tipo de corpo.
1. Passe a ID da organização no cabeçalho usando a chave &quot;x-gw-ims-org-id&quot;. Para o valor , use a ID da organização (&quot;XXX@AdobeOrg&quot;).

Veja um exemplo de um evento de APIs de assimilação de fluxo:

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

Para facilitar a identificação do local onde a parte &quot;dados&quot; deve ser colada, é possível usar uma ferramenta de visualização JSON, como [Formatador JSON](https://jsonformatter.curiousconcept.com){target=&quot;_blank&quot;}.

Para solucionar problemas de APIs de assimilação de fluxo, consulte [Documentação do Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target=&quot;_blank&quot;}.
