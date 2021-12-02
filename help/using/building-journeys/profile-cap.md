---
title: Tampa do perfil
description: Tampa do perfil
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 496c7666-a133-4aeb-be8e-c37b3b9bf5f9
hide: true
hidefromtoc: true
source-git-commit: b5ce2ea81d4091b4fa9c09e83573f9043c5e55a8
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 2%

---


# Estabelecer sua reputação como remetente

Se você mudou recentemente para outro provedor de serviços de email, endereço IP ou domínio de email ou subdomínio, é necessário estabelecer sua reputação como remetente. Caso contrário, seus deliveries poderão ser bloqueados ou movidos para a pasta de spam da caixa de correio dos recipients.

Para aquecer o IP, você pode aumentar gradualmente o número de deliveries. Veja isso [caso de uso](../building-journeys/ramp-up-deliveries-uc.md).

## Tipo de condição de limite de perfil {#profile_cap}

Outros tipos de condição são detalhados nesta seção [seção](../building-journeys/condition-activity.md).

Use esse tipo de condição para definir um número máximo de perfis para um caminho de jornada. Quando esse limite é atingido, os perfis de entrada assumem um caminho alternativo.

Você pode usar esse tipo de condição para aumentar o volume de seus deliveries. Veja isso [caso de uso](../building-journeys/ramp-up-deliveries-uc.md).

O limite padrão é 1000. Você pode definir um valor inteiro de 1 a 20.000.

O contador se aplica somente à versão do jornada selecionada. O contador é redefinido para zero após um mês. Após uma redefinição, os perfis de entrada seguem o caminho nominal novamente até que o limite do contador seja atingido.

O caminho nominal sempre tem prioridade sobre o caminho alternativo, mesmo se você mover o caminho alternativo acima do caminho nominal na tela de jornada.

![](../assets/profile-cap-condition.png)

## Caso de uso: aumentar seus deliveries

Se você mudou recentemente para outro provedor de serviços de email, endereço IP ou domínio de email ou subdomínio, é necessário estabelecer sua reputação como remetente. Caso contrário, seus deliveries poderão ser bloqueados ou movidos para a pasta de spam da caixa de correio dos recipients. Saiba como aumentar sua reputação de email com o aquecimento de IP no [Guia de práticas recomendadas de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html){target=&quot;_blank&quot;}.

Para aquecer o IP, você pode aumentar gradualmente o número de deliveries. Leia mais sobre [otimização da capacidade de entrega no Journey Optimizer](../deliverability.md).

A finalidade desse caso de uso é criar uma jornada para aumentar seus deliveries de email. Para configurar essa jornada, siga estas etapas:

1. Criar uma jornada. [Leia mais](../building-journeys/journey-gs.md).

1. Adicione um **[!UICONTROL Condition]** para a jornada. [Leia mais](../building-journeys/condition-activity.md).

1. No **[!UICONTROL Condition]** configurações de atividade, defina o número máximo de recipients para seu delivery:

   1. No **[!UICONTROL Condition]** configurações da atividade, defina a variável **[!UICONTROL Type]** campo para **[!UICONTROL Profile cap]**. [Leia mais](profile-cap.md#profile_cap).

   1. Defina as **[!UICONTROL Limit]** para o número máximo de recipients para esse delivery.

   ![](../assets/profile-cap-condition.png)

   Você pode aumentar gradualmente esse limite até o número total de assinantes.

1. Adicione um **[!UICONTROL Message]** atividade para o caminho nominal após a **[!UICONTROL Condition]** atividade .

   ![](../assets/ramp-up-deliveries-message.png)

   Quando a jornada é executada, a mensagem é enviada para os perfis de entrada, até o número máximo de perfis que você especificou. Quando esse limite é atingido, os perfis de entrada seguem o caminho alternativo.

1. Complete a jornada com as atividades de sua escolha.

Após o aquecimento do IP, você pode remover essa condição.

