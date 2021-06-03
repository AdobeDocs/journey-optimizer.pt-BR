---
title: Criar predefinições de mensagem
description: Saiba como criar predefinições de mensagens de email e de notificação por push
source-git-commit: 4353b8f01bb4e47f6f2384e464341c0ee80ecaf2
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---


# Criar predefinições de mensagem

Com [!DNL Journey Optimizer], você pode configurar predefinições de mensagens que definem todos os parâmetros técnicos necessários para mensagens de email e de notificação por push (tipo de email, email e nome do remetente, aplicativos móveis etc.).

Você pode configurar quantas predefinições de mensagem desejar, dependendo das diferentes marcas que precisam se comunicar.

Após configurar as predefinições de mensagem, é possível selecioná-las ao criar mensagens na lista **[!UICONTROL Presets]**.

## Criar uma predefinição de mensagem {#create-message-preset}

Para criar uma predefinição de mensagem, siga estas etapas:

1. Acesse o menu **[!UICONTROL Channels]** / **[!UICONTROL Message presets]** e clique em **[!UICONTROL Create Message preset]**.

   ![](../assets/preset-create.png)

1. Forneça um nome e uma descrição (opcional) para a predefinição, em seguida, especifique os canais que deseja configurar.

   ![](../assets/preset-general.png)

1. Defina as configurações de email e notificação por push:

   Para o canal de email, especifique:

   * O tipo de comunicações que será enviado com a predefinição (mensagens transacionais ou de marketing),
   * O [subdomínio](about-subdomain-delegation.md) a ser usado para enviar emails,
   * O [pool IP](ip-pools.md) para associar com a predefinição,
   * Os parâmetros de cabeçalho a serem usados para os emails enviados usando a predefinição.

   ![](../assets/preset-email.png)

   Para o canal de notificação por push, especifique os aplicativos móveis IOS e/ou Android que serão usados para suas mensagens. Para obter mais informações sobre como configurar seu ambiente para enviar notificações por push, consulte [esta seção](../push-configuration.md).

   ![](../assets/preset-push.png)

1. Depois que todos os parâmetros tiverem sido configurados, clique em **[!UICONTROL Submit]** para confirmar. Você também pode salvar a predefinição de mensagem como rascunho e retomar sua configuração posteriormente.

   ![](../assets/preset-submit.png)

1. Depois que a predefinição de mensagem tiver sido criada, ela será exibida na lista com o status **[!UICONTROL Processing]**.

   Durante essa etapa, várias verificações serão executadas para verificar se foram configuradas corretamente. O tempo de processamento é de aproximadamente 48h a 72h e pode levar de 7 a 10 dias.

   Essas verificações incluem testes de deliverability realizados pela equipe de deliverability do Adobe:

   * validação de SPF,
   * Validação de DKIM,
   * validação de registro MX,
   * Verificar a inclusão de IPs na blacklist,
   * Helo host check,
   * Verificação do conjunto IP,
   * Registro A/PTR, verificação de subdomínio t/m/res.

1. Depois que as verificações são bem-sucedidas, a predefinição de mensagem recebe o status **[!UICONTROL Active]** . Ele está pronto para ser usado para entregar mensagens.

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/preset-active.png)

## Monitorar predefinições de mensagem

Todas as predefinições de mensagem são exibidas no menu **[!UICONTROL Channels]** / **[!UICONTROL Message presets]**. Os filtros estão disponíveis para ajudar você a navegar pela lista (tipo de canal, usuário, status).

![](../assets/preset-filters.png)

As predefinições de mensagem podem ter os seguintes status:

* **[!UICONTROL Draft]**: A predefinição de mensagem foi salva como rascunho e ainda não foi enviada. Abra-o para retomar a configuração.
* **[!UICONTROL Processing]**: A predefinição de mensagem foi enviada e está passando por várias etapas de verificação.
* **[!UICONTROL Active]**: A predefinição de mensagem foi verificada e pode ser selecionada para criar mensagens.
* **[!UICONTROL Failed]**: Uma ou várias verificações falharam durante a verificação da predefinição de mensagem.
* **[!UICONTROL De-activated]**: A predefinição de mensagem é desativada. Ele não pode ser usado para criar novas mensagens.

## Editar predefinições de mensagem

Para editar uma predefinição de mensagem, primeiro é necessário desativá-la para torná-la indisponível para criar novas mensagens (as mensagens publicadas usando essa predefinição não serão afetadas e continuarão funcionando). Em seguida, é necessário duplicar a predefinição de mensagem para criar uma nova versão que será usada para criar novas mensagens:

1. Acesse a lista de predefinições de mensagens e desative a predefinição de mensagens que deseja editar.

   ![](../assets/preset-deactivate.png)

1. Duplique a predefinição de mensagem desativada. Uma cópia com o status **[!UICONTROL Draft]** é adicionada automaticamente à lista.

   ![](../assets/preset-duplicated.png)

1. Abra a predefinição de mensagem duplicada, modifique-a de acordo com suas necessidades e envie suas alterações. A predefinição de mensagem passará pelo mesmo ciclo de validação que durante a etapa de [criação](#create-message-preset).

1. Depois de validado, ele obtém o status **[!UICONTROL Active]** e está pronto para ser usado para criar novas mensagens.

   >[!NOTE]
   >
   >As predefinições de mensagens desativadas não podem ser excluídas para evitar qualquer problema nas jornadas que usam essas predefinições para enviar mensagens.