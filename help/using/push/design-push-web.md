---
solution: Journey Optimizer
product: journey optimizer
title: Criar uma notificação por push
description: Saiba como criar uma notificação por push da Web no Journey Optimizer
feature: Push
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
source-git-commit: 6cac68836bf8aa12cfabae70d60df97383287053
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 3%

---

# Criar uma notificação por push da Web {#design-push-notification}

>[!AVAILABILITY]
>
>Atualmente, as notificações por push da Web no Journey Optimizer não oferecem suporte ao recurso **Notificação silenciosa**, mas estarão disponíveis posteriormente.

Depois de criar sua campanha ou jornada de notificação por push na Web, você pode prosseguir com o design do conteúdo e da estrutura de acordo com seus requisitos. Observe que, antes de enviar qualquer notificação por push na Web, é necessário configurar primeiro esse canal na [Configuração de canal](push-configuration-web.md).

<!--
## Send a silent notification {#silent-notification}

A silent push notification (also called a background notification) is a hidden message sent to your web application without alerting the user.

To enable a silent notification, enable the **[!UICONTROL Silent Notification]** option. When this option is used, the notification is delivered directly to the application, and no alert, banner, or sound is shown to the user.

Use the **Custom Data** section to include additional information in the form of key-value pairs. 

![](assets/web-silent.png)
-->

## Título e corpo {#push-title-body}

Para redigir a mensagem, clique nos campos **[!UICONTROL Título]** e **[!UICONTROL Corpo]**. Use o editor de personalização para definir o conteúdo, [personalizar dados](../personalization/personalize.md) e adicionar [conteúdo dinâmico](../personalization/get-started-dynamic-content.md).

Clique em **[!UICONTROL Editar texto com o assistente de IA]** para gerar conteúdo facilmente usando o assistente de IA do Journey Optimizer.

![](assets/web-design-body.png)

## Comportamento ao clicar {#on-click-behavior}

Use o campo **[!UICONTROL Comportamento de clique no corpo]** para definir um deep link que determina o que acontece quando um usuário clica no corpo da notificação. Isso permite enviar os usuários diretamente para uma página ou seção específica do aplicativo da Web.

![](assets/web-onclick.png)

## Adicionar mídia {#add-media-push}

Insira a URL da mídia no campo **[!UICONTROL Adicionar mídia]**. Você também pode incluir tokens de personalização no URL para personalizar o conteúdo de cada usuário.

Clique em ![Editar texto com o assistente de IA](assets/do-not-localize/Smock_ImageAdd_18_N.svg) para gerar mídia rapidamente usando o Assistente de IA do Journey Optimizer.

![](assets/web-media.png)

## Adicionar botões {#add-buttons-push}

Torne as notificações por push da Web interativas adicionando botões ao conteúdo.

Observe que os botões só são visíveis quando o dispositivo está desbloqueado. Se a tela estiver bloqueada, somente o **[!UICONTROL Título]** e a **[!UICONTROL Mensagem]** serão exibidos.

Use a opção **[!UICONTROL Adicionar Botão]** para definir o rótulo de cada botão e a ação associada, conforme detalhado abaixo:

* **[!UICONTROL Deeplink]**: redirecione os usuários para um modo de exibição, seção ou guia específico no aplicativo. Insira o URL do deep link no campo associado.

* **[!UICONTROL URL da Web]**: redirecionar usuários para uma página da Web externa. Insira o URL no campo associado.

![](assets/push_buttons.png)

## Dados personalizados {#custom-data}

Na seção **[!UICONTROL Dados personalizados]**, você pode adicionar pares de valores chave personalizados à carga de notificação. Esses valores podem ser usados pelo aplicativo web para acionar ações específicas ou personalizar a experiência do usuário. Para obter mais informações sobre como configurar notificações por push no Adobe Experience Platform, consulte [esta seção](push-gs.md)

![](assets/web-custom.png)

