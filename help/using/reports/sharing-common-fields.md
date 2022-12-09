---
solution: Journey Optimizer
product: journey optimizer
title: campos comuns de eventos journeystep
description: campos comuns de eventos journeystep
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 42aec986-2352-456a-a725-7f1585ae01f8
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 0%

---

# campos comuns de eventos journeystep {#sharing-common-fields}

Esse grupo de campos será compartilhado por journeyStepEvent e journeyStepProfileEvent.

Esses são os campos XDM comuns que [!DNL Journey Optimizer] envia para a Adobe Experience Platform. Campos comuns serão enviados para cada etapa que é processada em uma jornada. Campos mais específicos são usados para ações e enriquecimentos personalizados.

Alguns desses campos estão disponíveis apenas em padrões de processamento específicos (execução de ação, busca de dados etc.) para limitar o tamanho dos eventos.

## entrada {#entrance-field}

Indica se o usuário entrou na jornada. Se não estiver presente, assumimos que o valor é false.

Tipo: booleano

Valores: true/false

## reentrada {#reentrance-field}

Indica se o usuário entrou novamente na jornada com a mesma instância. Se não estiver presente, assumimos que o valor é false.

Tipo: booleano

Valores: true/false

## instanceEnded {#instance-ended-field}

Indica se a instância terminou (com êxito ou não).

Tipo: booleano

## eventID {#eventid-field}

ID do evento no processamento, para o processamento da etapa. Se o evento for externo, o valor será eventId. Se o evento for interno, o valor será eventId interno (como scheduledNotificationReceived, executionAction, etc.).

Tipo: string

## nodeID {#nodeid-field}

ID do nó do cliente (na tela).

Tipo: string

## stepID {#stepdid-field}

Id exclusiva da etapa que está sendo processada no momento.

Tipo: string

## stepName {#stepname-field}

Nome da etapa que está sendo processada no momento.

Tipo: string

## stepType {#steptype-field}

Tipo da etapa.

Tipo: string

Valores possíveis:

* Condição
* Ação
* Scheduler
* Temporizador

## stepStatus {#stepstatus-field}

Status da etapa, representando o status da etapa, quando o processamento foi concluído (e o evento de etapa foi acionado).

Tipo: string

O status pode ser:

* encerrado: a etapa não tem transição e seu processamento foi concluído com êxito.
* erro: o processamento da etapa gerou um erro.
* transições: a etapa está aguardando a transição de um evento para outra etapa.
* limitado: a etapa falhou em um erro de limitação, gerado durante uma ação ou enriquecimento.
* tempo limite: a etapa falhou em um erro de tempo limite, gerado durante uma ação ou enriquecimento.
* instanceTimedout: a etapa interrompeu o processamento porque a instância atingiu o tempo limite.

## journeyID {#journeyid-field}

ID da jornada.

Tipo: string

## journeyVersionID {#journeyversionid-field}

ID da versão da jornada. Essa id representa a referência de identidade para a jornada, no caso de journeyStepEvent.

Tipo: string

## journeyVersionName {#journeyversionname-field}

Nome da versão da jornada.

Tipo: string

## journeyVersion {#journeyversion-field}

Versão da versão da jornada.

Tipo: string

## instanceID {#instanceid-field}

ID interna da instância da jornada.

Tipo: string

## externalKey {#externalkey-field}

Chave externa extraída do evento para processá-la.

Tipo: string

## parentStepID {#parenstepid-field}

ID da etapa principal da etapa processada atual na instância.

Tipo: string

## parentStepName {#parentstepname-field}

Nome da etapa do pai da etapa atual.

Tipo: string

## parentTransitionID {#parenttransitionid-field}

Id da transição que trouxe a instância para a etapa processada.

Tipo: string

## parentTransitionName {#parenttransitionname-field}

Nome da transição que trouxe a instância para a etapa processada.

Tipo: string

## inTest {#intest-field}

Indicado se a jornada está no modo de teste ou não.

Tipo: booleano

## processingTime {#processingtime-field}

Tempo total em milissegundos desde a entrada da etapa da instância até o fim do processamento.

Tipo: long

## instanceType {#instancetype-field}

Indica o tipo de instância, se for em lote ou unitário.

Tipo: string

Valores: lote/unidade

## periodicidadeIndex {#recurrenceindex-field}

Índice da recorrência se a jornada for em lote e recorrente (a primeira execução tem recorrênciaIndex = 1).

Tipo: long

## isBatchToUnitary {#isbatchtounitary-field}

Indica se essa instância unitária foi acionada a partir de uma instância de lote.

Tipo: booleano

## batchExternalKey {#batchexternalkey-field}

Chave externa para o evento batch.

Tipo: string

## batchInstanceID {#batchinstanceid-field}

essa é a ID da instância de lote.

Tipo: string

## batchUnitaryBranchID {#batchunitarybranchid-field}

se a instância tiver sido acionada a partir de uma instância de lote, a ID de ramificação unitária.

Tipo: string
