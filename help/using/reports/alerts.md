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
source-git-commit: 6386a5ee5a0d1f221beab67f43636c599531736a
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 4%

---

# Introdução a alertas {#alerts}

O Journey Optimizer aproveita os recursos de alerta do Adobe Experience Platform. Isso permite que você acesse alertas do sistema por meio da interface. Você pode visualizar os alertas disponíveis e assiná-los.

Quando um determinado conjunto de condições em suas operações é atingido (como um problema em potencial quando o sistema ultrapassa um limite), as mensagens de alerta são entregues a todos os usuários em sua organização que se subscreveram a elas.

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

Saiba mais sobre alertas no Adobe Experience Platform [documentação](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=pt-BR).

Para saber como assinar alertas e configurá-los, consulte este [página](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html).

>[!AVAILABILITY]
>
>Algumas alterações de design estão em andamento para o alerta &quot;Acionador de leitura de público-alvo sem sucesso&quot;, portanto, esse alerta está pausado por enquanto e foi removido temporariamente da interface do usuário. Quando essas alterações forem liberadas, o alerta será exibido novamente e você poderá assinar.

No menu esquerdo, em **Administração**, clique em **Alertas**. Um alerta pré-configurado para o Journey Optimizer está disponível. Esse alerta avisa se uma ação personalizada falhar. Consideramos que houve uma falha em que mais de 1% dos erros ocorreram em uma ação personalizada específica nos últimos 5 minutos. Isso é avaliado a cada 30 segundos.

![](assets/alerts-custom-action.png)


<!--A pre-configured alert for Journey Optimizer is available. This alert will warn you if a read segment node has not processed any profile during the defined time frame.

![](assets/alerts1.png)-->

Se ocorrer um comportamento inesperado, uma notificação de alerta será enviada aos assinantes do alerta por email ou diretamente no Journey Optimizer, no canto superior direito da interface, com base nas preferências do usuário.

Quando um alerta é resolvido, você recebe uma notificação &quot;Resolvido&quot;. Para o alerta de ação personalizada, isso pode acontecer por dois motivos:
* Nos últimos 5 minutos, não houve erro nessa ação personalizada (ou erros abaixo do limite de 1%).
* Nenhum perfil alcançou a ação personalizada.

Quando [exibição de regras de alerta na interface do usuário do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html), você pode assinar cada regra individualmente. Ao assinar alertas por meio do [Notificações de Eventos de E/S](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html)No entanto, as regras de alerta são organizadas em diferentes pacotes de assinatura. O nome de inscrição do evento de E/S correspondente ao alerta de ação personalizada é: &quot;Falha na ação personalizada de Jornada&quot;.

<!--The I/O event subscription name corresponding to the Read segment alert is: "Journey read segment Delays, Failures and Errors".-->

>[!WARNING]
>
>Esses alertas se aplicam somente a jornadas ativas. Os alertas não serão disparados para jornadas em modo de teste.

