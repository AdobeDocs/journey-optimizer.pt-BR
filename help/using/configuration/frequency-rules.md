---
solution: Journey Optimizer
product: journey optimizer
title: Regras de frequência
description: Saiba como definir regras de frequência
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: mensagem, frequência, regras, pressão
exl-id: 49248fb6-5a91-45b2-9de8-2f078d59c0fc
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '977'
ht-degree: 12%

---

# Regras de frequência de mensagem {#frequency-rules}

[!DNL Journey Optimizer] permite controlar a frequência com que os usuários receberão uma mensagem ou inserirão em uma jornada, definindo regras entre canais que excluirão automaticamente perfis excessivamente solicitados de mensagens e ações.

Por exemplo, você não quer que sua marca envie mais de 3 mensagens de marketing por mês para seus clientes.

Para fazer isso, você pode usar uma regra de frequência que limitará o número de mensagens enviadas com base em um ou mais canais durante um período de calendário mensal.

>[!NOTE]
>
>As regras de frequência de mensagem são diferentes do gerenciamento de recusa, que permite que os usuários cancelem a assinatura do recebimento de comunicações de uma marca. [Saiba mais](../privacy/opt-out.md#opt-out-management)

➡️ [Descubra este recurso no vídeo](#video)

## Regras de acesso {#access-rules}

As regras estão disponíveis na **[!UICONTROL Administração]** > **[!UICONTROL Regras]** menu. Todas as regras são listadas, classificadas por data de modificação.

Use o ícone de filtro para filtrar na categoria, no status e/ou no canal. Você também pode pesquisar no rótulo da mensagem.

![](assets/message-rules-filter.png)

### Permissões{#permissions-frequency-rules}

Para acessar, criar, editar ou excluir regras de frequência de mensagem, você deve ter a variável **[!UICONTROL Gerenciar regras de frequência]** permissão.

Usuários com a **[!UICONTROL Exibir regras de frequência]** as permissões do podem exibir regras, mas não para modificá-las ou excluí-las.

![](assets/message-rules-access.png)

Saiba mais sobre permissões em [esta seção](../administration/high-low-permissions.md).

## Criar uma regra {#create-new-rule}

>[!CONTEXTUALHELP]
>id="ajo_rules_category"
>title="Selecionar a categoria da regra de mensagem"
>abstract="Quando ativadas e aplicadas a uma mensagem, todas as regras de frequência correspondentes à categoria selecionada serão automaticamente aplicadas a essa mensagem. Atualmente, somente a categoria Marketing está disponível."

>[!CONTEXTUALHELP]
>id="ajo_rules_capping"
>title="Definir o limite para a regra"
>abstract="Especifique o número máximo de mensagens enviadas a um perfil de cliente a cada mês. O limite de frequência será baseado em um período de calendário mensal e será redefinido no início de cada mês."

>[!CONTEXTUALHELP]
>id="ajo_rules_channel"
>title="Definir os canais aos quais a regra se aplica"
>abstract="Selecione pelo menos um canal. O limite se aplica em canais como uma contagem total."

Para criar uma nova regra, siga as etapas abaixo.

1. Acesse o **[!UICONTROL Regras de frequência de mensagem]** e, em seguida, clique em **[!UICONTROL Criar regra]**.

   ![](assets/message-rules-create.png)

1. Defina o nome da regra.

   ![](assets/message-rules-details.png)

1. Selecionar a categoria da regra de mensagem.

   >[!NOTE]
   >
   >Atualmente, somente o **[!UICONTROL Marketing]** está disponível.

1. Defina o limite para sua regra, o que significa o número máximo de mensagens que podem ser enviadas para um perfil de usuário individual a cada mês.

   ![](assets/message-rules-capping.png)

   >[!NOTE]
   >
   >O limite de frequência baseia-se num período de calendário mensal. Ele é redefinido no início de cada mês.

1. Selecione o canal que deseja usar para esta regra: **[!UICONTROL Email]** ou **[!UICONTROL Notificação por push]**.

   ![](assets/message-rules-channels.png)

   >[!NOTE]
   >
   >Você deve selecionar pelo menos um canal para criar a regra.

1. Selecione vários canais se desejar aplicar o limite em todos os canais selecionados como uma contagem total.

   Por exemplo, defina o limite como 15 e selecione os canais de email e push. Se um perfil já tiver recebido 10 emails de marketing e 5 notificações por push de marketing, ele será excluído do próximo delivery de qualquer email de marketing ou notificação por push.

1. Clique em **[!UICONTROL Salvar como rascunho]** para confirmar a criação da regra. Sua mensagem é adicionada à lista de regras, com a variável **[!UICONTROL Rascunho]** status.

   ![](assets/message-rules-created.png)

## Ativar uma regra {#activate-rule}

Quando criada, uma regra de frequência de mensagem tem a variável **[!UICONTROL Rascunho]** e ainda não está afetando nenhuma mensagem. Para habilitá-lo, clique nas reticências ao lado da regra e selecione **[!UICONTROL Ativar]**.

![](assets/message-rules-activate.png)

Ativar uma regra afetará as mensagens que ela se aplicar à próxima execução. Saiba como [aplicar uma regra de frequência a uma mensagem](#apply-frequency-rule).

>[!NOTE]
>
>Pode levar até 10 minutos para que uma regra seja totalmente ativada. Não é necessário modificar mensagens ou republicar jornadas para que uma regra entre em vigor.

Para desativar uma regra de frequência de mensagem, clique nas reticências ao lado da regra e selecione **[!UICONTROL Desativar]**.

![](assets/message-rules-deactivate.png)

O status da regra será alterado para **[!UICONTROL Inativo]** e a regra não se aplicará a execuções futuras de mensagens. As mensagens atualmente em execução não serão afetadas.

>[!NOTE]
>
>Desativar uma regra não afeta ou redefine nenhuma contagem em perfis individuais.

## Aplicar uma regra de frequência a uma mensagem {#apply-frequency-rule}

Para aplicar uma regra de frequência a uma mensagem, siga as etapas abaixo.

1. Ao criar um [jornada](../building-journeys/journey-gs.md), adicione uma mensagem selecionando um dos canais definidos para a regra.

1. Selecione a categoria definida para a variável [regra criada](#create-new-rule).

   ![](assets/journey-message-category.png)

   >[!NOTE]
   >
   >Atualmente, somente o **[!UICONTROL Marketing]** está disponível para as regras de frequência de mensagem.

1. Você pode clicar no botão **[!UICONTROL Regra de frequência]** para exibir a tela de regras de frequência em uma nova guia. [Saiba mais](#access-rules)

   Todas as regras de frequência que correspondem à categoria e aos canais selecionados serão automaticamente aplicadas a esta mensagem.

   >[!NOTE]
   >
   >Mensagens em que a categoria selecionada é **[!UICONTROL Transacional]** não serão avaliadas com base nas regras de frequência.

1. Você pode visualizar o número de perfis excluídos do delivery na [Relatório global](../reports/global-report.md)e no [Relatório ao vivo](../reports/live-report.md), onde as regras de frequência serão listadas como um possível motivo para os usuários excluídos do delivery.

>[!NOTE]
>
>Várias regras podem ser aplicadas ao mesmo canal, mas uma vez que o limite inferior é atingido, o perfil será excluído dos próximos deliveries.

## Exemplo: combinar várias regras {#frequency-rule-example}

Você pode combinar várias regras de frequência de mensagem, como descrito no exemplo abaixo.

1. [Criar uma regra](#create-new-rule) chamado *Limite geral de marketing*:

   * Selecione os canais Email e Push .
   * Defina o limite como 12.

   ![](assets/message-rules-ex-overall-cap.png)

1. Para restringir ainda mais o número de notificações por push baseadas em marketing enviadas por um usuário, crie uma segunda regra chamada *Push*:

   * Selecione Canal de push.
   * Defina o limite como 4.

   ![](assets/message-rules-ex-push-cap.png)

1. Salvar e [ativar](#activate-rule) a regra.

1. Crie um email e selecione o **[!UICONTROL Marketing]** categoria para essa mensagem. [Saiba mais](../email/create-email.md)

1. Crie uma notificação por push e selecione o **[!UICONTROL Marketing]** categoria para essa mensagem. [Saiba mais](../push/create-push.md)

Nesse cenário, um perfil individual:
* Pode receber até 12 mensagens de marketing por mês;
* mas serão excluídas das notificações por push de marketing depois de terem recebido quatro notificações por push.

>[!NOTE]
>
>Ao testar as regras de frequência, é recomendável usar um [perfil de teste](../segment/creating-test-profiles.md), pois assim que o limite de frequência de um perfil é atingido, não há como redefinir o contador até o mês seguinte. Desativar uma regra permitirá que perfis com limites recebam mensagens, mas não removerá ou excluirá quaisquer incrementos de contador.

## Vídeo tutorial {#video}

Saiba como criar, ativar, testar e relatar regras de frequência.

>[!VIDEO](https://video.tv.adobe.com/v/344451?quality=12)
