---
solution: Journey Optimizer
product: journey optimizer
title: Rastrear suas mensagens
description: Saiba como adicionar links e rastrear mensagens enviadas
feature: Monitoring
topic: Content Management
role: User
level: Intermediate
exl-id: 689e630a-00ca-4893-8bf5-6d1ec60c52e7
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%

---

# Adicionar links e rastrear mensagens {#tracking}

Use [!DNL Journey Optimizer] para adicionar links ao seu conteúdo e rastrear as mensagens enviadas para monitorar o comportamento dos recipients.

## Habilitar rastreamento {#enable-tracking}

Você pode ativar o rastreamento no nível da mensagem de email marcando a variável **[!UICONTROL Email opens]** e/ou **[!UICONTROL Click on email]** ao criar sua mensagem dentro de uma jornada ou campanha.

>[!BEGINTABS]

>[!TAB Ativar o rastreamento em uma jornada]

![](assets/message-tracking-journey.png)

>[!TAB Ativar o rastreamento em uma campanha]

![](assets/message-tracking-campaign.png)

>[!ENDTABS]

>[!NOTE]
>
>Ambas as opções são ativadas por padrão.

Isso permitirá rastrear o comportamento dos recipients por meio de:

* **[!UICONTROL Email opens]**: Mensagens que foram abertas.
* **[!UICONTROL Click on email]**: Cliques em links em um email.

## Inserir links {#insert-links}

Ao criar uma mensagem, você pode adicionar links ao seu conteúdo.

>[!NOTE]
>
>When [o rastreamento está ativado](#enable-tracking), todos os links incluídos no conteúdo da mensagem são rastreados.

Para inserir links no seu conteúdo de email, siga as etapas abaixo:

1. Selecione um elemento e clique em **[!UICONTROL Insert link]** na barra de ferramentas contextual.

   ![](assets/message-tracking-insert-link.png)

1. Escolha o tipo de link que deseja criar:

   * **[!UICONTROL External link]**: Insira um link para um URL externo.

   * **[!UICONTROL Landing page]**: Insira um link para uma landing page. Saiba mais em [esta seção](../landing-pages/get-started-lp.md)

   * **[!UICONTROL One click Opt-out]**: Insira um link para permitir que os usuários cancelem rapidamente a assinatura de suas comunicações, sem a necessidade de confirmar a recusa. Saiba mais em [esta seção](../privacy/opt-out.md#one-click-opt-out).

   * **[!UICONTROL External Opt-in/Subscription]**: Insira um link para aceitar as comunicações de recebimento da sua marca.

   * **[!UICONTROL External Opt-out/Unsubscription]**: Insira um link para cancelar a assinatura do recebimento de comunicações da sua marca. Saiba mais sobre o gerenciamento de não participação no [esta seção](../privacy/opt-out.md#opt-out-management).

   * **[!UICONTROL Mirror page]**: Insira um link para exibir o conteúdo do email em um navegador da Web. Saiba mais em [esta seção](#mirror-page).

   ![](assets/message-tracking-links.png)

1. Você pode personalizar seus links. Saiba mais sobre URLs personalizados em [esta seção](../personalization/personalization-syntax.md#perso-urls).

1. Salve as alterações.

1. Depois que o link for criado, você ainda poderá modificá-lo da variável **[!UICONTROL Component settings]** painel à direita.

   * Você pode editar o link e alterar seu tipo.
   * Você pode optar por sublinhar o link ou não, marcando a opção correspondente.

   ![](assets/message-tracking-link-settings.png)

>[!NOTE]
>
>As mensagens de email de tipo de marketing devem incluir um [link para opção de não participação](../privacy/opt-out.md#opt-out-management), que não é necessário para mensagens transacionais. A categoria da mensagem (**[!UICONTROL Marketing]** ou **[!UICONTROL Transactional]**) é definido na variável [superfície do canal](../configuration/channel-surfaces.md#email-type) (ou seja, predefinição de mensagem) e ao criar a mensagem.

## Link para uma mirror page {#mirror-page}

A mirror page é uma página HTML acessível online por um navegador da Web. Seu conteúdo é idêntico ao conteúdo do email.

Para adicionar um link a uma mirror page no seu email, [inserir um link](#insert-links) e selecione **[!UICONTROL Mirror page]** como o tipo de link.

![](assets/message-tracking-mirror-page.png)

A mirror page é criada automaticamente.

>[!IMPORTANT]
>
>Os links de mirror pages são gerados automaticamente e não podem ser editados. Eles contêm todos os dados personalizados criptografados necessários para renderizar o email original. Como resultado, o uso de atributos personalizados com valores grandes pode gerar URLs de mirror pages longas, o que pode impedir que o link funcione em navegadores da Web com tamanho máximo de URLs.

Depois que o email for enviado, quando os recipients clicarem no link da mirror page, o conteúdo do email será exibido no navegador padrão.

>[!NOTE]
>
>No [prova](preview.md#send-proofs) enviado aos perfis de teste, o link para a mirror page não está ativo. Ela só é ativada nas mensagens finais.

O período de retenção de uma mirror page é de 60 dias. Após esse atraso, a mirror page não estará mais disponível.

## Gerenciar rastreamento {#manage-tracking}

O [Email Designer](content-from-scratch.md) permite gerenciar os URLs rastreados, como editar o tipo de rastreamento para cada link.

1. Clique no botão **[!UICONTROL Links]** ícone do painel esquerdo para exibir a lista de todos os URLs do seu conteúdo que serão rastreados.

   Essa lista permite que você tenha uma visualização centralizada e localize cada URL no conteúdo do email.

1. Para editar um link, clique no ícone de lápis correspondente.

   ![](assets/message-tracking-edit-links.png)

1. Você pode modificar o **[!UICONTROL Tracking Type]** se necessário:

   ![](assets/message-tracking-edit-a-link.png)

   Para cada URL rastreado, é possível definir o modo de rastreamento para um destes valores:

   * **[!UICONTROL Tracked]**: Ativa o rastreamento nesse URL.
   * **[!UICONTROL Opt out]**: Considera esse URL como recusa ou cancelamento de subscrição.
   * **[!UICONTROL Mirror page]**: Considera esse URL como sendo de mirror page.
   * **[!UICONTROL Never]**: Nunca ativa o rastreamento desse URL. <!--This information is saved: if the URL appears again in a future message, its tracking is automatically deactivated.-->

Os relatórios sobre aberturas e cliques estão disponíveis no [Relatório ao vivo](../reports/live-report.md) e na [Relatório global](../reports/global-report.md).
