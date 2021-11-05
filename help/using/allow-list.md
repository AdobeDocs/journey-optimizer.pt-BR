---
title: Lista de permissões
description: Saiba como usar a lista de permissões.
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: 70ab8f57-c132-4de1-847b-11f0ab14f422
source-git-commit: e1d0afb70af4ab31db56f90c189c085ba8d1eb7c
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 1%

---

# Lista de permissões {#allow-list}

Agora é possível definir uma lista específica de segurança de envio no [sandbox](administration/sandboxes.md) , para ter um ambiente seguro para fins de teste. Em uma instância de não produção, em que podem ocorrer erros, a lista de permissões garante que você não tenha risco de enviar mensagens indesejadas para seus clientes.

A lista de permissões permite especificar endereços de email ou domínios individuais que serão os únicos recipients ou domínios autorizados a receber os emails enviados de uma sandbox específica. Isso pode impedir que você envie emails acidentalmente para endereços de clientes reais quando estiver em um ambiente de teste.

>[!CAUTION]
>
>Este recurso é **not** disponível em sandboxes de produção. Ela se aplica somente ao canal de email.

## Ative a lista de permissões {#enable-allow-list}

Para ativar a lista de permissões em uma sandbox de não produção, é necessário atualizar as configurações gerais usando o ponto final da API correspondente no Serviço de predefinições de mensagens.

* Com essa API, você também pode desativar o recurso a qualquer momento.

* Você pode atualizar a lista de permissões antes ou depois de habilitar o recurso.

* A lógica de lista de permissões se aplica quando o recurso está ativado **e** se a lista de permissões for **not** vazio. Saiba mais [nesta seção](#logic).

<!--To enable this feature on a non-production sandbox, update the allowed list so that it is no longer empty. To disable it, clear up the allowed list so that it is again empty.

Learn more on the allowed list logic in this section.
-->

>[!NOTE]
>
>Quando ativado, o recurso de lista de permissões é honrado ao executar jornadas, mas também ao testar mensagens com [provas](preview.md#send-proofs) e teste de jornadas usando o [modo de teste](building-journeys/testing-the-journey.md).

## Adicionar entidades à lista de permissões {#add-entities}

Para adicionar novos endereços de email ou domínios à lista de permissões para uma sandbox específica, chame a API de supressão com a função `ALLOWED` para a variável `listType` atributo. Por exemplo:

![](assets/allow-list-api.png)

Você pode executar o **Adicionar**, **Excluir** e **Get** operações.

>[!NOTE]
>
>A lista de permissões pode conter até 1.000 entradas.

<!--
Learn more on making these API calls in the API reference documentation.
Found this link in Experience Platform documentation, but may not be the final one: (https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=en).-->

## Lógica da lista de permissões {#logic}

<!-- When the allowed list is enabled (enable-allow-list) at the sandbox level using the API call above, the following applies.-->

Quando a lista de permissões for **empty**, a lógica de lista de permissões não é aplicada. Isso significa que você pode enviar emails para qualquer perfil, desde que não estejam no [lista de supressão](suppression-list.md).

Quando a lista de permissões for **not empty**, a lógica de lista de permissões é aplicada:

* Se uma entidade for **não na lista de permissões**, e não na lista de supressão, o recipient correspondente não receberá o email, o motivo sendo **[!UICONTROL Not allowed]**.

* Se uma entidade for **na lista de permissões**, e não na lista de supressão, o email pode ser enviado para o recipient correspondente. No entanto, se a entidade também estiver no [lista de supressão](suppression-list.md), o recipient correspondente não receberá o email, o motivo sendo **[!UICONTROL Suppressed]**.

>[!NOTE]
>
>Os perfis com **[!UICONTROL Not allowed]** são excluídos durante o processo de envio da mensagem. Portanto, enquanto a variável **Relatórios de Jornada** mostrará esses perfis como tendo sido movidos pela jornada ([Ler segmento](building-journeys/read-segment.md) e [Mensagem](building-journeys/journeys-message.md) atividades), **Relatórios de email** não os incluirá no **[!UICONTROL Sent]** métricas como são filtradas antes do envio do email.
>
>Saiba mais sobre o [Relatório ao vivo](reports/live-report.md) e [Relatório Global](reports/global-report.md).

## Relatórios de exclusão {#reporting}

Quando esse recurso é ativado em uma sandbox de não produção, é possível recuperar endereços de email ou domínios que foram excluídos de um envio porque não estavam na lista de permissões. Para fazer isso, você pode usar a variável [Serviço de query Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;} para fazer as chamadas de API abaixo.

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
