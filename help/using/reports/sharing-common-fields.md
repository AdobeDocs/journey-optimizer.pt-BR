---
title: campos comuns de eventos journeystep
description: campos comuns de eventos journeystep
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 42aec986-2352-456a-a725-7f1585ae01f8
source-git-commit: 6d744c0289e81ab2229f02c44ead43943b945b89
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 9%

---

# campos comuns de eventos journeystep {#sharing-common-fields}

Esse grupo de campos será compartilhado por journeyStepEvent e journeyStepProfileEvent.

Esses são os campos XDM comuns que [!DNL Journey Optimizer] envia para o Adobe Experience Platform. Campos comuns serão enviados para cada etapa que é processada em uma jornada. Campos mais específicos são usados para ações e enriquecimentos personalizados.

Alguns desses campos estão disponíveis apenas em padrões de processamento específicos (execução de ação, busca de dados etc.) para limitar o tamanho dos eventos.

## entrada {#entrance-field}

Indica se o usuário inseriu a jornada. Se não estiver presente, assumimos que o valor é false.

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

Tipo: sequência de caracteres

## nodeID {#nodeid-field}

ID do nó do cliente (na tela).

Tipo: sequência de caracteres

## stepID {#stepdid-field}

Id exclusiva da etapa que está sendo processada no momento.

Tipo: sequência de caracteres

## stepName {#stepname-field}

Nome da etapa que está sendo processada no momento.

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

Status da etapa, representando o status da etapa, quando o processamento foi concluído (e o evento de etapa foi acionado).

Tipo: sequência de caracteres

O status pode ser:

* encerrado: a etapa não tem transição e seu processamento foi concluído com êxito.
* erro: o processamento da etapa gerou um erro.
* transições: a etapa está aguardando a transição de um evento para outra etapa.
* limitado: a etapa falhou em um erro de limitação, gerado durante uma ação ou enriquecimento.
* tempo limite: a etapa falhou em um erro de tempo limite, gerado durante uma ação ou enriquecimento.
* instanceTimedout: a etapa interrompeu o processamento porque a instância atingiu o tempo limite.

## journeyID {#journeyid-field}

ID da jornada.

Tipo: sequência de caracteres

## journeyVersionID {#journeyversionid-field}

ID da versão do jornada. Essa id representa a referência de identidade para a jornada, no caso de journeyStepEvent.

Tipo: sequência de caracteres

## journeyVersionName {#journeyversionname-field}

Nome da versão do jornada.

Tipo: sequência de caracteres

## journeyVersion {#journeyversion-field}

Versão da versão do jornada.

Tipo: sequência de caracteres

## instanceID {#instanceid-field}

ID interna da instância do jornada.

Tipo: sequência de caracteres

## externalKey {#externalkey-field}

Chave externa extraída do evento para processá-la.

Tipo: sequência de caracteres

## parentStepID {#parenstepid-field}

ID da etapa principal da etapa processada atual na instância.

Tipo: sequência de caracteres

## parentStepName {#parentstepname-field}

Nome da etapa do pai da etapa atual.

Tipo: sequência de caracteres

## parentTransitionID {#parenttransitionid-field}

Id da transição que trouxe a instância para a etapa processada.

Tipo: sequência de caracteres

## parentTransitionName {#parenttransitionname-field}

Nome da transição que trouxe a instância para a etapa processada.

Tipo: sequência de caracteres

## inTest {#intest-field}

Indicado se essa jornada está no modo de teste ou não.

Tipo: booleano

## processingTime {#processingtime-field}

Tempo total em milissegundos desde a entrada da etapa da instância até o fim do processamento.

Tipo: long

## instanceType {#instancetype-field}

Indica o tipo de instância, se for em lote ou unitário.

Tipo: sequência de caracteres

Valores: lote/unidade

## periodicidadeIndex {#recurrenceindex-field}

Índice da recorrência se a jornada for em lote e recorrente (a primeira execução tem recorrênciaIndex = 1).

Tipo: long

## isBatchToUnitary {#isbatchtounitary-field}

Indica se essa instância unitária foi acionada a partir de uma instância de lote.

Tipo: booleano

## batchExternalKey {#batchexternalkey-field}

Chave externa para o evento batch.

Tipo: sequência de caracteres

## batchInstanceID {#batchinstanceid-field}

essa é a ID da instância de lote.

Tipo: sequência de caracteres

## batchUnitaryBranchID {#batchunitarybranchid-field}

se a instância tiver sido acionada a partir de uma instância de lote, a ID de ramificação unitária.

Tipo: sequência de caracteres
