---
title: Adicionar mensagens em campanhas
description: Saiba como adicionar mensagens em uma campanha
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: 87f9a4661b64cf24a8cd62bb9c70d5f1c9fcaddf
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 80%

---


# Adicionar mensagens em campanhas{#messages-in- campaigns}

Em suas campanhas, selecione o canal para projetar e personalizar a mensagem que deseja enviar para o público-alvo. Ao adicionar um email, um SMS ou um Push à campanha, você pode enviá-lo imediatamente ou agendar a mensagem.

>[!NOTE]
>Você também pode criar jornadas para enviar mensagens acionadas. Saiba mais [nesta seção](messages-in-journeys.md).

Saiba como adicionar e configurar mensagens em uma campanha [nesta seção](../campaigns/create-campaign.md)

Saiba mais sobre as etapas detalhadas para criar o conteúdo da mensagem na página a seguir:

* [Criar um email](create-email.md)
* [Criar uma notificação por push](create-push.md)
* [Criar uma mensagem de SMS.](create-sms.md)

## Habilitar otimização de tempo de envio{#sto-in-journeys}

Para notificações por email e por push, é possível habilitar a **[!UICONTROL Send-time optimization]**.

Use a **[!UICONTROL Send-time optimization]** para agendar tempos de envio personalizados para cada usuário a fim de aumentar as taxas de abertura e de clique de suas mensagens. [Saiba mais](../messages/send-time-optimization.md).

## Parâmetros avançados{#adv-settings}

Parâmetros avançados são somente leitura e ocultos por padrão.

Para acessar os parâmetros avançados, clique no ícone **[!UICONTROL Show read-only fields]** na parte superior do painel de mensagens.

![](assets/show-read-only.png)

Parâmetros avançados são exibidos na parte inferior do painel de mensagens. Esses parâmetros são definidos pelo [administrador do sistema](../start/path/administrator.md) na [superfície de canal](../configuration/channel-surfaces.md) (ou seja, predefinição de mensagem) associada à mensagem.

Para notificações por push, é possível exibir os seguintes parâmetros: Token, AppID, AppPlatform.

![](assets/push-adv-parameters.png)

Para emails, é possível exibir o endereço de email principal.

Para uso específico, é possível substituir esses valores em contextos específicos. Para forçar um valor, clique no ícone **Habilitar substituição de parâmetro** à direita do campo. Essa opção pode ser útil, por exemplo, para:

* Testar um email; você pode adicionar seu endereço de email. Após publicar a jornada, o email será enviado para você.
* Consultar o endereço de email dos assinantes de uma lista. Saiba mais [neste caso de uso](../building-journeys/message-to-subscribers-uc.md).

Clique no mesmo ícone para ocultar configurações avançadas.

## Procurar mensagens{#browse-message}

Quando várias mensagens são usadas em uma jornada, é possível alternar de uma para outra a partir da tela **Editar conteúdo**.

![](assets/inline-messages-multi-content.png)

Você pode então [verificar alertas](alerts.md) e [simular](../design/preview.md) cada conteúdo em uma única visualização.

## Duplicar uma mensagem {#duplicate-message}

Você pode copiar uma mensagem existente da tela de jornada.

Para fazer isso, siga as etapas abaixo:

1. Selecione a mensagem que deseja copiar.

1. Use o botão **[!UICONTROL Copy]** no painel **[!UICONTROL Action]**.

   ![](assets/message-duplicate.png)

1. Pressione **Crtl+V** para colar a mensagem.

   A mensagem será adicionada às telas de jornada. Todas as definições e configurações serão copiadas para a nova mensagem.

   ![](assets/message-duplicated.png)

1. Renomeie a mensagem para poder diferenciar a mensagem inicial da cópia, por exemplo, ao editar mensagens, conforme abaixo:

   ![](assets/multi-message.png)


>[!NOTE]
>
>Para emails, você também pode transformar uma mensagem existente em um modelo. [Saiba mais](../design/email-templates.md).

## Excluir uma mensagem{#delete-message}

Para excluir uma mensagem, use o ícone de lixeira na parte superior do painel de atividade do canal.

![](assets/delete-message.png)

Use o botão **[!UICONTROL Confirm]** para validar.
