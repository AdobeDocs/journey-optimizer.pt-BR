---
solution: Journey Optimizer
product: journey optimizer
title: Aumente seus deliveries
description: Saiba como incrementar suas entregas
feature: Journeys, Use Cases, IP Warmup Plans
topic: Content Management
role: User, Data Engineer
level: Intermediate, Experienced
hide: true
hidefromtoc: true
keywords: capacidade de entrega, jornada, caso de uso, email, reputação
exl-id: 83d1b68d-011a-4109-b5f0-6ca1ade2944d
source-git-commit: e34c39c02f71361277f28b1a116a54390875f93d
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 2%

---

# Caso de uso: incremente seus deliveries{#use-case-ramp-up-your-deliveries}

Se você mudou recentemente para outro provedor de serviços de email, endereço IP, domínio de email ou subdomínio, é necessário estabelecer sua reputação como remetente. Caso contrário, seus deliveries poderão ser bloqueados ou movidos para a pasta de spam da caixa de correio dos recipients. Saiba como aumentar sua reputação de email com o aquecimento de IP no [Guia de práticas recomendadas de capacidade de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=pt-BR){target="_blank"}.

Para aquecer seu IP, você pode aumentar gradualmente o número de deliveries. Leia mais sobre [otimização da entrega no Journey Optimizer](../reports/deliverability.md).

O objetivo deste caso de uso é criar uma jornada para incrementar suas entregas de email. Para configurar essa jornada, siga estas etapas:

1. Criar uma jornada. [Leia mais](journey-gs.md).

1. Adicione uma atividade **[!UICONTROL Condition]** à jornada. [Leia mais](condition-activity.md).

1. Nas configurações da atividade **[!UICONTROL Condição]**, defina o número máximo de destinatários para sua entrega:

   1. Nas configurações de atividade de **[!UICONTROL Condição]**, defina o campo **[!UICONTROL Tipo]** como **[!UICONTROL Limite de perfis]**. [Leia mais](condition-activity.md#profile_cap).

   1. Defina o campo **[!UICONTROL Limit]** para o número máximo de destinatários desta entrega.

   ![](assets/profile-cap-condition.png)

   É possível aumentar gradualmente esse limite até o número total de assinantes.

1. Adicione uma atividade de ação **[!UICONTROL Email]** ao caminho nominal após a atividade **[!UICONTROL Condição]**.

   ![](assets/ramp-up-deliveries-message.png)

   Quando a jornada for executada, a mensagem será enviada para os perfis de entrada, até o número máximo de perfis especificado. Quando esse limite é atingido, os perfis que entram pegam o caminho alternativo.

1. Conclua a jornada com as atividades de sua escolha.

Após o aquecimento do IP, é possível remover essa condição.
