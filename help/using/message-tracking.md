---
title: Rastrear suas mensagens
description: Saiba como rastrear mensagens enviadas
feature: Monitoramento
topic: Gerenciamento de conteúdo
role: User
level: Intermediate
source-git-commit: e27472cc6186cf7cb25fdb93d15720fc837c58bb
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 2%

---

# Rastreamento de mensagens {#tracking}

Use [!DNL Journey Optimizer] para rastrear as mensagens enviadas e o comportamento dos recipients.

## Habilitar rastreamento {#enable-tracking}

Você pode habilitar o rastreamento no nível da mensagem marcando as opções **[!UICONTROL Open Tracking for email]** e/ou **[!UICONTROL Click Tracking for email]** ao [criar a mensagem](create-message.md).

![](assets/message-tracking.png)

>[!NOTE]
>
>Ambas as opções são ativadas por padrão.

Isso permitirá rastrear o comportamento dos recipients por meio de:
* **[!UICONTROL Open Tracking for email]**: Mensagens que foram abertas.
* **[!UICONTROL Click Tracking for email]**: Cliques em links em um email.

## Inserir links {#insert-links}

Ao criar uma mensagem, você pode adicionar links ao seu conteúdo.

>[!NOTE]
>
>Quando [tracking está ativado](#enable-tracking), todos os links incluídos no conteúdo da mensagem são rastreados.

Para inserir links no seu conteúdo de email, siga as etapas abaixo:

1. Selecione um elemento e clique em **[!UICONTROL Insert link]** na barra de ferramentas contextual.

   ![](assets/message-tracking-insert-link.png)

1. Escolha o tipo de link que deseja criar:

   * **[!UICONTROL External link]**: Insira um link para um URL externo.

   * **[!UICONTROL Unsubscription link]**: Insira um link para cancelar a assinatura do recebimento de comunicações da sua marca. Saiba mais sobre o gerenciamento de não participação em [esta seção](consent.md#opt-out-management).

   * **[!UICONTROL Mirror page]**: Insira um link para exibir o conteúdo do email em um navegador da Web.

   ![](assets/message-tracking-links.png)

1. É possível personalizar os links usando apenas uma expressão simples. Saiba mais sobre personalização em [esta seção](personalization/personalization-syntax.md).

1. Salve as alterações.

1. Depois que o link é criado, você ainda pode modificá-lo do painel **[!UICONTROL Component settings]** à direita.

   * Clique no ícone de lápis para editar o link.
   * Você pode optar por sublinhar o link ou não, marcando a opção correspondente.

   ![](assets/message-tracking-link-settings.png)

## Gerenciar o rastreamento {#manage-tracking}

O [Email Designer](create-email-content.md) permite gerenciar os URLs rastreados, como editar o tipo de rastreamento para cada link.

1. Clique no ícone **[!UICONTROL Links]** no painel esquerdo para exibir a lista de todos os URLs do seu conteúdo que serão rastreados.

   Essa lista permite que você tenha uma visualização centralizada e localize cada URL no conteúdo do email.

1. Para editar um link, clique no ícone de lápis correspondente.

   ![](assets/message-tracking-edit-links.png)

1. Você pode modificar o **[!UICONTROL Tracking Type]** se necessário:


   ![](assets/message-tracking-edit-a-link.png)

   Para cada URL rastreado, é possível definir o modo de rastreamento para um destes valores:

   * **[!UICONTROL Tracked]**: Ativa o rastreamento nesse URL.
   * **[!UICONTROL Opt out]**: Considera esse URL como recusa ou cancelamento de subscrição.
   * **[!UICONTROL Mirror page]**: Considera esse URL como sendo de mirror page.
   * **[!UICONTROL Never]**: Nunca ativa o rastreamento desse URL.  <!--This information is saved: if the URL appears again in a future message, its tracking is automatically deactivated.-->

O número de mensagens que foram abertas e o número de links que foram clicados são listados na guia [Executions](message-monitoring.md).

Os relatórios sobre aberturas e cliques estão disponíveis no [Email Live report](reports/email-live-report.md) e no [Email Global report](reports/email-global-report.md).


