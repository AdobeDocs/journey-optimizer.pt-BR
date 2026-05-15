---
solution: Journey Optimizer
product: journey optimizer
title: Crie webhooks de feedback para campanhas acionadas por API no Journey Optimizer
description: Saiba como criar webhooks de feedback para campanhas acionadas por API no Journey Optimizer.
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
exl-id: a46f29a4-5115-4feb-8b2c-751765be2b36
TQID: https://experienceleague.adobe.com/RPopgwZfOcaw-uHvqVnforixMTAH57urwF2ViaZQemQ
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32id: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: fe338112-e2ce-4876-8989-fc4d497613f1
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 302
ht-degree: 0%

---

# Criar webhooks de feedback para campanhas acionadas por API {#webhooks}

Os webhooks de feedback permitem que você receba atualizações de status em tempo real para mensagens enviadas por meio de campanhas acionadas por API transacional. Ao configurar um webhook, você pode receber automaticamente os resultados do delivery diretamente para seus sistemas, permitindo monitoramento, registro e processamento automatizado.

Você pode gerenciar configurações de webhook no menu **[!UICONTROL Administração]** / **[!UICONTROL Canais]** / **[!UICONTROL Configurações de webhook de comentários]**.

![](assets/webhook-list.png)

>[!NOTE]
>Somente uma configuração de webhook por combinação de **Organização + sandbox** é permitida.

## Criar um webhook de feedback

Para criar um webhook, siga estas etapas:

1. Navegue até **[!UICONTROL Administração]** / **[!UICONTROL Canais]** / **[!UICONTROL Configurações do webhook de comentários]**.

1. Clique em **Criar Webhook de Feedback**.

1. Na seção **[!UICONTROL Configuração Básica]**, forneça os seguintes detalhes:

   ![](assets/webhook-config.png)

   * **Nome do Webhook** - Insira um nome descritivo para identificar o webhook.
   * **Canais** - Selecione os canais para os quais este webhook deve receber feedback (Email e/ou SMS).
   * **URL do Webhook** - Forneça o ponto de extremidade HTTPS onde os eventos de comentários devem ser entregues.

1. Na seção **[!UICONTROL Autenticação]**, selecione o método de autenticação:

   ![](assets/webhook-authentication.png)

   * **Sem Autenticação** - Nenhum cabeçalho de autenticação foi adicionado.
   * **Autenticação JWT** - Forneça os detalhes necessários se o ponto de extremidade exigir autenticação JWT.

1. Na seção **[!UICONTROL Parâmetros de cabeçalho]**, configure cabeçalhos personalizados adicionais para serem enviados com cada solicitação de webhook.

   ![](assets/webhook-header.png)

1. Clique em **[!UICONTROL Enviar]** para salvar a configuração.

>[!NOTE]
>
>Você pode editar um webhook a qualquer momento. Para fazer isso, abra-o no inventário e clique no botão **[!UICONTROL Editar]**.

## Estrutura de carga do Webhook

Após a execução de uma mensagem, **[!DNL Journey Optimizer]** envia a seguinte carga para o ponto de extremidade configurado.

```
{
  "requestId": "8NoByJneShCdCGRnrGS1t1m3CdA73dhR",
  "imsOrg": "myImsOrg",
  "sandbox": {
    "id": "068abf40-575e-11ea-8512-9b1bfdb82603",
    "name": "prod"
  },
  "channel": "email",
  "eventType": "message.feedback",
  "messageExecution": {
    "messageExecutionID": "HUMA-26362805",
    "messageType": "transactional",
    "campaignID": "16f24a15-7e21-477c-848a-d5695ca7f137",
    "campaignVersionID": "2ca10c10-56dd-4505-87cd-fa5da84e7a5d"
  },
  "messageDeliveryFeedback": {
    "feedbackStatus": {
      "value": "bounce"
    },
    "offers": null,
    "messageExclusion": null,
    "messageFailure": {
      "category": "sync",
      "type": "Ignored",
      "code": "25",
      "reason": "Admin Failure"
    },
    "retryCount": 0
  },
  "identityMap": {
    "email": [
      {
        "id": "john.doe@luma.com",
        "primary": true
      }
    ]
  }
}
```

O webhook pode capturar os seguintes eventos:

* Enviado
* Entregue
* Rejeição (veja o exemplo acima)
* Erros

Cada solicitação recebida também inclui uma requestId exclusiva enviada de volta para o webhook.

## Próximas etapas {#next}

Depois que um webhook de feedback for criado, você poderá habilitá-lo ao configurar um público da **campanha** acionada pela API transacional. Saiba mais nesta seção: [Habilitar webhooks](../campaigns/api-triggered-campaign-audience.md#webhook)
