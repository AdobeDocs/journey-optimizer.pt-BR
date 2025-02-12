---
solution: Journey Optimizer
product: journey optimizer
title: Adicionar uma ação de canal interna a uma jornada
description: Saiba como adicionar uma ação de canal integrada a uma jornada
feature: Journeys, Activities, Channels Activity
topic: Content Management
role: User
level: Intermediate
keywords: jornada, mensagem, push, sms, email, no aplicativo, web, cartão de conteúdo, experiência baseada em código
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 56a1ef1ba256d1aac3593d8a61e67bdc42c17d32
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 27%

---

# Usar ações de canal integradas {#add-a-message-in-a-journey}

>[!CONTEXTUALHELP]
>id="ajo_message_activity"
>title="Ação de canal integrada"
>abstract="O Journey Optimizer inclui recursos de ação de canal integrada. Você pode simplesmente adicionar à sua jornada uma atividade de saída (email, mensagem de texto (SMS/MMS), push) ou de entrada (no aplicativo, web, experiência baseada em código, cartão de conteúdo) e definir as configurações e o conteúdo. Em seguida, ela é executada e enviada no contexto da jornada."

O [!DNL Journey Optimizer] vem com recursos de ação de canal incorporados. Você pode simplesmente adicionar à sua jornada uma atividade de saída (email, mensagem de texto (SMS/MMS), push) ou de entrada (no aplicativo, web, experiência baseada em código, cartão de conteúdo) e definir as configurações e o conteúdo. Em seguida, ela é executada e enviada no contexto da jornada.

>[!NOTE]
>
>Você também pode configurar ações específicas para enviar mensagens para você. [Saiba mais](#recommendation)

Para adicionar uma ação de canal integrada a uma jornada, siga as etapas abaixo.

1. Inicie sua jornada com uma atividade [Evento](general-events.md) ou [Ler público](read-audience.md).

1. Na seção **Ações** da paleta, arraste e solte na tela uma atividade de saída (**email**, **push**, **SMS**) ou de entrada (**No aplicativo**, **Web**, **experiência baseada em código**, **cartão de conteúdo**).

   ![](assets/journey-web-activity.png)

1. Configure sua atividade.

   * Saiba mais sobre as etapas detalhadas para criar o conteúdo da mensagem da seguinte maneira:

     <table style="table-layout:fixed">
      <tr style="border: 0;">
      <td>
      <a href="../email/create-email.md">
      <img alt="Lead" src="../assets/do-not-localize/email.jpg">
      </a>
      <div><a href="../email/create-email.md"><strong>Criar emails</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../push/create-push.md">
      <img alt="Pouco frequente" src="../assets/do-not-localize/push.jpg">
      </a>
      <div>
      <a href="../push/create-push.md"><strong>Criar notificações por push<strong></a>
      </div>
      <p>
      </td>
      <td>
      <a href="../sms/create-sms.md">
      <img alt="Validação" src="../assets/do-not-localize/sms.jpg">
      </a>
      <div>
      <a href="../sms/create-sms.md"><strong>Criar mensagens de texto (SMS/MMS)</strong></a>
      </div>
      <p>
      </td>
      </tr>
      </table>

     >[!NOTE]
     >
     >Para emails e notificações por push, é possível ativar a Otimização de tempo de envio. [Saiba mais](send-time-optimization.md)

   * Saiba mais sobre as etapas detalhadas para criar sua ação de entrada da seguinte maneira:

     <table style="table-layout:fixed">
      <tr style="border: 0;">
      <td>
      <a href="../in-app/create-in-app.md">
      <img alt="Lead" src="../assets/do-not-localize/in-app.jpg">
      </a>
      <div><a href="../in-app/create-in-app.md"><strong>Criar mensagens no aplicativo</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../web/create-web.md">
      <img alt="Lead" src="../assets/do-not-localize/web-create.jpg">
      </a>
      <div><a href="../web/create-web.md"><strong>Criar experiências da Web</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../content-card/create-content-card.md">
      <img alt="Lead" src="../assets/do-not-localize/sms-config.jpg">
      </a>
      <div><a href="../content-card/create-content-card.md"><strong>Criar cartões de conteúdo</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../code-based/create-code-based.md">
      <img alt="Pouco frequente" src="../assets/do-not-localize/web-design.jpg">
      </a>
      <div>
      <a href="../code-based/create-code-based.md"><strong>Criar experiências baseadas em código<strong></a>
      </div>
      <p>
      </td>
      </tr>
      </table>

     >[!NOTE]
     >
     >Cada atividade de mensagem de entrada vem com uma atividade de 3 dias **Aguardar**. [Saiba mais](wait-activity.md#auto-wait-node)


## Atualizar conteúdo ao vivo {#update-live-content}

Você pode atualizar o conteúdo de uma ação de canal integrada em uma jornada em tempo real.

Para fazer isso, abra a jornada em tempo real, selecione a atividade de canal e clique em **Editar conteúdo**.

![](assets/add-a-message2.png)

No entanto, não é possível alterar os atributos usados na personalização, sejam eles atributos de perfil ou dados contextuais (de propriedades de evento ou jornada).

Se você modificou dados contextuais, a seguinte mensagem de erro será exibida: `ERR_AUTHORING_JOURNEYVERSION_201`

Se você modificou atributos de perfil, a seguinte mensagem de erro será exibida: `ERR_AUTHORING_JOURNEYVERSION_202`

Observe que, para a atividade no aplicativo, qualquer alteração pode ser feita no conteúdo enquanto a jornada está ativa, mas os acionadores no aplicativo não podem ser modificados.

## Enviar com ações personalizadas {#recommendation}

Em vez de usar os recursos de mensagem incorporados, você pode usar ações personalizadas para configurar a conexão de um sistema de terceiros para enviar mensagens ou chamadas de API.

* Se você estiver usando um sistema de terceiros para enviar mensagens, poderá criar uma ação personalizada. [Saiba mais](../action/action.md)

* Se estiver trabalhando com o Adobe Campaign, consulte estas seções:

   * [[!DNL Journey Optimizer] e o Campaign v7/v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] e Campaign Standard](../action/acs-action.md)