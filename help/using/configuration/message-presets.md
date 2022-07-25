---
title: Configurar superfícies do canal
description: Saiba como configurar e monitorar superfícies de canais
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 9038528f-3da0-4e0e-9b82-b72c67b42391
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '1462'
ht-degree: 1%

---

# Configurar superfícies do canal {#message-presets-creation}

Com [!DNL Journey Optimizer], é possível configurar superfícies do canal (ou seja, predefinições de mensagem) que definem todos os parâmetros técnicos necessários para suas mensagens: tipo de email, email e nome do remetente, aplicativos móveis e muito mais.

>[!CAUTION]
>
> * Para criar, editar e excluir superfícies de canais, você deve ter a variável [Gerenciar a superfície do canal](../administration/high-low-permissions.md#manage-channel-surface).
>
> * Você deve executar o [Configuração de email](#configure-email-settings), [Configuração por push](../configuration/push-configuration.md) e [Configuração de SMS](../configuration/sms-configuration.md) etapas antes de criar superfícies de canal.


Depois que as superfícies do canal forem configuradas, você poderá selecioná-las ao criar mensagens de uma jornada.

➡️ [Saiba como criar e usar superfícies de email neste vídeo](#video-presets)

## Criar uma superfície de canal {#create-message-preset}

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets"
>title="Detalhes e configurações da superfície do canal"
>abstract="Ao configurar uma superfície de canal, é possível selecionar o canal ao qual ele se aplica e definir todos os parâmetros técnicos necessários para seus deliveries, como tipo de email, subdomínio a ser usado, nome do remetente, aplicativos móveis etc."

Para criar uma superfície de canal, siga estas etapas:

1. Acesse o **[!UICONTROL Channels]** > **[!UICONTROL Branding]** > **[!UICONTROL Channel surfaces]** , em seguida, clique em **[!UICONTROL Create channel surface]**.

   ![](assets/preset-create.png)

1. Insira um nome e uma descrição (opcional) para a superfície, em seguida, selecione os canais a serem configurados.

   ![](assets/preset-general.png)

   >[!NOTE]
   >
   > Os nomes devem começar com uma letra (A-Z). Ela só pode conter caracteres alfanuméricos. Você também pode usar o sublinhado `_`, ponto`.` e hífen `-` caracteres.

1. Se você selecionou a variável **[!UICONTROL Email]** , defina suas configurações conforme descrito em [esta seção](email-settings.md).

   ![](assets/preset-email.png)

1. Se você selecionou a variável **[!UICONTROL Push Notification]** , selecione pelo menos uma plataforma (**iOS** e/ou **Android**) e selecione os aplicativos móveis que serão usados para cada plataforma.

   ![](assets/preset-push.png)

   >[!NOTE]
   >
   >Para obter mais informações sobre como configurar o ambiente para enviar notificações por push, consulte [esta seção](push-gs.md).

1. Se você selecionou a variável **[!UICONTROL SMS]** , defina suas configurações conforme descrito em [esta seção](sms-configuration.md#message-preset-sms).

   ![](assets/preset-sms.png)

   >[!NOTE]
   >
   >Para obter mais informações sobre como configurar seu ambiente para enviar mensagens SMS, consulte [esta seção](sms-configuration.md).

1. Depois que todos os parâmetros tiverem sido configurados, clique em **[!UICONTROL Submit]** para confirmar. Você também pode salvar a superfície do canal como rascunho e retomar sua configuração posteriormente.

   ![](assets/preset-submit.png)

   >[!NOTE]
   >
   >Não é possível continuar com a criação da superfície enquanto o pool de IP selecionado estiver em [edição](ip-pools.md#edit-ip-pool) (**[!UICONTROL Processing]** e nunca foi associado ao subdomínio selecionado. [Saiba mais](#subdomains-and-ip-pools)
   >
   >Salve a superfície como rascunho e aguarde até que o pool de IP tenha a variável **[!UICONTROL Success]** status para retomar a criação da superfície.

1. Depois que a superfície do canal for criada, ela será exibida na lista com a variável **[!UICONTROL Processing]** status.

   Durante essa etapa, várias verificações serão executadas para verificar se foram configuradas corretamente. O tempo de processamento está por vir **48h-72h** e pode **7 a 10 dias úteis**.

   Essas verificações incluem testes técnicos e de configuração realizados pela equipe de Adobe:

   * Validação de SPF
   * Validação de DKIM
   * Validação de registro MX
   * Verificar IPs inclua na lista de bloqueios
   * Verificação do anfitrião
   * Verificação de pool de IPs
   * Registro A/PTR, verificação de subdomínio t/m/res

   >[!NOTE]
   >
   >Se as verificações não forem bem-sucedidas, saiba mais sobre os possíveis motivos de falha em [esta seção](#monitor-message-presets).

1. Depois que as verificações são bem-sucedidas, a superfície do canal recebe a variável **[!UICONTROL Active]** status. Ele está pronto para ser usado para entregar mensagens.

   ![](assets/preset-active.png)

## Superfícies do canal do monitor {#monitor-message-presets}

Todas as superfícies dos seus canais são exibidas na seção **[!UICONTROL Channels]** > **[!UICONTROL Channel surfaces]** menu. Os filtros estão disponíveis para ajudar você a navegar pela lista (canal, usuário, status).

![](assets/preset-filters.png)

Depois de criadas, as superfícies do canal podem ter os seguintes status:

* **[!UICONTROL Draft]**: A superfície do canal foi salva como rascunho e ainda não foi enviada. Abra-o para retomar a configuração.
* **[!UICONTROL Processing]**: A superfície do canal foi enviada e está passando por várias etapas de verificação.
* **[!UICONTROL Active]**: A superfície do canal foi verificada e pode ser selecionada para criar mensagens.
* **[!UICONTROL Failed]**: Uma ou várias verificações falharam durante a verificação da superfície do canal.
* **[!UICONTROL Deactivated]**: A superfície do canal está desativada. Ele não pode ser usado para criar novas mensagens.

No caso de falha na criação da superfície do canal, os detalhes sobre cada motivo possível de falha são descritos abaixo.

Se um desses erros ocorrer, entre em contato com o [Atendimento ao cliente do Adobe](https://helpx.adobe.com/br/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;} para obter assistência.

* **Falha na validação do SPF**: O SPF (Sender Policy Framework) é um protocolo de autenticação de email que permite especificar IPs autorizados que podem enviar emails de um determinado subdomínio. Falha na validação de SPF significa que os endereços IP no registro SPF não correspondem aos endereços IP usados para enviar emails para os provedores de caixa de correio.

* **Falha na validação do DKIM**: DKIM (DomainKeys Identified Mail) permite que o servidor do recipient verifique se a mensagem recebida foi enviada pelo remetente genuíno do domínio associado e se o conteúdo da mensagem original não foi alterado no caminho. Falha na validação DKIM significa que os servidores de email de recebimento não podem verificar a autenticidade do conteúdo da mensagem e sua associação com o domínio de envio.:

* **Falha na validação do registro MX**: Falha na validação de registro MX (Mail eXchange) significa que os servidores de email responsáveis por aceitar emails de entrada em nome de um determinado subdomínio não estão configurados corretamente.

* **Falha nas configurações da capacidade de entrega**: A falha das configurações de deliverability pode ocorrer devido a qualquer um dos seguintes motivos:
   * incluir na lista de bloqueios dos IPs alocados
   * Inválido `helo` name
   * Emails enviados de IPs diferentes dos especificados no pool de IP da superfície correspondente
   * Não é possível enviar emails para caixas de entrada dos principais ISPs, como Gmail e Yahoo

## Editar uma superfície de canal {#edit-message-preset}

Para editar uma superfície do canal, siga as etapas abaixo.

>[!NOTE]
>
>Não é possível editar o **[!UICONTROL Push notification settings]**. Se uma superfície de canal estiver configurada apenas para o canal de notificação por push, ela não será editável.

1. Na lista, clique em um nome de superfície do canal para abri-lo.

   ![](assets/preset-name.png)

1. Edite as propriedades conforme desejado.

   >[!NOTE]
   >
   >Se uma superfície de canal tiver a **[!UICONTROL Active]** , o **[!UICONTROL Name]**, **[!UICONTROL Select channel]** e **[!UICONTROL Subdomain]** Os campos estão esmaecidos e não podem ser editados.

1. Clique em **[!UICONTROL Submit]** para confirmar as alterações.

   ![](assets/preset-confirm-update.png)

   >[!NOTE]
   >
   >Você também pode salvar a superfície do canal como rascunho e retomar a atualização posteriormente.

Depois que as alterações forem enviadas, a superfície do canal passará por um ciclo de validação semelhante ao vigente quando [criação de uma superfície de canal](#create-message-preset). O tempo de processamento da edição pode demorar até **3 horas**.

>[!NOTE]
>
>Se você só editar a variável **[!UICONTROL Description]**, **[!UICONTROL Email type]** e/ou **[!UICONTROL Email retry parameters]** , a atualização é instantânea.

### Detalhes da atualização {#update-details}

Para superfícies de canal com a variável **[!UICONTROL Active]** , você pode verificar os detalhes da atualização. Para fazer isso:

Clique no botão **[!UICONTROL Recent update]** ícone que é exibido ao lado do nome da superfície ativa.

![](assets/preset-recent-update-icon.png)

<!--You can also access the update details from an active channel surface while update is in progress.-->

No **[!UICONTROL Recent update]** você pode ver informações como o status da atualização e a lista de alterações solicitadas.

![](assets/preset-recent-update-screen.png)

### Atualizar status {#update-statuses}

Uma atualização da superfície do canal pode ter os seguintes status:

* **[!UICONTROL Processing]**: A atualização da superfície do canal foi enviada e está passando por várias etapas de verificação.
* **[!UICONTROL Success]**: A superfície de canal atualizada foi verificada e pode ser selecionada para criar mensagens.
* **[!UICONTROL Failed]**: Uma ou várias verificações falharam durante a verificação de atualização da superfície do canal.

Cada status é detalhado abaixo.

#### Processamento

Várias verificações de deliverability serão executadas para verificar se a superfície foi atualizada corretamente.

>[!NOTE]
>
>Se você só editar a variável **[!UICONTROL Description]**, **[!UICONTROL Email type]** e/ou **[!UICONTROL Email retry parameters]** , a atualização é instantânea.

O tempo de processamento pode demorar até **3 horas**. Saiba mais sobre as verificações realizadas durante o ciclo de validação em [esta seção](#create-message-preset).

Se você editar uma superfície que já estava ativa:

* O seu estatuto permanece **[!UICONTROL Active]** enquanto o processo de validação estiver em andamento.

* O **[!UICONTROL Recent update]** ícone é exibido ao lado do nome da superfície na lista de superfícies do canal.

* Durante o processo de validação, as mensagens configuradas usando essa superfície ainda usam a versão mais antiga da superfície.

>[!NOTE]
>
>Não é possível modificar uma superfície de canal enquanto a atualização estiver em curso. Ainda é possível clicar no nome, mas todos os campos estão esmaecidos. As alterações não serão refletidas até que a atualização seja bem-sucedida.

#### Sucesso {#success}

Depois que o processo de validação for bem-sucedido, a nova versão da superfície será automaticamente usada em todas as mensagens que usam essa superfície. No entanto, pode ser necessário aguardar:
* alguns minutos antes de ser consumido pelas mensagens unitárias,
* até ao lote seguinte para que a superfície seja eficaz em mensagens por lote.

#### Falha {#failed}

Se o processo de validação falhar, a versão mais antiga da superfície ainda será usada.

Saiba mais sobre os possíveis motivos de falha em [esta seção](#monitor-message-presets).

Quando a atualização falhar, a superfície torna-se editável novamente. Você pode clicar no nome e atualizar as configurações que precisam ser corrigidas.

## Desativar uma superfície de canal {#deactivate-preset}

Para criar uma **[!UICONTROL Active]** superfície do canal indisponível para criar novas mensagens, você pode desativá-la. No entanto, as mensagens das jornadas que atualmente usam essa superfície não serão afetadas e continuarão funcionando.

>[!NOTE]
>
>Não é possível desativar uma superfície de canal durante o processamento de uma atualização. Aguarde até que a atualização seja bem-sucedida ou tenha falhado. Saiba mais sobre [superfícies de canal de edição](#edit-message-preset) e no [status de atualização](#update-statuses).

1. Acesse a lista de superfícies do canal.

1. Na superfície ativa de sua escolha, clique no botão **[!UICONTROL More actions]** botão.

1. Selecione **[!UICONTROL Deactivate]**.

   ![](assets/preset-deactivate.png)

>[!NOTE]
>
>Não é possível excluir superfícies de canal desativadas para evitar problemas nas jornadas que usam essas superfícies para enviar mensagens.

Não é possível editar diretamente uma superfície de canal desativada. No entanto, você pode duplicá-lo e editar a cópia para criar uma nova versão que será usada para criar novas mensagens. Também é possível ativá-la novamente e aguardar até que a atualização seja bem-sucedida na edição.

![](assets/preset-activate.png)

## Vídeo tutorial{#video-presets}

Saiba como criar superfícies de canal, usá-las e como delegar um subdomínio e criar um pool de IP.

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
