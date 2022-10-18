---
solution: Journey Optimizer
product: journey optimizer
title: Aumente suas entregas
description: Saiba como aumentar suas entregas
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 83d1b68d-011a-4109-b5f0-6ca1ade2944d
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 3%

---

# Caso de uso: aumentar seus deliveries{#use-case-ramp-up-your-deliveries}

Se você mudou recentemente para outro provedor de serviços de email, endereço IP ou domínio de email ou subdomínio, é necessário estabelecer sua reputação como remetente. Caso contrário, seus deliveries poderão ser bloqueados ou movidos para a pasta de spam da caixa de correio dos recipients. Saiba como aumentar sua reputação de email com o aquecimento de IP no [Guia de práticas recomendadas de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html){target=&quot;_blank&quot;}.

Para aquecer o IP, você pode aumentar gradualmente o número de deliveries. Leia mais sobre [otimização da capacidade de entrega no Journey Optimizer](../reports/deliverability.md).

A finalidade desse caso de uso é criar uma jornada para aumentar seus deliveries de email. Para configurar essa jornada, siga estas etapas:

1. Criar uma jornada. [Leia mais](journey-gs.md).

1. Adicione um **[!UICONTROL Condição]** para a jornada. [Leia mais](condition-activity.md).

1. No **[!UICONTROL Condição]** configurações de atividade, defina o número máximo de recipients para seu delivery:

   1. No **[!UICONTROL Condição]** configurações da atividade, defina a variável **[!UICONTROL Tipo]** campo para **[!UICONTROL Tampa do perfil]**. [Leia mais](condition-activity.md#profile_cap).

   1. Defina as **[!UICONTROL Limite]** para o número máximo de recipients para esse delivery.

   ![](assets/profile-cap-condition.png)

   Você pode aumentar gradualmente esse limite até o número total de assinantes.

1. Adicione um **[!UICONTROL Email]** atividade de ação para o caminho nominal após a **[!UICONTROL Condição]** atividade .

   ![](assets/ramp-up-deliveries-message.png)

   Quando a jornada é executada, a mensagem é enviada para os perfis de entrada, até o número máximo de perfis que você especificou. Quando esse limite é atingido, os perfis de entrada seguem o caminho alternativo.

1. Complete a jornada com as atividades de sua escolha.

Após o aquecimento do IP, você pode remover essa condição.
