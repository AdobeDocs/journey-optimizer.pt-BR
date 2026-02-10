---
solution: Journey Optimizer
product: journey optimizer
title: Enviar dados para o AEP
description: Saiba como enviar dados para o AEP
feature: Journeys, Use Cases
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
keywords: jornada, caso de uso
version: Journey Orchestration
source-git-commit: 70653bafbbe8f1ece409e3005256d9dff035b518
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 2%

---

# Caso de uso: criar uma ação personalizada para enviar dados a [!DNL Adobe Experience Platform]{#send-data-to-aep}

Se você migrou recentemente para outro provedor de serviços de email, endereço IP ou domínio ou subdomínio de email, estabeleça sua reputação como remetente. Caso contrário, os deliveries podem ser bloqueados ou movidos para as pastas de spam dos recipients. Para obter orientação, consulte o [Manual de práticas recomendadas de capacidade de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=pt-BR){target="_blank"}.

Para aquecer seu IP, você pode aumentar gradualmente o número de deliveries. Leia mais sobre [otimização da entrega no Journey Optimizer](../reports/deliverability.md).

O objetivo deste caso de uso é criar uma jornada para incrementar suas entregas de email. Para configurar essa jornada, siga estas etapas:

1. Criar uma jornada. [Leia mais](journey-gs.md).

1. Adicione uma atividade **[!UICONTROL Condition]** à jornada. [Leia mais](condition-activity.md).

1. Nas configurações da atividade **[!UICONTROL Condição]**, defina o número máximo de destinatários para sua entrega:

   1. Nas configurações de atividade de **[!UICONTROL Condição]**, defina o campo **[!UICONTROL Tipo]** como **[!UICONTROL Limite de perfis]**. [Leia mais](condition-activity.md#profile_cap).

   1. Defina o campo **[!UICONTROL Limit]** para o número máximo de destinatários desta entrega.

   ![Condição de limite de perfil para controlar o volume de execução da ação personalizada](assets/profile-cap-condition.png)

   É possível aumentar gradualmente esse limite até o número total de assinantes.

1. Adicione uma atividade de ação **[!UICONTROL Email]** ao caminho nominal após a atividade **[!UICONTROL Condição]**.

   ![Jornada com ação personalizada para enviar dados ao sistema externo](assets/ramp-up-deliveries-message.png)

   Quando a jornada for executada, a mensagem será enviada para os perfis de entrada, até o número máximo de perfis especificado. Quando esse limite é atingido, os perfis que entram pegam o caminho alternativo.

1. Conclua a jornada com as atividades de sua escolha.

Após o aquecimento do IP, é possível remover essa condição.
