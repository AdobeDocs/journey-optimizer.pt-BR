---
solution: Journey Optimizer
product: journey optimizer
title: Enviar dados para a AEP
description: Saiba como enviar dados para a AEP
feature: Journeys, Use Cases
topic: Content Management
role: User, Data Engineer
level: Intermediate, Experienced
keywords: jornada, caso de uso
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 2%

---

# Caso de uso: criar uma ação personalizada para enviar dados ao Adobe Experience Platform{#send-data-to-aep}

Se você mudou recentemente para outro provedor de serviços de email, endereço IP, domínio de email ou subdomínio, é necessário estabelecer sua reputação como remetente. Caso contrário, seus deliveries poderão ser bloqueados ou movidos para a pasta de spam da caixa de correio dos recipients. Saiba como aumentar sua reputação de email com o aquecimento de IP no [Guia de práticas recomendadas de capacidade de delivery](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=pt-BR){target="_blank"}.

Para aquecer seu IP, você pode aumentar gradualmente o número de deliveries. Leia mais sobre [otimização da capacidade de entrega no Journey Optimizer](../reports/deliverability.md).

O objetivo deste caso de uso é criar uma jornada para incrementar suas entregas de email. Para configurar essa jornada, siga estas etapas:

1. Criar uma jornada. [Leia mais](journey-gs.md).

1. Adicionar um **[!UICONTROL Condição]** atividade para a jornada. [Leia mais](condition-activity.md).

1. No **[!UICONTROL Condição]** configurações da atividade, defina o número máximo de recipients para seu delivery:

   1. No **[!UICONTROL Condição]** configurações de atividade, defina o **[!UICONTROL Tipo]** campo para **[!UICONTROL Limite de perfil]**. [Leia mais](condition-activity.md#profile_cap).

   1. Defina o **[!UICONTROL Limite]** para o número máximo de recipients para esse delivery.

   ![](assets/profile-cap-condition.png)

   É possível aumentar gradualmente esse limite até o número total de assinantes.

1. Adicionar um **[!UICONTROL E-mail]** atividade de ação para o caminho nominal após o **[!UICONTROL Condição]** atividade.

   ![](assets/ramp-up-deliveries-message.png)

   Quando a jornada for executada, a mensagem será enviada para os perfis de entrada, até o número máximo de perfis especificado. Quando esse limite é atingido, os perfis que entram pegam o caminho alternativo.

1. Conclua a jornada com as atividades de sua escolha.

Após o aquecimento do IP, é possível remover essa condição.
