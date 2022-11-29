---
solution: Journey Optimizer
product: journey optimizer
title: Adicionar uma mensagem em uma jornada
description: Saiba como adicionar uma mensagem em uma jornada
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 0b19af568b33d29f4b35deeab6def17919cfe824
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 20%

---

# Email, SMS, Push{#add-a-message-in-a-journey}

[!DNL Journey Optimizer] O vem com recursos de mensagem integrados. Você pode simplesmente adicionar, em sua jornada, uma atividade de push, SMS ou mensagem de email e [definir configurações e conteúdo](../messages/messages-in-journeys.md). Em seguida, é executado e enviado no contexto da jornada.

Você também pode configurar ações específicas para enviar mensagens:

* Se você estiver usando um sistema de terceiros para enviar mensagens, é possível criar uma ação personalizada. Saiba mais nesta [seção](../action/action.md).

* Se estiver trabalhando com o Campaign e o Journey Optimizer, consulte estas seções:

   * [[!DNL Journey Optimizer] e Campaign Classic v7/Campaign v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] e Campaign Standard](../action/acs-action.md)

Para adicionar uma mensagem em uma jornada, siga as etapas abaixo:

1. Inicie a jornada com uma atividade de [Evento](general-events.md) ou [Segmento de leitura](read-segment.md).

1. Na seção **Ações** da paleta, arraste e solte na tela uma atividade de **email**, **SMS** ou **push**.

   ![](../messages/assets/add-a-message.png)


   Todas as etapas para configurar a mensagem e definir seu conteúdo são detalhadas em [esta seção](../messages/get-started-content.md).

## Atualizar conteúdo ao vivo{#update-live-content}

Você pode atualizar o conteúdo de uma mensagem (email, sms, push) em uma jornada ao vivo.

Para fazer isso, abra a jornada ao vivo, selecione a atividade de mensagem e clique em **Editar conteúdo**.

![](assets/add-a-message2.png)

No entanto, não é possível alterar os atributos usados na personalização, sejam eles atributos de perfil ou dados contextuais (das propriedades de evento ou jornada).
