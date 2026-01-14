---
solution: Journey Optimizer
product: journey optimizer
title: Introdução às jornadas
description: Introdução às jornadas - Saiba mais sobre os tipos de jornada, fluxo de trabalho, recursos e práticas recomendadas para criar experiências do cliente personalizadas no Adobe Journey Optimizer
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: jornada, descobrir, introdução, unitário, público-alvo de leitura, qualificação de público-alvo, evento de negócios, tempo real, agendada, em lote, acionada por evento, fluxo de trabalho, orquestração, personalização, multicanal
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
version: Journey Orchestration
source-git-commit: 522dba0516268a17e72f56c0f28205ba60709d78
workflow-type: ht
source-wordcount: '1448'
ht-degree: 100%

---


# Introdução às jornadas{#jo-general-principle}

O Adobe Journey Optimizer permite criar jornadas do cliente personalizadas e de várias etapas que se adaptam em tempo real ao comportamento e às necessidades do público-alvo. Com uma tela intuitiva de arrastar e soltar, é possível orquestrar mensagens e ações em vários canais, aproveitando dados contextuais e o direcionamento de público-alvo para obter o máximo impacto. 

Este guia fornece um roteiro claro para ajudar a entender os fundamentos da jornada, escolher o tipo de jornada certo para o caso de uso e criar com confiança jornadas que proporcionem experiências ao cliente significativas e oportunas.

## O que são jornadas?

As **jornadas** são experiências do cliente automatizadas e em várias etapas que orquestram interações personalizadas entre canais em resposta ao comportamento do cliente, eventos de negócios ou campanhas programadas.

Use [!DNL Journey Optimizer] para:

* Crie casos de uso de **orquestração em tempo real** com dados contextuais armazenados em eventos ou fontes de dados 
* Projete **cenários avançados com várias etapas** que respondam dinamicamente ao comportamento do cliente e aos eventos de negócios
* Forneça **1:1 experiências personalizadas** em grande escala com email, push, SMS, no aplicativo, web e muito mais

![Interface do designer de jornadas com paleta, tela e painel de propriedades](assets/journey38.png)

➡️ **Pronto para começar a criar?** [Crie sua primeira jornada](journey-gs.md) em 5 minutos.

### Jornadas vs. campanhas: quando usar cada uma {#journeys-vs-campaigns-intro}

O Adobe Journey Optimizer oferece três abordagens para alcançar os clientes: **Jornadas** (1:1 orquestração em tempo real), **Campanhas** (entrega simples em lote ou acionada por API) e **Campanhas orquestradas** (fluxos de trabalho de tela em lote com dados de várias entidades).

**Decisão rápida:**

* Use as **Jornadas** para experiências em várias etapas orientadas por comportamento em que cada cliente avança no seu próprio ritmo
* Use **Campanhas de ação/API** para a entrega de mensagens simples, agendada ou acionada aos públicos-alvo
* Use **Campanhas orquestradas** para fluxos de trabalho em lote complexos que exigem segmentação de várias entidades e contagens exatas de pré-envio

<!-- waiting for DOCAC-13912
➡️ **[View detailed comparison: Journeys vs Campaigns](../start/journeys-vs-campaigns.md)** - Includes decision guide, use cases, and feature availability-->

## Escolha seu tipo de jornada {#journey-types}

O Adobe Journey Optimizer oferece suporte a quatro tipos de jornada, cada um projetado para diferentes mecanismos de entrada e cenários de negócios:

* **Jornadas unitárias**: experiências acionadas por eventos em tempo real (confirmações de pedidos, emails de boas-vindas)
* **Jornadas de público-alvo de leitura**: comunicações em lote agendadas para segmentos de público-alvo (informativos, campanhas promocionais)
* **Jornadas de qualificação de público-alvo**: respostas em tempo real a alterações de associação de público-alvo (atualizações do VIP, reengajamento)
* **Jornadas de evento de negócios**: condições de negócio que afetam vários clientes (alertas de estoque, promoções)

<!-- waiting for DOCAC-13912 
➡️ **[Journey types and selection guide](journey-types-selection.md)** - Detailed comparison, decision tree, and feature compatibility matrix -->

## Criar com o designer de jornadas {#journey-designer}

O **[designer de jornadas](using-the-journey-designer.md)** é a tela visual para criar experiências do cliente. Com uma interface intuitiva de arrastar e soltar, é possível orquestrar cada etapa da jornada sem escrever código.

![Interface do designer de jornadas com paleta, tela e painel de propriedades](assets/journey38.png)

### O que você pode fazer no designer:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=pt-BR)

**Definir pontos de entrada**

Escolha como os clientes entram: por meio de um evento, segmento de público-alvo ou qualificação de público-alvo.

[Saiba mais sobre o gerenciamento da entrada](entry-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=pt-BR)

**Envio de mensagens**

Use ações de canal integradas para email, push, SMS/MMS, no aplicativo, web e mais. Tudo isso criado no Journey Optimizer.

[Enviar mensagens nas jornadas](journeys-message.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=pt-BR)

**Adicionar lógica e condições**

Ramifique a jornada com base em atributos de perfil, na associação de público-alvo ou em eventos em tempo real.

[Condições de uso](condition-activity.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=pt-BR)

**Aproveitar dados**

Use dados contextuais de eventos, da Adobe Experience Platform ou de serviços de API de terceiros.

[Trabalhar com fontes de dados](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=pt-BR)

**Conectar sistemas externos**

Crie ações personalizadas para integrar sistemas de terceiros e enviar mensagens ou acionar fluxos de trabalho.

[Configurar ações personalizadas](../action/about-custom-action-configuration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=pt-BR)

**Adicionar atividades de orquestração**

Use tempos de espera, saltos, atualizações de perfil e o gerenciamento de público-alvo para criar fluxos sofisticados.

[Explorar todas as atividades](about-journey-activities.md)
:::

::::

➡️ **Aprendizado prático:** [assista ao vídeo do designer de jornadas](#video) ou [explore casos de uso de ponta a ponta](jo-use-cases.md)

## Seu fluxo de trabalho de criação de jornadas {#workflow}

A criação de jornadas bem-sucedidas segue um processo claro que pode ser repetido. Este é o fluxo de trabalho passo a passo:

**1. Plano** → **2. Projeto** → **3. Teste** → **4. Publicar** → **5. Monitorar** → **6. Otimizar**

### &#x200B;1. Planeje a jornada {#plan}

Antes de abrir o designer, esclareça os objetivos:

* **Qual é a meta?** (por exemplo: integrar novos clientes, reengajar usuários inativos)
* **Quem é o público-alvo?** (segmento específico, pessoas orientadas por eventos)
* **Qual tipo de jornada se encaixa?** (Consulte os [tipos de jornada](#journey-types) acima)
* **Quais canais você usará?** (email, push, SMS, etc.)

### &#x200B;2. Projete na tela {#design}

Use o designer de jornadas para criar o fluxo:

* **Definir condições de entrada**: defina como os perfis entram (evento, público-alvo, qualificação)
* **Adicionar lógica de orquestração** - Inclua tempos de espera, condições e pontos de decisão
* **Configurar mensagens** - Projete as comunicações ou use modelos existentes
* **Configurar ações**: configure ações integradas ou personalizadas para execução
* **Definir critérios de saída** - Especifique quando e como os perfis concluem a jornada

[Saiba como usar o designer de jornadas →](using-the-journey-designer.md)

### &#x200B;3. Teste antes de ativar {#test}

Sempre teste a jornada para detectar problemas antes que os clientes os enfrentem:

* Use o **modo de teste** para simular a jornada com perfis de teste
* Use a **execução de teste** para visualizar a execução da jornada sem afetar os dados reais ou enviar mensagens
* Verifique se todas as condições, mensagens e ações funcionam conforme esperado
* Verifique o momento, os fluxos de dados e a personalização

[Teste a jornada →](testing-the-journey.md) | [Saiba mais sobre a execução de teste →](journey-dry-run.md)

### &#x200B;4. Publique a jornada {#publish}

Quando o teste for concluído, publique para ativar a jornada:

* Revise as configurações e as propriedades finais
* Publique para ativar para clientes reais
* Observação: as jornadas ativas podem ser interrompidas, mas não editadas (é necessário criar uma nova versão)

[Publique a jornada →](publish-journey.md)

### &#x200B;5. Monitore o desempenho {#monitor}

Rastreie o desempenho da jornada no mundo real:

* Visualize relatórios e análises da jornada
* Monitore as taxas de entrada, conclusão e erro
* Defina alertas para problemas críticos

[Monitorar e relatar →](report-journey.md) | [Configurar alertas →](../reports/alerts.md)

### &#x200B;6. Otimizar e iterar {#optimize}

Use insights para aprimorar:

* Analise métricas de engajamento e taxas de conversão
* Teste otimização de tempo de envio
* Crie novas versões da jornada com melhorias
* Use recomendações viabilizadas por IA

[Otimize as jornadas →](optimize.md) | [Otimização do tempo de envio →](send-time-optimization.md)

➡️ **Pronto(a) para começar?** [Crie sua primeira jornada agora →](journey-gs.md)

## Casos de uso reais {#use-cases}

Aprenda com exemplos práticos que demonstram como aplicar os conceitos da jornada para resolver desafios de marketing comuns:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=pt-BR)

**Dê boas-vindas a novos assinantes**

Quando um cliente assinar o serviço, acione uma jornada de boas-vindas que o incentive a concluir as etapas de integração.

[Exibir caso de uso →](message-to-subscribers-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg?lang=pt-BR)

**Otimização de tempo de envio**

Use a IA para enviar emails quando cada cliente tiver uma maior probabilidade de engajamento, maximizando as taxas de abertura e de clique.

[Exibir caso de uso →](send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=pt-BR)

**Incrementar entregas**

Aumente gradualmente o volume de mensagens para aquecer a reputação de envio e evitar problemas com a capacidade de entrega.

[Exibir caso de uso →](ramp-up-deliveries-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=pt-BR)

**Direcionar por dia da semana**

Envie conteúdos diferentes com base no dia da semana em que os clientes entram na jornada para maior relevância.

[Exibir caso de uso →](weekday-email-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=pt-BR)

**Campanhas multicanal**

Orquestre experiências fluidas nos canais de email, push, SMS e web em uma única jornada.

[Exibir caso de uso →](journeys-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=pt-BR)

**Todos os casos de uso**

Explore a biblioteca completa de casos de uso da jornada com implementações passo a passo.

[Procurar todos →](jo-use-cases.md) | [Biblioteca de casos de uso →](/help/rp_landing_pages/journey-use-cases-landing-page.md)
:::

::::

## Explore os recursos da jornada {#capabilities}

À medida que se sentir mais confortável com a criação de jornadas, explore esses recursos avançados para criar experiências do cliente sofisticadas:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=pt-BR)

**Expressões avançadas**

Crie condições dinâmicas e personalização com o editor de expressão para manipulação de dados e lógica complexa.

[Saiba mais sobre expressões](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg?lang=pt-BR)

**Gerenciamento de fuso horário**

Lide com os públicos-alvo globais com ajustes automáticos de fuso horário e tempos de envio ideais.

[Gerenciar fusos horários](timezone-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=pt-BR)

**Modo de teste e execução de teste**

Valide jornadas com perfis de teste antes de ativá-las e visualize a execução sem afetar os dados reais.

[Use a execução de teste](journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=pt-BR)

**Copiar para a sandbox**

Duplique jornadas em sandboxes para simplificar os fluxos de trabalho de teste e implantação.

[Copie jornadas](copy-to-sandbox.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=pt-BR)

**Tags e organização**

Use tags para categorizar e filtrar jornadas, melhorando o gerenciamento em grande escala.

[Organize com tags](tags.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=pt-BR)

**Controle da taxa de transferência**

Limite a taxa de transferência de mensagens para gerenciar a reputação de envio e evitar a sobrecarga dos sistemas.

[Controle a taxa de transferência](limit-throughput.md)
:::

::::

[Visualizar todos os recursos da jornada →](/help/rp_landing_pages/manage-journey-landing-page.md)

## Saiba mais assistindo {#video}

Obtenha uma introdução visual aos componentes da jornada e conheça as noções básicas para criar jornadas na tela:

>[!VIDEO](https://video.tv.adobe.com/v/3430346?captions=por_br&quality=12)

➡️ **Quer mais vídeos?** [Explore tutoriais em vídeo para a jornada](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}

## Perguntas comuns {#common-questions}

+++ Qual é a diferença entre uma jornada e uma campanha?

O Adobe Journey Optimizer oferece três abordagens:

* **Jornadas**: 1:1 orquestração em tempo real em que cada perfil percorre as etapas no seu próprio ritmo. A melhor opção para experiências orientadas por comportamento em várias etapas com lógica condicional (por exemplo: integração, abandono de carrinho).

* **Campanhas (ação e acionadas por API)**: entrega simples de mensagens a públicos-alvo, com execução simultânea para todos os perfis, por meio de um cronograma ou do acionador da API. A melhor opção para campanhas promocionais, informativos e mensagens transacionais.

* **Campanhas orquestradas**: fluxos de trabalho em lotes de várias etapas com segmentação complexa usando dados relacionais (perfis + produtos/lojas/reservas). Todos os perfis processados juntos, com as contagens exatas de pré-envio. A melhor opção para promoções sazonais, lançamentos de produtos e campanhas que exigem dados de várias entidades.

**Principais diferenças**: as jornadas mantêm o estado individual do cliente para ações em tempo real. As Campanhas de ação/API fornecem mensagens simples em lote. As Campanhas orquestradas fornecem telas de fluxo de trabalho em lote com recursos de segmentação de várias entidades.

<!-- waiting for DOCAC-13912 - [See detailed comparison](#journeys-vs-campaigns) -->
[Saiba mais sobre Campanhas orquestradas](../orchestrated/gs-orchestrated-campaigns.md)

+++

<!-- Waiting for DOCAC-13912
+++ Which journey type should I use?

Use the [decision guide](#decision-guide) or [comparison table](#journey-types-comparison) to choose between Unitary, Read Audience, Audience Qualification, and Business Event journeys based on your trigger mechanism and use case.

+++
-->

+++ Posso editar uma jornada em tempo real?

É possível editar elementos limitados (nome, conteúdo da mensagem), mas alterações estruturais exigem a criação de uma nova versão. [Saiba mais sobre as versões da jornada](publish-journey.md#journey-versions)

+++

➡️ **Mais perguntas?** [Visualize todas as perguntas frequentes sobre jornadas](journey-faq.md) com mais de 40 respostas detalhadas

## Precisa de ajuda? {#help}

### Links rápidos para tarefas comuns

* **[Crie sua primeira jornada](journey-gs.md)** - Guia passo a passo para iniciantes
* **[Perguntas frequentes sobre jornadas](journey-faq.md)** - Perguntas comuns respondidas
* **[Solução de problemas](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)** - Diagnosticar e corrigir problemas
* **[Referência de códigos de erro](error-codes-reference.md)** - Compreenda as mensagens de erro
* **[Medidas de proteção e limitações](../start/guardrails.md)** - Limites técnicos e práticas recomendadas

### Receber notificações sobre problemas

Configure os **[alertas da jornada](../reports/alerts.md)** para receber notificações em tempo real quando as jornadas encontram erros ou padrões incomuns.

### Recursos adicionais

* **[Hub de gerenciamento de jornadas](/help/rp_landing_pages/manage-journey-landing-page.md)** - Ferramentas de filtragem, otimização e gerenciamento de perfil
* **[Referência das atividades da jornada](/help/rp_landing_pages/about-journey-building-landing-page.md)** - Guia completo para todos os tipos de atividades
* **[Solução de problemas de execução](troubleshooting-execution.md)** - Depurar problemas de execução da jornada
* **[Solução de problemas de atividades de entrada](troubleshooting-inbound.md)** - Corrigir problemas de entrada e qualificação

**Pronto(a) para criar sua primeira jornada?** [Comece agora →](journey-gs.md)
