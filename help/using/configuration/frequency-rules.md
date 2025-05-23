---
solution: Journey Optimizer
product: journey optimizer
title: Configurar regras de negócios
description: Saiba como definir regras de frequência de negócios
feature: Rules
topic: Content Management
role: User
level: Intermediate
hidefromtoc: true
hide: true
robots: noindex
googlebot: noindex
keywords: mensagem, frequência, regras, pressão
exl-id: 49248fb6-5a91-45b2-9de8-2f078d59c0fc
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '1267'
ht-degree: 14%

---

# Configurar regra de negócios {#frequency-rules}

>[!CONTEXTUALHELP]
>id="ajo_business_rules_message_frequency_rules"
>title="Regras de negócios"
>abstract="Regras de frequência de mensagem são um tipo de regra de negócios que restringe o número de vezes que usuários recebem mensagens ou entram em jornadas em um ou vários canais. Essas regras entre canais excluem automaticamente perfis excessivamente solicitados de mensagens e ações."

[!DNL Journey Optimizer] permite controlar a frequência com que os usuários receberão uma mensagem ou entrarão em uma jornada em um ou vários canais. Regras de frequência de mensagem que excluem automaticamente perfis excessivamente solicitados de mensagens e ações.

Por exemplo, para uma marca, uma regra poderia ser não enviar mais de 4 mensagens de marketing por mês para seus clientes. Para fazer isso, você pode usar uma regra de negócios que limitará o número de mensagens enviadas com base em um ou mais canais durante um período de calendário mensal.

![](assets/do-not-localize/sms-dm-rules.gif)

>[!NOTE]
>
>As regras de negócios são diferentes do gerenciamento de recusa, que permite que os usuários cancelem a inscrição do recebimento de comunicações de uma marca. [Saiba mais](../privacy/opt-out.md#opt-out-management)

➡️ [Descubra este recurso no vídeo](#video)

## Acessar regras de negócios {#access-rules}

Regras de negócio estão disponíveis no menu **[!UICONTROL Administração]** > **[!UICONTROL Regras de negócio]**. Todas as regras são listadas e classificadas por data de modificação. Use o ícone de filtro para filtrar a categoria, o status e/ou o canal. Também é possível pesquisar pelo rótulo da mensagem.

![](assets/message-rules-filter.png)

### Permissões{#permissions-frequency-rules}

Para acessar, criar, editar ou excluir regras de negócios, você deve ter a permissão **[!UICONTROL Gerenciar regras de frequência]**.

Os usuários com a permissão **[!UICONTROL Exibir regras de frequência]** podem exibir regras, mas não podem modificá-las ou excluí-las.

![](assets/message-rules-access.png)

Saiba mais sobre permissões [nesta seção](../administration/high-low-permissions.md).

## Criar uma regra de negócios {#create-new-rule}

>[!CONTEXTUALHELP]
>id="ajo_rules_category"
>title="Selecionar a categoria da regra da mensagem"
>abstract="Quando ativadas e aplicadas a uma mensagem, todas as regras de negócios correspondentes à categoria selecionada são automaticamente aplicadas a essa mensagem. Atualmente, somente a categoria Marketing está disponível."

>[!CONTEXTUALHELP]
>id="ajo_rules_capping"
>title="Definir o limite para a regra de negócios"
>abstract="Especifique o número máximo de mensagens enviadas a um perfil de cliente no intervalo de tempo escolhido. O limite de frequência será baseado no período do calendário selecionado e redefinido no início do intervalo de tempo correspondente."

>[!CONTEXTUALHELP]
>id="ajo_rules_channel"
>title="Definir os canais aos quais a regra de negócios se aplica"
>abstract="Selecione pelo menos um canal. O limite se aplica em canais como uma contagem total."

Para criar uma nova regra de negócios, siga as etapas abaixo.

1. Acesse a lista **[!UICONTROL Regras de negócio]** e clique em **[!UICONTROL Criar regra]**.

   ![](assets/message-rules-create.png)

1. Defina o nome da regra e selecione a categoria de regra de mensagem.

   >[!NOTE]
   >
   >Somente a categoria **[!UICONTROL Marketing]** está disponível.

   ![](assets/message-rules-details.png)

1. Na lista suspensa **[!UICONTROL Duração]**, selecione um período para a limitação a ser aplicada. [Saiba mais](#frequency-cap)

1. Defina o limite para sua regra, o que significa o número máximo de mensagens que podem ser enviadas para um perfil de usuário individual a cada mês ou semana <!--or day--> - de acordo com sua seleção acima.

   <!--![](assets/message-rules-capping.png)-->

1. Selecione o canal que deseja usar para esta regra: **[!UICONTROL Email]**, **[!UICONTROL Notificação por push]**, **[!UICONTROL SMS]** ou **[!UICONTROL Correspondência direta]**.

   ![](assets/message-rules-channels.png)

   >[!NOTE]
   >
   >Você deve selecionar pelo menos um canal para criar a regra.

1. Selecione vários canais se desejar aplicar o limite em todos os canais selecionados como uma contagem total.

   Por exemplo, defina o limite como 15 e selecione os canais de email e de push. Se um perfil já tiver recebido 10 emails de marketing e 5 notificações por push de marketing para o período selecionado, esse perfil será excluído da próxima entrega de qualquer email de marketing ou notificação por push.

1. Clique em **[!UICONTROL Salvar como rascunho]** para confirmar a criação da regra. Sua mensagem foi adicionada à lista de regras, com o status **[!UICONTROL Rascunho]**.

   ![](assets/message-rules-created.png)

### Limite de frequência {#frequency-cap}

Na lista suspensa **[!UICONTROL Duração]**, selecione se deseja que o limite seja aplicado mensal ou semanalmente.

>[!NOTE]
>
>O limite de frequência diária também está disponível por demanda. [Saiba mais](#daily-frequency-cap)

O limite de frequência se baseia no período de calendário selecionado. Ela é redefinida no início do intervalo de tempo correspondente.

![](assets/message-rules-capping-duration.png)

O prazo de validade do contador para cada período é o seguinte:

* **[!UICONTROL Mensal]**: o limite de frequência é válido até o último dia do mês às 23:59:59 UTC. Por exemplo, a expiração mensal de janeiro é 01-31 23:59:59 UTC.

* **[!UICONTROL Semanalmente]**: o limite de frequência é válido até sábado, 23:59:59 UTC dessa semana, pois a semana do calendário começa no domingo. A expiração ocorre independentemente da criação da regra. Por exemplo, se a regra for criada na quinta-feira, ela será válida até o sábado às 23:59:59.

### Limite de frequência diário {#daily-frequency-cap}

Além de mensalmente e semanalmente, o limite de frequência diária também está disponível sob demanda. Para obter mais informações, entre em contato com o representante da Adobe.

O limite de frequência diária é válido para o dia até 23:59:59 UTC e é redefinido para 0 no início do dia seguinte.

>[!NOTE]
>
>Para garantir a precisão das regras diárias de limite de frequência, é recomendado o uso de [segmentação por transmissão](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html?lang=pt-BR){target="_blank"}. Saiba mais sobre os métodos de avaliação de público em [esta seção](../audience/about-audiences.md#evaluation-method-in-journey-optimizer).

## Ativar uma regra de negócios {#activate-rule}

Quando criada, uma regra de negócios tem o status **[!UICONTROL Rascunho]** e ainda não está afetando nenhuma mensagem. Para habilitá-la, clique nas reticências ao lado da regra e selecione **[!UICONTROL Ativar]**.

![](assets/message-rules-activate.png)

A ativação de uma regra afetará qualquer mensagem à qual ela se aplica em sua próxima execução. Saiba como [aplicar uma regra de negócios a uma mensagem](#apply-frequency-rule).

>[!NOTE]
>
>Pode levar até 10 minutos para que uma regra seja totalmente ativada. Não é necessário modificar mensagens ou republicar jornadas para que uma regra entre em vigor.

Para desativar uma regra de negócios, clique nas reticências ao lado da regra e selecione **[!UICONTROL Desativar]**.

![](assets/message-rules-deactivate.png)

O status da regra será alterado para **[!UICONTROL Inativo]** e a regra não se aplicará a futuras execuções de mensagem. As mensagens em execução no momento não serão afetadas.

>[!NOTE]
>
>A desativação de uma regra não afeta nem redefine nenhuma contagem em perfis individuais.

## Aplicar uma regra de negócios a uma mensagem {#apply-frequency-rule}

Para aplicar uma regra de negócios a uma mensagem, siga as etapas abaixo.

1. Ao criar uma [jornada](../building-journeys/journey-gs.md), adicione uma mensagem selecionando um dos canais definidos para a regra.

1. Selecione a categoria que você definiu para a [regra criada](#create-new-rule).

   ![](assets/journey-message-category.png)

   >[!NOTE]
   >
   >Atualmente, apenas a categoria **[!UICONTROL Marketing]** está disponível para regras de negócios.

1. Você pode clicar no link **[!UICONTROL Regra de frequência]** para exibir a tela de regras de frequência em uma nova guia. [Saiba mais](#access-rules)

   Todas as regras que correspondem à categoria e aos canais selecionados serão aplicadas automaticamente a esta mensagem.

   >[!NOTE]
   >
   >As mensagens em que a categoria selecionada é **[!UICONTROL Transacional]** não serão avaliadas em relação às regras de frequência.

1. Você pode visualizar o número de perfis excluídos da entrega no [Relatório do Customer Journey Analytics](../reports/report-gs-cja.md) e no [Relatório em tempo real](../reports/live-report.md), em que as regras de negócios serão listadas como um possível motivo para os usuários excluídos da entrega.

>[!NOTE]
>
>Várias regras podem ser aplicadas ao mesmo canal, mas quando o limite inferior for atingido, o perfil será excluído dos próximos deliveries.

## Exemplo: combinar várias regras {#frequency-rule-example}

É possível combinar várias regras de negócios, conforme descrito no exemplo abaixo.

1. [Crie uma regra de negócios](#create-new-rule) chamada *Limite de Marketing Geral*:

   * Selecione todos os canais.
   * Defina o limite para 12 mensais.

   ![](assets/message-rules-ex-overall-cap.png)

1. Para restringir ainda mais o número de notificações por push com base em marketing enviadas por um usuário, crie uma segunda regra chamada *Push Marketing Cap*:

   * Selecione Canal de push.
   * Defina o limite como 4 por mês.

   ![](assets/message-rules-ex-push-cap.png)

1. Salve e [ative](#activate-rule) a regra.

1. [Crie uma mensagem](../building-journeys/journeys-message.md) para cada canal através do qual deseja se comunicar e selecione a categoria **[!UICONTROL Marketing]** para cada mensagem. [Saiba como aplicar uma regra de negócios](#apply-frequency-rule)

   ![](assets/journey-message-category.png)


<!--
Learn how to create a message for the different channels in the following sections:
* [Create an email](../email/create-email.md)
* [Create a push notification](../push/create-push.md)
* [Create an SMS](../sms/create-sms.md)
* [Create a direct mail](../direct-mail/create-direct-mail.md)

Create an email and select the **[!UICONTROL Marketing]** category for that message. [Learn more](../email/create-email.md)

Create a push notification and select the **[!UICONTROL Marketing]** category for that message. [Learn more](../push/create-push.md)

Create an SMS and select the **[!UICONTROL Marketing]** category for that message. [Learn more](../sms/create-sms.md)

Create a direct mail and select the **[!UICONTROL Marketing]** category for that message. [Learn more](../direct-mail/create-direct-mail.md)
-->

Nesse cenário, um perfil individual:
* pode receber até 12 mensagens de marketing por mês;
* mas serão excluídos das notificações por push de marketing depois que receberem 4 notificações por push.

>[!NOTE]
>
>Ao testar regras de negócios, é recomendável usar um [perfil de teste](../audience/creating-test-profiles.md) recém-criado, pois, quando o limite de frequência de um perfil é atingido, não há como redefinir o contador até o próximo mês. A desativação de uma regra permitirá que perfis limitados recebam mensagens, mas não removerá nem excluirá incrementos de contador.

## Vídeo tutorial {#video}

Saiba como criar, ativar, testar e relatar regras de negócios.

>[!VIDEO](https://video.tv.adobe.com/v/344451?quality=12)
