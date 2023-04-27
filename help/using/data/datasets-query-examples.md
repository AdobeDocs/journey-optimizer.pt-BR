---
solution: Journey Optimizer
product: journey optimizer
title: Exemplos de consultas do conjunto de dados
description: Exemplos de consultas do conjunto de dados
feature: Reporting
topic: Content Management
role: User
level: Intermediate
keywords: conjunto de dados, otimizador, casos de uso
exl-id: 26ba8093-8b6d-4ba7-becf-b41c9a06e1e8
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '850'
ht-degree: 1%

---

# Casos de uso do conjunto de dados {#tracking-datasets}

Nesta página, você encontrará a lista de conjuntos de dados do Adobe Journey Optimizer e casos de uso relacionados:

[Conjunto de dados de eventos de experiência de rastreamento de email](#email-tracking-experience-event-dataset)
[Conjunto de dados do evento de feedback de mensagem](#message-feedback-event-dataset)
[Conjunto de dados do evento de experiência de rastreamento de push](#push-tracking-experience-event-dataset)
[Evento de etapa de Jornada](#journey-step-event)
[Conjunto de dados do evento de decisão](#ode-decisionevents)
[Conjunto de dados do evento de feedback CCO](#bcc-feedback-event-dataset)
[Conjunto de dados da entidade](#entity-dataset)

Para exibir a lista completa de campos e atributos para cada schema, consulte o [Dicionário de esquema Journey Optimizer](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=pt-BR){target="_blank"}.

## Conjunto de dados de eventos de experiência de rastreamento de email{#email-tracking-experience-event-dataset}

_Nome na interface : Conjunto de dados de eventos de experiência de rastreamento de email CJM_

Conjunto de dados do sistema para assimilar eventos de experiência de rastreamento de email do Journey Optimizer.

O schema relacionado é o Esquema de evento da experiência de rastreamento de email CJM.

Esta query mostra as contagens de diferentes interações de email (aberturas, cliques) de uma determinada mensagem:

```sql
select
    _experience.customerJourneyManagement.messageInteraction.interactionType AS interactionType,
    count(1) eventCount
from cjm_email_tracking_experience_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.messageExecutionID IN ('UMA-30647505')
group by
    _experience.customerJourneyManagement.messageInteraction.interactionType
```

Esta query mostra o detalhamento das contagens de diferentes interações de email (aberturas, cliques) por mensagem para uma determinada jornada:

```sql
select
    _experience.customerJourneyManagement.messageExecution.messageExecutionID AS messageExecutionID,
    _experience.customerJourneyManagement.messageInteraction.interactionType AS interactionType,
    count(1) eventCount
from cjm_email_tracking_experience_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
group by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageInteraction.interactionType
order by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageInteraction.interactionType
limit 100;
```

## Conjunto de dados do evento de feedback de mensagem{#message-feedback-event-dataset}

_Nome na interface: Conjunto de dados do evento de feedback de mensagem CJM_

Conjunto de dados para assimilar eventos de feedback de aplicativos de email e de push do Journey Optimizer.

O schema relacionado é o Esquema de Evento de Feedback de Mensagem CJM.

Esta consulta mostra as contagens de diferentes status de feedback de email (enviado, rejeição, etc.) para uma determinada mensagem:

```sql
select
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus AS feedbackStatus,
    count(1) eventCount
from cjm_message_feedback_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.messageExecutionID IN ('UMA-30647505')
group by
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus;
```

Esta consulta mostra o detalhamento de contagens de diferentes status de feedback de email (enviado, rejeição, etc.) por mensagem para uma determinada jornada:

```sql
select
    _experience.customerJourneyManagement.messageExecution.messageExecutionID AS messageExecutionID,
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus AS feedbackStatus,
    count(1) eventCount
from cjm_message_feedback_event_dataset
where
     _experience.customerJourneyManagement.messageExecution.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
group by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus
order by
    _experience.customerJourneyManagement.messageExecution.messageExecutionID,
    _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus
limit 100;
```

Em nível de agregação, relatório em nível de domínio (classificado por domínios principais): Nome do domínio, mensagem enviada, rejeições

```sql
SELECT split_part(_experience.customerJourneyManagement.emailChannelContext.address, '@', 2) AS recipientDomain, SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' THEN 1 ELSE 0 END)AS sentCount , SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'bounce' THEN 1 ELSE 0 END )AS bounceCount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY recipientDomain ORDER BY sentCount DESC;
```

Envios de email diariamente:

```sql
SELECT date_trunc('day', TIMESTAMP) AS rolluptimestamp, SUM( CASE WHEN _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'sent' THEN 1 ELSE 0 END) AS deliveredcount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY date_trunc('day', TIMESTAMP) ORDER BY rolluptimestamp ASC;
```

Descubra se uma determinada ID de email recebeu um email ou não e, se não, qual foi o erro, a categoria de devolução, o código:

```sql
SELECT _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS status, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type AS bouncetype FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' AND _experience.customerjourneymanagement.emailchannelcontext.address = 'user@domain.com' AND TIMESTAMP >= now() - INTERVAL '7' DAY ORDER BY status ASC
```

Encontre a lista de todas as IDs de email individuais que tiveram um erro específico, categoria de devolução ou código nos últimos x horas/dias ou associadas a um delivery de mensagem específico:

```sql
SELECT _experience.customerjourneymanagement.emailchannelcontext.address AS emailid, _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS status, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type AS bouncetype FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' AND _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus != 'sent' AND TIMESTAMP >= now() - INTERVAL '10' HOUR AND _experience.customerjourneymanagement.messageexecution.messageexecutionid = 'BMA-45237824' ORDER BY emailid
```

Taxa de rejeição permanente no nível agregado:

```sql
select hardBounceCount, case when sentCount > 0 then(hardBounceCount/sentCount)*100.0 else 0 end as hardBounceRate from ( select SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'bounce' AND _experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.type = 'Hard' THEN 1 ELSE 0 END)AS hardBounceCount , SUM( CASE WHEN _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' THEN 1 ELSE 0 END )AS sentCount from cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' )
```

Erros permanentes agrupados por código de devolução:

```sql
SELECT _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.reason AS failurereason, COUNT(*) AS hardbouncecount FROM cjm_message_feedback_event_dataset WHERE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'bounce' AND _experience.customerjourneymanagement.messagedeliveryfeedback.messagefailure.type = 'Hard' AND _experience.customerjourneymanagement.messageprofile.channel._id = 'https://ns.adobe.com/xdm/channels/email' GROUP BY failurereason
```

### Identificar endereços em quarentena após uma interrupção do ISP{#isp-outage-query}

No caso de uma interrupção do Provedor de serviços de Internet (ISP), é necessário identificar os endereços de email erroneamente marcados como rejeições (em quarentena) para domínios específicos, durante um período de tempo. Para obter esses endereços, use a seguinte query:

```sql
SELECT
    _experience.customerJourneyManagement.emailChannelContext.address AS RecipientAddress,
    timestamp AS EventTime,
    _experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.reason AS "Invalid Recipient"
FROM cjm_message_feedback_event_dataset
WHERE
    eventtype = 'message.feedback' AND
    DATE(timestamp) BETWEEN '<start-date-time>' AND '<end-date-time>' AND
    _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'bounce' AND
    _experience.customerJourneyManagement.emailChannelContext.address ILIKE '%domain.com%'
ORDER BY timestamp DESC;
```

em que o formato das datas é: AAAA-MM-DD HH:MM:S.

Depois de identificados, remova esses endereços da lista de supressão do Journey Optimizer. [Saiba mais](../configuration/manage-suppression-list.md#remove-from-suppression-list).

## Conjunto de dados do evento de experiência de rastreamento de push {#push-tracking-experience-event-dataset}

_Nome na interface: Conjunto de dados do evento de experiência de rastreamento de push CJM_

Conjunto de dados para assimilar eventos de experiência de rastreamento móvel para push do Journey Optimizer.

O schema relacionado é o Esquema de Evento de Experiência de Rastreamento de Push CJM.

Exemplo de consulta:

```sql
select _experience.customerJourneyManagement.pushChannelContext.platform, sum(pushNotificationTracking.customAction.value)  from cjm_push_tracking_experience_event_dataset
group by _experience.customerJourneyManagement.pushChannelContext.platform

select  _experience.customerJourneyManagement.pushChannelContext.platform, SUM (_experience.customerJourneyManagement.messageInteraction.offers.offerCount) from cjm_email_tracking_experience_event_dataset
  group by _experience.customerJourneyManagement.pushChannelContext.platform
```

## Evento de etapa de Jornada{#journey-step-event}

_Nome interno: Eventos de etapa do Jornada (conjunto de dados do sistema)_

Conjunto de dados para assimilar eventos de etapa na jornada.

O schema relacionado é o schema Jornada Step Event para o Journey Orchestration.

Esta consulta mostra o detalhamento das contagens de sucesso de ação por rótulo de ação para uma determinada jornada:

```sql
select
    _experience.journeyOrchestration.stepEvents.actionName AS actionLabel,
    count(1) actionSuccessCount
from journey_step_events
where
     _experience.journeyOrchestration.stepEvents.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
     AND _experience.journeyOrchestration.stepEvents.actionID IS NOT NULL
     AND _experience.journeyOrchestration.stepEvents.actionType IS NOT NULL
     AND _experience.journeyOrchestration.stepEvents.actionExecutionErrorCode IS NULL
group by
    _experience.journeyOrchestration.stepEvents.actionName;   
```

Esta consulta mostra o detalhamento das contagens da etapa inseridas por nodeId e nodeLabel para uma determinada jornada. nodeId está incluído aqui, pois nodeLabel pode ser o mesmo para nós de jornada diferentes.

```sql
select
    _experience.journeyOrchestration.stepEvents.nodeID AS nodeID,
    _experience.journeyOrchestration.stepEvents.nodeName AS nodeLabel,
    count(1) stepEnteredCount
from journey_step_events
where
     _experience.journeyOrchestration.stepEvents.journeyVersionID IN ('0e86ac62-c315-48cc-ab4f-3f8b741ae667')
     AND _experience.journeyOrchestration.stepEvents.journeyNodeProcessed = TRUE
     AND _experience.journeyOrchestration.stepEvents.eventID IS DISTINCT FROM 'createInstance'
group by
    _experience.journeyOrchestration.stepEvents.nodeID,
    _experience.journeyOrchestration.stepEvents.nodeName; 
```

## Conjunto de dados do evento de decisão{#ode-decisionevents}

_Nome na interface: ODE DecisionEvents (conjunto de dados do sistema)_

Conjunto de dados para assimilar apresentações de oferta para os usuários.

O schema relacionado é o ODE DecisionEvents.

Este query mostra todas as ofertas retornadas no dia anterior:

```sql
SELECT date_format(Decision.Timestamp, 'MM/dd/yyyy') as Date
,HOUR(Decision.timestamp) as Hour
,COUNT(*)  as Count
FROM ode_decisionevents_b699fa78_efec_41b1_99fa_78efecc1b1ef_decision AS Decision
WHERE date_format(Decision.timestamp, 'MM/dd/yyyy') = date_format(CURRENT_DATE, 'MM/dd/yyyy') and Decision._experience.decisioning.propositionDetails.activity[0].id = 'xcore:offer-activity:13ab41890a335ad6'
GROUP BY date_format(Decision.Timestamp, 'MM/dd/yyyy')
,HOUR(Decision.timestamp)
ORDER BY 1, 2 DESC;
```

Este query mostra o número de vezes que ofertas foram propostas nos últimos 30 dias de uma atividade/decisão específica e sua prioridade de oferta associada.

```sql
select proposedOffers.id,proposedOffers.name, po._experience.decisioning.ranking.priority, count(proposedOffers.id) as ProposedCount from (
select explode(propositionexplode.selections) AS proposedOffers from
(select explode(_experience.decisioning.propositionDetails) AS propositionexplode,timestamp FROM ode_decisionevents_itca_decisioning_20200925_235340_379  where date_format(timestamp, 'MM/dd/yyyy') >= date_format(DATE_ADD(CURRENT_DATE, -30), 'MM/dd/yyyy') and _experience.decisioning.propositionDetails.activity[0].id = 'xcore:offer-activity:12ae6f35a055c6f0')) a, decision_object_repository_personalized_offers po where proposedOffers.id LIKE 'xcore:personalized-offer%' and po._id=proposedOffers.id
group by proposedOffers.id, proposedOffers.name, po._experience.decisioning.ranking.priority;
```

<!--
## Consent Service Dataset{#consent-service-dataset}

_Name in the interface: CJM Consent Service Dataset (system dataset)_

Dataset for Journey Optimizer Consent service.

The related schema is CJM Consent Service Schema.

Query to list email IDs that have consented to receive email:

```sql
select key as email FROM (
  select explode(value) FROM (
  select explode(consents.idSpecific)
  from cjm_consent_service_dataset
 )
)
where value.marketing.email.val == 'y'
```

Query to return consent value for an email ID where email ID would be the input:

```sql
select value.marketing.email.val FROM (
  select explode(value) FROM (
  select explode(consents.idSpecific)
  from cjm_consent_service_dataset
 )
```
-->

## Conjunto de dados do evento de feedback CCO{#bcc-feedback-event-dataset}

_Nome na interface: Conjunto de dados de eventos de feedback CCO AJO (conjunto de dados do sistema)_

Conjunto de dados para armazenar informações para mensagens CCO.

Consulta para todas as mensagens CCO em 2 dias (para uma campanha específica):

```sql
SELECT bcc.*
FROM ajo_bcc_feedback_event_dataset AS bcc
WHERE 
    bcc._experience.customerJourneyManagement.messageExecution.messageExecutionID = '<message-execution-id>' AND 
    bcc.timestamp >= now() - INTERVAL '2' day; 
```

Consulte o conjunto de dados de feedback para mostrar aos usuários que não receberam (todas as rejeições e supressões) e que têm entrada CCO para uma mensagem específica:

```sql
SELECT 
    distinct bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress AS OriginalRecipientAddress 
FROM ajo_bcc_feedback_event_dataset  AS bcc 
WHERE 
    bcc.timestamp > now() - INTERVAL '2' DAY AND     bcc._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND      bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress != '' AND
    ( 
            bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress NOT IN ( 
        SELECT distinct mfe._experience.customerJourneyManagement.emailChannelContext.address
        FROM cjm_message_feedback_event_dataset AS mfe 
        WHERE 
            mfe.timestamp > now() - INTERVAL '2' DAY AND 
            mfe._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND
            mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus = 'sent'
        )  
    OR     bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress IN ( 
        SELECT distinct mfe._experience.customerJourneyManagement.emailChannelContext.address
        FROM cjm_message_feedback_event_dataset AS mfe 
        WHERE 
        mfe.timestamp > now() - INTERVAL '2' DAY AND 
            mfe._experience.customerJourneyManagement.messageExecution.messageExecutionID  = '<message-execution-id>' AND 
            mfe._experience.customerJourneyManagement.messageDeliveryfeedback.messageFailure.category = 'async' AND 
            mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus
```

## Conjunto de dados da entidade{#entity-dataset}

_Nome na interface: ajo_entity_dataset (conjunto de dados do sistema)_

Conjunto de dados para armazenar metadados da entidade para mensagens enviadas ao usuário final.

O schema relacionado é o Esquema de Entidade AJO.

Esse conjunto de dados fornece acesso aos metadados definidos pelo profissional de marketing, o que permite obter melhores insights de relatório quando os conjuntos de dados do Journey Optimizer são exportados para visualização de relatórios em ferramentas externas. Isso é obtido usando o atributo messageID que ajuda a compilar vários conjuntos de dados, como Conjunto de dados de feedback de mensagem e Conjuntos de dados de rastreamento de evento de experiência, para obter detalhes do delivery de mensagem do envio para o rastreamento no nível do perfil.

**Observações importantes**

* Uma entrada para uma mensagem é criada somente após a publicação da jornada ou campanha.

* Você pode ver a entrada 30 minutos após a publicação da campanha/jornada.

>[!NOTE]
>
>Por enquanto, há duas entradas para cada publicação de mensagem no conjunto de dados da entidade por motivos de compatibilidade futuros. Isso não afeta sua capacidade de usar consultas de associação conforme necessário em todos os conjuntos de dados para buscar as informações desejadas.

Se desejar classificar, em seus relatórios, os emails enviados por uma jornada específica de acordo com a ação que os enviou. você pode ingressar no conjunto de dados do Feedback de mensagem com o conjunto de dados da entidade. Os campos a serem usados são: `_experience.decisioning.propositions.scopeDetails.correlationID` e `_id field in entity dataset`.

A consulta a seguir ajuda a obter o template de mensagem associado para uma determinada campanha:

```sql
SELECT
  AE._experience.customerJourneyManagement.entities.channelDetails.template
from
  ajo_entity_dataset AE
    WHERE AE._experience.customerJourneyManagement.entities.campaign.campaignVersionID = 'd7a01136-b113-4ef2-8f59-b6001f7eef6e'
```

A consulta a seguir ajuda a obter os Detalhes da Jornada e o assunto do email associado a todos os eventos de feedback:

```sql
SELECT 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionName, 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionID, 
  AE._experience.customerJourneyManagement.entities.journey.journeyVersionID, 
  AE._experience.customerJourneyManagement.entities.channelDetails.email.subject 
from 
  ajo_entity_dataset AE 
  INNER JOIN cjm_message_feedback_event_dataset MF ON AE._experience.customerJourneyManagement.entities.channelDetails.messageID = MF._experience.customerJourneyManagement.messageExecution.messageID 
WHERE 
  AE._experience.customerJourneyManagement.entities.channelDetails.channel._id = 'https://ns.adobe.com/xdm/channels/email' 
  AND MF._experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' 
  AND AE._experience.customerJourneyManagement.entities.journey.journeyVersionID IS NOT NULL
```

É possível compilar eventos de etapa do jornada, Feedback de mensagem e conjuntos de dados de rastreamento para obter as estatísticas de um perfil específico:

```sql
SELECT 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionName, 
  AE._experience.customerJourneyManagement.entities.journey.journeyActionID, 
  AE._experience.customerJourneyManagement.entities.journey.journeyVersionID, 
  AE._experience.customerJourneyManagement.entities.channelDetails.email.subject,
    JE._EXPERIENCE.JOURNEYORCHESTRATION.STEPEVENTS.PROFILEID,
    JE._EXPERIENCE.JOURNEYORCHESTRATION.STEPEVENTS.NODENAME
from 
  ajo_entity_dataset AE 
  INNER JOIN cjm_message_feedback_event_dataset MF 
    ON AE._experience.customerJourneyManagement.entities.channelDetails.messageID = MF._experience.customerJourneyManagement.messageExecution.messageID 
    INNER JOIN journey_step_events JE
    ON AE._experience.customerJourneyManagement.entities.journey.journeyActionID = JE._experience.journeyOrchestration.stepEvents.actionID
WHERE 
  AE._experience.customerJourneyManagement.entities.channelDetails.channel._id = 'https://ns.adobe.com/xdm/channels/email' 
  AND MF._experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'sent' 
  AND AE._experience.customerJourneyManagement.entities.journey.journeyVersionID IS NOT NULL
```
