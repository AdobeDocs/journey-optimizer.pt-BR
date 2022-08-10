---
title: Introdução a mensagens
description: Saiba como criar e enviar mensagens personalizadas no Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 712dc172-6c0d-4ce8-ba16-de99d65fc641
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 100%

---

# Introdução a mensagens {#get-started-messages}

>[!CONTEXTUALHELP]
>id="ajo_journey_message"
>title="Ações do canal"
>abstract="Use as ações do canal para enviar uma mensagem de push, SMS ou email."

Use o [!DNL Journey Optimizer] para criar e enviar notificações por push e SMS e mensagens de email personalizadas. Todas as mensagens são editáveis em linha como parte de uma ação na tela da jornada. Use o recurso Salvar como modelo para reutilizar seu conteúdo facilmente. É possível:

* Usar os **recursos de design de email** do [!DNL Journey Optimizer] para criar ou importar emails responsivos.

* Aproveitar o **Adobe Experience Manager Assets Essentials** para enriquecer seus emails e criar e gerenciar seu próprio banco de dados de ativos.

* Encontrar **fotos do Adobe Stock** para criar seu conteúdo e melhorar o design de emails.

* Melhorar a experiência dos clientes criando **notificações por push, SMS e emails** personalizados com base nos atributos de perfil.

* **Enviar deliveries** com base nesses conteúdos e rastrear o comportamento do cliente.

>[!NOTE]
>
>Os usuários podem acessar, criar, editar e/ou publicar jornadas dependendo de seu perfil de produto. Saiba mais sobre permissões de usuário [nesta seção](../administration/permissions.md).


## Adicionar mensagens em suas jornadas{#messages-in-journeys}

>[!CONTEXTUALHELP]
>id="ajo_message_category"
>title="Categoria da mensagem"
>abstract="Escolha Marketing para mensagens comerciais ou Transacional para mensagens não comerciais, como confirmação de pedidos, notificações de redefinição de senha ou informações de entrega"

>[!CONTEXTUALHELP]
>id="ajo_message_surface"
>title="Superfície de canal"
>abstract="Uma superfície de canal é uma instância desse canal que tem todas as configurações para fornecer uma ação com sucesso por meio de uma campanha ou jornada. É definida por um administrador do sistema."

Para adicionar mensagens em suas jornadas, basta adicionar uma atividade de push, SMS ou email na tela da jornada.

1. Inicie a jornada com uma atividade de [Evento](../building-journeys/general-events.md) ou [Segmento de leitura](../building-journeys/read-segment.md).

1. Na seção **Ações** da paleta, arraste e solte na tela uma atividade de **email**, **SMS** ou **push**.

   ![](assets/add-a-message.png)

1. Insira um rótulo e uma descrição.

1. Selecione a **[!UICONTROL Category]** da mensagem: escolha **Marketing** para mensagens comerciais ou **Transacional** para mensagens não comerciais, como confirmações de pedidos, notificações de redefinição de senha ou informações de entrega.

   >[!CAUTION]
   >
   >Se você definiu [regras de frequência](../configuration/frequency-rules.md) para um canal e categoria específicos, elas são aplicadas automaticamente à mensagem ao selecionar esse canal e categoria. Atualmente, somente a categoria **[!UICONTROL Marketing]** está disponível para regras de frequência.

   ![](assets/inline-message-category.png)

   >[!CAUTION]
   >
   >As mensagens do tipo Marketing devem incluir um [link para opção de não participação](../messages/consent.md#opt-out-management). Isso não é necessário para mensagens transacionais, pois essas mensagens podem ser enviadas a perfis que cancelaram a assinatura de comunicações de marketing.

1. Selecione a **[!UICONTROL Surface]** de canal (ou seja, predefinição de mensagem) a ser usada para enviar a mensagem.

   Uma superfície é uma configuração que foi definida por um [Administrador do sistema](../start/path/administrator.md). Ela contém todos os parâmetros técnicos para enviar a mensagem, como parâmetros de cabeçalho, subdomínio, aplicativos móveis etc. [Saiba mais](../configuration/channel-surfaces.md).

   >[!CAUTION]
   >
   >Você deve escolher uma superfície de canal válida para a categoria e o canal de mensagens selecionados.

   É possível acessar e modificar o rótulo, a descrição e a superfície da mensagem a qualquer momento usando o botão **[!UICONTROL Properties]** na interface da mensagem.

1. Criar o conteúdo da mensagem.

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

Clique no mesmo ícone para redefinir para o parâmetro padrão.


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
