---
solution: Journey Optimizer
product: journey optimizer
title: Trabalhar com eventos de etapa do jornada
description: Saiba como trabalhar com eventos de etapa do jornada no Adobe Journey Optimizer - entenda o que são, por que são importantes e como usá-los para análise e otimização
feature: Journeys, Reporting
topic: Content Management
role: Data Engineer, Data Architect, Admin, User
level: Intermediate, Experienced
keywords: jornada, eventos de etapa, análises, relatórios, monitoramento, XDM
hide: true
hidefromtoc: true
exl-id: 9f8e7d6c-5b4a-3928-1756-849302a11c2b
source-git-commit: df3abb7da17eb21e5e4120b55bdeb61fec3e202d
workflow-type: tm+mt
source-wordcount: '875'
ht-degree: 1%

---

# Trabalhar com eventos de etapa do jornada {#work-with-journey-step-events}

Os eventos de etapa de Jornada são eventos gerados automaticamente que capturam informações detalhadas sobre cada etapa que um perfil realiza à medida que avançam por uma jornada no Adobe Journey Optimizer. Esses eventos fornecem visibilidade abrangente do desempenho do jornada e habilitam recursos avançados de análise.

## O que são eventos de etapa de jornada? {#what-are-step-events}

Os eventos de etapa de Jornada são eventos XDM (Experience Data Model) gerados pelo sistema que o Adobe Journey Optimizer cria e envia automaticamente para a Adobe Experience Platform sempre que um perfil se move de um nó para outro em uma jornada. Cada evento corresponde a uma ação ou transição específica na experiência de jornada do cliente.

Há dois tipos principais de eventos de etapa de jornada:

- **journeyStepEvent**: eventos relacionados à progressão de perfil individual por meio de etapas de jornada
- **journeyStepProfileEvent**: eventos que incluem informações adicionais de contexto do perfil

### O que aciona os eventos de etapa de jornada? {#event-triggers}

Os eventos de etapa de Jornada são gerados automaticamente para várias atividades de jornada:

- **Eventos de entrada**: quando um perfil entra em uma jornada
- **Execução da ação**: quando mensagens são enviadas ou ações personalizadas são executadas
- **Avaliação de condição**: quando os perfis passam pelos pontos de decisão
- **Atividades de espera**: quando perfis entram e saem dos nós de espera
- **Eventos de saída**: quando perfis concluem ou saem de uma jornada
- **Tratamento de erros**: quando ocorrerem erros durante a execução da jornada

>[!NOTE]
>
>Os eventos de etapa de Jornada são ativados por padrão em todas as instâncias. Não é possível modificar ou atualizar os esquemas e conjuntos de dados que foram criados durante o provisionamento para eventos da etapa. Esses esquemas e conjuntos de dados estão no modo somente leitura.

## Por que os eventos de etapa do jornada são importantes {#why-step-events-matter}

Os eventos de etapa de Jornada fornecem valor essencial para organizações que usam o Adobe Journey Optimizer:

### Análise e monitoramento em tempo real {#real-time-analytics}

- **Acompanhamento de desempenho da Jornada**: monitore em tempo real como os perfis fluem pelas suas jornadas
- **Análise de conversão**: entender pontos de distribuição e caminhos de conversão bem-sucedidos
- **Detecção de erros**: identifique e solucione problemas à medida que ocorrerem

### Integração de dados e insights {#data-integration}

- **Análise entre plataformas**: combinar dados do jornada com outras fontes de dados do Adobe Experience Platform
- **Visualização do Customer 360**: crie perfis abrangentes do cliente que incluam interações do jornada
- **Modelagem de atribuição**: conecte os pontos de contato do jornada aos resultados de negócios downstream

### Oportunidades de otimização {#optimization}

- **Insights de teste A/B**: analisar o desempenho de diferentes caminhos de jornada
- **Aprimoramento do Personalization**: use os dados de comportamento da jornada para melhorar experiências futuras
- **Eficiência operacional**: identificar gargalos e otimizar o design da jornada

## Como usar os eventos de etapa do jornada {#how-to-use-step-events}

### Acesso aos dados do evento de etapa do jornada {#accessing-data}

Os dados do evento de etapa do Jornada são armazenados automaticamente no Adobe Experience Platform e podem ser acessados por meio de:

1. **Consultas do Data Lake**: use SQL para consultar o conjunto de dados `journey_step_events`
2. **Customer Journey Analytics**: analisar dados de jornada por meio de ferramentas de análise avançadas
3. **Relatório em tempo real**: acesse dados por meio dos recursos de relatório integrados da Journey Optimizer
4. **APIs**: acesse programaticamente os dados do evento para aplicativos personalizados

### Principais pontos de dados disponíveis {#key-data-points}

Os eventos de etapa de Jornada capturam informações abrangentes, incluindo:

- **Identificação da Jornada**: ID, versão e nome da Jornada
- **Informações do perfil**: ID do perfil e identidades associadas
- **Detalhes da etapa**: nome do nó, tipo de etapa e status de execução
- **Carimbos de data e hora**: tempo preciso de cada etapa de jornada
- **Resultados da ação**: status de sucesso/falha e detalhes da execução
- **Informações de erro**: códigos de erro detalhados e descrições quando ocorrem problemas

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

- Use `journeyVersionID` em vez de `journeyVersionName` para melhorar o desempenho da consulta
- Filtrar por intervalos de datas para melhorar a velocidade da consulta em conjuntos de dados grandes
- Aproveitar as identidades de perfil que correspondem à configuração do namespace do jornada

**Qualidade dos dados**

- Monitorar regularmente [eventos descartados](sharing-field-list.md#discarded-events) para identificar problemas de dados
- Validar se os esquemas de evento correspondem aos requisitos de análise
- Implementar a manipulação adequada de erros em consultas personalizadas

**Estratégias de análise**

- Combine eventos de etapa de jornada com dados de feedback da mensagem para atribuição completa
- Use a análise baseada em tempo para entender a velocidade da jornada e os gargalos
- Criar análises de coorte para comparar diferentes variações de jornada

### Recursos avançados de análise {#advanced-analytics}

**integração com o Customer Journey Analytics**
Os eventos de etapa de Jornada podem ser analisados usando o Customer Journey Analytics para:

- Modelagem de atribuição avançada
- Visualização de jornada entre canais
- Análise preditiva dos resultados da jornada

**Decisão em tempo real**
Use os padrões de evento de etapa do jornada para:

- Acionar personalização em tempo real
- Implementar a otimização dinâmica do jornada
- Ativar recomendações contextuais de próxima ação

## Recursos adicionais {#additional-resources}

### Links de documentação {#documentation-links}

- **[Visão geral do compartilhamento de etapas do Jornada](sharing-overview.md)**: entender como os dados do jornada fluem para o Adobe Experience Platform
- **[Dicionário de esquemas internos](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=pt-BR)**: referência de esquema XDM completa
- **[Relatórios do Journey Optimizer](report-gs-cja.md)**: visão geral dos recursos de relatórios no Journey Optimizer

### Guias de integração {#integration-guides}

- **[Adobe Customer Journey Analytics](cja-ajo.md)**: Analisando dados do Journey Optimizer no CJA
- **[Gerenciamento de dados](../data/export-datasets.md)**: exportação e gerenciamento de dados do jornada
- **[Privacidade e governança](../privacy/audit-logs.md)**: considerações de governança de dados para eventos do jornada

Os eventos de etapa de Jornada formam a base da análise de jornada avançada no Adobe Journey Optimizer. Ao entender e aproveitar esses eventos de maneira eficaz, você pode obter insights profundos sobre o comportamento do cliente, otimizar o desempenho da jornada e criar experiências mais personalizadas para seus clientes.
