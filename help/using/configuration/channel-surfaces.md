---
solution: Journey Optimizer
product: journey optimizer
title: Configurar superfícies de canais
description: Saiba como configurar e monitorar superfícies de canal
feature: Surface, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: canal, superfície, técnico, parâmetros, otimizador
exl-id: 9038528f-3da0-4e0e-9b82-b72c67b42391
source-git-commit: 99c509a00a3e8a4dbf9ae8a5b16aa799b0af2e13
workflow-type: tm+mt
source-wordcount: '1651'
ht-degree: 8%

---

# Configurar superfícies de canais {#set-up-channel-surfaces}

>[!CONTEXTUALHELP]
>id="ajo_admin_channel_surfaces"
>title="Superfície de canal"
>abstract="Uma superfície de canal é uma configuração definida por um administrador do sistema. Contém todos os parâmetros técnicos para enviar a mensagem, como parâmetros de cabeçalho, subdomínio, aplicativos móveis etc."

Com [!DNL Journey Optimizer], você pode configurar superfícies de canal (ou seja, predefinições de mensagem) que definem todos os parâmetros técnicos necessários para suas mensagens: tipo de email, email e nome do remetente, aplicativos móveis, configuração de SMS e muito mais.

>[!CAUTION]
>
> * Para criar, editar e excluir superfícies de canal, você deve ter a [Gerenciar predefinições de mensagens](../administration/high-low-permissions.md#administration-permissions) permissão.
>
> * Você deve executar o [Configuração de email](../email/get-started-email-config.md), [Configuração de push](../push/push-configuration.md), [Configuração de SMS](../sms/sms-configuration.md) e [Configuração de correspondência direta](../direct-mail/direct-mail-configuration.md) etapas antes de criar superfícies de canal.

Depois que as superfícies de canal forem configuradas, você poderá selecioná-las ao criar mensagens de uma jornada ou campanha.

<!--
➡️ [Learn how to create and use email surfaces in this video](#video-presets)
-->

## Criar uma superfície de canal {#create-channel-surface}

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets_header"
>title="Configurações da superfície de canal"
>abstract="Ao configurar uma superfície de canal, selecione o canal ao qual se aplica e defina todos os parâmetros técnicos necessários para seu envio, como tipo de email, nome do remetente, aplicativos móveis, configuração de SMS e muito mais."

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets"
>title="Configurações da superfície de canal"
>abstract="Para criar ações, como emails de uma jornada ou campanha, primeiro crie uma superfície de canal que defina todas as configurações técnicas necessárias para suas mensagens. É necessário ter a permissão Gerenciar predefinições de mensagens para criar, editar e excluir superfícies de canais."

>[!CONTEXTUALHELP]
>id="ajo_surface_marketing_action"
>title="Selecionar uma ação de marketing"
>abstract="Escolha uma ação de marketing na superfície para associar uma política de consentimento à mensagem."

Para criar uma superfície de canal, siga estas etapas:

1. Acesse o **[!UICONTROL Canais]** > **[!UICONTROL Marcas]** > **[!UICONTROL Superfícies de canal]** e clique em **[!UICONTROL Criar superfície de canal]**.

   ![](assets/preset-create.png)

1. Insira um nome e uma descrição (opcional) para a superfície e selecione os canais a serem configurados.

   ![](assets/preset-general.png)

   >[!NOTE]
   >
   > Os nomes devem começar com uma letra (A-Z). Ele só pode conter caracteres alfanuméricos. Também é possível usar sublinhado `_`, ponto`.` e hífen `-` caracteres.

1. Se você selecionou a variável **[!UICONTROL E-mail]** canal, defina as configurações conforme descrito em [nesta seção](../email/email-settings.md).

   ![](assets/preset-email.png)

1. Para o **[!UICONTROL Notificação por push]** canal, selecione pelo menos uma plataforma -  **iOS** e/ou **Android** - e os aplicativos móveis a serem usados para cada plataforma.

   ![](assets/preset-push.png)

   >[!NOTE]
   >
   >Para obter mais informações sobre como configurar o ambiente para enviar notificações por push, consulte [nesta seção](../push/push-gs.md).

1. Para o **[!UICONTROL SMS]** canal, defina as configurações conforme detalhado em [nesta seção](../sms/sms-configuration.md#message-preset-sms).

   ![](assets/preset-sms.png)

   >[!NOTE]
   >
   >Para obter mais informações sobre como configurar o seu ambiente para enviar mensagens SMS, consulte [nesta seção](../sms/sms-configuration.md).

<!--
1. Select a **[!UICONTROL Marketing action]** to associate consent policies to the messages using this surface. All consent policies associated with that marketing action are leveraged in order to respect the preferences of your customers. [Learn more](../action/consent.md#marketing-actions)

    >[!NOTE]
    >
    >Consent policies are currently only available for organizations that have purchased the **Healthcare Shield** and **Privacy and Security Shield** add-on offerings. [Learn more](https://experienceleague.adobe.com/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield.html){target="_blank"}

    ![](assets/surface-marketing-action.png)

    >[!NOTE]
    >
    >You can only select one marketing action.-->

1. Após configurar todos os parâmetros, clique em **[!UICONTROL Enviar]** para confirmar. Você também pode salvar a superfície de canal como rascunho e retomar sua configuração posteriormente.

   ![](assets/preset-submit.png)

   >[!NOTE]
   >
   >Você não pode continuar com a criação da superfície de email enquanto o pool de IP selecionado estiver em [edição](ip-pools.md#edit-ip-pool) (**[!UICONTROL Processando]** e nunca foi associado ao subdomínio selecionado. [Saiba mais](#subdomains-and-ip-pools)
   >
   >Salve a superfície como rascunho e aguarde até que o pool de IP tenha a **[!UICONTROL Sucesso]** status para retomar a criação da superfície.

1. Depois que a superfície de canal é criada, ela é exibida na lista com o **[!UICONTROL Processando]** status.

   Durante essa etapa, várias verificações serão executadas para verificar se ela foi configurada corretamente. <!--The processing time is around **48h-72h**, and can take up to **7-10 business days**.-->

   >[!NOTE]
   > Ao criar uma superfície de email para um subdomínio, o tempo de processamento varia conforme detalhado abaixo:
   >
   > * Para **novos subdomínios**, o processo de criação da primeira superfície de canal pode levar **10 minutos a 10 dias**.
   > * Para **sandboxes de não produção** ou se o subdomínio selecionado for **já usado** em outra superfície de canal aprovada, o processo leva apenas até **3 horas**.


   Essas verificações incluem os testes técnicos e de configuração realizados pela equipe do Adobe:

   * Validação de SPF
   * Validação de DKIM
   * Validação de registro MX
   * Verificar IPs em incluir na lista de bloqueios
   * Helo verificação de host
   * Verificação do pool de IPs
   * Registro A/PTR, verificação de subdomínio t/m/res
   * Registro FBL (esta verificação será executada somente na primeira vez que uma superfície de email for criada para um determinado subdomínio)

   >[!NOTE]
   >
   >Se as verificações não forem bem-sucedidas, saiba mais sobre os possíveis motivos de falha no [nesta seção](#monitor-channel-surfaces).

1. Depois que as verificações forem bem-sucedidas, a superfície de canal obterá a variável **[!UICONTROL Ativo]** status. Ele está pronto para ser usado para enviar mensagens.

   ![](assets/preset-active.png)

## Monitorar superfícies de canal {#monitor-channel-surfaces}

Todas as superfícies do canal são exibidas na **[!UICONTROL Canais]** > **[!UICONTROL Superfícies de canal]** menu. Os filtros estão disponíveis para ajudá-lo a navegar pela lista (canal, usuário, status).

![](assets/preset-filters.png)

Depois de criadas, as superfícies de canal podem ter os seguintes status:

* **[!UICONTROL Rascunho]**: a superfície de canal foi salva como rascunho e ainda não foi enviada. Abra-o para retomar a configuração.
* **[!UICONTROL Processando]**: a superfície de canal foi enviada e está passando por várias etapas de verificação.
* **[!UICONTROL Ativo]**: A superfície de canal foi verificada e pode ser selecionada para criar mensagens.
* **[!UICONTROL Failed]**: uma ou várias verificações falharam durante a verificação da superfície de canal.
* **[!UICONTROL Desativado]**: a superfície de canal está desativada. Ele não pode ser usado para criar novas mensagens.

Em caso de falha na criação de uma superfície de canal, os detalhes sobre cada possível motivo de falha são descritos abaixo.

Se um desses erros ocorrer, entre em contato com [Atendimento ao cliente Adobe](https://helpx.adobe.com/br/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target="_blank"} para obter assistência.

* **Falha na validação do SPF**: SPF (Sender Policy Framework) é um protocolo de autenticação de email que permite especificar IPs autorizados que podem enviar emails de um determinado subdomínio. Falha na validação do SPF significa que os endereços IP no registro SPF não correspondem aos endereços IP usados para enviar emails para os provedores de caixa de correio.

* **Falha na validação de DKIM**: DKIM (DomainKeys Identified Mail) permite que o servidor do recipient verifique se a mensagem recebida foi enviada pelo remetente original do domínio associado e se o conteúdo da mensagem original não foi alterado no caminho. Falha na validação do DKIM significa que os servidores de email de recebimento não podem verificar a autenticidade do conteúdo da mensagem e sua associação com o domínio de envio.:

* **Falha na validação do registro MX**: falha na validação do registro MX (Mail eXchange) significa que os servidores de email responsáveis por aceitar emails de entrada em nome de um determinado subdomínio não estão configurados corretamente.

* **Falha nas configurações de entrega**: a falha das configurações de capacidade de entrega pode ocorrer devido a qualquer um dos seguintes motivos:
   * ➡ Incluir na lista de bloqueios dos IPs alocados
   * Inválido `helo` name
   * Emails sendo enviados de IPs diferentes daqueles especificados no pool de IPs da superfície correspondente
   * Não é possível enviar emails para caixas de entrada dos principais ISPs

## Editar uma superfície de canal {#edit-channel-surface}

Para editar uma superfície de canal, siga as etapas abaixo.

>[!NOTE]
>
>Não é possível editar o **[!UICONTROL Configurações de notificação por push]**. Se uma superfície de canal for configurada apenas para o canal de Notificações por push, ela não será editável.

1. Na lista, clique em um nome de superfície de canal para abri-la.

   ![](assets/preset-name.png)

1. Edite as propriedades conforme desejado.

   >[!NOTE]
   >
   >Se uma superfície de canal tiver o **[!UICONTROL Ativo]** status, a variável **[!UICONTROL Nome]**, **[!UICONTROL Selecionar canal]** e **[!UICONTROL Subdomínio]** Os campos estão esmaecidos e não podem ser editados.

1. Clique em **[!UICONTROL Enviar]** para confirmar as alterações.

   >[!NOTE]
   >
   >Você também pode salvar a superfície de canal como rascunho e retomar a atualização posteriormente.

Depois que as alterações forem enviadas, a superfície de canal passará por um ciclo de validação semelhante ao em vigor quando [criação de uma superfície de canal](#create-channel-surface). O tempo de processamento da edição pode levar até **3 horas**.

>[!NOTE]
>
>Se você editar apenas a variável **[!UICONTROL Descrição]**, **[!UICONTROL Tipo de email]** e/ou **[!UICONTROL Parâmetros de nova tentativa de email]** , a atualização é instantânea.

### Detalhes da atualização {#update-details}

Para superfícies de canal que têm o **[!UICONTROL Ativo]** você poderá verificar os detalhes da atualização. Para fazer isso:

Clique em **[!UICONTROL Atualização recente]** ícone que é exibido ao lado do nome da superfície ativa.

![](assets/preset-recent-update-icon.png)

<!--You can also access the update details from an active channel surface while update is in progress.-->

No **[!UICONTROL Atualização recente]** você pode ver informações como o status da atualização e a lista de alterações solicitadas.

<!--![](assets/preset-recent-update-screen.png)-->

### Atualizar status {#update-statuses}

Uma atualização da superfície de canal pode ter os seguintes status:

* **[!UICONTROL Processando]**: a atualização da superfície de canal foi enviada e está passando por várias etapas de verificação.
* **[!UICONTROL Sucesso]**: a superfície de canal atualizada foi verificada e pode ser selecionada para criar mensagens.
* **[!UICONTROL Failed]**: uma ou várias verificações falharam durante a verificação de atualização da superfície de canal.

Cada status é detalhado abaixo.

#### Processamento {#surface-processing}

Várias verificações de deliverability serão realizadas para verificar se a superfície foi atualizada corretamente.

>[!NOTE]
>
>Se você editar apenas a variável **[!UICONTROL Descrição]**, **[!UICONTROL Tipo de email]** e/ou **[!UICONTROL Parâmetros de nova tentativa de email]** , a atualização é instantânea.

O tempo de processamento pode levar até **3 horas**. Saiba mais sobre as verificações realizadas durante o ciclo de validação no [nesta seção](#create-channel-surface).

Se você editar uma superfície que já estava ativa:

* Seu status permanece **[!UICONTROL Ativo]** enquanto o processo de validação está em andamento.

* A variável **[!UICONTROL Atualização recente]** O ícone é exibido ao lado do nome da superfície na lista de superfícies do canal.

* Durante o processo de validação, as mensagens configuradas usando essa superfície ainda estão usando a versão mais antiga da superfície.

>[!NOTE]
>
>Não é possível modificar uma superfície de canal enquanto a atualização está em andamento. Você ainda pode clicar no nome, mas todos os campos estarão esmaecidos. As alterações não serão refletidas até que a atualização seja bem-sucedida.

#### Sucesso {#success}

Depois que o processo de validação for bem-sucedido, a nova versão da superfície será usada automaticamente em todas as mensagens que usam essa superfície. No entanto, talvez seja necessário aguardar:
* alguns minutos antes de ser consumido pelas mensagens unitárias,
* até o próximo lote para que a superfície seja efetiva em mensagens em lote.

#### Falhou {#failed}

Se o processo de validação falhar, a versão mais antiga da superfície ainda será usada.

Saiba mais sobre os possíveis motivos de falha no [nesta seção](#monitor-channel-surfaces).

Se a atualização falhar, a superfície se tornará editável novamente. Você pode clicar no nome e atualizar as configurações que precisam ser corrigidas.

## Desativar uma superfície de canal {#deactivate-a-surface}

Para tornar um **[!UICONTROL Ativo]** superfície de canal indisponível para criar novas mensagens. você pode desativá-la. No entanto, as mensagens de jornadas que atualmente usam essa superfície não serão afetadas e continuarão funcionando.

>[!NOTE]
>
>Não é possível desativar uma superfície de canal enquanto uma atualização está sendo processada. Aguarde até que a atualização seja bem-sucedida ou tenha falhado. Saiba mais sobre [editar superfícies de canal](#edit-channel-surface) e no [atualizar status](#update-statuses).

1. Acesse a lista de superfícies de canal.

1. Para a superfície ativa de sua escolha, clique no link **[!UICONTROL Mais ações]** botão.

1. Selecionar **[!UICONTROL Desativar]**.

   ![](assets/preset-deactivate.png)

>[!NOTE]
>
>As superfícies de canal desativadas não podem ser excluídas para evitar problemas no jornada que usa essas superfícies para enviar mensagens.

Não é possível editar diretamente uma superfície de canal desativada. No entanto, é possível duplicá-la e editar a cópia para criar uma nova versão que será usada para criar novas mensagens. Você também pode ativá-la novamente e aguardar até que a atualização seja bem-sucedida para editá-la.

![](assets/preset-activate.png)

<!--
## How-to video{#video-presets}

Learn how to create channel surfaces, how to use them and how to delegate a subdomain and create an IP pool.

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
-->
