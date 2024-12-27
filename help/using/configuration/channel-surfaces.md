---
solution: Journey Optimizer
product: journey optimizer
title: Definir configurações de canal
description: Saiba como definir e monitorar configurações de canal
feature: Surface, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: canal, superfície, técnico, parâmetros, otimizador
exl-id: 9038528f-3da0-4e0e-9b82-b72c67b42391
source-git-commit: 4cd7e193079f0e9d141d28ca80dd0cf7a899fbea
workflow-type: tm+mt
source-wordcount: '1737'
ht-degree: 12%

---

# Definir configurações de canal {#set-up-channel-surfaces}

>[!CONTEXTUALHELP]
>id="ajo_admin_channel_surfaces"
>title="Configuração de canais"
>abstract="Uma configuração de canais é uma configuração que foi definida por um(a) admin de sistema. Contém todos os parâmetros técnicos para enviar a mensagem, como parâmetros de cabeçalho, subdomínio, aplicativos móveis etc."

>[!CONTEXTUALHELP]
>id="ajo_admin_marketing_action"
>title="Ação de marketing"
>abstract="Escolha as ações de marketing para vincular políticas de consentimento às mensagens usando essa configuração. Todas as políticas de consentimento conectadas à ação de marketing serão usadas para respeitar as preferências dos clientes."

Com o [!DNL Journey Optimizer], você pode definir configurações de canal (ou seja, predefinições de mensagem) que definem todos os parâmetros técnicos necessários para suas mensagens: tipo de email, email e nome do remetente, aplicativos móveis, configuração de SMS e muito mais.

>[!CAUTION]
>
> * Para criar, editar e excluir configurações de canal, você deve ter a permissão [Gerenciar predefinições de mensagens](../administration/high-low-permissions.md#administration-permissions).
>
> * Você deve executar as etapas de [Configuração de email](../email/get-started-email-config.md), [Configuração de push](../push/push-configuration.md), [Configuração de SMS](../sms/sms-configuration.md), [Configuração no aplicativo](../in-app/inapp-configuration.md), [Configuração baseada em código](../code-based/code-based-configuration.md), [Configuração da Web](../web/web-configuration.md) e [Configuração de correspondência direta](../direct-mail/direct-mail-configuration.md) antes de criar as configurações de canal.

Depois que as configurações de canal forem definidas, você poderá selecioná-las ao criar mensagens de uma jornada ou campanha.

Você também pode usar a configuração de canal guiada para automatizar e validar a configuração de canal em uma experiência unificada, acelerando o processo de introdução ao Journey Optimizer. [Saiba mais](set-mobile-config.md)

<!--
➡️ [Learn how to create and use email configurations in this video](#video-presets)
-->

## Criar uma configuração de canais {#create-channel-surface}

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets_header"
>title="Definições da configuração de canais"
>abstract="Ao definir uma configuração de canais, selecione o canal ao qual ela se aplica e defina todos os parâmetros técnicos necessários para seu envio, como tipo de email, nome do remetente, aplicativos móveis, configuração de SMS, entre outros."

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets"
>title="Definições da configuração de canais"
>abstract="Para criar ações como emails de uma jornada ou campanha, você deve primeiro criar uma configuração de canal que defina todas as configurações técnicas necessárias para suas mensagens. Você deve ter a permissão Gerenciar predefinições de mensagens para criar, editar e excluir configurações de canais."

>[!CONTEXTUALHELP]
>id="ajo_surface_marketing_action"
>title="Selecione uma ação de marketing"
>abstract="Escolha uma ação de marketing na configuração para associar uma política de consentimento à mensagem."

Para criar uma configuração de canal, siga estas etapas:

1. Acesse o menu **[!UICONTROL Canais]** > **[!UICONTROL Configurações gerais]** > **[!UICONTROL Configurações de canal]** e clique em **[!UICONTROL Criar configuração de canal]**.

   ![](assets/preset-create.png)

1. Insira um nome e uma descrição (opcional) para a configuração e selecione o canal a ser configurado.

   ![](assets/preset-general.png)

   >[!NOTE]
   >
   > Os nomes devem começar com uma letra (A-Z). Ele só pode conter caracteres alfanuméricos. Também é possível usar sublinhado `_`, ponto`.` e hífen `-` caracteres.

1. Para atribuir rótulos de uso de dados personalizados ou de núcleo à configuração, você pode selecionar **[!UICONTROL Gerenciar acesso]**. [Saiba mais sobre OLAC (Controle de Acesso em Nível de Objeto)](../administration/object-based-access.md).

1. Selecione seu canal.

1. Selecione **[!UICONTROL Ação de marketing]**(s) para associar políticas de consentimento às mensagens que usam essa configuração. Todas as políticas de consentimento associadas à ação de marketing são utilizadas para respeitar as preferências dos clientes. [Saiba mais](../action/consent.md#surface-marketing-actions)

   >[!NOTE]
   >
   >Atualmente, as políticas de consentimento estão disponíveis apenas para organizações que compraram as ofertas complementares do **Healthcare Shield** e do **Privacy and Security Shield**.

   ![](assets/surface-marketing-action.png)

1. Depois que todos os parâmetros tiverem sido configurados, clique em **[!UICONTROL Enviar]** para confirmar. Você também pode salvar a configuração do canal como rascunho e retomar a configuração posteriormente.

   ![](assets/preset-submit.png)

   >[!NOTE]
   >
   >Não é possível continuar com a criação da configuração de email enquanto o pool de IP selecionado estiver em [edição](ip-pools.md#edit-ip-pool) (status **[!UICONTROL Processando]**) e não tiver sido associado ao subdomínio selecionado. [Saiba mais](#subdomains-and-ip-pools)
   >
   >Salve a configuração como rascunho e aguarde até que o pool de IP tenha o status **[!UICONTROL Sucesso]** para retomar a criação da configuração.

1. Depois que a configuração do canal é criada, ela é exibida na lista com o status **[!UICONTROL Processando]**.

   Durante essa etapa, várias verificações serão executadas para verificar se ela foi configurada corretamente. <!--The processing time is around **48h-72h**, and can take up to **7-10 business days**.-->

   >[!NOTE]
   > Ao criar uma configuração de email para um subdomínio, o tempo de processamento varia conforme detalhado abaixo:
   >
   > * Para **novos subdomínios**, o processo de criação da primeira configuração de canal pode levar de **10 min a 10 dias**.
   > * Para **sandboxes de não produção** ou se o subdomínio selecionado for **já usado** em outra configuração de canal aprovada, o processo levará apenas **3 horas**.


   Essas verificações incluem os testes técnicos e de configuração realizados pela equipe do Adobe:

   * Validação de SPF
   * Validação do DKIM
   * Validação de registro MX
   * Verificar IPs em incluir na lista de bloqueios
   * Helo verificação de host
   * Verificação do pool de IPs
   * Registro A/PTR, verificação de subdomínio t/m/res
   * Registro FBL (essa verificação será executada somente na primeira vez que uma configuração de email for criada para um determinado subdomínio)

   >[!NOTE]
   >
   >Se as verificações não forem bem-sucedidas, saiba mais sobre os possíveis motivos de falha em [esta seção](#monitor-channel-surfaces).

1. Depois que as verificações forem bem-sucedidas, a configuração do canal obterá o status **[!UICONTROL Ativo]**. Ele está pronto para ser usado para enviar mensagens.

   ![](assets/preset-active.png)

## Monitorar configurações de canal {#monitor-channel-surfaces}

Todas as suas configurações de canal são exibidas no menu **[!UICONTROL Canais]** > **[!UICONTROL Configurações de canal]**. Os filtros estão disponíveis para ajudá-lo a navegar pela lista (canal, usuário, status).

![](assets/preset-filters.png)

Depois de criadas, as configurações de canal podem ter os seguintes status:

* **[!UICONTROL Rascunho]**: a configuração de canal foi salva como rascunho e ainda não foi enviada. Abra-o para retomar a configuração.
* **[!UICONTROL Processando]**: a configuração de canal foi enviada e está passando por várias etapas de verificação.
* **[!UICONTROL Ativo]**: a configuração de canal foi verificada e pode ser selecionada para criar mensagens.
* **[!UICONTROL Falha]**: uma ou várias verificações falharam durante a verificação da configuração do canal.
* **[!UICONTROL Desativado]**: a configuração do canal está desativada. Ele não pode ser usado para criar novas mensagens.

Em caso de falha na criação de um canal, os detalhes sobre cada possível motivo de falha são descritos abaixo.

Se um desses erros ocorrer, entre em contato com o [Atendimento ao cliente do Adobe](https://helpx.adobe.com/br/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target="_blank"} para obter assistência.

* **Falha na validação do SPF**: o SPF (Estrutura de Política do Remetente) é um protocolo de autenticação de email que permite especificar IPs autorizados que podem enviar emails de um determinado subdomínio. Falha na validação do SPF significa que os endereços IP no registro SPF não correspondem aos endereços IP usados para enviar emails para os provedores de caixa de correio.

* **Falha na validação do DKIM**: o DKIM (DomainKeys Identified Mail) permite que o servidor do destinatário verifique se a mensagem recebida foi enviada pelo remetente original do domínio associado e se o conteúdo da mensagem original não foi alterado no caminho. Falha na validação do DKIM significa que os servidores de email de recebimento não podem verificar a autenticidade do conteúdo da mensagem e sua associação com o domínio de envio.:

* **Falha na validação do registro MX**: falha na validação do registro MX (Mail eXchange) significa que os servidores de email responsáveis por aceitar emails de entrada em nome de um determinado subdomínio não estão configurados corretamente.

* **Falha nas configurações de entrega**: a falha nas configurações de entrega pode ocorrer devido a qualquer um dos seguintes motivos:
   * ➡ Incluir na lista de bloqueios dos IPs alocados
   * Nome `helo` inválido
   * Emails sendo enviados de IPs diferentes daqueles especificados no pool de IPs da configuração correspondente
   * Não é possível enviar emails para caixas de entrada dos principais ISPs

## Editar uma configuração de canal {#edit-channel-surface}

Para editar uma configuração de canal, siga as etapas abaixo.

>[!NOTE]
>
>Você não pode editar as **[!UICONTROL configurações de notificação por push]**. Se uma configuração de canal for definida apenas para o canal de Notificação por push, ela não será editável.

1. Na lista, clique em um nome de configuração de canal para abri-lo.

   ![](assets/preset-name.png)

1. Edite as propriedades conforme desejado.

   >[!NOTE]
   >
   >Se uma configuração de canal tiver o status **[!UICONTROL Ativo]**, os campos **[!UICONTROL Nome]**, **[!UICONTROL Selecionar canal]** e **[!UICONTROL Subdomínio]** estarão esmaecidos e não poderão ser editados.

1. Clique em **[!UICONTROL Enviar]** para confirmar as alterações.

   >[!NOTE]
   >
   >Você também pode salvar a configuração do canal como rascunho e retomar a atualização posteriormente.

Depois que as alterações forem enviadas, a configuração do canal passará por um ciclo de validação semelhante ao que está em vigor ao [criar uma configuração de canal](#create-channel-surface). O tempo de processamento da edição pode levar até **3 horas**.

>[!NOTE]
>
>Se você editar apenas os campos **[!UICONTROL Descrição]**, **[!UICONTROL Tipo de email]** e/ou **[!UICONTROL Parâmetros de nova tentativa de email]**, a atualização será instantânea.

### Detalhes da atualização {#update-details}

Para configurações de canal com o status **[!UICONTROL Ativo]**, você pode verificar os detalhes da atualização. Para fazer isso:

Clique no ícone **[!UICONTROL Atualização recente]** que é exibido ao lado do nome da configuração ativa.

![](assets/preset-recent-update-icon.png)

<!--You can also access the update details from an active channel configuration while update is in progress.-->

Na tela **[!UICONTROL Atualização recente]**, você pode ver informações como o status da atualização e a lista de alterações solicitadas.

<!--![](assets/preset-recent-update-screen.png)-->

### Atualizar status {#update-statuses}

Uma atualização de configuração de canal pode ter os seguintes status:

* **[!UICONTROL Processando]**: a atualização de configuração de canal foi enviada e está passando por várias etapas de verificação.
* **[!UICONTROL Êxito]**: a configuração de canal atualizada foi verificada e pode ser selecionada para criar mensagens.
* **[!UICONTROL Falha]**: uma ou várias verificações falharam durante a verificação de atualização de configuração de canal.

Cada status é detalhado abaixo.

#### Processamento {#surface-processing}

Várias verificações de deliverability serão executadas para verificar se a configuração foi atualizada corretamente.

>[!NOTE]
>
>Se você editar apenas os campos **[!UICONTROL Descrição]**, **[!UICONTROL Tipo de email]** e/ou **[!UICONTROL Parâmetros de nova tentativa de email]**, a atualização será instantânea.

O tempo de processamento pode levar até **3 horas**. Saiba mais sobre as verificações realizadas durante o ciclo de validação em [esta seção](#create-channel-surface).

Se você editar uma configuração que já estava ativa:

* Seu status permanece **[!UICONTROL Ativo]** enquanto o processo de validação está em andamento.

* O ícone **[!UICONTROL Atualização recente]** é exibido próximo ao nome da configuração na lista de configurações de canal.

* Durante o processo de validação, as mensagens configuradas usando essa configuração ainda estão usando a versão mais antiga da configuração.

>[!NOTE]
>
>Não é possível modificar uma configuração de canal enquanto a atualização está em andamento. Você ainda pode clicar no nome, mas todos os campos estarão esmaecidos. As alterações não serão refletidas até que a atualização seja bem-sucedida.

#### Sucesso {#success}

Quando o processo de validação for bem-sucedido, a nova versão da configuração será usada automaticamente em todas as mensagens que usam essa configuração. No entanto, talvez seja necessário aguardar:
* alguns minutos antes de ser consumido pelas mensagens unitárias,
* até o próximo lote para que a configuração entre em vigor nas mensagens em lote.

#### Com falha {#failed}

Se o processo de validação falhar, a versão mais antiga da configuração ainda será usada.

Saiba mais sobre os possíveis motivos de falha em [esta seção](#monitor-channel-surfaces).

Se a atualização falhar, a configuração se tornará editável novamente. Você pode clicar no nome e atualizar as configurações que precisam ser corrigidas.

## Desativar uma configuração de canal {#deactivate-a-surface}

Para tornar uma configuração de canal **[!UICONTROL Ativa]** indisponível para criar novas mensagens, você pode desativá-la. No entanto, as mensagens de jornadas que estão usando essa configuração no momento não serão afetadas e continuarão funcionando.

>[!NOTE]
>
>Não é possível desativar uma configuração de canal enquanto uma atualização está sendo processada. Aguarde até que a atualização seja bem-sucedida ou tenha falhado. Saiba mais sobre [edição de configurações de canal](#edit-channel-surface) e sobre [atualização de status](#update-statuses).

1. Acesse a lista de configurações de canal.

1. Para a configuração ativa de sua escolha, clique no botão **[!UICONTROL Mais ações]**.

1. Selecione **[!UICONTROL Desativar]**.

   ![](assets/preset-deactivate.png)

>[!NOTE]
>
>As configurações de canal desativadas não podem ser excluídas para evitar problemas no jornada que usa essas configurações para enviar mensagens.

Não é possível editar diretamente uma configuração de canal desativada. No entanto, é possível duplicá-la e editar a cópia para criar uma nova versão que será usada para criar novas mensagens. Você também pode ativá-la novamente e aguardar até que a atualização seja bem-sucedida para editá-la.

![](assets/preset-activate.png)


## Vídeo tutorial{#video-presets}

Saiba o que são configurações de canal e como elas são usadas no Adobe Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/3433124/?learn=on)
