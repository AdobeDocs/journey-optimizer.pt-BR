---
solution: Journey Optimizer
product: journey optimizer
title: Revisar e ativar uma campanha
description: Saiba como revisar e ativar campanhas no Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: campaign, review, validation, ativating, ativating, otimizer
exl-id: 86f35987-f0b7-406e-9ae6-0e4a2e651610
source-git-commit: d93b7ce225294257f49caee6ac08cfb575611a93
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 3%

---


# Executar uma campanha acionada por API {#execute}

Depois que sua campanha for ativada, é necessário recuperar a solicitação de cURL de amostra gerada e usá-la na API para criar sua carga e acionar a campanha.

## Leitura obrigatória {#must-read}

* **Datas de início/término da campanha** - Se você tiver configurado uma data de início e/ou término específica ao criar a campanha, ela não será executada fora dessas datas, e as chamadas de API falharão.

* **Tempo limite de chamada** - A chamada para a API REST de Execução de Mensagem Interativa tem um tempo limite de 60 segundos. No entanto, tentativas internas estão em vigor no caso de tempos limite inesperados para garantir o delivery.

## Acionar a campanha {#trigger}

1. Abra a campanha e copie e cole a solicitação de carga da seção **[!UICONTROL cURL request]**. Essa carga inclui todas as variáveis de personalização (perfil e contexto) usadas na mensagem. Ele fica disponível assim que a campanha é ativada.

   ![](assets/api-triggered-curl.png)

   >[!IMPORTANT]
   >
   >Os pontos de extremidade na seção cURL diferem entre as [campanhas padrão e de alta taxa de transferência](../campaigns/api-triggered-high-throughput.md).

1. Use essa solicitação de cURL nas APIs para criar sua carga e acionar a campanha. Para obter mais informações, consulte a [documentação da API de Execução de Mensagens Interativas](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution), onde todos os pontos de extremidade para campanhas padrão e de Alta Taxa de Transferência são listados.

   Exemplos de chamadas de API também estão disponíveis em [esta página](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples/).
