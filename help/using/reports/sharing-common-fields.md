---
solution: Journey Optimizer
product: journey optimizer
title: campos comuns de eventos journey steps
description: campos comuns de eventos journey steps
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 42aec986-2352-456a-a725-7f1585ae01f8
TQID: https://experienceleague.adobe.com/MWcV6FkgtiFJd9Y7q8CvTXQsL68cD5JcvqjmoEyiYhI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a9f73820-6899-47c2-a597-3fec28ab756a
  - id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2:
  - id: d145add9-d5b9-481b-aa8a-e15e6bb7f813
  - id: a7289281-9ae4-47b1-b8cf-4028b98af776
  - id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 634
ht-degree: 0%

---

# campos comuns de eventos journey steps {#sharing-common-fields}

Este grupo de campos será compartilhado pelos seguintes eventos: **journeyStepEvent** e **journeyStepProfileEvent**.

Esses são os campos XDM comuns que [!DNL Journey Optimizer] envia para a Adobe Experience Platform. Campos comuns serão enviados para cada etapa processada em uma jornada. Campos mais específicos são usados para ações e enriquecimentos personalizados.

Alguns desses campos só estão disponíveis em padrões de processamento específicos (execução de ação, busca de dados etc.) para limitar o tamanho dos eventos.


>[!NOTE]
>
>Saiba mais sobre os atributos de propriedades de jornada [nesta seção](../building-journeys/expression/journey-properties.md#journey-properties-fields).


## entrada {#entrance-field}

Indica se o usuário inseriu a jornada. Se não estiver presente, assumimos que o valor é false.

Tipo: booleano

Valores: true/false

## reentrada {#reentrance-field}

Indica se o usuário inseriu novamente a jornada com a mesma instância. Se não estiver presente, assumimos que o valor é false.

Tipo: booleano

Valores: true/false

## instanceEnded {#instance-ended-field}

Indica se a instância terminou (com sucesso ou não).

Tipo: booleano

## eventID {#eventid-field}

ID do evento em processamento, para o processamento da etapa. Se o evento for externo, o valor será seu eventId. Se o evento for interno, o valor será o eventId interno (como scheduledNotificationReceived, performedAction, etc.).

Tipo: sequência de caracteres

## nodeID {#nodeid-field}

ID do nó do cliente (da tela).

Tipo: sequência de caracteres

## stepID {#stepdid-field}

Identificador exclusivo da etapa que está sendo processada.

Tipo: sequência de caracteres

## stepName {#stepname-field}

Nome da etapa que está sendo processada.

Tipo: sequência de caracteres

## stepType {#steptype-field}

Tipo da etapa.

Tipo: sequência de caracteres

Valores possíveis:

* Condição
* Ação
* Scheduler
* Temporizador

## stepStatus {#stepstatus-field}

Status da etapa, representando o status da etapa, quando seu processamento foi concluído (e o evento da etapa acionado).

Tipo: sequência de caracteres

O status pode ser:

* encerrado: a etapa não tem transição e seu processamento foi encerrado com êxito.
* erro: o processamento da etapa gerou um erro.
* transições: a etapa está aguardando um evento passar para outra etapa.
* capped: a etapa falhou em um erro de limite, gerado durante uma ação ou enriquecimento.
* tempo limite: a etapa falhou em um erro de tempo limite, gerado durante uma ação ou enriquecimento.
* instanceTimedout: a etapa interrompeu o processamento porque a instância atingiu o tempo limite.

## journeyID {#journeyid-field}

ID da jornada.

Tipo: sequência de caracteres

## journeyVersionID {#journeyversionid-field}

ID da versão do jornada. No caso de journeyStepEvent, essa id representa a referência de identidade para a jornada.

Tipo: sequência de caracteres

>[!NOTE]
>
>Para fins de solução de problemas, recomendamos usar journeyVersionID em vez de journeyVersionName ao consultar jornadas.

## journeyVersionName {#journeyversionname-field}

Nome da versão do jornada.

Tipo: sequência de caracteres

>[!NOTE]
>
>Para fins de solução de problemas, recomendamos usar journeyVersionID em vez de journeyVersionName ao consultar jornadas.

## journeyVersion {#journeyversion-field}

Versão da versão do jornada.

Tipo: sequência de caracteres

## instanceID {#instanceid-field}

ID interna da instância do jornada.

Tipo: sequência de caracteres

## externalKey {#externalkey-field}

Chave externa extraída do evento para processá-lo.

Tipo: sequência de caracteres

## parentStepID {#parenstepid-field}

ID da etapa principal da etapa processada atual na instância.

Tipo: sequência de caracteres

## parentStepName {#parentstepname-field}

Nome da etapa principal da etapa atual.

Tipo: sequência de caracteres

## parentTransitionID {#parenttransitionid-field}

Id da transição que trouxe a instância para a etapa processada.

Tipo: sequência de caracteres

## parentTransitionName {#parenttransitionname-field}

Nome da transição que levou a instância à etapa processada.

Tipo: sequência de caracteres

## inTest {#intest-field}

Indicado se essa jornada está no modo de teste ou não.

Tipo: booleano

## processingTime {#processingtime-field}

Tempo total em milissegundos desde a entrada da etapa da instância até o final do processamento.

Tipo: longo

## instanceType {#instancetype-field}

Indica o tipo de instância, se for batch ou unitário.

Tipo: sequência de caracteres

Valores: batch/unitário

## recurrenceIndex {#recurrenceindex-field}

Índice da recorrência se a jornada for em lote e recorrente (a primeira execução tem recurrenceIndex = 1).

Tipo: longo

## isBatchToUnitary {#isbatchtounitary-field}

Indica se esta instância unitária foi disparada de uma instância em lote.

Tipo: booleano

## batchExternalKey {#batchexternalkey-field}

Chave externa para evento batch.

Tipo: sequência de caracteres

## batchInstanceID {#batchinstanceid-field}

essa é a ID da instância do lote.

Tipo: sequência de caracteres

## batchUnitaryBranchID {#batchunitarybranchid-field}

se a instância tiver sido acionada a partir de uma instância de lote, ID de ramificação unitária.

Tipo: sequência de caracteres

## exitCriteriaID

ID do exitCriteria

Tipo: sequência de caracteres

## exitCriteriaName

Nome do exitCriteria

Tipo: sequência de caracteres