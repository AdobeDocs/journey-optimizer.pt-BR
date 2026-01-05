---
solution: Journey Optimizer
product: Journey Optimizer
title: Testar, validar e aprovar
description: Descubra todos os recursos de teste e aprovação no Journey Optimizer. Visualize o conteúdo, simule jornadas, valide emails, execute experimentos, detecte conflitos e configure fluxos de trabalho de aprovação antes do lançamento.
feature: Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: testar, validar, aprovar, aprovação, controle de qualidade, controle de qualidade, perfis de teste, personalização, renderização, verificação de spam, experimento de conteúdo, teste a/b, detecção de conflitos, seed-list, provas, dados de amostra, fluxo de trabalho de aprovação, teste de email, fluxo de trabalho de validação
redpen-status: CREATED_||_2025-08-11_20-30-59
exl-id: a770412f-2f80-459d-8cce-32212154d154
source-git-commit: fb13aee243757de7fe47bdd9d9ebad47069e24ba
workflow-type: tm+mt
source-wordcount: '3103'
ht-degree: 5%

---

# Testar, validar e aprovar{#section-overview}

Esta seção aborda todos os recursos de teste e aprovação no Journey Optimizer. Você encontrará ferramentas para pré-visualizar o conteúdo com perfis de teste, validar a lógica da jornada, verificar a renderização de email e as pontuações de spam, executar experimentos A/B, detectar conflitos e configurar fluxos de trabalho de aprovação.

Esta página de aterrissagem ajuda você a escolher a abordagem de teste correta com base no que está criando (campanhas versus jornadas), orienta você nos fluxos de trabalho de teste recomendados e fornece acesso rápido a todos os recursos de teste e aprovação. Comece com [Escolha sua abordagem de teste](#choose-your-testing-approach) abaixo para identificar quais ferramentas se aplicam ao seu caso de uso.

## Visão geral dos recursos de teste

**Tipos de teste disponíveis:**

* Teste de conteúdo: Visualizar e validar o conteúdo da mensagem antes de enviar → [Testar campanhas](#testing-campaigns), [Testar personalização](#testing-personalization)
* Teste de lógica de jornada: simular a progressão do cliente por meio de caminhos de jornada → [Testando jornadas](#testing-journeys)
* Teste técnico: Validar renderização, capacidade de entrega e autenticação → [Validação técnica](#2-technical-validation)
* Teste de desempenho: Comparar variações de conteúdo usando experimentos A/B → [Experimentos de conteúdo](#content-experiments--ab-testing)
* Teste de conflito: detectar sobreposições de campanha e jornada → [Detecção de conflito](#conflict-detection)
* Teste de aprovação: workflows de revisão estruturados antes da ativação → [Workflows de aprovação](#approval-workflows-for-journeys-and-campaigns)

**Principais recursos por contexto:**

| Recurso | Aplicável a | Restrições de canal | Pré-requisitos | Finalidade principal | Documentação |
|------------|-----------|---------------------|--------------|-----------------|---------------|
| [Perfis de teste](../using/content-management/test-profiles.md) | Campanhas, Jornadas | Todos os canais | Perfis de teste criados | Pré-visualizar conteúdo personalizado | [Guia](#testing-campaigns) |
| [Dados de entrada de exemplo](../test-approve/simulate-sample-input.md) | Campanhas, Jornadas | Email, SMS, Push, Web, Baseado em código, No aplicativo, Cartões de conteúdo | Arquivo CSV/JSON | Testar várias variantes de personalização | [Guia](#simulate-content-variations) |
| [Modo de teste](../using/building-journeys/testing-the-journey.md) | Somente jornadas | N/D | Jornada de rascunho, namespace configurado | Simular a progressão do perfil | Cartão [1&rbrace;](#test-your-journey) |
| [Execução seca](../using/building-journeys/journey-dry-run.md) | Somente jornadas | N/D | Jornada criada | Analisar caminhos de execução | Cartão [1&rbrace;](#journey-dry-run) |
| [Renderização de email](../using/content-management/rendering.md) | Campanhas, Jornadas | Somente email | Integração Litmus | Verificar exibição entre clientes | [Fluxo de trabalho](#2-technical-validation) |
| [Pontuação de spam](../using/content-management/spam-report.md) | Campanhas, Jornadas | Somente email | None | Validação da capacidade de entrega | [Fluxo de trabalho](#2-technical-validation) |
| [Listas de propagação](../using/configuration/seed-lists.md) | Campanhas, Jornadas | Somente email | Seed list configurado | Monitoramento das partes interessadas | Cartão [1&rbrace;](#seed-lists-for-stakeholder-monitoring) |
| [Experimentos de conteúdo](../using/content-management/get-started-experiment.md) | Somente campanhas | Todos os canais | None | Teste A/B e bandit multi-armed | Cartão [1&rbrace;](#content-experiments--ab-testing) |
| [Detecção de conflitos](../using/conflict-prioritization/conflicts.md) | Campanhas, Jornadas (limit.) | Todos os canais | None | Evitar mensagens excessivas por parte do cliente | Cartão [1&rbrace;](#conflict-detection) |
| [Fluxos de trabalho de aprovação](../using/test-approve/gs-approval.md) | Campanhas, Jornadas | Todos os canais | Política de aprovação criada | Processo de revisão estruturado | Cartão [1&rbrace;](#approval-workflows-for-journeys-and-campaigns) |
| [Playground do Personalization](../using/personalization/personalize.md#playground) | Todas | Todos os canais | None | Aprender e testar a sintaxe de personalização | Cartão [1&rbrace;](#personalization-playground) |

**Fluxos de trabalho de teste comuns:**

1. Pré-desenvolvimento: Use o [playground de personalização](#testing-personalization) para saber a sintaxe
2. Durante o desenvolvimento: visualize com [perfis de teste](#testing-campaigns), valide com [dados de entrada de exemplo](#simulate-content-variations)
3. Pré-inicialização: executar [testes técnicos](#2-technical-validation) (renderização, spam), verificar [conflitos](#conflict-detection), enviar para [aprovação](#approval-workflows-for-journeys-and-campaigns)
4. Pós-lançamento: Monitorar com relatórios ao vivo (consulte [Monitoramento e solução de problemas](#monitoring--troubleshooting)), iterar com base nos resultados


## Por que o teste e a aprovação são importantes

Os processos de teste e aprovação servem como quality gates (portais de qualidade) essenciais que protegem a reputação da sua marca e garantem o sucesso da campanha. É por isso que eles são importantes:

* **Detectar erros antes que eles cheguem aos clientes** - Identifique links com falha, personalização incorreta, problemas de renderização e falhas lógicas em um ambiente controlado em que as correções são rápidas e sem riscos.

* **Melhore a capacidade de entrega** - Teste pontuações de spam, valide a autenticação de email e verifique a renderização entre clientes de email para maximizar as taxas de posicionamento e de engajamento da caixa de entrada.

* **Garanta a consistência da marca** - Visualize o conteúdo com diferentes perfis de teste para verificar se a personalização é exibida corretamente para vários segmentos de clientes e mantém os padrões da marca.

* **Validar jornadas complexas** - Simular fluxos de jornada de várias etapas para confirmar se os acionadores são acionados corretamente, se as condições são avaliadas corretamente e se os clientes recebem as mensagens certas na hora certa.

* **Estabelecer responsabilidade** - Implementar fluxos de trabalho de aprovação formais que exigem a aprovação das partes interessadas, criando uma propriedade clara e reduzindo lançamentos de campanhas não autorizadas ou prematuras.

* **Economize tempo e recursos** - Detecte problemas no início do ciclo de desenvolvimento quando as correções são mais baratas e rápidas, evitando correções dispendiosas pós-lançamento ou escalonamentos do atendimento ao cliente.

## Principal terminologia

**[Perfis de teste](../using/content-management/test-profiles.md)** = Perfis de clientes sintéticos (não clientes reais) usados para visualizar conteúdo personalizado. Sinalizado no Serviço de perfil do cliente em tempo real. Necessário para modo de teste e pré-visualização de conteúdo. [Saiba como criar perfis de teste](../using/audience/creating-test-profiles.md)

**[Modo de teste](../using/building-journeys/testing-the-journey.md)** = recurso de simulação de Jornada que envia perfis de teste por caminhos de jornada. Limitações: somente jornadas de rascunho, exige namespace, somente perfis de teste. [Consulte a documentação do modo de teste](../using/building-journeys/testing-the-journey.md)

**[Dry run](../using/building-journeys/journey-dry-run.md)** = ferramenta de análise de execução de Jornada que rastreia caminhos sem enviar mensagens ou fazer chamadas de API. Caso de uso: validar a lógica sem consumir recursos. [Saiba mais sobre simulação](../using/building-journeys/journey-dry-run.md)

**[Dados de entrada de exemplo](../test-approve/simulate-sample-input.md)** = arquivos CSV ou JSON contendo valores de atributo de perfil para personalização de teste. Suporta até 30 variantes. Alternativa para criar perfis de teste. [Como simular variações de conteúdo](../test-approve/simulate-sample-input.md)

**[Seed lists](../using/configuration/seed-lists.md)** = Endereços de email de participantes internos incluídos automaticamente em entregas reais (não envios de teste). Somente canal de email. Caso de uso: monitoramento de qualidade e conformidade. [Configurar listas de propagação](../using/configuration/seed-lists.md)

**[Experimentos de conteúdo](../using/content-management/get-started-experiment.md)** = testes A/B ou experimentos de bandit com vários braços comparando variações de conteúdo. Somente campanhas, não disponível em jornadas. [Introdução a experimentos](../using/content-management/get-started-experiment.md) | [Criar experimentos](../using/content-management/content-experiment.md)

**[Provas](../using/content-management/proofs.md)** = Teste entregas de email enviadas para endereços de email específicos usando dados de perfil de teste. Diferente de listas de propagação (provas são envios manuais de teste, listas de propagação são cópias automáticas das partes interessadas). [Enviar provas](../using/content-management/proofs.md)

**[Detecção de conflitos](../using/conflict-prioritization/conflicts.md)** = Ferramenta que identifica campanhas sobrepostas e jornadas direcionadas aos mesmos públicos. Suporte limitado à jornada: unitário, Qualificação de público-alvo e Somente público-alvo de leitura. [Saiba mais sobre o gerenciamento de conflitos](../using/conflict-prioritization/gs-conflict-prioritization.md)

**[Fluxos de trabalho de aprovação](../using/test-approve/gs-approval.md)** = Processo de revisão em várias etapas que requer a aprovação da parte interessada antes da ativação. Requer configuração de política de aprovação. [Configurar aprovações](../using/test-approve/gs-approval.md) | [Criar políticas](../using/test-approve/approval-policies.md)

**[Testes de renderização](../using/content-management/rendering.md)** = Validação de exibição de email entre clientes de email (Gmail, Outlook, Apple Mail) e dispositivos. Requer integração com Litmus. [Testar renderização de email](../using/content-management/rendering.md)

**[Playground do Personalization](../using/personalization/personalize.md#playground)** = Ambiente de aprendizagem interativo para experimentar com sintaxe de personalização e testar expressões com dados de amostra. Não é necessário nenhum conjunto de dados ativo. [Acessar o playground](../using/personalization/personalize.md#playground)

## Árvore decisória para seleção do método de teste

Use essa árvore decisória para identificar rapidamente as ferramentas de teste corretas para seu cenário específico. Responda a cada pergunta com base no contexto (o que você está criando, o que precisa validar e qual canal está usando) para navegar diretamente para os recursos e a documentação relevantes.

+++ **Pergunta 1: O que você está testando?**

* Campanha → [Campanhas de teste](#testing-campaigns)
* Jornada → [Testando jornadas](#testing-journeys)
* Expressões Personalization → [Playground do Personalization](#testing-personalization)
+++

+++**Pergunta 2: Que aspecto precisa de validação?**

* Conteúdo e personalização → [Perfis de teste](#testing-campaigns) ou [dados de entrada de amostra](#simulate-content-variations)
* Exibição de email → [Testes de renderização de email](#2-technical-validation)
* Capacidade de entrega → [Verificações de pontuação de spam](#2-technical-validation)
* Lógica e fluxo de jornada → [Modo de teste](#testing-journeys) ou [simulação](#journey-dry-run)
* Comparação de desempenho → [Experimento de conteúdo](#content-experiments--ab-testing) (somente campanhas)
* Conflitos de temporização → [Detecção de conflitos](#conflict-detection)
* Análise das partes interessadas → [Fluxo de trabalho de aprovação](#approval-workflows-for-journeys-and-campaigns)
+++

+++**Pergunta 3: Que canal?**

* Email → Todos os métodos de teste disponíveis (consulte [Campanhas de teste](#testing-campaigns))
* SMS, Push → [Teste de conteúdo](#testing-campaigns), [dados de entrada de exemplo](#simulate-content-variations), [fluxos de trabalho de aprovação](#approval-workflows-for-journeys-and-campaigns)
* Web, No aplicativo, Baseado em código → [Teste de conteúdo](#testing-campaigns), [dados de entrada de amostra](#simulate-content-variations), [fluxos de trabalho de aprovação](#approval-workflows-for-journeys-and-campaigns)
* Vários canais → Teste cada canal separadamente
+++

+++**Pergunta 4: Quando no fluxo de trabalho?**

* Antes de construir → [Personalization playground](#personalization-playground) para aprendizado
* Durante a compilação → [Perfis de teste](#testing-campaigns) e [dados de entrada de amostra](#simulate-content-variations) para validação
* Antes da inicialização → [Testes de renderização](#2-technical-validation), [verificações de spam](#email-spam-report), [detecção de conflitos](#conflict-detection), [aprovações](#approval-workflows-for-journeys-and-campaigns)
* Após a inicialização → [Relatórios ao vivo](../using/building-journeys/report-journey.md) e [monitoramento](#monitoring--troubleshooting)
+++


## Escolha sua abordagem de teste

A abordagem de teste correta depende do que você está criando e do que é necessário validar. Use este guia para identificar as ferramentas de teste mais relevantes para o seu cenário.

### Testar campanhas

**Para todas as campanhas:**

* Visualizar e testar o conteúdo usando [perfis de teste](../using/content-management/test-profiles.md) ou [dados de entrada de exemplo](../test-approve/simulate-sample-input.md)
* Verificar [renderização de email](../using/content-management/rendering.md) entre dispositivos e clientes (somente canal de email)
* Executar [verificações de pontuação de spam](../using/content-management/spam-report.md) (somente canal de email)
* Revisar [conflitos](../conflict-prioritization/conflicts.md) com outras campanhas e jornadas
* Configurar [listas de propagação](../configuration/seed-lists.md) para monitoramento das partes interessadas (somente canal de email)
* Enviar para [aprovação](../using/test-approve/gs-approval.md) antes da ativação

**Para teste A/B e otimização:**

* Crie [experimentos de conteúdo](../using/content-management/get-started-experiment.md) para testar vários tratamentos e medir o desempenho

**Para campanhas acionadas por API:**

* Use a [API de Simulação de Campanha](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"} para acionar trabalhos de prova de forma programática

### Jornadas de teste

**Para todas as jornadas:**

* Use o [modo de teste](../using/building-journeys/testing-the-journey.md) para simular a progressão do perfil (somente jornadas de rascunho, requer namespace) ou [dry run](../using/building-journeys/journey-dry-run.md) para analisar os caminhos de execução sem enviar mensagens
* Testar mensagens individuais usando [visualização e provas](../using/content-management/preview-test.md)
* Verificar [conflitos](../conflict-prioritization/conflicts.md) com outras jornadas e campanhas
* Enviar para [aprovação](../using/test-approve/gs-approval.md) antes de publicar

**Para jornadas complexas:**

* Usar o modo de teste e testar juntos para validar completamente a lógica de ramificação e os caminhos de execução
* Testar condições de entrada e atributos de perfil diferentes sistematicamente

**Observação:** a detecção de conflitos e o limite de jornadas estão disponíveis somente para jornadas unitárias, de Qualificação de Público-Alvo e de Leitura de Público-Alvo.

### Teste de personalização

**Antes de criar o conteúdo:**

* Experimente no [playground de personalização](../using/personalization/personalize.md#playground) para saber sintaxe e testar expressões com dados de amostra

**Durante a criação do conteúdo:**

* Visualize com [perfis de teste](../using/content-management/test-profiles.md) para validar as renderizações de personalização corretamente
* Teste vários cenários usando [dados de entrada de amostra](../test-approve/simulate-sample-input.md) de arquivos CSV/JSON (suporta até 30 variantes)

## Práticas recomendadas de teste

Para maximizar a eficácia de seus esforços de teste, siga estas práticas recomendadas:

1. **Testar antes e com frequência** - Não espere até que uma campanha seja totalmente criada. Teste o conteúdo, a personalização e a lógica de forma incremental à medida que você desenvolve.

1. **Use perfis de teste realistas** - [Crie perfis de teste](../using/audience/creating-test-profiles.md) que representem com precisão os segmentos de público-alvo, incluindo casos de borda e diferentes cenários de personalização.

1. **Testar em dispositivos e clientes** - Verifique a [renderização de email](../using/content-management/rendering.md) em clientes de email populares (Gmail, Outlook, Apple Mail) e dispositivos (desktop, celular, tablet) para garantir uma exibição consistente (somente canal de email).

1. **Valide a personalização completamente** - Teste com vários [perfis de teste](../using/content-management/test-profiles.md) que tenham valores de atributo diferentes para confirmar se os tokens de personalização são renderizados corretamente e os valores de fallback funcionam. Use o [playground de personalização](../using/personalization/personalize.md#playground) para experimentar expressões de personalização e testar o código com dados de exemplo antes de aplicá-los às suas campanhas.

1. **Testar variações de conteúdo com dados de amostra** - Use [dados de entrada de amostra](../test-approve/simulate-sample-input.md) de arquivos CSV ou JSON para testar até 30 cenários de personalização sem criar vários perfis de teste, economizando tempo e garantindo uma cobertura abrangente. Suporta email, SMS, push, Web, experiência baseada em código, no aplicativo e canais de cartões de conteúdo.

1. **Usar listas de propagação para monitoramento das partes interessadas** - Configure [listas de propagação](../configuration/seed-lists.md) para incluir automaticamente as partes interessadas internas que receberão cópias de todas as entregas no tempo de execução para monitoramento de qualidade e verificação de conformidade (somente canal de email).

1. **Simular caminhos de jornada** - Para jornadas complexas com várias ramificações, use o [modo de teste](../using/building-journeys/testing-the-journey.md) para testar diferentes condições de entrada e atributos de perfil para validar todos os caminhos possíveis. Disponível para jornadas de rascunho que usam um namespace.

1. **Verificar indicadores de capacidade de entrega** - Revisar [pontuações de spam](../using/content-management/spam-report.md), status de autenticação e métricas de integridade de email antes de envios grandes (somente canal de email).

1. **Documentar resultados do teste** - Mantenha registros dos resultados do teste, problemas encontrados e resoluções para melhorar futuros processos de teste e compartilhar aprendizados com a sua equipe.

1. **Envolva as partes interessadas antecipadamente** - Compartilhe visualizações e resultados de teste com as partes interessadas antes da [aprovação formal](../using/test-approve/gs-approval.md) para coletar comentários e alinhar as expectativas.

## Fluxo de trabalho de teste recomendado

Siga esta abordagem sistemática para garantir testes completos e aprovações tranquilas:

### &#x200B;1. Desenvolvimento e visualização de conteúdo

Comece criando seu conteúdo e usando os recursos de visualização para verificar o design e a personalização iniciais:

* Crie seu [email](../using/email/create-email.md), [SMS](../using/sms/create-sms.md), [notificação por push](../using/push/create-push.md) ou outro conteúdo de canal

* Use o recurso **[Simular conteúdo](../using/content-management/preview-test.md)** para visualizar com perfis de teste

* Verificar [tokens de personalização](../using/personalization/personalization-syntax.md), conteúdo dinâmico e valores de fallback

* Experimente com expressões de personalização no **[playground de personalização](../using/personalization/personalize.md#playground)** para testar e refinar seu código com dados de amostra antes de aplicar ao conteúdo ativo

* Teste várias variações usando **[dados de entrada de amostra](../test-approve/simulate-sample-input.md)** de arquivos CSV/JSON para validar a personalização em vários cenários de perfil

* Verificar [renderização](../using/content-management/rendering.md) em telas de tamanhos diferentes e clientes de email

### &#x200B;2. Validação técnica

Validar aspectos técnicos que afetam a capacidade de entrega e a funcionalidade:

* Execute [verificações de pontuação de spam](../using/content-management/spam-report.md) para identificar possíveis problemas de entrega

* Testar links para garantir que não estejam quebrados e rastreiem corretamente

* Validar a configuração da [autenticação de email](../using/configuration/dmarc-record.md) (SPF, DKIM, DMARC)

* Revise a renderização do HTML e verifique se há problemas de compatibilidade de CSS

* Testar [design responsivo](../using/email/content-from-scratch.md) em dispositivos móveis e desktop

* Verifique se há [possíveis conflitos](../conflict-prioritization/conflicts.md) com outras campanhas e jornadas para evitar problemas de tempo e fadiga da mensagem do cliente

### &#x200B;3. Teste de Jornada (somente jornada)

Se você estiver testando uma jornada, valide a lógica de orquestração:

* Ative o **[Modo de teste](../using/building-journeys/testing-the-journey.md)** para simular a progressão do perfil através da jornada

* Teste diferentes [condições de entrada](../using/building-journeys/entry-management.md) e qualificações de público

* Verificar se as [atividades de espera](../using/building-journeys/wait-activity.md), [condições](../using/building-journeys/condition-activity.md) e a lógica de ramificação funcionam corretamente

* Use **[Dry run](../using/building-journeys/journey-dry-run.md)** para jornadas complexas para analisar caminhos de execução sem enviar mensagens

* Verifique se os [eventos](../using/event/about-events.md) são acionados corretamente e se as [ações personalizadas](../using/action/about-custom-action-configuration.md) são executadas conforme esperado

### &#x200B;4. Apresentação da aprovação

Quando o teste for concluído e os problemas forem resolvidos:

* Enviar a campanha ou a jornada para aprovação de acordo com a [política de aprovação](../using/test-approve/approval-policies.md) da sua organização

* Incluir resultados e documentação de teste com a [solicitação de aprovação](../using/test-approve/request-approval.md)

* Resolva qualquer comentário ou solicitação de mudança de [aprovadores](../using/test-approve/review-approve-request.md)

* Faça as revisões necessárias e teste novamente se as alterações forem significativas

### &#x200B;5. Verificação de pré-lançamento

Antes de ativar sua campanha ou jornada:

* Executar uma revisão final de todas as configurações, públicos e [agendamentos](../using/building-journeys/journey-properties.md)

* Verificar se todas as aprovações estão implementadas e documentadas

* Confirme se os horários de envio e os [fusos horários](../using/building-journeys/timezone-management.md) estão corretos

* Habilitar [monitoramento e alertas](../using/reports/alerts.md) para acompanhar o desempenho após a inicialização

### &#x200B;6. Monitorar e iterar

Após o lançamento, continue o monitoramento para detectar problemas antecipadamente:

* Configurar [alertas do sistema](../using/reports/alerts.md) para erros de jornada, altas taxas de rejeição ou baixo engajamento

* Revise os [relatórios ao vivo](../using/building-journeys/report-journey.md) para acompanhar o desempenho em relação às expectativas

* Esteja preparado para [pausar ou modificar](../using/building-journeys/journey-pause.md) jornadas se surgirem problemas críticos

* Documentar as lições aprendidas para melhorar os futuros processos de teste

## Testes em ação: casos de uso

Veja como os conceitos de teste se aplicam a cenários do mundo real:

| Caso de uso | O que você vai aprender | Foco do teste principal |
|----------|-------------------|-------------------|
| **[Enviar mensagens multicanais](../using/building-journeys/journeys-uc.md)** | Teste uma jornada que combine Ler público-alvo, eventos de reação e mensagens de email/push. Valide todo o fluxo, desde o direcionamento de público até a entrega de mensagens. | Coordenação multicanal, eventos de reação, validação completa do fluxo, etapas de teste e publicação |
| **[Enviar uma mensagem aos assinantes](../using/building-journeys/message-to-subscribers-uc.md)** | Teste jornadas que direcionem listas de assinaturas com endereçamento de email dinâmico. Valide expressões de personalização para um direcionamento de assinante correto. | Expressões do Personalization, endereçamento dinâmico, direcionamento de lista de assinaturas |
| **[Enviar mensagens associadas ao tempo](../using/building-journeys/weekday-email-uc.md)** | Teste jornadas com condições baseadas em tempo para garantir que as mensagens sejam enviadas em dias específicos. Validar atividades de espera e lógica de programação. | Condições baseadas em tempo, atividades de espera, validação de programação |
| **[Saiba mais sobre casos de uso do jornada](../using/building-journeys/jo-use-cases.md)** | Acesse uma coleção abrangente de exemplos práticos que abrangem eventos de experiência, mensagens multicanais e integrações externas do sistema. | Vários cenários, padrões avançados, testes de integração |

## Testar e aprovar o conteúdo

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=pt-BR)

Visualizar, testar e validar o conteúdo

Saiba como visualizar, testar e validar um conteúdo personalizado por meio de perfis de teste, testes de renderização de email, avaliações de pontuação de spam e muito mais.

[Explore a prévia e teste do conteúdo](preview-test-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=pt-BR)

Fluxos de trabalho de aprovação para jornadas e campanhas

Entenda como configurar, gerenciar e executar processos de aprovação para garantir o controle de qualidade de jornadas e campanhas.

[Saiba mais sobre fluxos de trabalho de aprovação](approve-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=pt-BR)

Teste a jornada

Valide sua jornada antes de publicá-la testando-a com perfis específicos para garantir que eventos, condições e ações funcionem conforme esperado. Disponível para jornadas de rascunho que usam um namespace.

[Teste a jornada](../using/building-journeys/testing-the-journey.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=pt-BR)

Execução de teste de jornada

Realize uma execução de teste para simular e validar o caminho de execução da jornada, identificando possíveis problemas antes da ativação.

[Saiba mais sobre a execução de teste da jornada](../using/building-journeys/journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=pt-BR)

Monitoramento e solução de problemas

Acesse recursos abrangentes de solução de problemas, alertas do sistema e códigos de erro para resolver problemas de execução e desempenho de jornadas.

[Exibir monitoramento e solução de problemas](troubleshoot-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code.svg?lang=pt-BR)

Personalization Playground

Experimente expressões de personalização em um ambiente seguro. Teste o código com dados de amostra e visualize os resultados antes de aplicar a campanhas e jornadas.

[Saiba mais sobre o Personalization Playground](../using/personalization/personalize.md#playground)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/data.svg)

Experimentos de conteúdo e teste A/B

Otimize suas campanhas testando várias variações de conteúdo e medindo o desempenho para identificar os tratamentos com melhor desempenho. Disponível somente para campanhas (suporta experimentos de A/B e bandit multiarmado).

[Saiba Mais Sobre Experimentos De Conteúdo](../using/content-management/get-started-experiment.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=pt-BR)

Listas de seeds para monitoramento pelas partes interessadas

Inclua automaticamente endereços internos de partes interessadas nos deliveries para monitorar mensagens reais enviadas aos clientes para garantia de qualidade e conformidade. Disponível somente para canal de email.

[Configurar Seed Lists](../using/configuration/seed-lists.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bell.svg?lang=pt-BR)

Detecção de conflitos

Identifique possíveis sobreposições entre campanhas e jornadas para evitar sobrecarregar os clientes com muitas comunicações simultâneas. Disponível para campanhas e unitário, Qualificação de público-alvo e jornadas Ler público-alvo.

[Detectar conflitos](../using/conflict-prioritization/conflicts.md)
:::

::::

## Recursos adicionais

### Guias essenciais de teste e validação

* [Simular Variações de Conteúdo](../test-approve/simulate-sample-input.md) - Teste até 30 cenários de personalização usando arquivos CSV ou JSON. Ideal para testes de conteúdo multilíngue sem criar vários perfis de teste. Oferece suporte a email, SMS, push, Web, baseado em código, no aplicativo e cartões de conteúdo.

* [Criação de Perfis de Teste](../using/audience/creating-test-profiles.md) - Crie e gerencie perfis de teste para simular cenários de clientes. Saiba como sinalizar perfis para teste, definir atributos e organizar segmentos de teste.

* [Relatório de spam por email](../using/content-management/spam-report.md) - Verifique as pontuações de spam antes de enviar para melhorar a capacidade de entrega e a inserção na caixa de entrada. Obtenha recomendações acionáveis para otimização de conteúdo.

* [Perguntas frequentes sobre o Jornada](../using/building-journeys/journey-faq.md) - consulte rapidamente perguntas comuns sobre testes, execução e solução de problemas do jornada.

### Dependências e relacionamentos

Entenda como os recursos de teste se conectam entre si e com seus fluxos de trabalho mais amplos do Journey Optimizer. Esta seção mapeia pré-requisitos, dependências upstream/downstream e combinações de recursos comuns.

+++**Pré-requisitos (necessários antes do teste)**

* Perfis de teste devem ser criados antes do uso do modo de teste ou pré-visualização de conteúdo
* As políticas de aprovação devem ser configuradas antes do envio para aprovação
* Seed lists deve ser criadas antes de adicionar a campanhas/jornadas
* Integração Litmus necessária para testes de renderização de email
* A jornada deve estar em status de rascunho para usar o modo de teste
* A jornada deve ter o namespace configurado para usar o modo de teste

+++

+++**Do que depende o teste (upstream)**

* Criação de conteúdo: campanhas ou jornadas necessárias para teste
* Perfis de teste: obrigatório para modo de teste e pré-visualização de conteúdo
* Políticas de aprovação: obrigatório para workflows de aprovação
* Configuração: configurações de canal, autenticação de email, configurações de domínio

+++

+++**O que depende de teste (downstream)**

* Ativação de campanha/jornada: não é possível ativar sem resolver erros
* Publicação: pode ser necessária aprovação antes da publicação
* Monitoramento ao vivo: Monitoramento e relatórios pós-lançamento
* Otimização: use os resultados de teste para refinar campanhas futuras

+++

+++**Recursos relacionados**

* Testes + fluxos de trabalho de aprovação = Processo de controle de qualidade
* Teste + Detecção de conflitos = evitar o excesso de mensagens do cliente
* Testes + experimentos de conteúdo = Otimização do desempenho
* Testes + Emissão de relatórios = ciclo de aprimoramento contínuo
* Perfis de teste + Personalization = Validação de conteúdo
* Execução a seco + Modo de teste = Validação abrangente de jornada

+++

+++**Combinações comuns de recursos**

* Teste de conteúdo: Perfis de teste + Dados de entrada de amostra + Playground do Personalization
* Validação de email: testes de renderização + pontuações de spam + perfis de teste + provas
* Validação da jornada: modo de teste + simulação + perfis de teste
* Lista de verificação de pré-lançamento: todos os testes técnicos + Detecção de conflitos + Fluxos de trabalho de aprovação

+++

### Perguntas comuns

+++**P: Que teste é necessário antes de iniciar uma campanha?**

**Mínimo:** Visualização de conteúdo com perfis de teste + verificação de pontuação de spam (email)
**Recomendado:** + Renderização de email + Detecção de conflitos + Fluxo de trabalho de aprovação
**Prática recomendada:** + Teste de dados de entrada de amostra + Listas de propagação + Experimento A/B (se estiver otimizando)

+++

+++**P: Como faço para testar a personalização sem criar muitos perfis de teste?**

**Solução primária:** Use [dados de entrada de exemplo](../test-approve/simulate-sample-input.md) com arquivos CSV/JSON (suporta até 30 variantes)
**Alternativa:** Crie de 3 a 5 [perfis de teste](../using/audience/creating-test-profiles.md) representativos que abrangem segmentos-chave
**Ferramenta de aprendizado:** Experimente primeiro em [playground de personalização](../using/personalization/personalize.md#playground)

+++

+++**P: Qual é a diferença entre o modo de teste e a simulação para o jornada?**

**Modo de teste:** Envia perfis de teste por meio de jornada, aciona ações reais e gera mensagens de teste. Requer jornada de rascunho + namespace.
**Execução sem erros:** Rastreia caminhos de execução sem enviar nada. Funciona em qualquer status de jornada. Nenhuma mensagem enviada, nenhuma ação executada.
**Use juntos:** Modo de teste para teste de mensagem + Dry run para validação lógica = cobertura abrangente.

+++

+++**P: Posso testar jornadas no status produção/ativo?**

**Modo de teste:** Não - somente jornadas de rascunho
**Execução sem erros:** Sim - funciona em qualquer status de jornada
**Visualização de conteúdo:** Sim - visualizar mensagens individuais a qualquer momento
**Solução alternativa:** duplicar jornada em tempo real no rascunho para validação do modo de teste completo

+++

+++**P: Quais recursos de teste exigem integrações externas?**

**Renderização de email:** Requer integração Litmus (licença separada)
**Todos os outros:** Integrado ao Journey Optimizer, sem necessidade de integrações adicionais
**Observação:** perfis de teste exigem o Serviço de Perfil do Cliente em Tempo Real (incluído)

+++

+++**P: Como testar campanhas acionadas por API?**

**Opção 1:** Use a [API de Simulação de Campanha](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"} para testes programáticos
**Opção 2:** Visualizar conteúdo com perfis de teste na interface
**Opção 3:** Enviar provas para testar endereços de email
**Prática recomendada:** combine todos os três para obter uma validação abrangente

+++


### Tópicos relacionados

* [Gerenciamento de conteúdo](content-management-landing-page.md) - Saiba como projetar, visualizar e gerenciar conteúdo usando modelos, fragmentos e o Email Designer. Práticas recomendadas de criação de conteúdo principal para uma identidade visual consistente.

* [Reporting &amp; Analytics](reporting-landing-page.md) - Analise o desempenho da campanha e do jornada com relatórios, painéis e métricas abrangentes. Tome decisões orientadas por dados para otimizar as experiências do cliente.

* [Configuração de Jornada](configure-journeys-landing-page.md) - Configure fontes de dados, eventos e ações personalizadas para habilitar a orquestração de jornada sofisticada. Estabeleça as bases técnicas para a criação de jornadas.

* [Gerenciamento de campanhas](../using/campaigns/get-started-with-campaigns.md) - Explore diferentes tipos de campanhas e saiba como criar, agendar e otimizar campanhas em lote e em tempo real para obter o máximo impacto.
