---
title: Casos de uso da página de aterrissagem
description: Descubra os casos de uso mais comuns com landing pages no Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Intermediate
hidefromtoc: true
hide: true
exl-id: 8c00d783-54a3-45d9-bd8f-4dc58804d922
source-git-commit: bbc2adabac63ffb813ea2630f29aec552fc3f4df
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 19%

---

# Casos de uso da página de aterrissagem {#lp-use-cases}

Abaixo estão alguns exemplos de como você pode usar [!DNL Journey Optimizer] páginas de aterrissagem para que seus clientes optem por receber algumas ou todas as suas comunicações.

<!--The main use cases are:
* Subscription to a service
* Opt-in
* Opt-out-->

## Assinatura de um serviço {#subscription-to-a-service}

Um dos casos de uso mais comuns consiste em convidar seus clientes para [assinar um serviço](subscription-list.md) (como um boletim informativo ou um evento) por meio de uma página de aterrissagem. As principais etapas são apresentadas no gráfico abaixo:

![](../assets/lp_subscription-uc.png)

Por exemplo, digamos que você organize um evento no próximo mês e deseje iniciar uma campanha de registro de evento<!--to keep your customers that are interested updated on that event-->. Para fazer isso, você enviará um email incluindo um link para uma landing page que permitirá que seus recipients se registrem neste evento. Os usuários que se registrarem serão adicionados à lista de assinaturas criada para essa finalidade.

### Configurar landing page

1. Crie a lista de subscrição do registro de eventos, que armazenará os usuários registrados. Saiba como criar uma lista de assinaturas [here](subscription-list.md#define-subscription-list).

   ![](../assets/lp_subscription-uc-list.png)

1. [Criar uma landing page](create-lp.md) para permitir que seus recipients se registrem no seu evento.

1. Configurar o registro [página de aterrissagem primária](create-lp.md#configure-primary-page).

1. Ao projetar o [conteúdo da página de aterrissagem](design-lp.md), selecione a lista de assinaturas criada para atualizá-la com os perfis que marcam a caixa de seleção de registro.

   ![](../assets/lp_subscription-uc-lp-list.png)

1. Crie uma página de &#39;agradecimento&#39; que será exibida aos recipients depois de enviarem o formulário de registro. Saiba como configurar landing subpages [here](create-lp.md#configure-subpages).

   ![](../assets/lp_subscription-uc-thanks.png)

1. [Publicar](create-lp.md#publish) a landing page.

1. [Criar uma mensagem de email](../create-message.md) para anunciar que o registro agora está aberto para o seu evento.

1. [Inserir um link](../message-tracking.md#insert-links) no conteúdo da mensagem. Selecionar **[!UICONTROL Landing page]** como **[!UICONTROL Link type]** e escolha a [página de aterrissagem](create-lp.md#configure-primary-page) que você criou para registro.

   ![](../assets/lp_subscription-uc-link.png)

1. Salve o conteúdo e [publique a mensagem](../publish-manage-message.md).

1. Envie sua mensagem por meio de um [jornada](../building-journeys/journey.md) para direcionar o tráfego para a landing page de registro.

   ![](../assets/lp_subscription-uc-journey.png)

   Depois que receberem o email, se seus recipients clicarem no link para a landing page, eles serão direcionados para a página &quot;obrigado&quot; e serão adicionados à lista de assinaturas.

### Enviar um email de confirmação {#send-confirmation-email}

Além disso, você pode enviar um email de confirmação para os recipients que se registraram para o seu evento. Para isso, siga as etapas abaixo.

1. Criar outro [jornada](../building-journeys/journey.md). Você pode fazer isso diretamente da landing page clicando no link **[!UICONTROL Create journey]** botão. Saiba mais [aqui](create-lp.md#configure-primary-page)

   ![](../assets/lp_subscription-uc-create-journey.png)

1. Expanda a **[!UICONTROL Events]** categoria e solte uma **[!UICONTROL Segment Qualification]** atividade na tela. Saiba mais [aqui](../building-journeys/segment-qualification-events.md)

1. Clique no botão **[!UICONTROL Segment]** e selecione a lista de subscrição criada.

   ![](../assets/lp_subscription-uc-confirm-journey.png)

1. Selecione o email de confirmação de sua escolha e envie-o por meio da jornada.

   ![](../assets/lp_subscription-uc-confirm-email.png)

Todos os usuários que se registraram para o seu evento receberão o email de confirmação.

<!--The event registration's subscription list tracks the profiles who registered and you can send them targeted event updates.-->

## Recusar {#opt-out}

Para permitir que seus recipients cancelem a assinatura de suas comunicações, você pode incluir um link para uma landing page de opt out em seus emails.

Saiba mais sobre como gerenciar o consentimento dos recipients e por que isso é importante em [esta seção](../consent.md).

### Gerenciamento de recusa {#opt-out-management}

Oferecer aos recipients a capacidade de cancelar a inscrição para receber comunicações de uma marca é um requisito legal. Saiba mais sobre a legislação aplicável na [documentação da Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=pt-BR#regulations){target=&quot;_blank&quot;}.

Portanto, você sempre deve incluir um **link para cancelar a inscrição** em cada email enviado aos recipients:

* Ao clicar nesse link, os recipients serão direcionados a uma página de aterrissagem que inclui um botão para confirmar a recusa.
* Ao clicar no botão recusar, os dados do perfil serão atualizados com essas informações.

### Configurar recusa {#configure-opt-out}

Para permitir que os recipients de um email cancelem a assinatura de suas comunicações por meio de uma landing page, siga as etapas abaixo.

1. Crie a landing page. [Saiba mais](create-lp.md)

1. Defina a página primária. [Saiba mais](create-lp.md#configure-primary-page)

1. [Design](design-lp.md) o conteúdo principal da página: usar a página de aterrissagem específica **[!UICONTROL Form]** , defina um **[!UICONTROL Opt-out]** e escolha atualizar **[!UICONTROL Channel (email)]**: o perfil que marcar a caixa de opção de não participação na página de aterrissagem será rejeitado em todas as suas comunicações.

   ![](../assets/lp_opt-out-primary-lp.png)

   <!--You can also build your own landing page and host it on the third-party system of your choice. To keep?-->

1. Adicionar uma confirmação [subpágina](create-lp.md#configure-subpages) que será exibido para os usuários que enviam o formulário.

   ![](../assets/lp_opt-out-subpage.png)

   >[!NOTE]
   >
   >Certifique-se de fazer referência à subpágina no **[!UICONTROL Call to action]** da seção **[!UICONTROL Form]** componente. [Saiba mais](design-lp.md)

1. Após configurar e definir o conteúdo de suas páginas, [publicar](create-lp.md#publish) a landing page.

   ![](../assets/lp_opt-out-publish.png)

1. [Criar uma mensagem de email](../create-message.md) em [!DNL Journey Optimizer].

1. Selecione o texto no seu conteúdo e [inserir um link](../message-tracking.md#insert-links) usando a barra de ferramentas contextual. Você também pode usar um link em um botão.

   ![](../assets/lp_opt-out-insert-link.png)

1. Selecionar **[!UICONTROL Landing page]** do **[!UICONTROL Link type]** e selecione a [página de aterrissagem](create-lp.md#configure-primary-page) que você criou para rejeitar.

   ![](../assets/lp_opt-out-landing-page.png)

1. Salve o conteúdo e [publique a mensagem](../publish-manage-message.md).

1. Envie sua mensagem por meio de uma jornada. [Saiba mais](../building-journeys/journey.md).

1. Depois que a mensagem é recebida, se um recipient clicar no link de cancelamento de subscrição no email, sua landing page será exibida.

   ![](../assets/lp_opt-out-submit-form.png)

   Se o recipient marcar a caixa e enviar o formulário:

   * O recipient que recusou a inscrição é redirecionado para a tela de mensagem de confirmação.

   * Os dados do perfil são atualizados e não receberão comunicações da sua marca, a menos que sejam subscritos novamente.

Para verificar se a escolha do perfil correspondente foi atualizada, acesse a Experience Platform e o perfil selecionando um namespace de identidade e um valor de identidade correspondente. Saiba mais na [documentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=pt-BR#getting-started){target=&quot;_blank&quot;}.

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
