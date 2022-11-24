---
solution: Journey Optimizer
product: journey optimizer
title: Adicionar mensagens em jornadas
description: Saiba como adicionar mensagens em uma jornada
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: acb5b65b-8787-4428-9924-36aa0a115926
source-git-commit: 88182f9f685efbd45dd5ecf8a09745f55305a78f
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 97%

---

# Adicionar mensagens em jornadas{#messages-in-journeys}

>[!CONTEXTUALHELP]
>id="ajo_message_category"
>title="Categoria da mensagem"
>abstract="Escolha Marketing para mensagens comerciais ou Transacional para mensagens não comerciais, como confirmação de pedidos, notificações de redefinição de senha ou informações de entrega"

>[!CONTEXTUALHELP]
>id="ajo_message_surface"
>title="Superfície de canal"
>abstract="Uma superfície de canal é uma instância desse canal que tem todas as configurações para fornecer uma ação com sucesso por meio de uma campanha ou jornada. É definida por um administrador do sistema."

Em suas jornadas, use as ações do canal para projetar e personalizar a mensagem que deseja enviar ao público-alvo. Ao adicionar um email, um SMS ou uma ação de push às telas de jornada, você está criando um envio acionado. Quando os contatos atingem essa ação de canal, o Adobe Journey Optimizer envia a mensagem automaticamente.


>[!NOTE]
>Você também pode criar campanhas para enviar mensagens programadas. Saiba mais [nesta seção](../campaigns/get-started-with-campaigns.md).


Para adicionar mensagens em uma jornada, basta adicionar uma atividade de push, SMS ou email na tela da jornada.

1. Inicie a jornada com uma atividade de [Evento](../building-journeys/general-events.md) ou [Segmento de leitura](../building-journeys/read-segment.md).

1. Na seção **Ações** da paleta, arraste e solte na tela uma atividade de **email**, **SMS** ou **push**.

   ![](assets/add-a-message.png)

1. Insira um rótulo e uma descrição.

1. Selecione a **[!UICONTROL Categoria]** da mensagem: escolha **Marketing** para mensagens comerciais ou **Transacional** para mensagens não comerciais, como confirmações de pedidos, notificações de redefinição de senha ou informações de entrega.

   ![](assets/inline-message-category.png)

   >[!CAUTION]
   >
   >* Se você definiu [regras de frequência](../configuration/frequency-rules.md) para um canal e categoria específicos, elas são aplicadas automaticamente à mensagem ao selecionar esse canal e categoria. Atualmente, somente a categoria **[!UICONTROL Marketing]** está disponível para regras de frequência.
   >
   >* As mensagens de marketing devem incluir um [link para opção de não participação](../privacy/opt-out.md#opt-out-management). Isso não é necessário para mensagens transacionais, pois essas mensagens podem ser enviadas a perfis que cancelaram a assinatura de comunicações de marketing.


1. Selecione a **[!UICONTROL Superfície]** de canal (ou seja, predefinição de mensagem) a ser usada para enviar a mensagem.

   Uma superfície é uma configuração que foi definida por um [Administrador do sistema](../start/path/administrator.md). Ela contém todos os parâmetros técnicos para enviar a mensagem, como parâmetros de cabeçalho, subdomínio, aplicativos móveis etc. [Saiba mais](../configuration/channel-surfaces.md).

   >[!CAUTION]
   >
   >Você deve escolher uma superfície de canal válida para a categoria e o canal de mensagens selecionados.

   É possível acessar e modificar o rótulo, a descrição e a superfície da mensagem a qualquer momento usando o botão **[!UICONTROL Propriedades]** na interface da mensagem.

1. Criar o conteúdo da mensagem.

   Saiba mais sobre as etapas detalhadas para criar o conteúdo da mensagem na página a seguir:

   * [Criar um email](create-email.md)
   * [Criar uma notificação por push](create-push.md)
   * [Criar uma mensagem de SMS.](create-sms.md)

## Habilitar otimização de tempo de envio{#sto-in-journeys}

Para notificações por email e por push, é possível ativar a **[!UICONTROL Otimização de hora de envio]**.

Use a **[!UICONTROL Otimização de hora de envio]** para agendar tempos de envio personalizados para cada usuário a fim de aumentar as taxas de abertura e de clique de suas mensagens. [Saiba mais](../messages/send-time-optimization.md).

## Parâmetros avançados{#adv-settings}

Parâmetros avançados são somente leitura e ocultos por padrão.

Para acessar os parâmetros avançados, clique no ícone **[!UICONTROL Mostrar campos somente leitura]** na parte superior do painel de mensagens. Clique no mesmo ícone para ocultar as configurações avançadas.

![](assets/show-read-only.png)

Parâmetros avançados são exibidos na parte inferior do painel de mensagens. Esses parâmetros são definidos pelo [administrador do sistema](../start/path/administrator.md) na [superfície de canal](../configuration/channel-surfaces.md) (ou seja, predefinição de mensagem) associada à mensagem.

Para notificações por push, é possível exibir os seguintes parâmetros: Token, AppID, AppPlatform.

![](assets/push-adv-parameters.png)

Para email, é possível exibir o [endereço de email principal](../configuration/primary-email-addresses.md).

Em contextos específicos, é possível substituir esses valores para uso específico. Para forçar um valor, clique no ícone **[!UICONTROL Habilitar substituição de parâmetro]** à direita do campo.

![](assets/email-adv-parameters.png)

Essa opção pode ser útil, por exemplo, para:

* Teste um email. Você pode adicionar seu endereço de email; após publicar a jornada, o email será enviado para você.
* Consultar o endereço de email dos assinantes de uma lista. Saiba mais [neste caso de uso](../building-journeys/message-to-subscribers-uc.md).

>[!NOTE]
>
>A substituição de endereço de email deve ser usada somente para casos de uso específicos. Na maioria das vezes, não é necessário alterar o endereço de email, pois o valor definido como o endereço principal nos **[!UICONTROL Campos de execução]** é o que deve ser usado. [Saiba mais](../configuration/primary-email-addresses.md)

## Procurar mensagens{#browse-message}

Quando várias mensagens são usadas em uma jornada, é possível alternar de uma para outra a partir da tela **Editar conteúdo**.

![](assets/inline-messages-multi-content.png)

Você pode então [verificar alertas](alerts.md) e [simular](../design/preview.md) cada conteúdo em uma única visualização.

## Duplicar uma mensagem {#duplicate-message}

Você pode copiar uma mensagem existente da tela de jornada.

Para fazer isso, siga as etapas abaixo:

1. Selecione a mensagem que deseja copiar.

1. Use o botão **[!UICONTROL Copiar]** do painel **[!UICONTROL Ação]**.

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

Use o botão **[!UICONTROL Confirmar]** para validar.
