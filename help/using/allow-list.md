---
title: Lista de permissões
description: Saiba como usar a lista de permissões.
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
source-git-commit: 9408a93deecfb12f28a0a87c19fa0074c66844a9
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 1%

---

# Lista de permissões {#allow-list}

Agora é possível definir uma lista segura para envio específica no nível [sandbox](administration/sandboxes.md), para ter um ambiente seguro para fins de teste. Em uma instância de não produção, em que podem ocorrer erros, a lista de permissões garante que você não tenha risco de enviar mensagens indesejadas para seus clientes.

A lista de permissões permite especificar endereços de email ou domínios individuais que serão os únicos recipients ou domínios autorizados a receber os emails enviados de uma sandbox específica. Isso pode impedir que você envie emails acidentalmente para endereços de clientes reais quando estiver em um ambiente de teste.

>[!CAUTION]
>
>Esse recurso está **não** disponível nas sandboxes de produção. Ela se aplica somente ao canal de email.

## Ative a lista de permissões {#enable-allow-list}

Para ativar a lista de permissões em uma sandbox de não produção, é necessário atualizar as configurações gerais usando o ponto final da API correspondente no Serviço de predefinições de mensagens.

* Com essa API, você também pode desativar o recurso a qualquer momento.

* Você pode atualizar a lista de permissões antes ou depois de habilitar o recurso.

* A lógica de lista de permissões se aplica quando o recurso é ativado **e** se a lista de permissões for **e não** vazia. Saiba mais [nesta seção](#logic).

<!--To enable this feature on a non-production sandbox, update the allowed list so that it is no longer empty. To disable it, clear up the allowed list so that it is again empty.

Learn more on the allowed list logic in this section.
-->

>[!NOTE]
>
>Quando ativado, o recurso de lista de permissões é honrado ao executar jornadas, mas também ao testar mensagens com [provas](preview.md#send-proofs) e testar jornadas usando o [modo de teste](building-journeys/testing-the-journey.md).

## Adicionar entidades à lista de permissões {#add-entities}

Para adicionar novos endereços de email ou domínios à lista de permissões para uma sandbox específica, você deve chamar a API de supressão com o valor `ALLOWED` para o atributo `listType` . Por exemplo:

![](assets/allow-list-api.png)

Você pode executar as operações **Adicionar**, **Excluir** e **Obter**.

>[!NOTE]
>
>A lista de permissões pode conter até 1.000 entradas.

<!--
Learn more on making these API calls in the API reference documentation.
Found this link in Experience Platform documentation, but may not be the final one: (https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=en).-->

## Lógica da lista de permissões {#logic}

<!-- When the allowed list is enabled (enable-allow-list) at the sandbox level using the API call above, the following applies.-->

Quando a lista de permissões é **empty**, a lógica de lista de permissões não é aplicada. Isso significa que você pode enviar emails para qualquer perfil, desde que não estejam na [lista de supressão](suppression-list.md).

Quando a lista de permissões for **not empty**, a lógica de lista de permissões será aplicada:

* Se uma entidade não estiver **na lista de permissões** e não estiver na lista de supressão, o recipient correspondente não receberá o email, sendo o motivo **[!UICONTROL Not allowed]**.

* Se uma entidade estiver **na lista de permissões**, e não na lista de supressão, o email poderá ser enviado para o recipient correspondente. No entanto, se a entidade também estiver na [lista de supressão](suppression-list.md), o recipient correspondente não receberá o email, sendo o motivo **[!UICONTROL Suppressed]**.

>[!NOTE]
>
>Os perfis com status **[!UICONTROL Not allowed]** são excluídos durante o processo de envio da mensagem. Portanto, enquanto os **Relatórios de Jornada** mostrarão esses perfis como tendo sido movidos pela jornada ([Ler segmento](building-journeys/read-segment.md) e [Mensagem](building-journeys/journeys-message.md) atividades), os **Relatórios de email** não os incluirão nas métricas **[!UICONTROL Sent]**, pois são filtrados antes do envio de email.
>
>Saiba mais sobre o [Relatório ao vivo](reports/live-report.md) e [Relatório global](reports/global-report.md).

## Relatórios de exclusão {#reporting}

Quando esse recurso é ativado em uma sandbox de não produção, é possível recuperar endereços de email ou domínios que foram excluídos de um envio porque não estavam na lista de permissões. Para fazer isso, você pode usar o [Adobe Experience Platform Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;} para fazer as chamadas de API abaixo.

Para obter o **número de emails** que não foram enviados porque os recipients não estavam na lista de permissões, use a seguinte query:

```
SELECT count(distinct _id) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID = '<MESSAGE_EXECUTION_ID>' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

Para obter a **lista de endereços de email** que não foram enviados porque os recipients não estavam na lista de permissões, use a seguinte consulta:

```
SELECT distinct(_experience.customerJourneyManagement.emailChannelContext.address) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID IS NOT NULL AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

