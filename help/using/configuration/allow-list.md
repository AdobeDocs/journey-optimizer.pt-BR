---
solution: Journey Optimizer
product: journey optimizer
title: Lista permitida
description: Saiba como usar a lista de permissões
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: 70ab8f57-c132-4de1-847b-11f0ab14f422
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '976'
ht-degree: 0%

---

# Lista permitida {#allow-list}

É possível definir uma lista específica de segurança de envio no [sandbox](../administration/sandboxes.md) nível.

Essa lista de permissões permite especificar endereços de email individuais ou domínios que serão os únicos recipients ou domínios autorizados a receber os emails que você está enviando de uma sandbox específica.

>[!NOTE]
>
>Esse recurso está disponível em sandboxes de produção e não produção.

Por exemplo, em uma instância de não produção, em que podem ocorrer erros, a lista permitida garante que você não tenha risco de enviar mensagens indesejadas para endereços de clientes reais e, portanto, fornece um ambiente seguro para fins de teste.

Além disso, quando a lista permitida está ativa, mas vazia, nenhum email será enviado. Portanto, se você encontrar algum problema importante, poderá usar esse recurso para interromper todas as comunicações de saída do [!DNL Journey Optimizer] até que você corrija o problema. Saiba mais sobre o [lógica da lista permitida](#logic).

>[!CAUTION]
>
>Esse recurso se aplica somente ao canal de email.

## Acessar a lista de permissões {#access-allowed-list}

Para acessar a lista detalhada de domínios e endereços de email permitidos, acesse **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** e selecione **[!UICONTROL Allowed list]**.

![](assets/allow-list-access.png)

>[!CAUTION]
>
>As permissões para visualizar, exportar e gerenciar a lista permitida estão restritas a [Administradores de jornada](../administration/ootb-product-profiles.md#journey-administrator). Saiba mais sobre como gerenciar [!DNL Journey Optimizer] direitos de acesso dos usuários em [esta seção](../administration/permissions-overview.md).

Para exportar a lista de permissões como um arquivo CSV, selecione o **[!UICONTROL Download CSV]** botão.

Use o **[!UICONTROL Delete]** para remover permanentemente uma entrada.

Você pode pesquisar por domínios ou endereços de email e filtrar no **[!UICONTROL Address type]**. Depois de selecionado, você pode limpar o filtro exibido na parte superior da lista.

![](assets/allowed-list-filtering-example.png)

## Ativar a lista permitida {#enable-allow-list}

Para ativar a lista de permissões, siga as etapas abaixo.

1. Acesse o  **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL Allow list]** menu.

1. Selecione o botão de alternância.

   ![](assets/allow-list-edit.png)

1. Selecionar **[!UICONTROL Activate allowed list]**. A lista de permissões agora está ativa.

   ![](assets/allow-list-enable.png)

   >[!NOTE]
   >
   >Depois de ativar a lista de permissões, há uma latência de 5 minutos para que ela entre em vigor em suas jornadas e campanhas.

A lógica da lista permitida se aplica quando o recurso está ativo. Saiba mais em [esta seção](#logic).

>[!NOTE]
>
>Quando ativado, o recurso de lista permitida é respeitado ao executar jornadas, mas também ao testar mensagens com [provas](../email/preview.md#send-proofs) e testar as jornadas utilizando [modo de teste](../building-journeys/testing-the-journey.md).

## Desativar a lista permitida {#deactivate-allow-list}

Para desativar a lista de permissões, siga as etapas abaixo.

1. Acesse o  **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL Allow list]** menu.

1. Selecione o botão de alternância.

   ![](assets/allow-list-edit-active.png)

1. Selecionar **[!UICONTROL Deactivate allowed list]**. A lista de permissões não está mais ativa.

   ![](assets/allow-list-deactivate.png)

   >[!NOTE]
   >
   >Depois de desativar a lista de permissões, há uma latência de 5 minutos para que ela entre em vigor em suas jornadas e campanhas.

A lógica de lista permitida não se aplica quando o recurso é desativado. Saiba mais em [esta seção](#logic).

## Adicionar entidades à lista permitida {#add-entities}

Para adicionar novos endereços de email ou domínios à lista de permissões para uma sandbox específica, você pode [preencher manualmente a lista](#manually-populate-list)ou use uma [Chamada de API](#api-call-allowed-list).

>[!NOTE]
>
>A lista permitida pode conter até 1.000 entradas.

### Preencher manualmente a lista permitida {#manually-populate-list}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_add_header"
>title="Adicionar endereços ou domínios à lista permitida"
>abstract="Você pode adicionar manualmente novos endereços de email ou domínios à lista de permissões, selecionando-os um por um."

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_add"
>title="Adicionar endereços ou domínios à lista permitida"
>abstract="Você pode adicionar manualmente novos endereços de email ou domínios à lista de permissões, selecionando-os um por um."

Você pode preencher manualmente a variável [!DNL Journey Optimizer] lista de permissões adicionando um endereço de email ou um domínio pela interface do usuário.

>[!NOTE]
>
>Você só pode adicionar um endereço de email ou domínio por vez.

Para fazer isso, siga as etapas abaixo.

1. Selecione o **[!UICONTROL Add email or domain]** botão.

   ![](assets/allowed-list-add-email.png)

1. Escolha o tipo de endereço: **[!UICONTROL Email address]** ou **[!UICONTROL Domain address]**.

1. Insira o endereço de email ou domínio para o qual deseja enviar emails.

   >[!NOTE]
   >
   >Certifique-se de inserir um endereço de email válido (como abc@company.com) ou domínio (como abc.company.com).

1. Especifique um motivo, se necessário.

   ![](assets/allowed-list-add-email-address.png)

   >[!NOTE]
   >
   >Todos os caracteres ASCII compreendidos entre 32 e 126 são permitidos no **[!UICONTROL Reason]** campo. A lista completa pode ser encontrada em [esta página](https://en.wikipedia.org/wiki/Wikipedia:ASCII#ASCII_printable_characters){target=&quot;_blank&quot;} por exemplo.

1. Clique em **[!UICONTROL Submit]**.

### Adicionar entidades usando uma chamada de API {#api-call-allowed-list}

Para preencher a lista de permissões, você também pode chamar a API de supressão com a função `ALLOWED` para a variável `listType` atributo. Por exemplo:

![](assets/allow-list-api.png)

Você pode executar o **Adicionar**, **Excluir** e **Get** operações.

Saiba mais sobre como fazer chamadas de API no [APIs da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html)Documentação de referência de {target=&quot;_blank&quot;}.

## Lógica de lista permitida {#logic}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_logic"
>title="Gerenciar a lista de permissões"
>abstract="Quando a lista de permissões for ativada, somente os recipients incluídos na lista de permissões receberão mensagens de email dessa sandbox. Quando desativado, todos os recipients receberão emails."

Quando a lista de permissões é [ative](#enable-allow-list), aplica-se a seguinte lógica:

* Se a lista de permissões for **empty**, nenhum email será enviado.

* Se uma entidade for **na lista de permissões**, e não na lista de supressão, o email é enviado para os recipients correspondentes. No entanto, se a entidade também estiver no [lista de supressão](../reports/suppression-list.md), os recipients correspondentes não receberão o email, sendo o motivo **[!UICONTROL Suppressed]**.

* Se uma entidade for **não na lista de permissões** (e não na lista de supressão), os recipients correspondentes não receberão o email, o motivo sendo **[!UICONTROL Not allowed]**.

>[!NOTE]
>
>Os perfis com **[!UICONTROL Not allowed]** são excluídos durante o processo de envio da mensagem. Portanto, enquanto a variável **Relatórios de jornada** mostrará esses perfis como tendo se movido pela jornada ([Ler segmento](../building-journeys/read-segment.md) e [atividades de mensagem](../building-journeys/journeys-message.md)), **Relatórios de email** não os incluirá no **[!UICONTROL Sent]** métricas como são filtradas antes do envio do email.
>
>Saiba mais sobre o [Relatório ao vivo](../reports/live-report.md) e [Relatório Global](../reports/global-report.md).

Quando a lista de permissões é [desativado](#deactivate-allow-list), todos os emails que você está enviando da sandbox atual são enviados para todos os recipients (desde que não estejam na lista de supressão), incluindo endereços de cliente real.

## Relatórios de exclusão {#reporting}

Quando a lista de permissões está ativa, você pode recuperar endereços de email ou domínios que foram excluídos de um envio porque não estavam na lista de permissões. Para fazer isso, você pode usar a variável [Serviço de query da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;} para fazer as chamadas de API abaixo.

Para obter o **número de emails** que não foram enviados porque os recipients não estavam na lista de permissões, use a seguinte query:

```sql
SELECT count(distinct _id) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID = '<MESSAGE_EXECUTION_ID>' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

Para obter o **lista de endereços de email** que não foram enviados porque os recipients não estavam na lista de permissões, use a seguinte query:

```sql
SELECT distinct(_experience.customerJourneyManagement.emailChannelContext.address) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID IS NOT NULL AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```
