---
solution: Journey Optimizer
product: journey optimizer
title: Regras de frequência
description: Saiba como definir regras de frequência
feature: Rules
topic: Content Management
role: User
level: Intermediate
keywords: mensagem, frequência, regras, pressão
exl-id: 49248fb6-5a91-45b2-9de8-2f078d59c0fc
source-git-commit: 12f6c41252809bcc85bc076902f9a831a6c6e7d9
workflow-type: tm+mt
source-wordcount: '1219'
ht-degree: 11%

---

# Regras de frequência de mensagem {#frequency-rules}

[!DNL Journey Optimizer] permite controlar a frequência com que os usuários receberão uma mensagem ou entrarão em uma jornada definindo regras entre canais que excluirão automaticamente perfis excessivamente solicitados de mensagens e ações.

Por exemplo, para uma marca, uma regra poderia ser não enviar mais de 4 mensagens de marketing por mês para seus clientes. Para fazer isso, você pode usar uma regra de frequência que limitará o número de mensagens enviadas com base em um ou mais canais durante um período de calendário mensal.

![](assets/do-not-localize/sms-dm-rules.gif)

>[!NOTE]
>
>As regras de frequência de mensagem são diferentes do gerenciamento de recusa, que permite que os usuários cancelem a inscrição do recebimento de comunicações de uma marca. [Saiba mais](../privacy/opt-out.md#opt-out-management)

➡️ [Descubra este recurso no vídeo](#video)

## Regras de acesso {#access-rules}

As regras estão disponíveis no **[!UICONTROL Administração]** > **[!UICONTROL Regras]** menu. Todas as regras são listadas e classificadas por data de modificação.

Use o ícone de filtro para filtrar a categoria, o status e/ou o canal. Também é possível pesquisar pelo rótulo da mensagem.

![](assets/message-rules-filter.png)

### Permissões{#permissions-frequency-rules}

Para acessar, criar, editar ou excluir regras de frequência de mensagem, você deve ter a **[!UICONTROL Gerenciar regras de frequência]** permissão.

Usuários com o **[!UICONTROL Exibir regras de frequência]** As permissões do podem exibir regras, mas não podem modificá-las ou excluí-las.

![](assets/message-rules-access.png)

Saiba mais sobre permissões [nesta seção](../administration/high-low-permissions.md).

## Criar uma regra {#create-new-rule}

>[!CONTEXTUALHELP]
>id="ajo_rules_category"
>title="Selecionar a categoria da regra de mensagem"
>abstract="Quando ativadas e aplicadas a uma mensagem, todas as regras de frequência correspondentes à categoria selecionada serão automaticamente aplicadas a essa mensagem. Atualmente, somente a categoria Marketing está disponível."

>[!CONTEXTUALHELP]
>id="ajo_rules_capping"
>title="Definir o limite para a regra"
>abstract="Especifique o número máximo de mensagens enviadas a um perfil de cliente no intervalo de tempo escolhido. O limite de frequência será baseado no período do calendário selecionado e redefinido no início do intervalo de tempo correspondente. "

>[!CONTEXTUALHELP]
>id="ajo_rules_channel"
>title="Definir os canais aos quais a regra se aplica"
>abstract="Selecione pelo menos um canal. O limite se aplica em canais como uma contagem total."

Para criar uma nova regra, siga as etapas abaixo.

1. Acesse o **[!UICONTROL Regras de frequência de mensagem]** e clique em **[!UICONTROL Criar regra]**.

   ![](assets/message-rules-create.png)

1. Defina o nome da regra e selecione a categoria de regra de mensagem.

   >[!NOTE]
   >
   >Somente o **[!UICONTROL Marketing]** categoria está disponível.

   ![](assets/message-rules-details.png)

1. No **[!UICONTROL Duração]** selecione um intervalo de tempo para a limitação a ser aplicada. [Saiba mais](#frequency-cap)

1. Defina o limite para sua regra, o que significa o número máximo de mensagens que podem ser enviadas para um perfil de usuário individual a cada mês ou semana <!--or day--> - de acordo com sua seleção acima.

   <!--![](assets/message-rules-capping.png)-->

1. Selecione o canal que deseja usar para esta regra: **[!UICONTROL E-mail]**, **[!UICONTROL Notificação por push]**, **[!UICONTROL SMS]** ou **[!UICONTROL Correspondência direta]**.

   ![](assets/message-rules-channels.png)

   >[!NOTE]
   >
   >Você deve selecionar pelo menos um canal para criar a regra.

1. Selecione vários canais se desejar aplicar o limite em todos os canais selecionados como uma contagem total.

   Por exemplo, defina o limite como 15 e selecione os canais de email e de push. Se um perfil já tiver recebido 10 emails de marketing e 5 notificações por push de marketing para o período selecionado, esse perfil será excluído da próxima entrega de qualquer email de marketing ou notificação por push.

1. Clique em **[!UICONTROL Salvar como rascunho]** para confirmar a criação da regra. Sua mensagem é adicionada à lista de regras, com o **[!UICONTROL Rascunho]** status.

   ![](assets/message-rules-created.png)

### Limite de frequência {#frequency-cap}

No **[!UICONTROL Duração]** selecione se deseja que o limite seja aplicado mensal ou semanalmente.

>[!NOTE]
>
>O limite de frequência diária também está disponível por demanda. [Saiba mais](#daily-frequency-cap)

O limite de frequência se baseia no período de calendário selecionado. Ela é redefinida no início do intervalo de tempo correspondente.

![](assets/message-rules-capping-duration.png)

O prazo de validade do contador para cada período é o seguinte:

* **[!UICONTROL Mensal]**: o limite de frequência é válido até o último dia do mês às 23:59:59 UTC. Por exemplo, a expiração mensal de janeiro é 01-31 23:59:59 UTC.

* **[!UICONTROL Semanalmente]**: o limite de frequência é válido até sábado 23:59:59 UTC dessa semana, pois a semana do calendário começa no domingo. A expiração ocorre independentemente da criação da regra. Por exemplo, se a regra for criada na quinta-feira, essa regra será válida até o sábado às 23:59:59.

### Limite de frequência diário {#daily-frequency-cap}

Além de mensalmente e semanalmente, o limite de frequência diária também está disponível sob demanda. Para obter mais informações, entre em contato com o representante da Adobe.

O limite de frequência diária é válido para o dia até 23:59:59 UTC e redefine para 0 no início do dia seguinte.

>[!NOTE]
>
>Para garantir a precisão das regras de limite de frequência diária, a utilização de [segmentação por transmissão](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html){target="_blank"} é recomendada. Saiba mais sobre os métodos de avaliação de público-alvo no [nesta seção](../audience/about-audiences.md#evaluation-method-in-journey-optimizer).

## Ativar uma regra {#activate-rule}

Quando criada, uma regra de frequência de mensagem tem o **[!UICONTROL Rascunho]** e ainda não está afetando nenhuma mensagem. Para ativá-la, clique nas reticências ao lado da regra e selecione **[!UICONTROL Ativar]**.

![](assets/message-rules-activate.png)

A ativação de uma regra afetará qualquer mensagem à qual ela se aplica em sua próxima execução. Saiba como [aplicar uma regra de frequência a uma mensagem](#apply-frequency-rule).

>[!NOTE]
>
>Pode levar até 10 minutos para que uma regra seja totalmente ativada. Não é necessário modificar mensagens ou republicar jornadas para que uma regra entre em vigor.

Para desativar uma regra de frequência de mensagem, clique nas reticências ao lado da regra e selecione **[!UICONTROL Desativar]**.

![](assets/message-rules-deactivate.png)

O status da regra será alterado para **[!UICONTROL Inativo]** e a regra não se aplicará a execuções de mensagens futuras. As mensagens em execução no momento não serão afetadas.

>[!NOTE]
>
>A desativação de uma regra não afeta nem redefine nenhuma contagem em perfis individuais.

## Aplicar uma regra de frequência a uma mensagem {#apply-frequency-rule}

Para aplicar uma regra de frequência a uma mensagem, siga as etapas abaixo.

1. Ao criar uma [jornada](../building-journeys/journey-gs.md), adicione uma mensagem selecionando um dos canais que você definiu para a regra.

1. Selecione a categoria definida para o [regra que você criou](#create-new-rule).

   ![](assets/journey-message-category.png)

   >[!NOTE]
   >
   >Atualmente, somente o **[!UICONTROL Marketing]** A categoria está disponível para regras de frequência de mensagem.

1. Você pode clicar no link **[!UICONTROL Regra de frequência]** link para exibir a tela de regras de frequência em uma nova guia. [Saiba mais](#access-rules)

   Todas as regras de frequência correspondentes à categoria e aos canais selecionados serão aplicadas automaticamente a esta mensagem.

   >[!NOTE]
   >
   >Mensagens em que a categoria selecionada é **[!UICONTROL Transacional]** não serão avaliados em relação às regras de frequência.

1. Você pode exibir o número de perfis excluídos do delivery na variável [Relatório global](../reports/global-report.md), e no [Relatório ao vivo](../reports/live-report.md), em que as regras de frequência serão listadas como um possível motivo para os usuários excluídos do delivery.

>[!NOTE]
>
>Várias regras podem ser aplicadas ao mesmo canal, mas quando o limite inferior for atingido, o perfil será excluído dos próximos deliveries.

## Exemplo: combinar várias regras {#frequency-rule-example}

É possível combinar várias regras de frequência de mensagem, conforme descrito no exemplo abaixo.

1. [Criar uma regra](#create-new-rule) chamado *Limite de marketing geral*:

   * Selecione todos os canais.
   * Defina o limite para 12 mensais.

   ![](assets/message-rules-ex-overall-cap.png)

1. Para restringir ainda mais o número de notificações por push com base em marketing enviadas a um usuário, crie uma segunda regra chamada *Push Marketing Cap*:

   * Selecione Canal de push.
   * Defina o limite como 4 por mês.

   ![](assets/message-rules-ex-push-cap.png)

1. Salvar e [ativar](#activate-rule) a regra.

1. [Criar uma mensagem](../building-journeys/journeys-message.md) para cada canal por meio do qual deseja se comunicar e selecione o **[!UICONTROL Marketing]** categoria para cada mensagem. [Saiba como aplicar uma regra de frequência](#apply-frequency-rule)

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
>Ao testar as regras de frequência, é recomendável usar um recém-criado [perfil de teste](../audience/creating-test-profiles.md), pois quando o limite de frequência de um perfil é atingido, não há como redefinir o contador até o próximo mês. A desativação de uma regra permitirá que perfis limitados recebam mensagens, mas não removerá nem excluirá incrementos de contador.

## Vídeo explicativo {#video}

Saiba como criar, ativar, testar e relatar regras de frequência.

>[!VIDEO](https://video.tv.adobe.com/v/344451?quality=12)
