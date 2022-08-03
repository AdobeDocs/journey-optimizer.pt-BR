---
title: Introdução a mensagens
description: Saiba como criar e entregar mensagens personalizadas no Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 712dc172-6c0d-4ce8-ba16-de99d65fc641
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Introdução a mensagens {#get-started-messages}

>[!CONTEXTUALHELP]
>id="ajo_journey_message"
>title="Ações do canal"
>abstract="Use as ações do canal para enviar uma mensagem de push, SMS ou email."

Use [!DNL Journey Optimizer] para criar e entregar notificações por push, SMS e mensagens de email personalizadas. Todas as mensagens são editáveis em linha como parte de uma ação na Tela de Jornada.  Use o recurso Salvar como modelo para reutilizar seu conteúdo facilmente. É possível:

* Use [!DNL Journey Optimizer] **recursos de design de email** para criar ou importar emails responsivos.

* Aproveitamento **Adobe Experience Manager Assets Essentials** para enriquecer seus emails, crie e gerencie seu próprio banco de dados de ativos.

* Localizar **Fotos do Adobe Stock** para criar seu conteúdo e melhorar seu design de email.

* Melhore a experiência dos clientes criando **notificações por push, SMS e emails** com base em seus atributos de perfil.

* **Enviar deliveries** com base nesses conteúdos e rastreie o comportamento do cliente.

>[!NOTE]
>
>Os usuários podem acessar, criar, editar e/ou publicar jornadas dependendo de seu perfil de produto. Saiba mais sobre permissões de usuário [nesta seção](../administration/permissions.md).


## Adicionar mensagens em suas jornadas{#messages-in-journeys}

>[!CONTEXTUALHELP]
>id="ajo_message_category"
>title="Categoria de mensagem"
>abstract="Escolha Marketing para mensagens comerciais ou Transacional para mensagens não comerciais, como confirmação de pedido, notificações de redefinição de senha ou informações de delivery"

>[!CONTEXTUALHELP]
>id="ajo_message_surface"
>title="Superfície do canal"
>abstract="Uma superfície de canal é uma instância desse canal que tem todas as configurações para fornecer uma ação com êxito por meio de uma campanha ou jornada. Ele é definido por um administrador do sistema."

Para adicionar mensagens em suas jornadas, basta adicionar uma atividade de push, SMS ou email nas telas do jornada.

1. Inicie a jornada com uma [Evento](../building-journeys/general-events.md) ou [Ler segmento](../building-journeys/read-segment.md) atividade .

1. No **Ações** seção da paleta, arraste e solte uma **email**, um **SMS** ou **Empurrar** atividade na tela.

   ![](assets/add-a-message.png)

1. Insira um rótulo e uma descrição.

1. Selecionar a mensagem **[!UICONTROL Category]**: Choose **Marketing** para mensagens comerciais, ou **Transacional** para mensagens não comerciais, como confirmação de pedido, notificações de redefinição de senha ou informações de delivery.

   >[!CAUTION]
   >
   >Se você definiu [regras de frequência](../configuration/frequency-rules.md) para um canal e categoria específicos, eles são aplicados automaticamente à mensagem ao selecionar esse canal e categoria. Atualmente, somente o **[!UICONTROL Marketing]** está disponível para regras de frequência.

   ![](assets/inline-message-category.png)

   >[!CAUTION]
   >
   >As mensagens de tipo de marketing devem incluir um [link para opção de não participação](../messages/consent.md#opt-out-management). Isso não é necessário para mensagens transacionais, pois essas mensagens podem ser enviadas a perfis que cancelaram a assinatura nas comunicações de marketing.

1. Selecionar o canal **[!UICONTROL Surface]** (ou seja, predefinição de mensagem) a ser usada para enviar a mensagem.

   Uma superfície é uma configuração que foi definida por uma [Administrador do sistema](../start/path/administrator.md). Ela contém todos os parâmetros técnicos para enviar a mensagem, como parâmetros de cabeçalho, subdomínio, aplicativos móveis, etc. [Saiba mais](../configuration/channel-surfaces.md).

   >[!CAUTION]
   >
   >Você deve escolher uma superfície de canal válida para a categoria e o canal de mensagens selecionados.

   Você pode acessar e modificar o rótulo, a descrição e a superfície da mensagem a qualquer momento usando o **[!UICONTROL Properties]** na interface da mensagem.

1. Criar o conteúdo da mensagem.

   Saiba mais sobre as etapas detalhadas para criar o conteúdo da mensagem na seguinte página:

   * [Criar um email](create-email.md)
   * [Criar uma notificação por push](create-push.md)
   * [Criar uma mensagem de SMS.](create-sms.md)

## Ativar otimização de tempo de envio{#sto-in-journeys}

Para notificações por email e por push, é possível habilitar **[!UICONTROL Send-time optimization]**.

Use **[!UICONTROL Send-time optimization]** para agendar tempos de envio personalizados para cada usuário a fim de aumentar as taxas de abertura e de clique de suas mensagens. [Saiba mais](../messages/send-time-optimization.md).


## Parâmetros avançados{#adv-settings}

Parâmetros avançados são somente leitura e ocultos por padrão.

Para acessar parâmetros avançados, clique no botão **[!UICONTROL Show read-only fields]** ícone na parte superior do painel de mensagens.

![](assets/show-read-only.png)

Parâmetros avançados são exibidos na parte inferior do painel de mensagens. Esses parâmetros são definidos pela variável [administrador do sistema](../start/path/administrator.md) no [superfície do canal](../configuration/channel-surfaces.md) (ou seja, predefinição de mensagem) associada à mensagem.

Para notificações por push, você pode exibir os seguintes parâmetros: Token, AppID, AppPlatform.

![](assets/push-adv-parameters.png)

Para email, você pode exibir o endereço de email principal.

Para uso específico, é possível substituir esses valores em contextos específicos. Para forçar um valor, clique no botão **Habilitar substituição de parâmetro** à direita do campo . Essa opção pode ser útil, por exemplo, para:

* Teste um email e você pode adicionar seu endereço de email. Após publicar a jornada, o email será enviado para você.
* Consulte o endereço de email dos assinantes de uma lista. Saiba mais em [este caso de uso](../building-journeys/message-to-subscribers-uc.md).

Clique no mesmo ícone para redefinir para o parâmetro padrão.


## Procurar mensagens{#browse-message}

Quando várias mensagens são usadas em uma jornada, é possível alternar de uma para outra a partir da variável **Editar conteúdo** tela.

![](assets/inline-messages-multi-content.png)

Você pode [verificar alertas](alerts.md) e [simulação](../design/preview.md) cada conteúdo de uma única visualização.

## Duplicar uma mensagem {#duplicate-message}

Você pode copiar uma mensagem existente da tela de jornada.

Para fazer isso, siga as etapas abaixo:

1. Selecione a mensagem que deseja copiar.

1. Use o **[!UICONTROL Copy]** do botão **[!UICONTROL Action]** painel.

   ![](assets/message-duplicate.png)

1. Enter **crtl+V** para colar a mensagem.

   A mensagem é adicionada às telas de jornada. Todas as definições e configurações serão copiadas para a nova mensagem.

   ![](assets/message-duplicated.png)

1. Renomeie a mensagem para poder diferenciar a mensagem inicial da cópia, por exemplo, ao editar mensagens, conforme abaixo:

   ![](assets/multi-message.png)


>[!NOTE]
>
>Para emails, você também pode transformar uma mensagem existente em um modelo. [Saiba mais](../design/email-templates.md).

## Excluir uma mensagem{#delete-message}

Para excluir uma mensagem, use o ícone de lixeira na parte superior do painel de atividade do canal.

![](assets/delete-message.png)

Use o **[!UICONTROL Confirm]** botão para validar.
