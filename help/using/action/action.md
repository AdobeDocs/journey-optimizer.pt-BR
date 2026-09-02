---
solution: Journey Optimizer
product: journey optimizer
title: Introdução a ações
description: Saiba como trabalhar com ações
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Developer, Admin
level: Experienced
keywords: ações, jornada, mensagens, envio, conexões
exl-id: 7f0cda1d-daf0-4d4c-9978-ddef81473813
TQID: https://experienceleague.adobe.com/u-fLClLKK9cC7D2BwO5vxdW11tywPDRWzOMBtYUj5Ts
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
  - id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 62bc5f833b5612570ba50c98519a2f9c07d0bd5e
workflow-type: tm+mt
source-wordcount: 397
ht-degree: 35%

---

# Introdução a ações personalizadas {#about_actions}

>[!BEGINSHADEBOX]

**Nesta página:** Entenda como as ações e as ações personalizadas permitem fornecer experiências personalizadas e conectar sistemas de terceiros por meio de chamadas de API REST, para que você possa estender as jornadas além das mensagens integradas.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_action_list"
>title="Ações personalizadas"
>abstract="As ações são conexões através das quais você fornece experiências personalizadas em tempo real para clientes, como notificações por push, email, SMS ou qualquer outro meio de engajamento digital usado em sua empresa."

As ações são conexões através das quais você fornece experiências personalizadas em tempo real para clientes, como notificações por push, email, SMS ou qualquer outro meio de engajamento digital usado em sua empresa.

➡️ [Conheça este recurso no vídeo](#video)

[!DNL Journey Optimizer] vem com o recurso de mensagem interno. As ações personalizadas permitem configurar a conexão de um sistema de terceiros para enviar mensagens ou chamadas de API. Uma ação pode ser configurada com qualquer serviço de qualquer provedor que possa ser chamado por meio de uma REST API com conteúdo formatado em JSON.

* Se você estiver usando o Adobe Campaign v7 ou v8, uma integração estará disponível mediante solicitação. Consulte [esta página](../action/acc-action.md).

* Se você estiver usando um sistema de terceiros para enviar mensagens como Epsilon, Facebook, Adobe Developer, Firebase etc., será necessário criar e configurar uma ação personalizada. Consulte [esta página](../action/about-custom-action-configuration.md).

>[!CAUTION]
>
>A configuração de ações personalizadas deve ser executada por um **usuário técnico**.

As ações personalizadas são ações adicionais definidas por usuários técnicos e disponibilizadas aos profissionais de marketing: uma vez configuradas, elas são exibidas na paleta esquerda da sua jornada, na categoria **[!UICONTROL Ação]**. Saiba mais [nesta página](../building-journeys/about-journey-activities.md#action-activities).

Para exibir a lista de ações ou configurar uma nova ação, selecione **[!UICONTROL Configurações]** na seção de menu ADMINISTRAÇÃO. Na seção **[!UICONTROL Ações]**, clique em **[!UICONTROL Gerenciar]**. A lista de ações é exibida. Consulte [esta página](../start/user-interface.md) para obter mais informações sobre a interface.

![](assets/custom1.png)

Saiba como solucionar problemas de uma ação personalizada [nesta página dedicada](../action/troubleshoot-custom-action.md).

## Vídeo tutorial {#video}

Saiba como configurar ações personalizadas.

>[!VIDEO](https://video.tv.adobe.com/v/3428396?quality=12)

## Recursos adicionais

Navegue pelas seções abaixo para saber mais sobre como configurar e usar suas ações personalizadas:

* [Configurar ações personalizadas](../action/about-custom-action-configuration.md) - Saiba como criar e configurar uma ação personalizada
* [Usar ações personalizadas](../building-journeys/using-custom-actions.md) - Saiba como usar ações personalizadas em suas jornadas
* [Envio de coleções em parâmetros de ação personalizados](../building-journeys/collections.md) - Saiba como enviar uma coleção em parâmetros de ação personalizados que é preenchida dinamicamente no tempo de execução
* [Solução de problemas de ação personalizada](../action/troubleshoot-custom-action.md) - Saiba como solucionar problemas de uma ação personalizada

