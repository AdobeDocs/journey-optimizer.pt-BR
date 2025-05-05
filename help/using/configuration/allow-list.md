---
solution: Journey Optimizer
product: journey optimizer
title: Lista de permissões
description: Saiba como usar a lista de permissões
feature: Deliverability
topic: Content Management
role: Admin
level: Experienced
keywords: lista de permissões, lista, seguro, configuração
exl-id: 70ab8f57-c132-4de1-847b-11f0ab14f422
source-git-commit: 2af0e9237bbcc79456a31042ed8e42233bbccac3
workflow-type: tm+mt
source-wordcount: '1179'
ht-degree: 15%

---

# Lista de permissões {#allow-list}

É possível definir uma lista específica de segurança de envio no nível da [sandbox](../administration/sandboxes.md).

Essa lista de permissões permite especificar endereços de email ou domínios individuais que serão os únicos destinatários ou domínios autorizados a receber os emails enviados de uma sandbox específica.

>[!CAUTION]
>
>Esse recurso se aplica somente ao canal de email. Ele está disponível em sandboxes de produção e não produção.

Por exemplo, em uma instância de não produção, em que podem ocorrer erros, a lista de permissões garante que você não tenha risco de enviar mensagens indesejadas para endereços reais de clientes e, portanto, fornece um ambiente seguro para fins de teste.

Além disso, quando a lista de permissões estiver ativa, mas vazia, nenhum email será enviado. Portanto, se você encontrar algum problema grave, poderá usar este recurso para interromper todas as comunicações de saída de [!DNL Journey Optimizer] até que corrija o problema. Saiba mais sobre a [lógica de lista de permissões](#logic).

Além disso, é possível aproveitar a **API REST de supressão** do Journey Optimizer para controlar as mensagens enviadas usando listas de supressão e de permissões. [Saiba como trabalhar com a API REST de supressão](https://developer.adobe.com/journey-optimizer-apis/references/suppression/){target="_blank"}

## Acessar a lista de permissões {#access-allowed-list}

Para acessar a lista detalhada de domínios e endereços de email permitidos, vá para **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Configurações de email]** e selecione **[!UICONTROL Lista de permissões]**.

![](assets/allow-list-access.png)

>[!CAUTION]
>
>As permissões para exibir, exportar e gerenciar a lista de permissões são restritas a [Administradores do Jornada](../administration/ootb-product-profiles.md#journey-administrator). Saiba mais sobre como gerenciar os direitos de acesso de [!DNL Journey Optimizer] usuários em [esta seção](../administration/permissions-overview.md).

Para exportar a lista de permissões como um arquivo CSV, selecione o botão **[!UICONTROL Baixar CSV]**.

Use o botão **[!UICONTROL Excluir]** para remover permanentemente uma entrada.

Você pode pesquisar endereços de email ou domínios e filtrar por **[!UICONTROL Tipo de endereço]**. Depois de selecionado, é possível limpar o filtro exibido na parte superior da lista.

![](assets/allowed-list-filtering-example.png)

## Ativar a lista de permissões {#enable-allow-list}

Para ativar a lista de permissões, siga as etapas abaixo.

1. Acesse o menu **[!UICONTROL Canais]** > **[!UICONTROL Configuração de email]** > **[!UICONTROL Lista de permissões]**.

1. Selecione o botão de alternância.

   ![](assets/allow-list-edit.png)

1. Selecione **[!UICONTROL Ativar lista de permissões]**. A lista de permissões agora está ativa.

   ![](assets/allow-list-enable.png)

   >[!NOTE]
   >
   >After you activate the allowed list, there is a 10-minute delay before it takes effect in your journeys and campaigns. Similarly, updates to both the allowed list and suppression list can take up to 10 minutes to reflect.

A lógica de lista de permissões se aplica quando o recurso está ativo. Saiba mais [nesta seção](#logic).

>[!NOTE]
>
>Quando ativado, o recurso de lista de permissões é utilizado ao executar jornadas, mas também ao testar mensagens com [provas](../content-management/proofs.md) e jornadas de teste usando o [modo de teste](../building-journeys/testing-the-journey.md).

## Desativar a lista de permissões {#deactivate-allow-list}

Para desativar a lista de permissões, siga as etapas abaixo.

1. Acesse o menu **[!UICONTROL Canais]** > **[!UICONTROL Configuração de email]** > **[!UICONTROL Lista de permissões]**.

1. Selecione o botão de alternância.

   ![](assets/allow-list-edit-active.png)

1. Selecione **[!UICONTROL Desativar lista de permissões]**. A lista de permissões não está mais ativa.

   ![](assets/allow-list-deactivate.png)

   >[!NOTE]
   >
   >After you deactivate the allowed list, there is a 10-minute delay before it takes effect in your journeys and campaigns. Similarly, updates to both the allowed list and suppression list can take up to 10 minutes to reflect.

A lógica de lista de permissões não se aplica quando o recurso é desativado. Saiba mais [nesta seção](#logic).

## Adicionar entidades à lista de permissões {#add-entities}

Para adicionar novos domínios ou endereços de email à lista de permissões para uma sandbox específica, você pode [preencher manualmente a lista](#manually-populate-list) ou usar uma [chamada de API](#api-call-allowed-list).

>[!NOTE]
>
>A lista de permissões pode conter até 1.000 entradas.

### Preencher manualmente a lista de permissões {#manually-populate-list}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_add_header"
>title="Adicionar endereços ou domínios à lista de permissões"
>abstract="Você pode adicionar manualmente novos endereços de email ou domínios à lista de permissões selecionando-os um por um."

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_add"
>title="Adicionar endereços ou domínios à lista de permissões"
>abstract="Você pode adicionar manualmente novos endereços de email ou domínios à lista de permissões selecionando-os um por um."

Você pode preencher manualmente a lista de permissões [!DNL Journey Optimizer] adicionando um endereço de email ou um domínio por meio da interface do usuário.

>[!NOTE]
>
>Você só pode adicionar um endereço de email ou domínio por vez.

Para fazer isso, siga as etapas abaixo.

1. Selecione o botão **[!UICONTROL Adicionar email ou domínio]**.

   ![](assets/allowed-list-add-email.png)

1. Escolha o tipo de endereço: **[!UICONTROL Endereço de email]** ou **[!UICONTROL Endereço de domínio]**.

1. Insira o endereço de email ou domínio para o qual deseja enviar emails.

   >[!NOTE]
   >
   >Certifique-se de inserir um endereço de email (como abc@empresa.com) ou de domínio (como abc.empresa.com) válido.

1. Especifique um motivo, se necessário.

   ![](assets/allowed-list-add-email-address.png)

   >[!NOTE]
   >
   >Todos os caracteres ASCII entre 32 e 126 são permitidos no campo **[!UICONTROL Motivo]**. The full list can be found on [this page](https://en.wikipedia.org/wiki/ASCII#Printable_characters){target="_blank"} for example.

1. Clique em **[!UICONTROL Enviar]**.

### Adicionar entidades usando uma chamada de API {#api-call-allowed-list}

Para preencher a lista de permissões, você também pode chamar a API de supressão com o valor `ALLOWED` para o atributo `listType`. Por exemplo:

![](assets/allow-list-api.png)

Você pode executar as operações **Adicionar**, **Excluir** e **Obter**.

Learn more about making API calls in the [Adobe Experience Platform APIs](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=pt-BR){target="_blank"} reference documentation.

## Baixar a lista de permissões {#download-allowed-list}

Para exportar a lista de permissões como um arquivo CSV, siga as etapas abaixo:

1. Selecione o botão **[!UICONTROL Baixar CSV]**.

   ![](assets/allowed-list-download-csv.png)

1. Espere até que o arquivo seja gerado.

   ![](assets/allowed-list-download-generate.png)

   >[!NOTE]
   >
   >O tempo de download depende do tamanho do arquivo, o que significa o número de endereços na lista de permissões.
   >
   >Uma solicitação de download pode ser processada de cada vez para uma determinada sandbox.

1. Depois que o arquivo for gerado, você receberá uma notificação. Clique no ícone de sino na parte superior direita da tela para exibi-lo.

1. Clique na própria notificação para baixar o arquivo.

   ![](assets/allowed-list-download-notification.png)

   >[!NOTE]
   >
   >O link é válido por 24 horas.

## Lógica de lista de permissões {#logic}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_logic"
>title="Gerenciar a lista de permissões"
>abstract="Quando a lista de permissões for ativada, somente os recipients incluídos na lista de permissões receberão mensagens de email dessa sandbox. Quando desativado, todos os recipients receberão emails."

Quando a lista de permissões está [ativa](#enable-allow-list), a seguinte lógica é aplicada:

* Se a lista de permissões estiver **vazia**, nenhum email será enviado.

* Se uma entidade estiver **na lista de permissões**, e não na lista de supressão, o email será enviado ao(s) destinatário(s) correspondente(s). No entanto, se a entidade também estiver na [lista de supressão](../reports/suppression-list.md), os destinatários correspondentes não receberão o email, o motivo será **[!UICONTROL Suprimido]**.

* Se uma entidade **não estiver na lista de permissões** (e não na lista de supressão), os destinatários correspondentes não receberão o email, o motivo será **[!UICONTROL Não permitido]**.

>[!NOTE]
>
>Os perfis com status **[!UICONTROL Não permitido]** são excluídos durante o processo de envio da mensagem. Portanto, enquanto os **relatórios de Jornada** mostrarão esses perfis como tendo sido movidos pela jornada ([Ler público-alvo](../building-journeys/read-audience.md) e [atividades de mensagem](../building-journeys/journeys-message.md)), os **relatórios de email** não os incluirão nas métricas **[!UICONTROL Enviados]**, pois eles são filtrados antes do envio de email.
>
>Saiba mais sobre o [Relatório ao vivo](../reports/live-report.md) e o [Relatório do Customer Journey Analytics](../reports/report-gs-cja.md).

Quando a lista de permissões é [desativada](#deactivate-allow-list), todos os emails que você está enviando da sandbox atual são enviados para todos os destinatários (desde que não estejam na lista de supressão), incluindo endereços reais de clientes.

## Relatório de exclusão {#reporting}

Quando a lista de permissões está ativa, é possível recuperar endereços de email ou domínios que foram excluídos de um envio porque não estavam na lista de permissões. To do this, you can use the [Adobe Experience Platform Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html?lang=pt-BR){target="_blank"} to make the API calls below.

Para obter o **número de emails** que não foram enviados porque os destinatários não estavam na lista de permissões, use a seguinte consulta:

```sql
SELECT count(distinct _id) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID = '<MESSAGE_EXECUTION_ID>' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

Para obter a **lista de endereços de email** que não foram enviados porque os destinatários não estavam na lista de permissões, use a seguinte consulta:

```sql
SELECT distinct(_experience.customerJourneyManagement.emailChannelContext.address) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID IS NOT NULL AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```
