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
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 12%

---

# Adicionar links e rastrear mensagens {#tracking}

Use [!DNL Journey Optimizer] para adicionar links ao seu conteúdo e rastrear as mensagens enviadas para monitorar o comportamento dos recipients.

## Habilitar rastreamento {#enable-tracking}

Você pode ativar o rastreamento no nível da mensagem de email marcando a variável **[!UICONTROL Aberturas de email]** e/ou **[!UICONTROL Clique no email]** opções ao [criação da mensagem](../messages/get-started-content.md).

![](assets/message-tracking.png)

>[!NOTE]
>
>Ambas as opções são ativadas por padrão.

Isso permitirá rastrear o comportamento dos recipients por meio de:

* **[!UICONTROL Aberturas de email]**: Mensagens que foram abertas.
* **[!UICONTROL Clique no email]**: Cliques em links em um email.

## Inserir links {#insert-links}

Ao criar uma mensagem, você pode adicionar links ao seu conteúdo.

>[!NOTE]
>
>When [o rastreamento está ativado](#enable-tracking), todos os links incluídos no conteúdo da mensagem são rastreados.

Para inserir links no seu conteúdo de email, siga as etapas abaixo:

1. Selecione um elemento e clique em **[!UICONTROL Inserir link]** na barra de ferramentas contextual.

   ![](assets/message-tracking-insert-link.png)

1. Escolha o tipo de link que deseja criar:

   * **[!UICONTROL Link externo]**: Insira um link para um URL externo.

   * **[!UICONTROL Página de aterrissagem]**: Insira um link para uma landing page. Saiba mais [nesta seção](../landing-pages/get-started-lp.md)

   * **[!UICONTROL Um clique para recusar]**: Insira um link para permitir que os usuários cancelem rapidamente a assinatura de suas comunicações, sem a necessidade de confirmar a recusa. Saiba mais [nesta seção](../privacy/opt-out.md#one-click-opt-out).

   * **[!UICONTROL Aceitação/assinatura externa]**: Insira um link para aceitar as comunicações de recebimento da sua marca.

   * **[!UICONTROL Cancelamento/cancelamento de subscrição externo]**: Insira um link para cancelar a assinatura do recebimento de comunicações da sua marca. Saiba mais sobre o gerenciamento de recusa [nesta seção](../privacy/opt-out.md#opt-out-management).

   * **[!UICONTROL Mirror page]**: Insira um link para exibir o conteúdo do email em um navegador da Web. Saiba mais [nesta seção](#mirror-page).

   ![](assets/message-tracking-links.png)

1. Você pode personalizar seus links. Saiba mais sobre URLs personalizados [nesta seção](../personalization/personalization-syntax.md#perso-urls).

1. Salve as alterações.

1. Depois que o link for criado, você ainda poderá modificá-lo da variável **[!UICONTROL Configurações do componente]** painel à direita.

   * Você pode editar o link e alterar seu tipo.
   * Você pode optar por sublinhar o link ou não, marcando a opção correspondente.

   ![](assets/message-tracking-link-settings.png)

>[!NOTE]
>
>As mensagens de email de tipo de marketing devem incluir um [link para opção de não participação](../privacy/opt-out.md#opt-out-management), que não é necessário para mensagens transacionais. A categoria da mensagem (**[!UICONTROL Marketing]** ou **[!UICONTROL Transacional]**) é definida no nível da [superfície de canal](../configuration/channel-surfaces.md#email-type) (ou seja, predefinição da mensagem) e ao [criar a mensagem](../messages/get-started-content.md#create-new-message).

## Link para uma mirror page {#mirror-page}

A mirror page é uma página HTML acessível online através de um navegador da Web. Seu conteúdo é idêntico ao conteúdo do email.

Para adicionar um link a uma mirror page no seu email, [inserir um link](#insert-links) e selecione **[!UICONTROL Mirror page]** como o tipo de link.

![](assets/message-tracking-mirror-page.png)

A mirror page é criada automaticamente.

>[!NOTE]
>
>Não é possível editar o link gerado automaticamente.

Depois que o email for enviado, quando os recipients clicarem no link da mirror page, o conteúdo do email será exibido no navegador padrão.

>[!NOTE]
>
>No [prova](preview.md#send-proofs) enviado aos perfis de teste, o link para a mirror page não está ativo. Ela só é ativada nas mensagens finais.

O período de retenção de uma mirror page é de 60 dias. Após esse atraso, a mirror page não estará mais disponível.

## Gerenciar rastreamento {#manage-tracking}

O [Email Designer](create-email-content.md) permite gerenciar os URLs rastreados, como editar o tipo de rastreamento para cada link.

1. Clique no botão **[!UICONTROL Links]** ícone do painel esquerdo para exibir a lista de todos os URLs do seu conteúdo que serão rastreados.

   Essa lista permite que você tenha uma visualização centralizada e localize cada URL no conteúdo do email.

1. Para editar um link, clique no ícone de lápis correspondente.

   ![](assets/message-tracking-edit-links.png)

1. Você pode modificar o **[!UICONTROL Tipo de rastreamento]** se necessário:

   ![](assets/message-tracking-edit-a-link.png)

   Para cada URL rastreado, é possível definir o modo de rastreamento para um destes valores:

   * **[!UICONTROL Rastreado]**: Ativa o rastreamento nesse URL.
   * **[!UICONTROL Recusar]**: Considera esse URL como recusa ou cancelamento de subscrição.
   * **[!UICONTROL Mirror page]**: Considera esse URL como sendo de mirror page.
   * **[!UICONTROL Nunca]**: Nunca ativa o rastreamento desse URL. <!--This information is saved: if the URL appears again in a future message, its tracking is automatically deactivated.-->

Os relatórios sobre aberturas e cliques estão disponíveis no [Relatório ao vivo](../reports/live-report.md) e na [Relatório global](../reports/global-report.md).
