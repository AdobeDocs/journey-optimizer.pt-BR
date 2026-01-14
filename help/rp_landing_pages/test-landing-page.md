---
solution: Journey Optimizer
product: Journey Optimizer
title: Testar, validar e aprovar
description: Descubra todos os recursos de teste e aprovação no Journey Optimizer. Visualize o conteúdo, simule jornadas, valide emails, execute experimentos, detecte conflitos e configure fluxos de trabalho de aprovação antes do lançamento.
feature: Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: testar, validar, aprovar, aprovação, controle-de-qualidade, qa, perfis-de-teste, personalização, renderização, verificação-de-spam, experimento-de-conteúdo, teste-a/b, detecção-de-conflitos, lista-de-seeds, provas, dados-de-amostra, fluxo-de-trabalho-de-aprovação, teste-de-email, fluxo-de-trabalho-de-validação
redpen-status: CREATED_||_2025-08-11_20-30-59
exl-id: a770412f-2f80-459d-8cce-32212154d154
source-git-commit: c3535f39b351d671054031b9cc391bf6d9d83a09
workflow-type: ht
source-wordcount: '2328'
ht-degree: 100%

---

# Testar, validar e aprovar{#section-overview}

Esta seção aborda todos os recursos de teste e aprovação no Journey Optimizer. Você encontrará ferramentas para visualizar o conteúdo com perfis de teste, validar a lógica da jornada, verificar a renderização de email e as pontuações de spam, executar experimentos A/B, detectar conflitos e configurar fluxos de trabalho de aprovação.

Esta página de destino ajuda a escolher a abordagem de teste correta com base no que está sendo criado (campanhas ou jornadas), orienta nos fluxos de trabalho de teste recomendados e fornece acesso rápido a todos os recursos de teste e aprovação. Comece com [Escolha sua abordagem de teste](#choose-your-testing-approach) abaixo para identificar quais ferramentas se aplicam ao seu caso de uso. Para obter as definições dos principais termos de teste, consulte [Terminologia principal](#key-terminology).

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

Valide a jornada antes da publicação testando-a com perfis específicos para garantir que eventos, condições e ações funcionem conforme esperado. Disponível para jornadas de rascunho que usam um namespace.

[Teste a jornada](../using/building-journeys/testing-the-journey.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=pt-BR)

Execução de teste da jornada

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

Playground de personalização

Experimente expressões de personalização em um ambiente seguro. Teste o código com dados de amostra e visualize os resultados antes de aplicar a campanhas e jornadas.

[Saiba mais sobre o Playground de personalização](../using/personalization/personalize.md#playground)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=pt-BR)

Experimentos de conteúdo e teste A/B

Otimize as campanhas testando múltiplas variações de conteúdo e medindo o desempenho para identificar os tratamentos com melhor performance. Disponível somente para campanhas (é compatível com experimentos A/B e multi-armed bandit).

[Saiba mais sobre Experimentos de conteúdo](../using/content-management/get-started-experiment.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=pt-BR)

Listas de seeds para monitoramento pelas partes interessadas

Inclua automaticamente endereços internos de partes interessadas nas entregas para monitorar mensagens reais enviadas aos clientes e garantir o controle de qualidade e a conformidade. Disponível somente para canal de email.

[Configurar Listas de seeds](../using/configuration/seed-lists.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bell.svg?lang=pt-BR)

Detecção de conflitos

Identifique possíveis sobreposições entre campanhas e jornadas para evitar sobrecarregar os clientes com muitas comunicações simultâneas. Disponível para campanhas e jornadas unitárias, de Qualificação de público-alvo e de Público-alvo de leitura.

[Detectar conflitos](../using/conflict-prioritization/conflicts.md)
:::

::::

## Por que o teste e a aprovação são importantes

Os processos de teste e aprovação servem como estágios de qualidade essenciais que protegem a reputação da marca e garantem o sucesso da campanha. É por isso que eles são importantes:

* **Detecte erros antes que eles cheguem aos clientes** - Identifique links com falha, personalização incorreta, problemas de renderização e falhas lógicas em um ambiente controlado em que as correções são rápidas e sem riscos.

* **Melhore a capacidade de entrega** - Teste pontuações de spam, valide a autenticação de email e verifique a renderização nos clientes de email para maximizar as taxas de recebimento da caixa de entrada e de engajamento.

* **Garanta a consistência da marca**: visualize o conteúdo com diferentes perfis de teste para verificar se a personalização é exibida corretamente para os vários segmentos de clientes e mantém os padrões da marca.

* **Valide jornadas complexas** – simule fluxos de jornada de várias etapas para confirmar se os acionadores disparam corretamente, se as condições são avaliadas adequadamente e se os clientes recebem as mensagens certas na hora certa.

* **Estabeleça a responsabilidade**: implemente fluxos de trabalho de aprovação formal que exigem a aprovação das partes interessadas, criando uma propriedade clara e reduzindo lançamentos de campanhas não autorizadas ou prematuras.

* **Economize tempo e recursos** - Detecte problemas no início do ciclo de desenvolvimento, quando as correções são mais baratas e rápidas, evitando ajustes de alto custo no pós-lançamento ou acionamentos do serviço de atendimento ao cliente.

<!--## Testing capabilities overview

**Testing types available:**

* Content testing: Preview and validate message content before sending → [Choose your testing approach](#choose-your-testing-approach)
* Journey logic testing: Simulate customer progression through journey paths → [Choose your testing approach](#choose-your-testing-approach)
* Technical testing: Validate rendering, deliverability, and authentication → [Technical validation](#2-technical-validation)
* Performance testing: Compare content variations using A/B experiments → [Content Experiments & A/B Testing](#test--approve-content)
* Conflict testing: Detect campaign and journey overlaps → [Conflict Detection](#test--approve-content)
* Approval testing: Structured review workflows before activation → [Approval Workflows](#test--approve-content)

**Key capabilities by context:**

| Capability | Applies to | Channel restrictions | Prerequisites | Primary purpose |
|------------|-----------|---------------------|--------------|-----------------|
| [Test profiles](../using/content-management/test-profiles.md) | Campaigns, Journeys | All channels | Test profiles created | Preview personalized content |
| [Sample input data](../using/test-approve/simulate-sample-input.md) | Campaigns, Journeys | Email, SMS, Push, Web, Code-based, In-app, Content cards | CSV/JSON file | Test multiple personalization variants |
| [Test mode](../using/building-journeys/testing-the-journey.md) | Journeys only | N/A | Draft journey, namespace configured | Simulate profile progression |
| [Dry run](../using/building-journeys/journey-dry-run.md) | Journeys only | N/A | Journey created | Analyze execution paths |
| [Email rendering](../using/content-management/rendering.md) | Campaigns, Journeys | Email only | Litmus integration | Verify display across clients |
| [Spam score](../using/content-management/spam-report.md) | Campaigns, Journeys | Email only | None | Deliverability validation |
| [Seed lists](../using/configuration/seed-lists.md) | Campaigns, Journeys | Email only | Seed list configured | Stakeholder monitoring |
| [Content experiments](../using/content-management/get-started-experiment.md) | Campaigns only | All channels | None | A/B and multi-armed bandit testing |
| [Conflict detection](../using/conflict-prioritization/conflicts.md) | Campaigns, Journeys (limited) | All channels | None | Prevent customer over-messaging |
| [Approval workflows](../using/test-approve/gs-approval.md) | Campaigns, Journeys | All channels | Approval policy created | Structured review process |
| [Personalization playground](../using/personalization/personalize.md#playground) | All | All channels | None | Learn and test personalization syntax |

**Common testing workflows:**

1. Pre-development: Use [personalization playground](#test--approve-content) to learn syntax
2. During development: Preview with [test profiles](#choose-your-testing-approach), validate with [sample input data](#choose-your-testing-approach)
3. Pre-launch: Run [technical tests](#2-technical-validation) (rendering, spam), check [conflicts](#test--approve-content), submit for [approval](#test--approve-content)
4. Post-launch: Monitor with live reports (see [Monitoring & Troubleshooting](#test--approve-content)), iterate based on results

-->

<!--
## Decision tree for testing method selection

Use this decision tree to quickly identify the right testing tools for your specific scenario. Answer each question based on your context (what you're building, what you need to validate, and which channel you're using) to navigate directly to the relevant capabilities and documentation.

+++ **Question 1: What are you testing?**

* Campaign → [Choose your testing approach](#choose-your-testing-approach)
* Journey → [Choose your testing approach](#choose-your-testing-approach)
* Personalization expressions → [Personalization playground](#test--approve-content)
+++

+++**Question 2: What aspect needs validation?**

* Content and personalization → [Test profiles](#choose-your-testing-approach) or [sample input data](#choose-your-testing-approach)
* Email display → [Email rendering tests](#2-technical-validation)
* Deliverability → [Spam score checks](#2-technical-validation)
* Journey logic and flow → [Test mode](#choose-your-testing-approach) or [dry run](#test--approve-content)
* Performance comparison → [Content experiment](#test--approve-content) (campaigns only)
* Timing conflicts → [Conflict detection](#test--approve-content)
* Stakeholder review → [Approval workflow](#test--approve-content)
+++

+++**Question 3: What channel?**

* Email → All testing methods available (see [Choose your testing approach](#choose-your-testing-approach))
* SMS, Push → [Content testing](#choose-your-testing-approach), [sample input data](#choose-your-testing-approach), [approval workflows](#test--approve-content)
* Web, In-app, Code-based → [Content testing](#choose-your-testing-approach), [sample input data](#choose-your-testing-approach), [approval workflows](#test--approve-content)
* Multiple channels → Test each channel separately
+++

+++**Question 4: When in the workflow?**

* Before building → [Personalization playground](#test--approve-content) for learning
* During building → [Test profiles](#choose-your-testing-approach) and [sample input data](#choose-your-testing-approach) for validation
* Before launch → [Rendering tests](#2-technical-validation), [spam checks](#2-technical-validation), [conflict detection](#test--approve-content), [approvals](#test--approve-content)
* After launch → [Live reports](../using/building-journeys/report-journey.md) and [monitoring](#test--approve-content)
+++

-->

## Escolha a abordagem de teste

A abordagem de teste correta depende do que você está criando e do que é necessário validar. Use este guia para identificar as ferramentas de teste mais relevantes para o cenário.

>[!BEGINTABS]

>[!TAB Teste de campanhas]

**Para todas as campanhas:**

* Visualize e teste conteúdo usando [perfis de teste](../using/content-management/test-profiles.md) ou [dados de entrada de amostra](../using/test-approve/simulate-sample-input.md)
* Verifique a [renderização de email](../using/content-management/rendering.md) nos dispositivos e clientes (somente canal de email)
* Execute [verificações de pontuação de spam](../using/content-management/spam-report.md) (somente canal de email)
* Revise [conflitos](../using/conflict-prioritization/conflicts.md) com outras campanhas e jornadas
* Configure [listas de seeds](../using/configuration/seed-lists.md) para monitoramento das partes interessadas (somente canal de email)
* Envie para [aprovação](../using/test-approve/gs-approval.md) antes da ativação

**Para teste A/B e otimização:**

* Crie [experimentos de conteúdo](../using/content-management/get-started-experiment.md) para testar vários tratamentos e medir o desempenho

**Para campanhas acionadas por API:**

* Use a [API de simulação de campanhas](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target-&quot;_blank&quot;} para acionar tarefas de prova de forma programática

>[!TAB Teste de jornadas]

**Para todas as jornadas:**

* Use o [modo de teste](../using/building-journeys/testing-the-journey.md) para simular a progressão do perfil (somente jornadas de rascunho, requer namespace) ou a [execução de teste](../using/building-journeys/journey-dry-run.md) para analisar os caminhos de execução sem enviar mensagens
* Teste mensagens individuais usando [visualização e provas](../using/content-management/preview-test.md)
* Verifique [conflitos](../using/conflict-prioritization/conflicts.md) com outras jornadas e campanhas
* Envie para [aprovação](../using/test-approve/gs-approval.md) antes de publicar

**Para jornadas complexas:**

* Use o modo de teste e a execução de teste juntos para validar de forma abrangente a lógica de ramificação e os caminhos de execução
* Teste condições de entrada e atributos de perfil diferentes sistematicamente

**Observação:** a detecção de conflitos e o limite de jornadas estão disponíveis somente para jornadas unitárias, de Qualificação de público-alvo e de Público-alvo de leitura.

>[!TAB Teste de personalização]

**Antes de criar o conteúdo:**

* Experimente no [playground de personalização](../using/personalization/personalize.md#playground) para aprender a sintaxe e testar expressões com dados de amostra

**Durante a criação do conteúdo:**

* Visualize com [perfis de teste](../using/content-management/test-profiles.md) para validar as renderizações de personalização corretamente
* Teste vários cenários usando [dados de entrada de amostra](../using/test-approve/simulate-sample-input.md) de arquivos CSV/JSON (suporta até 30 variantes)

>[!ENDTABS]

## Práticas recomendadas de teste

Para maximizar a eficácia dos testes, siga estas práticas recomendadas:

1. **Testar antes e com frequência** - Não espere até que uma campanha seja totalmente criada. Teste o conteúdo, a personalização e a lógica de forma incremental à medida que você desenvolve.

1. **Use perfis de teste realistas**: [crie perfis de teste](../using/audience/creating-test-profiles.md) que representem com precisão os segmentos de público-alvo, incluindo casos extremos e diferentes cenários de personalização.

1. **Teste nos dispositivos e clientes** - Verifique a [renderização do email](../using/content-management/rendering.md) em clientes de email (Gmail, Outlook, Apple Mail) e dispositivos (desktop, dispositivos móveis, tablet) populares para garantir uma exibição consistente (somente canal de email).

1. **Valide a personalização de forma abrangente** - Teste com vários [perfis de teste](../using/content-management/test-profiles.md) que tenham valores de atributo diferentes para confirmar se os tokens de personalização são renderizados corretamente e os valores de fallback funcionam. Use o [playground de personalização](../using/personalization/personalize.md#playground) para experimentar expressões de personalização e testar o código com dados de amostra, antes de aplicá-los às campanhas.

1. **Teste variações de conteúdo com dados de amostra** - Use [dados de entrada de amostra](../using/test-approve/simulate-sample-input.md) de arquivos CSV ou JSON para testar até 30 cenários de personalização sem criar vários perfis de teste, economizando tempo e garantindo uma cobertura abrangente. É compatível com email, SMS, push, web, experiência baseada em código, no aplicativo e canais de cartões de conteúdo.

1. **Use listas de seeds para monitoramento das partes interessadas** - Configure [listas de seeds](../using/configuration/seed-lists.md) para incluir automaticamente as partes interessadas internas que receberão cópias de todas as entregas no tempo de execução, com o objetivo de um monitoramento de qualidade e verificação de conformidade (somente canal de email).

1. **Simule caminhos de jornada** - Em jornadas complexas com várias ramificações, use o [modo de teste](../using/building-journeys/testing-the-journey.md) para testar diferentes condições de entrada e atributos de perfil, validando todos os caminhos possíveis. Disponível para jornadas de rascunho que usam um namespace.

1. **Verifique indicadores de capacidade de entrega** - Revise [pontuações de spam](../using/content-management/spam-report.md), status de autenticação e métricas de integridade de email antes de envios grandes (somente canal de email).

1. **Documente os resultados do teste** - Mantenha registros dos resultados do teste, problemas encontrados e resoluções para aprimorar futuros processos de teste e compartilhar aprendizados com a equipe.

1. **Envolva as partes interessadas antecipadamente** - Compartilhe visualizações e resultados de teste com as partes interessadas antes da [aprovação formal](../using/test-approve/gs-approval.md) para obter feedback e alinhar as expectativas.

## Fluxo de trabalho de teste recomendado

Siga esta abordagem de quatro fases para validar campanhas e jornadas antes do lançamento:

| Fase | O que testar | Principais ações |
|-------|-------------|-------------|
| **1. Validação de conteúdo** | Personalização, projeto, renderização | [Visualize com perfis de teste](../using/content-management/preview-test.md), teste [múltiplas variações](../using/test-approve/simulate-sample-input.md) com CSV/JSON, verifique a [renderização](../using/content-management/rendering.md) nos dispositivos |
| **2. Verificações técnicas** | Capacidade de entrega, links, conflitos | Realize [verificações de pontuação de spam](../using/content-management/spam-report.md), valide links, verifique [conflitos](../using/conflict-prioritization/conflicts.md) com outras campanhas |
| **3. Lógica de jornada** (somente jornada) | Condições de entrada, fluxo, ramificação | Use o [modo de teste](../using/building-journeys/testing-the-journey.md) para simular a progressão, realize a [execução de teste](../using/building-journeys/journey-dry-run.md) para caminhos complexos |
| **4. Pré-lançamento** | Configurações, aprovações, monitoramento | Envie para [aprovação](../using/test-approve/gs-approval.md), verifique agendamentos e públicos-alvo, habilite [alertas](../using/reports/alerts.md) |

**Dica profissional:** comece com o [playground de personalização](../using/personalization/personalize.md#playground) para testar expressões antes de criar conteúdo e sempre verifique a [detecção de conflitos](../using/conflict-prioritization/conflicts.md) antes do lançamento para evitar mensagens excessivas.

## Testes em ação: casos de uso

Veja como os conceitos de teste se aplicam a cenários do mundo real:

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../using/building-journeys/journeys-uc.md">
<img alt="Envie mensagens multicanal" src="../using/assets/do-not-localize/start-journey.jpeg">
</a>
<div>
<a href="../using/building-journeys/journeys-uc.md"><strong>Envie mensagens multicanal</strong></a>
</div>
<p>
Teste uma jornada que combine Público-alvo de leitura, eventos de reação e mensagens de email/push. Valide todo o fluxo, desde o direcionamento de público-alvo até a entrega de mensagens. Concentre-se na coordenação multicanal, eventos de reação, validação de fluxo de ponta a ponta e etapas de teste/publicação.
</p>
</td>
<td>
<a href="../using/building-journeys/message-to-subscribers-uc.md">
<img alt="Envie uma mensagem aos assinantes" src="../using/assets/do-not-localize/start-quick.png">
</a>
<div>
<a href="../using/building-journeys/message-to-subscribers-uc.md"><strong>Envie uma mensagem aos assinantes</strong></a>
</div>
<p>
Teste jornadas que direcionem listas de assinaturas com endereçamento de email dinâmico. Valide expressões de personalização para um direcionamento de assinantes correto. Concentre-se em expressões de personalização, endereçamento dinâmico e direcionamento de lista de assinaturas.
</p>
</td>
<td>
<a href="../using/building-journeys/weekday-email-uc.md">
<img alt="Envie mensagens com prazo definido" src="../using/assets/do-not-localize/calendar.jpeg">
</a>
<div>
<a href="../using/building-journeys/weekday-email-uc.md"><strong>Envie mensagens com prazo definido</strong></a>
</div>
<p>
Teste jornadas com condições baseadas em tempo para garantir que as mensagens sejam enviadas em dias específicos. Valide atividades de espera e a lógica de agendamento. Concentre-se em condições baseadas em tempo, atividades de espera e validação de agendamento.
</p>
</td>
</tr></table>

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../using/building-journeys/jo-use-cases.md">
<img alt="Explore mais casos de uso de jornadas" src="../using/assets/do-not-localize/icon-quick-start.svg">
</a>
<div>
<a href="../using/building-journeys/jo-use-cases.md"><strong>Explorar mais casos de uso de jornadas</strong></a>
</div>
<p>
Acesse uma coleção abrangente de exemplos práticos que abordam eventos de experiência, mensagens multicanal e integrações de sistema externas. Explore vários cenários, padrões avançados e abordagens de teste de integração.
</p>
</td>
</tr></table>

## Terminologia principal

Familiarize-se com esses conceitos essenciais de testes para entender melhor os recursos de teste e aprovação do Journey Optimizer. Cada termo está vinculado à documentação detalhada.

**[Perfis de teste](../using/content-management/test-profiles.md)**: perfis de clientes sintéticos (clientes não reais) usados para visualizar conteúdo personalizado. Sinalizado no Serviço de perfil do cliente em tempo real. Exigido para o modo de teste e a visualização de conteúdo. [Saiba como criar perfis de teste](../using/audience/creating-test-profiles.md)

**[Modo de teste](../using/building-journeys/testing-the-journey.md)** - recurso de simulação de jornadas que envia perfis de teste por caminhos de jornada. Limitações: somente jornadas de rascunho, exige namespace, somente perfis de teste. [Consulte a documentação do modo de teste](../using/building-journeys/testing-the-journey.md)

**[Execução de teste](../using/building-journeys/journey-dry-run.md)** - ferramenta de análise de execução de jornada que rastreia caminhos sem enviar mensagens ou fazer chamadas de API. Caso de uso: validar a lógica sem consumir recursos. [Saiba mais sobre a execução de teste](../using/building-journeys/journey-dry-run.md)

**[Dados de entrada de amostra](../using/test-approve/simulate-sample-input.md)** - Arquivos CSV ou JSON contendo valores de atributo de perfil para personalização de testes. Suporta até 30 variantes. Alternativa para a criação de perfis de teste. [Como simular variações de conteúdo](../using/test-approve/simulate-sample-input.md)

**[Listas de seeds](../using/configuration/seed-lists.md)** - Endereços de email de partes interessadas internas incluídos automaticamente em entregas reais (não envios de teste). Somente canal de email. Caso de uso: monitoramento de qualidade e conformidade. [Configure listas de seeds](../using/configuration/seed-lists.md)

**[Experimentos de conteúdo](../using/content-management/get-started-experiment.md)** - Teste A/B ou experimentos multi-armed bandit comparando variações de conteúdo. Somente campanhas, não disponível em jornadas. [Introdução a experimentos](../using/content-management/get-started-experiment.md) | [Criar experimentos](../using/content-management/content-experiment.md)

**[Provas](../using/content-management/proofs.md)** - Teste entregas de email enviadas para endereços de email específicos usando os dados do perfil de teste. É diferente das listas de seeds (provas são envios manuais de teste, listas de seeds são cópias automáticas das partes interessadas). [Envio de provas](../using/content-management/proofs.md)

**[Detecção de conflitos](../using/conflict-prioritization/conflicts.md)** - Ferramenta que identifica campanhas e jornadas sobrepostas direcionadas aos mesmos públicos-alvo. Suporte limitado à jornada: apenas para os tipos unitário, Qualificação de público-alvo e Público-alvo de leitura. [Saiba mais sobre o gerenciamento de conflitos](../using/conflict-prioritization/gs-conflict-prioritization.md)

**[Fluxos de trabalho de aprovação](../using/test-approve/gs-approval.md)** - Processo de revisão em várias etapas que requer a aprovação da parte interessada antes da ativação. Requer configuração de política de aprovação. [Configurar aprovações](../using/test-approve/gs-approval.md) | [Criar políticas](../using/test-approve/approval-policies.md)

**[Testes de renderização](../using/content-management/rendering.md)** - Validação da exibição de email nos clientes de email (Gmail, Outlook, Apple Mail) e dispositivos. Requer integração com Litmus. [Teste a renderização de email](../using/content-management/rendering.md)

**[Playground de personalização](../using/personalization/personalize.md#playground)**: ambiente de aprendizagem interativo para experimentar a sintaxe de personalização e testar expressões com dados de amostra. Não é necessário nenhum conjunto de dados ativo. [Acesse o playground](../using/personalization/personalize.md#playground)

## Recursos adicionais

>[!BEGINTABS]

>[!TAB Guias essenciais]

* [Simular variações de conteúdo](../using/test-approve/simulate-sample-input.md) - Teste até 30 cenários de personalização com arquivos CSV ou JSON. Ideal para testes de conteúdo multilíngue sem precisar criar vários perfis de teste. Compatível com email, SMS, push, web, baseado em código, no aplicativo e cartões de conteúdo.

* [Criação de perfis de teste](../using/audience/creating-test-profiles.md): crie e gerencie perfis de teste para simular cenários do cliente. Saiba como sinalizar perfis para teste, definir atributos e organizar segmentos de teste.

* [Relatório de spam por email](../using/content-management/spam-report.md): verifique as pontuações de spam antes de enviar para melhorar a capacidade de entrega e a taxa de recebimento da caixa de entrada. Obtenha recomendações acionáveis para otimização de conteúdo.

* [Perguntas frequentes sobre jornadas](../using/building-journeys/journey-faq.md): referência rápida para perguntas comuns sobre testes da jornada, execução e solução de problemas.

>[!TAB Dependências e relacionamentos]

Entenda como os recursos de teste conectam-se uns com os outros e com os fluxos de trabalho mais amplos do Journey Optimizer. Esta seção mapeia pré-requisitos, dependências upstream/downstream e combinações de recursos comuns.

+++**Pré-requisitos (necessários antes do teste)**

* Perfis de teste devem ser criados antes do uso do modo de teste ou da visualização de conteúdo
* As políticas de aprovação devem ser configuradas antes do envio para aprovação
* As listas de seeds devem ser criadas antes da adição às campanhas/jornadas
* Integração Litmus necessária para testes de renderização de email
* A jornada deve estar em status de rascunho para usar o modo de teste
* A jornada deve ter o namespace configurado para usar o modo de teste

+++

+++**Do que depende o teste (upstream)**

* Criação de conteúdo: precisa de campanhas ou jornadas para testar
* Perfis de teste: obrigatórios para o modo de teste e a visualização de conteúdo
* Políticas de aprovação: obrigatórias para fluxos de trabalho de aprovação
* Configuração: configurações de canal, autenticação de email, configurações de domínio

+++

+++**O que depende de teste (downstream)**

* Ativação de campanha/jornada: não é possível ativar sem a solução dos erros
* Publicação: a aprovação pode ser necessária antes da publicação
* Monitoramento ao vivo: monitoramento e relatórios pós-lançamento
* Otimização: use os resultados do teste para refinar campanhas futuras

+++

+++**Recursos relacionados**

* Testes + Fluxos de trabalho de aprovação - Processo de controle de qualidade
* Testes + Detecção de conflitos — Evita o excesso de mensagens enviadas ao cliente
* Testes + Experimentos de conteúdo - Otimização do desempenho
* Testes + Relatórios - Ciclo de melhoria contínua
* Perfis de teste + Personalização - Validação de conteúdo
* Execução de teste + Modo de teste - Validação abrangente de jornada

+++

+++**Combinações comuns de recursos**

* Teste de conteúdo: Perfis de teste + Dados de entrada de amostra + Playground de personalização
* Validação de email: Testes de renderização + Pontuações de spam + Perfis de teste + Provas
* Validação de jornada: Modo de teste + Execução de teste + Perfis de teste
* Lista de verificação de pré-lançamento: Todos os testes técnicos + Detecção de conflitos + Fluxos de trabalho de aprovação

+++

>[!TAB Perguntas comuns]

+++**P: Quais são os testes necessários antes de iniciar uma campanha?**

**Mínimo:** Visualização de conteúdo com perfis de teste + Verificação de pontuação de spam (email)
**Recomendado:** + Renderização de email + Detecção de conflitos + Fluxo de trabalho de aprovação
**Prática recomendada:** + Teste de dados de entrada de amostra + Listas de seeds + Experimento A/B (se estiver otimizando)

+++

+++**P: Como faço para testar a personalização sem criar muitos perfis de teste?**

**Solução primária:** use [dados de entrada de amostra](../using/test-approve/simulate-sample-input.md) com arquivos CSV/JSON (suporta até 30 variantes)
**Alternativa:** crie de 3 a 5 [perfis de teste](../using/audience/creating-test-profiles.md) representativos que abrangem segmentos chave
**Ferramenta de aprendizado:** experimente primeiro no [playground de personalização](../using/personalization/personalize.md#playground)

+++

+++**P: Qual é a diferença entre o modo de teste e a execução de teste nas jornadas?**

**Modo de teste:** envia perfis de teste por meio da jornada, aciona ações reais e gera mensagens de teste. Requer jornada de rascunho + namespace.
**Execução de teste:** rastreia caminhos de execução sem enviar nada. Funciona em qualquer status de jornada. Nenhuma mensagem enviada, nenhuma ação executada.
**Use em conjunto:** Modo de teste para teste de mensagem + Execução de teste para validação de lógica - cobertura abrangente.

+++

+++**P: Posso testar jornadas no status produção/ativa?**

**Modo de teste:** não - somente jornadas de rascunho
**Execução de teste:** sim - funciona em qualquer status de jornada
**Visualização de conteúdo:** sim - visualize mensagens individuais a qualquer momento
**Solução alternativa:** duplique a jornada ativa como rascunho para validação completa no modo de teste

+++

+++**P: Quais recursos de teste exigem integrações externas?**

**Renderização de email:** requer integração Litmus (licença separada)
**Todos os outros:** integrado ao Journey Optimizer, sem a exigência de integrações adicionais
**Observação:** perfis de teste exigem o Serviço de perfil do cliente em tempo real (incluído)

+++

+++**P: Como testar campanhas acionadas por API?**

**Opção 1:** Use a [API de simulação de campanha](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target-&quot;_blank&quot;} para testes programáticos
**Opção 2:** Visualize conteúdo com perfis de teste na interface
**Opção 3:** Envie provas para testar endereços de email
**Prática recomendada:** combine todos os três para obter uma validação abrangente

+++

>[!ENDTABS]
