---
solution: Journey Optimizer
product: journey optimizer
title: Lista de campos de evento de etapa
description: Lista de campos de evento de etapa
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: e96efa67-ee47-40b9-b680-f5119d8c3481
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 9%

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

Este grupo de campos é específico do journeyStepEvent: este evento está relacionado ao jornada e não tem o identityMap, que descreve a identidade do perfil, se houver.

Para journeyStepEvent, também é necessário adicionar campos relacionados à identidade:

| Nome do campo | Tipo | Descrição |
|---|---|------------|
| ID | String | O identificador de perfil identifica o perfil enviado/usado em uma jornada. Por exemplo: foo@adobe.com. |
| namespace | String | Este campo descreve o namespace referenciado pelo perfil usado na Jornada. Por exemplo: Email, ECID |

## serviceEvents {#servicevents-field}

Este mixin contém todos os campos correspondentes a um trabalho de exportação de perfil. Esses eventos são gerados por atividade **Read Audience** para rastrear o ciclo de vida das operações de exportação de público (em fila, iniciado, concluído, erros). Diferentemente dos eventos de etapa regulares, serviceEvents não estão vinculados a perfis individuais, mas ao próprio nó Ler público, o que significa que eles podem não ter um identificador de perfil associado.

| Nome do campo | Tipo | Descrição |
|---|---|------------|
| ID | String | O identificador do trabalho de exportação de público acionado |
| status | String | O status do trabalho de exportação de público: em fila, iniciado, concluído |
| exportCountTotal | Número inteiro | O valor máximo possível do trabalho de exportação de público |
| exportCountRealized | Número inteiro | O número real de públicos-alvo exportados através do trabalho |
| exportCountFailed | Número inteiro | O número de públicos-alvo que falharam ao exportar pelo trabalho |
| exportSegmentID | String | O identificador do público que está sendo exportado |
| eventType | String | O tipo de evento que indica se é um evento de erro ou um evento de informações: Informações, Erro |
| eventCode | String | O código de erro que indica o motivo para eventType correspondente |

Saiba mais sobre eventTypes [nesta seção](#discarded-events).

## stepEvents {#stepevents-field}

Esta categoria contém os campos de evento de etapa originais. Consulte esta [seção](../reports/sharing-legacy-fields.md).


## Solução de problemas de tipos de evento descartados em eventos de etapa do Jornada  {#discarded-events}

Ao consultar eventos de etapa de jornada para registros com `eventCode = 'discard'`, você pode encontrar vários eventTypes.

Abaixo estão definições, causas comuns e etapas de solução de problemas para o descarte mais frequente `eventTypes`:

* **EXTERNAL_KEY_COMPUTATION_ERROR**: o sistema não pôde computar um identificador exclusivo (chave externa) para o cliente a partir dos dados do evento.

  **Causas comuns**: identificadores de clientes ausentes ou malformados (por exemplo, email, ID de cliente) na carga do evento.

  **Solução de problemas**: verifique a configuração do evento para identificadores necessários, certifique-se de que os dados do evento estejam completos e formatados corretamente.

* **NO_INTERESTED_JORNADA_FOR_SEGMENTMEMBERSHIP_EVENT**: um evento de qualificação de segmento foi recebido, mas nenhuma jornada está configurada para responder a este segmento.

  **Causas comuns**: nenhuma jornada usa o segmento como um acionador, as jornadas estão em estado de rascunho/interrompido ou as IDs de segmento não correspondem.

  **Solução de problemas**: verifique se pelo menos uma jornada está ativa e configurada para o segmento. Verifique as IDs do segmento.

* **JORNADA_INSTANCE_ID_NOT_CREATE**: o sistema falhou ao criar uma instância do jornada para o cliente.

  **Causas comuns**: eventos duplicados, volume de eventos alto, restrições de recursos do sistema.

  **Solução de problemas**: implemente a desduplicação, evite picos de tráfego, otimize o design da jornada e contate o suporte se for persistente.

* **EVENT_WITH_NO_JORNADA**: um evento foi recebido, mas nenhuma jornada ativa está configurada para responder a ele

  **Causas comuns**: nome/ID de evento incompatível, jornada não publicada, sandbox/organização incorreta, modo de teste/perfil incompatível.

  **Solução de problemas**: verifique a configuração do evento e do jornada, verifique o status do jornada, use as ferramentas de depuração.

* Para descartes que ocorrem em jornadas pausadas:

   * **PAUSED_JORNADA_VERSION**: descartes que ocorreram no ponto de entrada da jornada
   * **JORNADA_IN_PAUSED_STATE**: Descarta o que ocorreu quando os perfis estão em uma jornada

  Saiba mais sobre esses eventos e como solucioná-los na [seção Pausar uma Jornada](../building-journeys/journey-pause.md#troubleshoot-profile-discards-in-paused-journeys).

## Recursos adicionais

* [Amostras de consulta do conjunto de dados - Evento de Etapa de Jornada](../data/datasets-query-examples.md#journey-step-event).
* [Exemplos de consultas - Consultas baseadas em eventos](query-examples.md#event-based-queries).
* [Dicionário de esquemas interno](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=pt-BR)

