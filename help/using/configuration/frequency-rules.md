---
title: Regras de frequência
description: Saiba como definir regras de frequência
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 49248fb6-5a91-45b2-9de8-2f078d59c0fc
source-git-commit: 76eb73e875cbdeb7b5821f0c63435cf96c532adc
workflow-type: tm+mt
source-wordcount: '865'
ht-degree: 1%

---

# Regras de frequência de mensagem {#frequency-rules}

[!DNL Journey Optimizer] permite controlar a frequência com que os usuários receberão uma mensagem ou inserirão em uma jornada, definindo regras entre canais que excluirão automaticamente perfis excessivamente solicitados de mensagens e ações.

Por exemplo, você não quer que sua marca envie mais de 3 mensagens de marketing por mês para seus clientes.

Para fazer isso, você pode usar uma regra de frequência que limitará o número de mensagens enviadas com base em um ou mais canais durante um período de calendário mensal.

>[!NOTE]
>
>As regras de frequência de mensagem são diferentes do gerenciamento de recusa, que permite que os usuários cancelem a assinatura do recebimento de comunicações de uma marca. [Saiba mais](../messages/consent.md#opt-out-management)

## Regras de acesso {#access-rules}

As regras estão disponíveis na **[!UICONTROL Administration]** > **[!UICONTROL Rules]** menu. Todas as regras são listadas, classificadas por data de modificação.

Use o ícone de filtro para filtrar na categoria, no status e/ou no canal. Você também pode pesquisar no rótulo da mensagem.

![](assets/message-rules-filter.png)

### Permissões{#permissions-frequency-rules}

Para acessar, criar, editar ou excluir regras de frequência de mensagem, você deve ter a variável **[!UICONTROL Manage frequency rules]** permissão.

Usuários com a **[!UICONTROL View frequency rules]** as permissões do podem exibir regras, mas não para modificá-las ou excluí-las.

![](assets/message-rules-access.png)

Saiba mais sobre permissões em [esta seção](../administration/high-low-permissions.md).

## Criar uma regra {#create-new-rule}

Para criar uma nova regra, siga as etapas abaixo.

1. Acesse o **[!UICONTROL Message frequency rules]** e, em seguida, clique em **[!UICONTROL Create rule]**.

   ![](assets/message-rules-create.png)

1. Defina o nome da regra.

   ![](assets/message-rules-details.png)

1. Selecione a categoria da regra de mensagem.

   >[!NOTE]
   >
   >Atualmente, somente o **[!UICONTROL Marketing]** está disponível.

1. Defina o limite para sua regra, o que significa o número máximo de mensagens que podem ser enviadas para um perfil de usuário individual a cada mês.

   ![](assets/message-rules-capping.png)

   >[!NOTE]
   >
   >O limite de frequência baseia-se num período de calendário mensal. Ele é redefinido no início de cada mês.

1. Selecione o canal que deseja usar para esta regra: **[!UICONTROL Email]** ou **[!UICONTROL Push notification]**.

   ![](assets/message-rules-channels.png)

   >[!NOTE]
   >
   >Você deve selecionar pelo menos um canal para criar a regra.

1. Selecione vários canais se desejar aplicar o limite em todos os canais selecionados como uma contagem total.

   Por exemplo, defina o limite como 15 e selecione os canais de email e push. Se um perfil já tiver recebido 10 emails de marketing e 5 notificações por push de marketing, ele será excluído do próximo delivery de qualquer email de marketing ou notificação por push.

1. Clique em **[!UICONTROL Save as draft]** para confirmar a criação da regra. Sua mensagem é adicionada à lista de regras, com a variável **[!UICONTROL Draft]** status.

   ![](assets/message-rules-created.png)

## Ativar uma regra {#activate-rule}

Quando criada, uma regra de frequência de mensagem tem a variável **[!UICONTROL Draft]** e ainda não está afetando nenhuma mensagem. Para habilitá-lo, clique nas reticências ao lado da regra e selecione **[!UICONTROL Activate]**.

![](assets/message-rules-activate.png)

Ativar uma regra afetará as mensagens que ela se aplicar à próxima execução. Saiba como [aplicar uma regra de frequência a uma mensagem](#apply-frequency-rule).

>[!NOTE]
>
>Pode levar até 10 minutos para que uma regra seja totalmente ativada. Não é necessário modificar ou republicar mensagens ou jornadas para que uma regra entre em vigor.

Para desativar uma regra de frequência de mensagem, clique nas reticências ao lado da regra e selecione **[!UICONTROL Deactivate]**.

![](assets/message-rules-deactivate.png)

O status da regra será alterado para **[!UICONTROL Inactive]** e a regra não se aplicará a execuções futuras de mensagens. As mensagens atualmente em execução não serão afetadas.

>[!NOTE]
>
>Desativar uma regra não afeta ou redefine nenhuma contagem em perfis individuais.

## Aplicar uma regra de frequência a uma mensagem {#apply-frequency-rule}

Para aplicar uma regra de frequência a uma mensagem, siga as etapas abaixo.

1. Criar uma mensagem. [Saiba mais](../messages/get-started-content.md#create-new-message)

1. Selecione a categoria definida para a variável [regra criada](#create-new-rule).

   ![](assets/message-rules-msg-properties.png)

   >[!NOTE]
   >
   >Atualmente, somente o **[!UICONTROL Marketing]** está disponível para as regras de frequência de mensagem.

1. Selecione os canais escolhidos para a mensagem.

   ![](assets/message-rules-msg-channels.png)

1. Você pode clicar no botão **[!UICONTROL Frequency rule]** link para exibir as regras de frequência que serão aplicadas à categoria e aos canais selecionados.

   ![](assets/message-rules-msg-link.png)

   Uma nova guia será aberta para exibir as regras de frequência de mensagem correspondentes.

1. [Design](../design/design-emails.md) e [publicar](../messages/publish-manage-message.md) sua mensagem.

Todas as regras de frequência que correspondem à categoria e aos canais selecionados serão automaticamente aplicadas a esta mensagem.

>[!NOTE]
>
>Mensagens <!--that do not have any selected category or messages -->em que a categoria selecionada é **[!UICONTROL Transactional]** não serão avaliadas com base nas regras de frequência.

<!--Clicking the link out button next to the category selector will jump you over to the rules inventory screen to see which rules will be applied to the message.-->

Você pode visualizar o número de perfis excluídos do delivery na [Exibições ao vivo e globais](../reports/message-monitoring.md)e no [relatório ao vivo por email](../reports/email-live-report.md), onde as regras de frequência serão listadas como um possível motivo para os usuários excluídos do delivery.

>[!NOTE]
>
>Várias regras podem ser aplicadas ao mesmo canal, mas uma vez que o limite inferior é atingido, o perfil será excluído dos próximos deliveries.

## Exemplo: combinar várias regras {#frequency-rule-example}

Você pode combinar várias regras de frequência de mensagem, como descrito no exemplo abaixo.

1. [Criar uma regra](#create-new-rule) chamado *Limite geral de marketing*:

   * Selecione todos os canais (Email, Push).
   * Defina o limite como 12.

   ![](assets/message-rules-ex-overall-cap.png)

1. Para restringir ainda mais o número de notificações por push baseadas em marketing enviadas por um usuário, crie uma segunda regra chamada *Push*:

   * Selecione Canal de push.
   * Defina o limite como 4.

   ![](assets/message-rules-ex-push-cap.png)

1. Salvar e [ativar](#activate-rule) a regra.

1. Criar uma mensagem. [Saiba mais](../messages/get-started-content.md#create-new-message)

1. Selecione o **[!UICONTROL Marketing]** categoria .

   ![](assets/message-rules-ex-category-maktg.png)

1. Selecione o **[!UICONTROL Email]** e **[!UICONTROL Push Notification]** canais.

   ![](assets/message-rules-ex-channels.png)

1. Você pode clicar no botão **[!UICONTROL Frequency rule]** link para exibir as regras de frequência que serão aplicadas à categoria e aos canais selecionados.

1. [Design](../design/design-emails.md) e [publicar](../messages/publish-manage-message.md) sua mensagem.

Nesse cenário, um perfil individual:
* Pode receber até 12 mensagens de marketing por mês;
* mas serão excluídas das notificações por push de marketing depois de terem recebido quatro notificações por push.

>[!NOTE]
>
>Ao testar as regras de frequência, pode ser útil começar com uma [perfil de teste](../segment/creating-test-profiles.md), pois assim que o limite de frequência de um perfil é atingido, não há como redefinir o contador até o mês seguinte. Desativar uma regra permitirá que perfis com limites recebam mensagens, mas não removerá ou excluirá quaisquer incrementos de contador.
