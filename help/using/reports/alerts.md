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
source-git-commit: 731eb471c5765b0d3efbc9354c64c32cc5e56516
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 8%

---

# Introdução aos alertas {#alerts}

O Journey Optimizer aproveita os recursos de alerta do Adobe Experience Platform. Isso permite que você acesse alertas do sistema por meio da interface do usuário. Você pode visualizar os alertas disponíveis e assiná-los. Quando um determinado conjunto de condições em suas operações é atingido (como um possível problema quando o sistema viola um limite), as mensagens de alerta são enviadas a todos os usuários em sua organização que se inscreveram neles. Essas mensagens podem se repetir em um intervalo de tempo predefinido até que o alerta seja resolvido.

Saiba mais sobre alertas no Adobe Experience Platform [documentação](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=pt-BR).
Para saber como se inscrever em alertas e configurá-los, consulte esta seção [página](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html).

No menu esquerdo, em **Administração**, clique em **Alertas**.

<!--A pre-configured alert for Journey Optimizer is available. This alert will warn you if a read segment node has not processed any profile during the defined time frame.

![](assets/alerts1.png)-->

Se tal comportamento inesperado ocorrer, uma notificação de alerta será enviada aos assinantes do alerta por email, no canto superior direito da interface.

<!--![](assets/alerts2.png)-->

When [exibição de regras de alerta na interface do usuário do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html), é possível assinar cada regra individualmente. Ao assinar alertas por meio de [Notificações de Evento de E/S](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html), no entanto, as regras de alerta são organizadas em pacotes de assinatura diferentes.

<!--The I/O event subscription name corresponding to the Read segment alert is: "Journey read segment Delays, Failures and Errors".

>[!WARNING]
>
>These alerts apply only to live journeys. Alerts will not be triggered for journeys in test mode.-->
