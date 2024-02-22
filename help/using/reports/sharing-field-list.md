---
solution: Journey Optimizer
product: journey optimizer
title: Lista de campos de evento de etapa
description: Lista de campos de evento de etapa
feature: Journeys, Reporting
topic: Content Management
role: Data Engineer, Data Architect, Admin
level: Experienced
exl-id: e96efa67-ee47-40b9-b680-f5119d8c3481
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 17%

---

# Lista de campos de evento de etapa {#sharing-field-list}

Os campos de evento de etapa são organizados por categoria.

* Campos de informações de depuração
* Campos de jornada
* Campos de perfil
* Campos de evento de serviço

Para o atributo identityMap, a identidade primária é definida por padrão como &quot;primary = true&quot;.

## debugInfo {#debuginfo-field}

| Nome do campo | Tipo | Descrição |
|---|---|------------|
| requestId | String | A ID da solicitação usada pelo Journey Optimizer para rastrear o fluxo de uma solicitação. |

## jornada {#journey-field}

Esse grupo de campos é usado no esquema de jornada (em relação a journeyStepEvent). Ele contém os seguintes campos:

| Nome do campo | Tipo | Descrição |
|---|---|------------|
| ID | String | Identificador para a Jornada fornecida |
| VersionID | String | Id da versão do jornada. Essa id representa a identidade de uma jornada |
| name | String | Nome da jornada |
| descrição | String | Descrição da jornada |
| version | String | versão, representada como `major`.`minor` |

## perfil {#profile-field}

Este grupo de campos é específico do journeyStepEvent: esse evento está relacionado ao jornada e não tem o identityMap, que descreve a identidade do perfil, se houver.

Para journeyStepEvent, também é necessário adicionar campos relacionados à identidade:

| Nome do campo | Tipo | Descrição |
|---|---|------------|
| ID | String | O identificador de perfil identifica o perfil enviado/usado em uma jornada. Por exemplo: foo@adobe.com. |
| namespace | String | Este campo descreve o namespace referenciado pelo perfil usado na Jornada. Por exemplo: Email, ECID |

## serviceEvents {#servicevents-field}

Este mixin contém todos os campos correspondentes a um trabalho de exportação de perfil.

| Nome do campo | Tipo | Descrição |
|---|---|------------|
| ID | String | O identificador do trabalho de exportação de público acionado |
| status | String | O status do trabalho de exportação de público: em fila, iniciado, concluído |
| exportCountTotal | Número inteiro | O valor máximo possível do trabalho de exportação de público |
| exportCountRealized | Número inteiro | O número real de públicos-alvo exportados através do trabalho |
| exportCountFailed | Número inteiro | O número de públicos-alvo que falharam ao exportar pelo trabalho |
| exportSegmentID | String | O identificador do público que está sendo exportado |
| eventType | String | O tipo de evento que indica se é um evento de erro do evento info: Info, Error |
| eventCode | String | O código de erro que indica o motivo para eventType correspondente |

## stepEvents {#stepevents-field}

Esta categoria contém os campos de evento de etapa originais. Consulte esta [seção](../reports/sharing-legacy-fields.md).
