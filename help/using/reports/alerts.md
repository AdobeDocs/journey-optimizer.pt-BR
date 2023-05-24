---
solution: Journey Optimizer
product: journey optimizer
title: Alertas
description: Saiba como gerenciar alertas
feature: Alerts
topic: Administration
role: Admin
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: 1832f3395b07580e62f32c886a0a4256267b2970
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 6%

---

# Introdução a alertas {#alerts}

O Journey Optimizer aproveita os recursos de alerta do Adobe Experience Platform. Isso permite que você acesse alertas do sistema por meio da interface. Você pode visualizar os alertas disponíveis e assiná-los.

Quando um determinado conjunto de condições em suas operações é atingido (como um problema em potencial quando o sistema ultrapassa um limite), as mensagens de alerta são entregues a todos os usuários em sua organização que se subscreveram a elas. Essas mensagens podem se repetir em um intervalo predefinido até que o alerta seja resolvido.

Saiba mais sobre alertas no Adobe Experience Platform [documentação](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=pt-BR).
Para saber como assinar alertas e configurá-los, consulte este [página](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html).

>[!AVAILABILITY]
>
>Algumas alterações de design estão em andamento para o alerta &quot;Acionador de segmento de leitura malsucedido&quot;, portanto, esse alerta está pausado por enquanto e foi removido temporariamente da interface do usuário. Quando essas alterações forem liberadas, o alerta será exibido novamente e você poderá assinar.

No menu esquerdo, em **Administração**, clique em **Alertas**.

<!--A pre-configured alert for Journey Optimizer is available. This alert will warn you if a read segment node has not processed any profile during the defined time frame.

![](assets/alerts1.png)-->

Se ocorrer um comportamento inesperado, uma notificação de alerta será enviada aos assinantes do alerta por email, no canto superior direito da interface.

<!--![](assets/alerts2.png)-->


Quando [exibição de regras de alerta na interface do usuário do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html), você pode assinar cada regra individualmente. Ao assinar alertas por meio do [Notificações de Eventos de E/S](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html)No entanto, as regras de alerta são organizadas em diferentes pacotes de assinatura.

<!--The I/O event subscription name corresponding to the Read segment alert is: "Journey read segment Delays, Failures and Errors".

>[!WARNING]
>
>These alerts apply only to live journeys. Alerts will not be triggered for journeys in test mode.-->
