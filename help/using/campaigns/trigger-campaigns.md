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
source-git-commit: 45c95d5682b35c8afb161b75c88942c010b36d1c
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 3%

---

# Executar uma campanha acionada por API {#execute}

Depois que sua campanha for ativada, é necessário recuperar a solicitação de cURL de amostra gerada e usá-la na API para criar sua carga e acionar a campanha.

1. Abra a campanha e copie e cole a solicitação de carga da seção **[!UICONTROL cURL request]**. Essa carga inclui todas as variáveis de personalização (perfil e contexto) usadas na mensagem. Ele fica disponível assim que a campanha é ativada.

   ![](assets/api-triggered-curl.png)

1. Use essa solicitação de cURL nas APIs para criar sua carga e acionar a campanha. Para obter mais informações, consulte a [documentação da API de Execução de Mensagens Interativas](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution).


   Exemplos de chamadas de API também estão disponíveis em [esta página](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples/).

   >[!NOTE]
   >
   >Se você tiver configurado uma data de início e/ou término específica ao criar a campanha, ela não será executada fora dessas datas e as chamadas de API falharão.
