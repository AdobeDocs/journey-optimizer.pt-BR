---
solution: Journey Optimizer
product: journey optimizer
title: Esquema de exportação de mensagens do AJO
description: Saiba mais sobre os campos disponíveis no Conjunto de dados de exportação de mensagens do AJO
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: exportar, mensagens, conjunto de dados, esquema, emails, SMS
feature_v2: []
subfeature_v2:
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
source-git-commit: 0d9c480cc48c4352e82d1f4624c65fc16a60b959
workflow-type: tm+mt
source-wordcount: 447
ht-degree: 3%

---

# Esquema de exportação de mensagens do AJO {#ajo-message-export-schema}

>[!BEGINSHADEBOX]

**Nesta página:** Explore a estrutura e os campos individuais do Conjunto de Dados de Exportação de Mensagens do AJO que armazena conteúdo de mensagens de email e SMS enviadas no Adobe Experience Platform.

>[!ENDSHADEBOX]

Quando a **Exportação de Mensagens** está habilitada em uma configuração de canal de Email ou SMS, o conteúdo da mensagem enviada é gravado no **Conjunto de Dados de Exportação de Mensagens do AJO** em [!DNL Adobe Experience Platform].

Esta seção lista os campos disponíveis no conjunto de dados exportado.

## Campos do conjunto de dados

+++ _experience

**Campo:** `_experience`\
**Tipo:** objeto

+++

+++ _experience > customerJourneyManagement

**Campo:** `customerJourneyManagement`\
**Tipo:** objeto

+++

+++ _experience > customerJourneyManagement > messageDeliveryMetadata

**Campo:** `messageDeliveryMetadata`\
**Tipo:** objeto

+++

+++ _experience > customerJourneyManagement > messageDeliveryMetadata > emailMetadata

**Campo:** `emailMetadata`\
**Tipo:** objeto

* recipient

  **Campo:** `recipient`\
  **Tipo:** objeto

   * cco

     **Campo:** `bcc`\
     **Tipo:** matriz de cadeias de caracteres

   * cc

     **Campo:** `cc`\
     **Tipo:** matriz de cadeias de caracteres

   * email

     **Campo:** `email`\
     **Tipo:** cadeia de caracteres

   * name

     **Campo:** `name`\
     **Tipo:** cadeia de caracteres

* remetente

  **Campo:** `sender`\
  **Tipo:** objeto

   * email

     **Campo:** `email`\
     **Tipo:** cadeia de caracteres

   * errorEmail

     **Campo:** `errorEmail`\
     **Tipo:** cadeia de caracteres

   * name

     **Campo:** `name`\
     **Tipo:** cadeia de caracteres

   * replyToEmail

     **Campo:** `replyToEmail`\
     **Tipo:** cadeia de caracteres

   * replyToName

     **Campo:** `replyToName`\
     **Tipo:** cadeia de caracteres

+++

+++ _experience > customerJourneyManagement > messageDeliveryMetadata > smsMetadata

**Campo:** `smsMetadata`\
**Tipo:** objeto

* recipient

  **Campo:** `recipient`\
  **Tipo:** objeto

   * número

     **Campo:** `number`\
     **Tipo:** cadeia de caracteres

* remetente

  **Campo:** `sender`\
  **Tipo:** objeto

   * números

     **Campo:** `numbers`\
     **Tipo:** matriz de cadeias de caracteres

+++

+++ _experience > customerJourneyManagement > messageExecution

**Campo:** `messageExecution`\
**Tipo:** objeto

* público-alvo

  **Campo:** `audience`\
  **Tipo:** objeto

   * id

     **Campo:** `id`\
     **Tipo:** cadeia de caracteres

   * tipo

     **Campo:** `type`\
     **Tipo:** cadeia de caracteres

* fragmentPublicationIDs

  **Campo:** `fragmentPublicationIDs`\
  **Tipo:** matriz de cadeias de caracteres

* metadados

  **Campo:** `metadata`\
  **Tipo: mapa**

   * [Mapear Chave]

     **Tipo:** cadeia de caracteres

* parentSourceMeta

  **Campo:** `parentSourceMeta`\
  **Tipo:** objeto

   * sourceActionID

     **Campo:** `sourceActionID`\
     **Tipo:** cadeia de caracteres

   * sourceID

     **Campo:** `sourceID`\
     **Tipo:** cadeia de caracteres

   * sourceType

     **Campo:** `sourceType`\
     **Tipo:** cadeia de caracteres

   * sourceVersionID

     **Campo:** `sourceVersionID`\
     **Tipo:** cadeia de caracteres

* batchInstanceID

  **Campo:** `batchInstanceID`\
  **Tipo:** cadeia de caracteres

* campaignActionID

  **Campo:** `campaignActionID`\
  **Tipo:** cadeia de caracteres

* campaignID

  **Campo:** `campaignID`\
  **Tipo:** cadeia de caracteres

* campaignVersionID

  **Campo:** `campaignVersionID`\
  **Tipo:** cadeia de caracteres

* journeyActionID

  **Campo:** `journeyActionID`\
  **Tipo:** cadeia de caracteres

* journeyVersionID

  **Campo:** `journeyVersionID`\
  **Tipo:** cadeia de caracteres

* journeyVersionInstanceID

  **Campo:** `journeyVersionInstanceID`\
  **Tipo:** cadeia de caracteres

* journeyVersionNodeID

  **Campo:** `journeyVersionNodeID`\
  **Tipo:** cadeia de caracteres

* messageExecutionID

  **Campo:** `messageExecutionID`\
  **Tipo:** cadeia de caracteres

* messageID

  **Campo:** `messageID`\
  **Tipo:** cadeia de caracteres

* messagePublicationID

  **Campo:** `messagePublicationID`\
  **Tipo:** cadeia de caracteres

* messageType

  **Campo:** `messageType`\
  **Tipo:** cadeia de caracteres

* waveID

  **Campo:** `waveID`\
  **Tipo:** cadeia de caracteres

+++

+++ _experience > customerJourneyManagement > messageProfile

**Campo:** `messageProfile`\
**Tipo:** objeto

* canal

  **Campo:** `channel`\
  **Tipo:** objeto

   * contentTypes

     **Campo:** `contentTypes`\
     **Tipo:** matriz de cadeias de caracteres

   * locationTypes

     **Campo:** `locationTypes`\
     **Tipo:** matriz de cadeias de caracteres

   * metricTypes

     **Campo:** `metricTypes`\
     **Tipo:** matriz de cadeias de caracteres

   * _id

     **Campo:** `_id`\
     **Tipo:** cadeia de caracteres

   * _type

     **Campo:** `_type`\
     **Tipo:** cadeia de caracteres

   * mediaAction

     **Campo:** `mediaAction`\
     **Tipo:** cadeia de caracteres

   * mediaType

     **Campo:** `mediaType`\
     **Tipo:** cadeia de caracteres

   * modo

     **Campo:** `mode`\
     **Tipo:** cadeia de caracteres

   * referenceSource

     **Campo:** `referringSource`\
     **Tipo:** cadeia de caracteres

   * typeAtSource

     **Campo:** `typeAtSource`\
     **Tipo:** cadeia de caracteres

* isSendTimeOtimized

  **Campo:** `isSendTimeOptimized`\
  **Tipo:** booleano

* isTestExecution

  **Campo:** `isTestExecution`\
  **Tipo:** booleano

* messageProfileID

  **Campo:** `messageProfileID`\
  **Tipo:** cadeia de caracteres

* messageProfileTrackingID

  **Campo:** `messageProfileTrackingID`\
  **Tipo:** cadeia de caracteres

* requestID

  **Campo:** `requestID`\
  **Tipo:** cadeia de caracteres

* secondaryDimensionID

  **Campo:** `secondaryDimensionID`\
  **Tipo:** cadeia de caracteres

* secondaryDimensionName

  **Campo:** `secondaryDimensionName`\
  **Tipo:** cadeia de caracteres

* variante

  **Campo:** `variant`\
  **Tipo:** cadeia de caracteres

+++

+++ _experience > customerJourneyManagement > messageRenderedContent

**Campo:** `messageRenderedContent`\
**Tipo:** objeto

* emailContent

  **Campo:** `emailContent`\
  **Tipo:** objeto

   * html

     **Campo:** `html`\
     **Tipo:** cadeia de caracteres

   * assunto

     **Campo:** `subject`\
     **Tipo:** cadeia de caracteres

   * texto

     **Campo:** `text`\
     **Tipo:** cadeia de caracteres

* smsContent

  **Campo:** `smsContent`\
  **Tipo:** objeto

   * mídia

     **Campo:** `media`\
     **Tipo:** cadeia de caracteres

   * message

     **Campo:** `message`\
     **Tipo:** cadeia de caracteres

   * título

     **Campo:** `title`\
     **Tipo:** cadeia de caracteres

+++

+++ identityMap

**Campo:** `identityMap`\
**Tipo: mapa**

* [Mapear Chave]

  **Tipo:** matriz de objetos

   * authenticatedState

     **Campo:** `authenticatedState`\
     **Tipo:** cadeia de caracteres

   * id

     **Campo:** `id`\
     **Tipo:** cadeia de caracteres

   * principal

     **Campo:** `primary`\
     **Tipo:** booleano

+++

+++ eventType

**Campo:** `eventType`\
**Tipo:** cadeia de caracteres

+++

+++ productionBy

**Campo:** `producedBy`\
**Tipo:** cadeia de caracteres

+++

+++ carimbo de data e hora

**Campo:** `timestamp`\
**Tipo:** dateTime

+++

