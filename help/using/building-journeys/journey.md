---
solution: Journey Optimizer
product: journey optimizer
title: Introdução às jornadas
description: 'Introdução às jornadas: saiba mais sobre os tipos de jornada, fluxo de trabalho, recursos e práticas recomendadas para criar experiências do cliente personalizadas no [!DNL Adobe Journey Optimizer]'
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: jornada, descobrir, introdução, unitário, público-alvo de leitura, qualificação de público-alvo, evento de negócios, tempo real, agendada, em lote, acionada por evento, fluxo de trabalho, orquestração, personalização, multicanal
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/FsZLMlzVj6CcTqVp9BPUmiCf2piZL8zaj2WfWv8FMSQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: b15c7c2e-788c-4eb7-86a8-390565b0d2c9
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: fa683eda-48de-4558-af32-2673edcd44fe
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 6f35d9b951850220382e3662502b9e1d7ad6b990
workflow-type: tm+mt
source-wordcount: 2278
ht-degree: 70%

---

# Introdução às jornadas {#jo-general-principle}

>[!BEGINSHADEBOX]

**Nesta página:** conheça os fundamentos das jornadas no Adobe Journey Optimizer, incluindo os tipos de jornadas, o fluxo de trabalho de design, os principais recursos e as práticas recomendadas para criar experiências personalizadas do cliente.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_canvas"
>title="Criar uma jornada"
>abstract="A tela de arrastar e soltar orquestra mensagens e ações em vários canais, aproveitando dados contextuais e direcionamento de público-alvo para maximizar o impacto."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/orchestrate-journeys/create-journey/journey-gs" text="Criar a primeira jornada"


O [!DNL Adobe Journey Optimizer] permite criar jornadas de clientes personalizadas e com várias etapas, que se adaptam em tempo real ao comportamento e às necessidades do seu público-alvo. Com uma tela intuitiva de arrastar e soltar, é possível orquestrar mensagens e ações em vários canais, aproveitando dados contextuais e o direcionamento de público-alvo para obter o máximo impacto.

Este guia fornece um roteiro claro para ajudar a entender os fundamentos da jornada, escolher o tipo de jornada certo para o caso de uso e criar com confiança jornadas que proporcionem experiências ao cliente significativas e oportunas.

## O que são jornadas?

As **jornadas** são experiências do cliente automatizadas e em várias etapas que orquestram interações personalizadas entre canais em resposta ao comportamento do cliente, eventos de negócios ou campanhas programadas.

Use [!DNL Journey Optimizer] para:

* Crie casos de uso de **orquestração em tempo real** com dados contextuais armazenados em eventos ou fontes de dados
* Projete **cenários avançados com várias etapas** que respondam dinamicamente ao comportamento do cliente e aos eventos de negócios
* Forneça **1:1 experiências personalizadas** em grande escala com email, push, SMS, no aplicativo, web e muito mais

![Interface do designer de jornadas com paleta, tela e painel de propriedades](assets/journey38.png)

➡️ **Tudo pronto para começar a criar?** [Crie sua primeira jornada](journey-gs.md) em 5 minutos.

### Jornadas vs. campanhas: quando usar cada uma {#journeys-vs-campaigns-intro}

O [!DNL Adobe Journey Optimizer] oferece três abordagens para alcançar os clientes: **jornadas** (1:1 orquestração em tempo real), **campanhas** (entrega simples em lote ou acionada por API) e **campanhas orquestradas** (fluxos de trabalho de tela em lote com dados de várias entidades).

**Decisão rápida:**

* Use as **Jornadas** para experiências em várias etapas orientadas por comportamento em que cada cliente avança no seu próprio ritmo
* Use **campanhas acionadas por ação e API** para entrega de mensagens simples, agendadas ou acionadas para públicos-alvo
* Use **Campanhas orquestradas** para fluxos de trabalho em lote complexos que exigem segmentação de várias entidades e contagens exatas antes do envio

<!--
 waiting for DOCAC-13912
➡️ **[View detailed comparison: Journeys vs Campaigns](../start/journeys-vs-campaigns.md)** - Includes decision guide, use cases, and feature availability
-->

## Escolha seu tipo de jornada {#journey-types}

O [!DNL Adobe Journey Optimizer] aceita quatro tipos de jornada, cada um projetado para diferentes mecanismos de entrada e cenários de negócios:

* **jornadas unitárias**: experiências acionadas por eventos em tempo real (recuperação de abandono de carrinho, emails de boas-vindas)
* **Jornadas de público-alvo de leitura**: comunicações em lote agendadas para segmentos de público-alvo (informativos, campanhas promocionais)
* **Jornadas de qualificação de público-alvo**: respostas em tempo real a alterações de associação de público-alvo (atualizações do VIP, reengajamento)
* **Jornadas de evento de negócios**: condições de negócio que afetam vários clientes (alertas de estoque, promoções)

<!--
 waiting for DOCAC-13912 
➡️ **[Journey types: choose the right one](journey-types-selection.md)** - Detailed comparison, decision guide, and feature compatibility matrix 
-->

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

Use ações de canal integradas para email, push, SMS/MMS, no aplicativo, web, entre outros. Tudo isso criado no Journey Optimizer.

[Enviar mensagens nas jornadas](journey-action.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=pt-BR)

**Adicionar lógica e condições**

Ramifique a jornada com base em atributos de perfil, na associação de público-alvo ou em eventos em tempo real.

[Condições de uso](conditions.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=pt-BR)

**Aproveitar dados**

Use dados contextuais de eventos, a [!DNL Adobe Experience Platform] ou serviços de API de terceiros.

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

### &#x200B;1. Planejar a jornada {#plan}

Antes de abrir o designer, esclareça os objetivos:

* **Qual é a meta?** (por exemplo: integrar novos clientes, reengajar usuários inativos)
* **Quem é o público-alvo?** (segmento específico, pessoas orientadas por eventos)
* **Qual tipo de jornada se aplica?** (Consulte [tipos de jornada](#journey-types) acima)
* **Quais canais você pode usar?** (email, push, SMS, etc.)

### &#x200B;2. Projetar na tela {#design}

Use o designer de jornadas para criar o fluxo:

* **Definir condições de entrada**: defina como os perfis entram (evento, público-alvo, qualificação)
* **Adicionar lógica de orquestração** - Inclua tempos de espera, condições e pontos de decisão
* **Configurar mensagens** - Projete as comunicações ou use modelos existentes
* **Configurar ações**: configure ações integradas ou personalizadas para execução
* **Definir critérios de saída** - Especifique quando e como os perfis concluem a jornada

[Saiba como usar o designer de jornadas →](using-the-journey-designer.md)

### &#x200B;3. Testar antes de ativar {#test}

Sempre teste a jornada para detectar problemas antes que os clientes os enfrentem:

* Use o **modo de teste** para simular a jornada com perfis de teste
* Use a **execução de teste** para visualizar a execução da jornada sem afetar os dados reais ou enviar mensagens
* Verifique se todas as condições, mensagens e ações funcionam conforme esperado
* Verifique o momento, os fluxos de dados e a personalização

[Teste a jornada →](testing-the-journey.md) | [Saiba mais sobre a execução de teste →](journey-dry-run.md)

### &#x200B;4. Publicar a jornada {#publish}

Quando o teste for concluído, publique para ativar a jornada:

* Revise as configurações e as propriedades finais
* Publique para ativar para clientes reais
* Observação: as jornadas ativas podem ser interrompidas, mas não editadas (é necessário criar uma nova versão)

[Publique a jornada →](publish-journey.md)

### &#x200B;5. Monitorar o desempenho {#monitor}

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

➡️ **Tudo pronto para começar?** [Crie sua primeira jornada agora →](journey-gs.md)

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

[Procurar todos →](jo-use-cases.md) | [Biblioteca de casos de uso →](../../rp_landing_pages/journey-use-cases-landing-page.md)
:::

::::

## Explore os recursos da jornada {#capabilities}

À medida que se sentir mais confortável com a criação de jornadas, explore esses recursos avançados para criar experiências do cliente sofisticadas:

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=pt-BR)

**Expressões avançadas**

Crie condições dinâmicas e personalização com o editor de expressão para manipulação de dados e lógica complexa.

[Saiba mais sobre expressões](../../rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
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

[Copie jornadas](../configuration/copy-objects-to-sandbox.md#objects)
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

[Visualizar todos os recursos da jornada →](../../rp_landing_pages/manage-journey-landing-page.md)

## Saiba mais assistindo {#video}

Obtenha uma introdução visual aos componentes da jornada e conheça as noções básicas para criar jornadas na tela:

>[!VIDEO](https://video.tv.adobe.com/v/3430346?captions=por_br&quality=12)

➡️ **Quer mais vídeos?** [Explore tutoriais em vídeo sobre jornadas](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}

## Perguntas comuns {#common-questions}

+++ Qual é a diferença entre uma jornada e uma campanha?

O [!DNL Adobe Journey Optimizer] oferece três abordagens:

* **Jornadas**: 1:1 orquestração em tempo real em que cada perfil percorre as etapas no seu próprio ritmo. A melhor opção para experiências orientadas por comportamento em várias etapas com lógica condicional (por exemplo: integração, abandono de carrinho).

* **Campanhas (ação e acionadas por API)**: entrega simples de mensagens a públicos-alvo, com execução simultânea para todos os perfis, por meio de um cronograma ou do acionador da API. A melhor opção para campanhas promocionais, informativos e mensagens transacionais.

* **Campanhas orquestradas**: fluxos de trabalho em lote de várias etapas com segmentação complexa usando dados relacionais (perfis + produtos/lojas/reservas). Todos os perfis processados juntos, com as contagens exatas de pré-envio. A melhor opção para promoções sazonais, lançamentos de produtos e campanhas que exigem dados de várias entidades.

**Diferença principal**: as jornadas mantêm o estado individual do cliente em ações em tempo real; campanhas acionadas por ação e API entregam mensagens simples em lote; campanhas orquestradas fornecem tela de fluxo de trabalho em lote com recursos de segmentação de várias entidades.

<!-- waiting for DOCAC-13912 - [See detailed comparison](#journeys-vs-campaigns) -->
[Saiba mais sobre Campanhas orquestradas](../orchestrated/gs-orchestrated-campaigns.md)

+++

<!--
 Waiting for DOCAC-13912
+++ Which journey type should I use?

Use the [decision guide](#decision-guide) or [comparison table](#journey-types-comparison) to choose between Unitary, Read Audience, Audience Qualification, and Business Event journeys based on your trigger mechanism and use case.

+++
-->

+++ Posso editar uma jornada em tempo real?

É possível editar elementos limitados (nome, conteúdo da mensagem), mas alterações estruturais exigem a criação de uma nova versão. [Saiba mais sobre as versões da jornada](publish-journey.md#journey-versions)

+++

➡️ **Mais perguntas?** [Confira as Perguntas frequentes completas sobre jornadas](journey-faq.md), que contêm mais de 40 respostas detalhadas

## Precisa de ajuda? {#help}

Use estes links para obter orientação, solução de problemas e recursos.

### Links rápidos para tarefas comuns

* **[Crie sua primeira jornada](journey-gs.md)** - Guia passo a passo para iniciantes
* **[Perguntas frequentes sobre jornadas](journey-faq.md)** - Perguntas comuns respondidas
* **[Solução de problemas](../../rp_landing_pages/troubleshoot-journey-landing-page.md)** - Diagnosticar e corrigir problemas
* **[Referência de códigos de erro](error-codes-reference.md)** - Compreenda as mensagens de erro
* **[Medidas de proteção e limitações](../start/guardrails.md)** - Limites técnicos e práticas recomendadas

### Receber notificações sobre problemas

Configure os **[alertas da jornada](../reports/alerts.md)** para receber notificações em tempo real quando as jornadas encontram erros ou padrões incomuns.

### Recursos adicionais

* **[Hub de gerenciamento de jornadas](../../rp_landing_pages/manage-journey-landing-page.md)** - Ferramentas de filtragem, otimização e gerenciamento de perfil
* **[Referência das atividades da jornada](../../rp_landing_pages/about-journey-building-landing-page.md)** - Guia completo para todos os tipos de atividades
* **[Solução de problemas de execução](troubleshooting-execution.md)** - Depurar problemas de execução da jornada
* **[Solução de problemas de atividades de entrada](troubleshooting-inbound.md)** - Corrigir problemas de entrada e qualificação

**Tudo pronto para criar a primeira jornada?** [Comece agora →](journey-gs.md)

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** Esta página é o hub de introdução para o Adobe Journey Optimizer jornada, explicando quais são as jornadas, os quatro tipos de jornadas, o fluxo de trabalho de criação em seis etapas, casos de uso reais e links para recursos avançados.

**Intenções:**

* Entenda o que são jornadas e como elas se diferem de campanhas e campanhas orquestradas
* Escolha o tipo de jornada correto (Unitário, Público de leitura, Qualificação de público ou Evento comercial) para um caso de uso
* Siga o fluxo de trabalho de criação de jornadas de seis etapas: Planejar, Projetar, Testar, Publicar, Monitorar, Otimizar
* Use Simulação, Modo de teste ou Dry run para validar uma jornada antes de entrar em funcionamento
* Publicar uma jornada e monitorar o desempenho por meio de relatórios e alertas
* Explore recursos avançados como expressões, gerenciamento de fuso horário, cópia para sandbox e controle de taxa de transferência

**Glossário:**

* **Jornada**: uma experiência de cliente automatizada, em várias etapas, que orquestra interações personalizadas entre canais em resposta ao comportamento do cliente, eventos comerciais ou campanhas agendadas. *(específico do produto)*
* **Designer de Jornadas**: a tela visual de arrastar e soltar do AJO usada para compilar e configurar fluxos de jornada sem gravar código. *(específico do produto)*
* **Modo de teste**: um modo de validação de jornada que usa perfis de teste persistentes do Adobe Experience Platform (explicitamente sinalizados como perfis de teste) para percorrer uma jornada de rascunho antes de ser publicada. *(específico do produto)*
* **Dry run**: um modo de publicação especial que executa a jornada em dados de produção reais sem enviar comunicações ou atualizar perfis. *(específico do produto)*
* **Simulação**: um modo de validação que usa usuários temporários simulados gerados em tempo real; os usuários simulados não persistem no Adobe Experience Platform. *(específico do produto)*
* **Campanhas orquestradas**: fluxos de trabalho em lotes de várias etapas na AJO que usam dados relacionais (perfis + produtos/lojas/reservas) e processam todos os perfis junto com contagens exatas de pré-envio. *(específico do produto)*

**Medidas de Proteção:**

* O Live jornada não pode ser editado estruturalmente; as alterações exigem a criação de uma nova versão
* O modo de teste e a simulação devem ser usados antes da publicação para detectar problemas

**Terminologia:**

* Nome canônico: Jornada — Acrônimo: nenhum — variantes: jornada do cliente, jornada do AJO
* Sinônimos: &quot;Designer de jornada&quot; = &quot;tela&quot; = &quot;tela de jornada&quot;
* Não confunda: &quot;Jornada&quot; ≠ &quot;Campaign&quot; — As Jornadas mantêm o estado individual do cliente para experiências em tempo real e orientadas por comportamento em várias etapas; as campanhas entregam mensagens em lote para os públicos-alvo de acordo com um agendamento ou por meio do acionador da API
* Não confunda: &quot;Simulation&quot; ≠ &quot;Test mode&quot; ≠ &quot;Dry run&quot; — A simulação usa usuários temporários simulados; O modo de teste usa perfis de teste persistentes do AEP em uma jornada de rascunho; O Dry run é executado em relação aos dados reais de produção sem entrar em contato com os clientes ou atualizar os perfis

**Perguntas frequentes:**

* **P: Qual é a diferença entre uma jornada e uma campanha no Journey Optimizer?** — o Jornada fornece 1:1 orquestração em tempo real, onde cada perfil avança em seu próprio ritmo por meio da lógica condicional; Campanhas entregam mensagens simultaneamente a um público de acordo com um agendamento ou por meio de um acionador de API; campanhas orquestradas são fluxos de trabalho de tela em lote para segmentação complexa de várias entidades.
* **P: Posso editar uma jornada em tempo real?** — elementos limitados, como nome e conteúdo da mensagem, podem ser editados; mudanças estruturais exigem a criação de uma nova versão da jornada.
* **P: Quais são as etapas para criar uma jornada?** — O fluxo de trabalho de seis etapas é: planejar, projetar na tela, testar (modo de teste ou simulação), publicar, monitorar o desempenho e otimizar/iterar.
* **P: Como validar uma jornada sem enviar mensagens reais?** — use Simulação (usuários temporários simulados), Modo de teste (perfis de teste persistentes do AEP) ou Dry run (dados reais de produção sem contato com o cliente ou atualizações de perfil). A contagem de perfis de execuções secas para Perfis ativáveis e cota de jornada ativa.
* **P: Que tipo de jornada devo usar para um email de boas-vindas acionado por uma assinatura?** — Use uma jornada Unitária, que é acionada por um evento individual específico, como uma inscrição por assinatura.

+++
