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
source-git-commit: b4fda6a0bd3e633811c16ef6dc3a3171b3b350c8
workflow-type: tm+mt
source-wordcount: '1165'
ht-degree: 15%

---

# Lista de permissões {#allow-list}

É possível definir uma lista específica de segurança de envio no [sandbox](../administration/sandboxes.md) nível.

Essa lista de permissões permite especificar endereços de email ou domínios individuais que serão os únicos destinatários ou domínios autorizados a receber os emails enviados de uma sandbox específica.

>[!CAUTION]
>
>Esse recurso se aplica somente ao canal de email. Ele está disponível em sandboxes de produção e não produção.

Por exemplo, em uma instância de não produção, em que podem ocorrer erros, a lista de permissões garante que você não tenha risco de enviar mensagens indesejadas para endereços reais de clientes e, portanto, fornece um ambiente seguro para fins de teste.

Além disso, quando a lista de permissões estiver ativa, mas vazia, nenhum email será enviado. Portanto, se você encontrar algum problema grave, poderá usar esse recurso para interromper todas as comunicações de saída do [!DNL Journey Optimizer] até que você corrija o problema. Saiba mais sobre o [Lógica de lista de permissões](#logic).

Além disso, você pode aproveitar o Journey Optimizer **API REST de supressão** para controlar as mensagens de saída usando supressão e listas de permissões. [Saiba como trabalhar com a API REST de supressão](https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/monitor-reputation/manage-suppression-list.html?lang=pt-BR)

## Acessar a lista de permissões {#access-allowed-list}

Para acessar a lista detalhada de domínios e endereços de email permitidos, acesse **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Configuração de email]** e selecione **[!UICONTROL Lista de permissões]**.

![](assets/allow-list-access.png)

>[!CAUTION]
>
>As permissões para exibir, exportar e gerenciar a lista de permissões são restritas a [Administradores do Jornada](../administration/ootb-product-profiles.md#journey-administrator). Saiba mais sobre gerenciamento [!DNL Journey Optimizer] direitos de acesso dos usuários no [nesta seção](../administration/permissions-overview.md).

Para exportar a lista de permissões como um arquivo CSV, selecione o **[!UICONTROL Baixar CSV]** botão.

Use o **[!UICONTROL Excluir]** botão para remover permanentemente uma entrada.

Você pode pesquisar por endereços de email ou domínios e filtrar por **[!UICONTROL Tipo de endereço]**. Depois de selecionado, é possível limpar o filtro exibido na parte superior da lista.

![](assets/allowed-list-filtering-example.png)

## Ativar a lista de permissões {#enable-allow-list}

Para ativar a lista de permissões, siga as etapas abaixo.

1. Acesse o  **[!UICONTROL Canais]** > **[!UICONTROL Configuração de email]** > **[!UICONTROL Lista de permissões]** menu.

1. Selecione o botão de alternância.

   ![](assets/allow-list-edit.png)

1. Selecionar **[!UICONTROL Ativar lista de permissões]**. A lista de permissões agora está ativa.

   ![](assets/allow-list-enable.png)

   >[!NOTE]
   >
   >Após ativar a lista de permissões, há uma latência de 5 minutos para que ela entre em vigor em suas jornadas e campanhas.

A lógica de lista de permissões se aplica quando o recurso está ativo. Saiba mais [nesta seção](#logic).

>[!NOTE]
>
>Quando ativado, o recurso de lista de permissões é respeitado ao executar jornadas, mas também ao testar mensagens com [provas](../content-management/proofs.md) e jornadas de teste usando o [modo de teste](../building-journeys/testing-the-journey.md).

## Desativar a lista de permissões {#deactivate-allow-list}

Para desativar a lista de permissões, siga as etapas abaixo.

1. Acesse o  **[!UICONTROL Canais]** > **[!UICONTROL Configuração de email]** > **[!UICONTROL Lista de permissões]** menu.

1. Selecione o botão de alternância.

   ![](assets/allow-list-edit-active.png)

1. Selecionar **[!UICONTROL Desativar lista de permissões]**. A lista de permissões não está mais ativa.

   ![](assets/allow-list-deactivate.png)

   >[!NOTE]
   >
   >Depois de desativar a lista de permissões, há uma latência de 5 minutos para que ela entre em vigor em suas jornadas e campanhas.

A lógica de lista de permissões não se aplica quando o recurso é desativado. Saiba mais [nesta seção](#logic).

## Adicionar entidades à lista de permissões {#add-entities}

Para adicionar novos domínios ou endereços de email à lista de permissões para uma sandbox específica, você pode [preencher manualmente a lista](#manually-populate-list)ou use um [Chamada de API](#api-call-allowed-list).

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

É possível preencher manualmente a variável [!DNL Journey Optimizer] lista de permissões adicionando um endereço de email ou um domínio por meio da interface.

>[!NOTE]
>
>Você só pode adicionar um endereço de email ou domínio por vez.

Para fazer isso, siga as etapas abaixo.

1. Selecione o **[!UICONTROL Adicionar email ou domínio]** botão.

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
   >Todos os caracteres ASCII entre 32 e 126 são permitidos na variável **[!UICONTROL Motivo]** campo. Para referência, a lista completa pode ser encontrada [nesta página](https://en.wikipedia.org/wiki/Wikipedia:ASCII#ASCII_printable_characters){target="_blank"}.

1. Clique em **[!UICONTROL Enviar]**.

### Adicionar entidades usando uma chamada de API {#api-call-allowed-list}

Para preencher a lista de permissões, você também pode chamar a API de supressão com a variável `ALLOWED` valor para o `listType` atributo. Por exemplo:

![](assets/allow-list-api.png)

Você pode executar a **Adicionar**, **Excluir** e **Obter** operações.

Saiba mais sobre como fazer chamadas de API no [APIs do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html){target="_blank"} documentação de referência.

## Baixar a lista de permissões {#download-allowed-list}

Para exportar a lista de permissões como um arquivo CSV, siga as etapas abaixo:

1. Selecione o **[!UICONTROL Baixar CSV]** botão.

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

Quando a lista de permissões é [ativo](#enable-allow-list), aplica-se a seguinte lógica:

* Se a lista de permissões for **vazio**, nenhum email será enviado.

* Se uma entidade for **na lista de permissões**, e não na lista de supressão, o email é enviado aos recipients correspondentes. No entanto, se a entidade também estiver [lista de supressão](../reports/suppression-list.md), os recipients correspondentes não receberão o email, o motivo é **[!UICONTROL Suprimido]**.

* Se uma entidade for **não está na lista de permissões** (e não na lista de supressão), os recipients correspondentes não receberão o email, o motivo sendo **[!UICONTROL Não permitido]**.

>[!NOTE]
>
>Os perfis com **[!UICONTROL Não permitido]** Os status de são excluídos durante o processo de envio da mensagem. Por conseguinte, embora a **Jornada relatórios** mostrará esses perfis como tendo passado pela jornada ([Ler público-alvo](../building-journeys/read-audience.md) e [atividades de mensagem](../building-journeys/journeys-message.md)), o **Relatórios de email** não os incluirá no **[!UICONTROL Enviado]** métricas conforme são filtradas antes do envio de email.
>
>Saiba mais sobre o [Relatório ao vivo](../reports/live-report.md) e [Relatório global](../reports/global-report.md).

Quando a lista de permissões é [desativado](#deactivate-allow-list), todos os emails enviados da sandbox atual são enviados para todos os recipients (desde que não estejam na lista de supressão), incluindo endereços reais de clientes.

## Relatório de exclusão {#reporting}

Quando a lista de permissões está ativa, é possível recuperar endereços de email ou domínios que foram excluídos de um envio porque não estavam na lista de permissões. Para fazer isso, você pode usar o [Serviço de consulta Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"} para fazer as chamadas de API abaixo.

Para obter a **número de emails** que não foram enviados porque os destinatários não estavam na lista de permissões, use a seguinte query:

```sql
SELECT count(distinct _id) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID = '<MESSAGE_EXECUTION_ID>' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

Para obter a **lista de endereços de email** que não foram enviados porque os destinatários não estavam na lista de permissões, use a seguinte query:

```sql
SELECT distinct(_experience.customerJourneyManagement.emailChannelContext.address) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID IS NOT NULL AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```
