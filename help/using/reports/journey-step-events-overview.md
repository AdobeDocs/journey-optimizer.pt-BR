---
solution: Journey Optimizer
product: journey optimizer
title: Trabalhar com eventos de etapa da jornada
description: Saiba como trabalhar com eventos de etapa do jornada no Adobe Journey Optimizer - entenda o que são, por que são importantes e como usá-los para análise e otimização
feature: Journeys, Reporting
role: Developer, Admin, User
level: Intermediate, Experienced
keywords: jornada, eventos de etapa, análises, relatórios, monitoramento, XDM
exl-id: 2e7c5ea5-d8c5-416d-ab88-d2bc02043558
source-git-commit: 97fa287d94efb7fb95817fc15268e736517cb629
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 2%

---

# Trabalhar com eventos de etapa da jornada {#work-with-journey-step-events}

Os eventos de etapa de Jornada são eventos gerados automaticamente que capturam informações detalhadas sobre cada etapa que um [perfil](../audience/get-started-profiles.md) realiza à medida que avança em uma [jornada](../building-journeys/journey.md) no Adobe Journey Optimizer. Estes eventos fornecem visibilidade abrangente do [desempenho do jornada](../building-journeys/report-journey.md) e habilitam recursos de análise avançados.

## O que são eventos de etapa de jornada {#what-are-step-events}

Os eventos de etapa de Jornada são eventos [XDM (Experience Data Model)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target="_blank"} gerados pelo sistema que a Adobe Journey Optimizer cria e envia automaticamente para a [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=pt-BR){target="_blank"} sempre que um perfil se move de um nó para outro em uma jornada. Cada evento corresponde a uma [atividade de jornada](../building-journeys/about-journey-activities.md) específica ou transição na experiência de jornada do cliente.

Há dois tipos principais de eventos de etapa de jornada:

- **journeyStepEvent**: eventos relacionados à progressão de perfil individual por meio de etapas de jornada
- **journeyStepProfileEvent**: eventos que incluem informações adicionais de contexto do perfil

### O que aciona os eventos de etapa de jornada? {#event-triggers}

Os eventos de etapa de Jornada são gerados automaticamente para várias atividades de jornada:

- **Eventos de entrada**: quando um perfil [entra em uma jornada](../building-journeys/entry-management.md)
- **Execução da ação**: quando [mensagens são enviadas](../building-journeys/journey-action.md) ou [ações personalizadas](../building-journeys/using-custom-actions.md) são executadas
- **Avaliação de condição**: quando os perfis passam por [condições](../building-journeys/condition-activity.md) e pontos de decisão
- **Atividades de espera**: quando perfis entram e saem [nós de espera](../building-journeys/wait-activity.md)
- **Eventos de saída**: quando os perfis são concluídos ou [sair de uma jornada](../building-journeys/end-journey.md)
- **Tratamento de erros**: quando ocorrerem erros durante a execução da jornada

>[!NOTE]
>
>Os eventos de etapa de Jornada são ativados por padrão em todas as instâncias. Não é possível modificar ou atualizar os [esquemas e conjuntos de dados](sharing-overview.md) que foram criados durante o provisionamento para eventos de etapa. Esses esquemas e conjuntos de dados estão no modo somente leitura.

Saiba mais sobre [esquemas de evento de etapa do jornada](sharing-field-list.md).

## Por que os eventos de etapa do jornada são importantes {#why-step-events-matter}

Os eventos de etapa de Jornada fornecem valor essencial para organizações que usam o Adobe Journey Optimizer:

### Análise e monitoramento em tempo real {#real-time-analytics}

- **Acompanhamento de desempenho da Jornada**: monitore como os perfis fluem em suas jornadas em tempo real usando [relatórios ao vivo](live-report.md)
- **Análise de conversão**: entender os pontos de devolução e os caminhos de conversão bem-sucedidos com a [análise do jornada](journey-global-report-cja.md)
- **Detecção de erros**: identifique e solucione problemas à medida que eles ocorrem por meio de [monitoramento e alertas](alerts.md)

### Integração de dados e insights {#data-integration}

- **Análise entre plataformas**: combinar dados do jornada com outras [fontes de dados do Adobe Experience Platform](../datasource/adobe-experience-platform-data-source.md)
- **Visualização do cliente 360**: criar [perfis de clientes](../audience/get-started-profiles.md) abrangentes que incluam interações do jornada
- **Modelagem de atribuição**: conecte os pontos de contato do jornada aos resultados comerciais downstream usando o [Customer Journey Analytics](cja-ajo.md)

### Oportunidades de otimização {#optimization}

- **Insights de teste A/B**: analisar o desempenho de diferentes caminhos de jornada usando [experimentação](campaign-global-report-cja-experimentation.md)
- **Aprimoramento do Personalization**: use os dados de comportamento de jornada para melhorar experiências futuras com [conteúdo dinâmico](../personalization/dynamic-content.md)
- **Eficiência operacional**: identificar gargalos e otimizar o [design da jornada](../building-journeys/using-the-journey-designer.md)

## Como usar os eventos de etapa do jornada {#how-to-use-step-events}

### Acesso aos dados do evento de etapa do jornada {#accessing-data}

Os dados do evento de etapa do Jornada são armazenados automaticamente no Adobe Experience Platform e podem ser acessados por meio de:

1. **Consultas do Data Lake**: Use SQL para consultar o conjunto de dados `journey_step_events` com o [Serviço de Consulta](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=pt-BR){target="_blank"}
2. **Customer Journey Analytics**: analisar dados de jornada por meio de [ferramentas de análise avançadas](cja-ajo.md)
3. **Relatórios em tempo real**: acesse dados por meio dos [recursos de relatórios internos](gs-reports.md) da Journey Optimizer
4. **APIs**: acesse programaticamente os dados do evento para aplicativos personalizados

Saiba mais sobre [o acesso aos conjuntos de dados](../data/datasets-query-examples.md).

### Principais pontos de dados disponíveis {#key-data-points}

Os eventos de etapa de Jornada capturam informações abrangentes, incluindo:

- **Identificação da Jornada**: [ID da Jornada, versão e nome](sharing-journey-fields.md)
- **Informações do perfil**: [ID do perfil e identidades associadas](sharing-identity-fields.md)
- **Detalhes da etapa**: [Nome do nó, tipo de etapa e status de execução](sharing-common-fields.md)
- **Carimbos de data e hora**: tempo preciso de cada etapa de jornada
- **Resultados da ação**: [Status de êxito/falha e detalhes da execução](sharing-execution-fields.md)
- **Informações de erro**: [descrições e códigos de erro](sharing-field-list.md#discarded-events) detalhados quando ocorrem problemas

Explorar todas as [definições de campo disponíveis](sharing-field-list.md).

### Casos de uso comuns {#common-use-cases}

**Monitoramento de desempenho**

```sql
-- Example: Count profiles entering a journey in the last 24 hours
SELECT count(distinct _experience.journeyOrchestration.stepEvents.profileID)
FROM journey_step_events 
WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-id>'
AND _experience.journeyOrchestration.stepEvents.nodeType='start'
AND DATE(timestamp) > (now() - interval '24' hour);
```

**Análise de erro**

```sql
-- Example: Identify errors by journey node
SELECT _experience.journeyOrchestration.stepEvents.nodeName,
       count(distinct _experience.journeyOrchestration.stepEvents.profileID)
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.actionExecutionError IS NOT NULL
GROUP BY _experience.journeyOrchestration.stepEvents.nodeName;
```

**Jornada análise do funnel**

- Rastrear as taxas de conversão em cada etapa da jornada
- Identificar onde os perfis saem com mais frequência da jornada
- Medir o tempo gasto em diferentes fases da jornada

Saiba mais sobre [técnicas de consulta para análise do funnel](query-examples.md#common-queries).

## Amostras e recursos {#samples-resources}

### Exemplos e modelos de consulta {#query-examples}

Explore exemplos abrangentes de consulta para análise comum de eventos de etapa de jornada:

- **[Exemplos de consulta de evento de etapa do Jornada](query-examples.md)**: consultas SQL prontas para uso para cenários de análise comuns
- **[Amostras de consulta do conjunto de dados](../data/datasets-query-examples.md#journey-step-event)**: exemplos de consulta de conjuntos de dados de eventos de etapa de jornada
- **[Consultas baseadas em perfil](query-examples.md#profile-based-queries)**: controle jornadas e interações de perfil individuais

### Documentação de campo {#field-documentation}

Entenda a estrutura de dados completa dos eventos de etapa do jornada:

- **[Lista de campos de eventos de etapa de Jornada](sharing-field-list.md)**: referência abrangente de todos os campos disponíveis
- **[Campos comuns](sharing-common-fields.md)**: campos compartilhados em journeyStepEvent e journeyStepProfileEvent
- **[Campos de execução da ação](sharing-execution-fields.md)**: campos específicos do rastreamento da execução da ação
- **[Campos de Jornada](sharing-journey-fields.md)**: identificadores e metadados específicos de Jornada

### Práticas recomendadas e solução de problemas {#best-practices}

**Otimização do desempenho**

- Use `journeyVersionID` em vez de `journeyVersionName` para melhorar o desempenho da consulta ([saiba mais sobre as propriedades da jornada](../building-journeys/expression/journey-properties.md))
- Filtrar por intervalos de datas para melhorar a velocidade da consulta em conjuntos de dados grandes
- Aproveite as identidades de perfil que correspondem à sua [configuração de namespace de jornada](../building-journeys/entry-management.md)

**Qualidade dos dados**

- Monitorar regularmente [eventos descartados](sharing-field-list.md#discarded-events) para identificar problemas de dados
- Validar se os esquemas de evento correspondem aos requisitos de análise
- Implementar a manipulação adequada de erros em consultas personalizadas

**Estratégias de análise**

- Combine eventos de etapa de jornada com [dados de feedback da mensagem](../data/datasets-query-examples.md#message-feedback-event-dataset) para atribuição completa
- Use a análise baseada em tempo para entender a velocidade da jornada e os gargalos

### Recursos avançados de análise {#advanced-analytics}

**integração com o Customer Journey Analytics**
Os eventos de etapa de Jornada podem ser analisados usando o [Customer Journey Analytics](cja-ajo.md) para:

- Modelagem de atribuição avançada
- Visualização de jornada entre canais
- Análise preditiva dos resultados da jornada

Saiba como [configurar o Customer Journey Analytics](report-gs-cja.md) para dados do Journey Optimizer.

## Recursos adicionais {#additional-resources}

### Links de documentação {#documentation-links}

- **[Visão geral do compartilhamento de etapas do Jornada](sharing-overview.md)**: entender como os dados do jornada fluem para o Adobe Experience Platform
- **[Dicionário de esquemas internos](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=pt-BR){target="_blank"}**: referência de esquema XDM completa
- **[Relatórios do Journey Optimizer](report-gs-cja.md)**: visão geral dos recursos de relatórios no Journey Optimizer

### Guias de integração {#integration-guides}

- **[Adobe Customer Journey Analytics](cja-ajo.md)**: Analisando dados do Journey Optimizer no CJA
- **[Gerenciamento de dados](../data/export-datasets.md)**: exportação e gerenciamento de dados do jornada
- **[Privacidade e governança](../privacy/audit-logs.md)**: considerações de governança de dados para eventos do jornada


**Próximas etapas:**

- Comece com [criando seus primeiros relatórios de jornada](sharing-overview.md)
- Explore [exemplos de consulta](query-examples.md) para casos de uso específicos
- Saiba mais sobre as [práticas recomendadas de gerenciamento de jornadas](../building-journeys/journey.md)
