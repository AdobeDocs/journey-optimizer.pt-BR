---
solution: Journey Optimizer
product: journey optimizer
title: Alertas
description: Saiba como gerenciar alertas
feature: Alerts
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 6%

---

# Introdução aos alertas {#alerts}

O Journey Optimizer aproveita os recursos de alerta do Adobe Experience Platform. Isso permite que você acesse alertas do sistema por meio da interface do usuário. Você pode visualizar os alertas disponíveis e assiná-los. Quando um determinado conjunto de condições em suas operações é atingido (como um possível problema quando o sistema viola um limite), as mensagens de alerta são enviadas a todos os usuários em sua organização que se inscreveram neles. Essas mensagens podem se repetir em um intervalo de tempo predefinido até que o alerta seja resolvido.

Saiba mais sobre alertas no Adobe Experience Platform [documentação](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=pt-BR).
Para saber como se inscrever em alertas e configurá-los, consulte esta seção [página](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html).

No menu esquerdo, em **Administração**, clique em **Alertas**. Um alerta pré-configurado para Journey Optimizer está disponível. Esse alerta avisará se um nó de segmento de leitura não processou nenhum perfil durante o período de tempo definido.

![](assets/alerts1.png)

Se tal comportamento inesperado ocorrer, uma notificação de alerta será enviada aos assinantes do alerta por email e por notificação no aplicativo, no canto superior direito da interface.

![](assets/alerts2.png)

When [exibição de regras de alerta na interface do usuário da plataforma](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html), é possível assinar cada regra individualmente. Ao assinar alertas por meio de [Notificações de Evento de E/S](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html), no entanto, as regras de alerta são organizadas em pacotes de assinatura diferentes. O nome da assinatura do evento de E/S correspondente ao alerta de segmento Lido é: &quot;Jornada atrasos, falhas e erros do segmento de leitura&quot;.

>[!WARNING]
>
>Esses alertas se aplicam apenas às jornadas ativas. Os alertas não serão acionados para jornadas no modo de teste.