---
title: Casos de uso da página de aterrissagem
description: Descubra os casos de uso mais comuns com landing pages no Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Intermediate
hidefromtoc: true
hide: true
source-git-commit: 4d564ff89a8cb6c6d76161f2e6cedf39d33e70a0
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 21%

---

# Casos de uso da página de aterrissagem

Abaixo estão exemplos de como você pode usar [!DNL Journey Optimizer] páginas de aterrissagem para que seus clientes optem por receber algumas ou todas as suas comunicações.

<!--The main use cases are:
* Subscription to a service
* Opt-in
* Opt-out-->

## Assinatura de um serviço {#subscription-to-a-service}

As principais etapas para fazer com que seus recipients assinem um serviço são apresentadas abaixo.

![](../assets/lp_subscription-uc.png)

Por exemplo, digamos que você organize um evento no próximo mês e deseje iniciar uma campanha de registro de evento para manter seus clientes interessados atualizados sobre ele.

1. Crie a lista de subscrição do registro de eventos. Saiba mais sobre [listas de assinaturas](subscription-list.md)

1. [Criar uma landing page](create-lp.md), que permitirá que seus recipients se registrem no seu evento.

1. Configure e projete a landing page de registro, incluindo o link para a lista de assinaturas. Saiba mais sobre a criação da variável [página de aterrissagem primária](create-lp.md#configure-primary-page)

1. Crie uma página de agradecimento que será exibida aos recipients depois que eles enviarem o formulário de registro. Saiba mais sobre [subpáginas de aterrissagem](create-lp.md#configure-subpages)

1. Criar uma mensagem de email. Saiba mais sobre [criação de mensagens](../create-message.md)

1. [Inserir um link](../message-tracking.md#insert-links) na sua mensagem. Selecionar **[!UICONTROL Landing page]** como **[!UICONTROL Link type]** e escolha a [página de aterrissagem](create-lp.md#configure-primary-page) que você criou para registro.

   ![](../assets/lp_subscription-uc-link.png)

1. Salve o conteúdo e [publique a mensagem](../publish-manage-message.md).

1. Envie sua mensagem por meio de um [jornada](../building-journeys/journey.md) o para anunciar o registro agora está aberto para o seu evento e para direcionar o tráfego para a página de aterrissagem do registro.

   Depois que eles receberem o email, se seus recipients clicarem no link para a landing page, eles serão direcionados para a página de agradecimento e serão adicionados à lista de assinaturas.

1. Você pode enviar um email de confirmação para os recipients que se registraram para o seu evento. Para fazer isso, envie-o por outra jornada usando o **[!UICONTROL Segment qualification]** e selecione a lista de assinaturas criada como o segmento.

<!--The event registration's subscription list tracks the profiles who registered and you can send them targeted event updates.-->

## Recusar {#opt-out}

Para permitir que seus recipients cancelem a assinatura de suas comunicações, você pode incluir um link para uma landing page de opt out em seus emails.

Saiba mais sobre como gerenciar o consentimento dos recipients e por que isso é importante em [esta seção](../consent.md).

### Gerenciamento de recusa {#opt-out-management}

Oferecer a capacidade de cancelar a assinatura dos recipients ao receberem comunicações de uma marca é um requisito legal. Saiba mais sobre a legislação aplicável no [Documentação do Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html#regulations){target=&quot;_blank&quot;}.

Portanto, você sempre deve incluir um **link para cancelar a inscrição** em cada email enviado aos recipients:

* Ao clicar nesse link, os recipients serão direcionados a uma página de aterrissagem que inclui um botão para confirmar a recusa.
* Ao clicar no botão recusar, os dados do perfil serão atualizados com essas informações.

### Configurar recusa {#configure-opt-out}

Para permitir que os recipients de uma mensagem cancelem a assinatura de suas comunicações por meio de uma landing page, siga as etapas abaixo.

1. Crie seu [página de aterrissagem](create-lp.md). Usar a página de aterrissagem específica **[!UICONTROL Form]** , defina um **[!UICONTROL Opt-out]** e escolha atualizar **[!UICONTROL Channel (email)]**: o perfil que marcar a caixa de opção de não participação na página de aterrissagem será rejeitado em todas as suas comunicações. [Saiba mais](design-lp.md)

   <!--You can also build your own landing page and host it on the third-party system of your choice. To keep?-->

1. [Criar uma mensagem](../create-message.md) no [!DNL Journey Optimizer].

1. Selecione o texto no seu conteúdo e [inserir um link](../message-tracking.md#insert-links) usando a barra de ferramentas contextual. Você também pode usar um link em um botão.

   ![](../assets/lp_opt-out-insert-link.png)

1. Selecione o **[!UICONTROL Landing page]** na lista suspensa **[!UICONTROL Link type]**.

1. Selecione o [página de aterrissagem](create-lp.md#configure-primary-page) que você criou para rejeitar.

   ![](../assets/lp_opt-out-landing-page.png)

1. Clique em **[!UICONTROL Save]**.

1. Salve o conteúdo e [publique a mensagem](../publish-manage-message.md).

1. Envie sua mensagem por meio de um [jornada](../building-journeys/journey.md).

1. Depois que a mensagem for recebida, se o recipient clicar no link de cancelamento de inscrição, a página de aterrissagem será exibida.

   <!--![](../assets/lp_opt-out-lp-example.png)-->

1. Se o recipient clicar no link de recusa na landing page, os dados do perfil serão atualizados e não receberão comunicações da sua marca, a menos que tenham feito assinatura novamente.

   <!--The opted-out recipient is then redirected to a confirmation message screen indicating that opting out was successful.-->

   <!--![](../assets/lp_opt-out-confirmation-example.png)-->

Para verificar se a escolha do perfil correspondente foi atualizada, acesse a Experience Platform e o perfil selecionando um namespace de identidade e um valor de identidade correspondente. Saiba mais na [Documentação do Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target=&quot;_blank&quot;}.

![](../assets/lp_opt-out-profile-choice.png)

Na guia **[!UICONTROL Attributes]**, é possível ver que o valor de **[!UICONTROL choice]** foi alterado para **[!UICONTROL no]**.

<!--

### Other ways to opt out

You can also enable your recipients to unsubscribe whithout using landing pages.

* **One-click opt-out**

    You can add a one-click opt-out link into your email content. This will enable your recipients to quickly unsubscribe from your communications, without being redirected to a landing page where they need to confirm opting out. [Learn more](../message-tracking.md#one-click-opt-out-link)

* **Unsubscribe link in header**

    If the recipients' email client supports displaying an unsubscribe link in the email header, emails sent with [!DNL Journey Optimizer] automatically include this link. [Learn more](../consent.md#unsubscribe-email)
-->