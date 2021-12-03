---
title: Criar uma mensagem
description: Saiba como criar uma mensagem
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 186a43cd-c5eb-4de1-8713-95399d802d36
source-git-commit: d8c95350ac17658ce477d6aec50a9f418f4af0f2
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 4%

---

# Criar uma mensagem {#create-message}

As mensagens estão disponíveis no **[!UICONTROL Messages]** no painel de navegação esquerdo. Todas as mensagens são listadas, classificadas por data de publicação (para mensagens publicadas) ou data de criação (para mensagens de rascunho).

>[!NOTE]
>
>Os usuários podem acessar, criar, editar e/ou publicar mensagens dependendo de seu perfil de produto. Saiba mais sobre permissões de usuário [nesta seção](administration/permissions.md).

![](assets/messages-list.png)

Use o **[!UICONTROL Show recents]** alterne para adicionar links diretos às mensagens acessadas nos últimos 5 dias.

![](assets/show-recent-messages.png)

Use o ícone de filtro para exibir somente mensagens elaboradas, publicadas ou que estejam sendo publicadas. Também é possível pesquisar no rótulo da mensagem, conforme abaixo:

![](assets/filter-messages.png)

## Criar uma nova mensagem

Para criar uma nova mensagem, siga as etapas abaixo:

1. Acesse a lista de mensagens e clique em **[!UICONTROL Create Message]**.

1. Defina as propriedades da mensagem.

   ![](assets/create-message-properties.png)

   * Insira um **[!UICONTROL Title]** (obrigatório) e um **[!UICONTROL Description]**.

   * Selecione o **[!UICONTROL Message category]**: Marketing ou transacional.

   * Selecione o **[!UICONTROL Preset]** para usar na mensagem.

      As predefinições incluem todos os parâmetros necessários para que uma notificação por email e/ou por push seja enviada de acordo com sua marca. [Saiba mais sobre predefinições](configuration/message-presets.md).

   * Selecione os canais que deseja usar para essa mensagem: Notificação por email e/ou notificação por push. Você deve selecionar pelo menos um canal para criar a mensagem.
   Observe que você pode acessar e modificar o título, a descrição e a predefinição da mensagem a qualquer momento usando o **[!UICONTROL Properties]** na interface da mensagem.

1. Clique em **[!UICONTROL Create]** para confirmar a criação da mensagem. Sua mensagem é adicionada na lista de mensagens, no **[!UICONTROL Draft]** status.

   Uma guia está disponível para cada canal selecionado. Use essas guias para configurar o conteúdo de cada canal. Você pode remover uma guia selecionando-a e clicando no botão **[!UICONTROL Delete channel]** à direita.

   ![](assets/create-messages-content.png)

   Agora você pode criar o conteúdo da mensagem e adaptar as configurações. Informações detalhadas sobre a configuração de email e notificação por push estão disponíveis nas seguintes seções:

   * [Criar um email](create-email.md)
   * [Criar notificações por push](create-push.md)

   >[!NOTE]
   >   
   >Você pode personalizar suas mensagens usando os dados dos perfis usando o Editor de expressão. Para obter mais informações sobre personalização, consulte [esta seção](personalization/personalize.md).


1. Controle a renderização das mensagens e verifique as configurações de personalização com perfis de teste, usando a seção preview no lado esquerdo. Para obter mais informações, consulte [esta seção](preview.md).

   ![](assets/messages-simple-preview.png)

1. Verifique os alertas na seção superior do editor.  Alguns deles são avisos simples, mas outros podem impedir que você publique a mensagem. Saiba mais [nesta seção](alerts.md).

1. Agora você pode publicar sua mensagem clicando no link **[!UICONTROL Publish]** , ou mantenha-o como rascunho e publique-o posteriormente. Para obter mais informações sobre como publicar mensagens, consulte [esta seção](publish-manage-message.md).

## Duplicar uma mensagem

Para criar uma mensagem a partir de uma existente, use o **[!UICONTROL Duplicate]** na interface da mensagem. Todas as configurações e configurações serão copiadas para a nova mensagem

![](assets/message-duplicate.png)

É possível renomear a mensagem antes de confirmar a duplicação.

![](assets/message-duplicate-confirm.png)

Uma mensagem de confirmação é exibida na parte inferior da janela assim que a nova mensagem é criada.

Também é possível duplicar uma mensagem da lista de mensagens, usando o ícone dedicado.

![](assets/message-duplicate-from-list.png)

O mesmo processo de confirmação se aplica.
