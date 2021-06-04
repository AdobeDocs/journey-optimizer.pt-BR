---
title: Criar predefinições de mensagem
description: Saiba como configurar e monitorar predefinições de mensagens
source-git-commit: 5490a12f7babc7d615f22f919e58b8eff51cf79c
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 0%

---


# Criar predefinições de mensagem

Com [!DNL Journey Optimizer], é possível configurar predefinições de mensagens que definem todos os parâmetros técnicos necessários para mensagens de email e de notificação por push: tipo de email, email e nome do remetente, aplicativos móveis e muito mais.

>[!CAUTION]
>
> A configuração de predefinições de mensagens é restrita aos Administradores do Jornada. [Saiba mais](../administration/ootb-product-profiles.md#journey-administrator)



Após configurar as predefinições de mensagem, é possível selecioná-las ao criar mensagens na lista **[!UICONTROL Presets]**.

## Criar uma predefinição de mensagem {#create-message-preset}

Para criar uma predefinição de mensagem, siga estas etapas:

1. Acesse o menu **[!UICONTROL Channels]** / **[!UICONTROL Message presets]** e clique em **[!UICONTROL Create Message preset]**.

   ![](../assets/preset-create.png)


1. Insira um nome e uma descrição (opcional) para a predefinição, em seguida, selecione os canais a serem configurados.

   ![](../assets/preset-general.png)


   >[!NOTE]
   >
   > Os nomes devem começar com uma letra (A-Z). Ela só pode conter caracteres alfanuméricos. Você também pode usar caracteres de sublinhado `_`, pontos`.` e hífen `-`.

1. Defina as configurações de **email**.

   ![](../assets/preset-email.png)

   * Selecione o tipo de mensagem que será enviada com a predefinição: **Transacional** ou **Marketing**

      >[!CAUTION]
      >
      > **** As mensagens transacionais podem ser enviadas para perfis que cancelaram a assinatura em comunicações de marketing. Essas mensagens só podem ser enviadas em contextos específicos, como redefinição de senha, status do pedido, notificação de delivery, por exemplo.

   * Selecione o subdomínio a ser usado para enviar os emails. [Saiba mais](about-subdomain-delegation.md)
   * Selecione o pool de IP a ser associado à predefinição. [Saiba mais](ip-pools.md)
   * Insira os parâmetros de cabeçalho para os emails enviados usando a predefinição.

      >[!NOTE]
      >
      > * Os nomes devem começar com uma letra (A-Z). Ela só pode conter caracteres alfanuméricos. Você também pode usar caracteres de sublinhado `_`, pontos`.` e hífen `-`.
         > 
         > 
      * Exceto para o **Responder para (encaminhar email)**, o domínio de endereços de email deve usar o subdomínio selecionado atual.



1. Defina as configurações de **notificação por push**.

   ![](../assets/preset-push.png)

   * Selecione pelo menos uma plataforma: **iOS** e/ou **Android**

   * Selecione os aplicativos móveis a serem usados para cada plataforma.

      Para obter mais informações sobre como configurar seu ambiente para enviar notificações por push, consulte [esta seção](../push-configuration.md).

1. Depois que todos os parâmetros tiverem sido configurados, clique em **[!UICONTROL Submit]** para confirmar. Você também pode salvar a predefinição de mensagem como rascunho e retomar sua configuração posteriormente.

   ![](../assets/preset-submit.png)

1. Depois que a predefinição de mensagem tiver sido criada, ela será exibida na lista com o status **[!UICONTROL Processing]**.

   Durante essa etapa, várias verificações serão executadas para verificar se foram configuradas corretamente. O tempo de processamento é de cerca de **48h-72h** e pode demorar até **7-10 dias**.

   Essas verificações incluem testes de deliverability realizados pela equipe de deliverability do Adobe:


   * Validação de SPF
   * Validação de DKIM
   * Validação de registro MX
   * Verificar IPs inclua na lista de bloqueios
   * Verificação do anfitrião
   * Verificação de pool de IPs
   * Registro A/PTR, verificação de subdomínio t/m/res


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
   >As predefinições de mensagens desativadas não podem ser excluídas para evitar qualquer problema no jornada usando essas predefinições para enviar mensagens.

