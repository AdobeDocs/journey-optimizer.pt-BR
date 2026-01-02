---
solution: Journey Optimizer
product: journey optimizer
title: Journey Orchestration - Guia completo
description: Guia abrangente para começar a usar a orquestração de jornadas no Adobe Journey Optimizer
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
keywords: jornada, orquestração, introdução, integração, recursos
source-git-commit: d1fd0b60ae60c2642108a1eb308564c9d04f5f9e
workflow-type: tm+mt
source-wordcount: '851'
ht-degree: 47%

---


# Journey Orchestration - Guia completo{#journey-orchestration-guide}

As jornadas no Adobe Journey Optimizer permitem criar jornadas personalizadas e de várias etapas para o cliente que se adaptam em tempo real ao comportamento e às necessidades do seu público-alvo. Usando uma tela intuitiva de arrastar e soltar, você pode orquestrar mensagens e ações em vários canais, aproveitando dados contextuais e o direcionamento de público-alvo para obter o máximo impacto.

Quer você esteja explorando acionadores em tempo real, gerenciando propriedades do jornada ou usando ferramentas avançadas como ações e expressões personalizadas, este guia fornece um roteiro claro para projetar e refinar com confiança jornadas que proporcionem experiências relevantes e oportunas ao cliente.

## O que são jornadas?

Use o [!DNL Journey Optimizer] para criar casos de uso de orquestração em tempo real usando dados contextuais armazenados em eventos ou fontes de dados. Crie cenários avançados com várias etapas que respondam ao comportamento do cliente e aos eventos comerciais em tempo real.

O designer de jornadas do Journey Optimizer oferece tudo que profissionais de marketing e de jornadas precisam para orquestrar jornadas 1:1 de várias etapas nos canais. Isso inclui uma tela intuitiva com interface de arrastar e soltar para criar cada etapa da jornada, definir o público-alvo e incluir as mensagens, ofertas e conteúdo nos canais que os membros do público-alvo verão com base no comportamento, nos dados contextuais e nos eventos de negócios.

![Interface do designer do Jornada com paleta, tela e painel de propriedades](assets/journey38.png)

**Pronto para começar a criar?** Saiba como criar e projetar sua primeira jornada nesta [página](journey-gs.md).


## Principais recursos {#capabilities}

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=pt-BR)

**Entrega em lote e em tempo real**

Envie uma **entrega unitária** em tempo real acionada quando um evento é recebido, ou **em lote** usando os públicos-alvo da Adobe Experience Platform.

[Saiba mais sobre entrada de jornada](entry-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=pt-BR)

**Dados contextuais**

Aproveite **dados contextuais** de eventos, informações da Adobe Experience Platform ou dados de serviços de API de terceiros.

[Trabalhar com fontes de dados](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=pt-BR)

**Ações internas**

Use as **ações de canal integradas** para enviar mensagens criadas no [!DNL Journey Optimizer] por email, push, SMS/MMS e muito mais.

[Enviar mensagens no jornada](journeys-message.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=pt-BR)

**Ações personalizadas**

Crie **ações personalizadas** se estiver usando um sistema de terceiros para enviar mensagens ou se conectar a APIs externas.

[Configurar ações personalizadas](../action/about-custom-action-configuration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=pt-BR)

**Designer do Visual jornada**

Com o **Designer de jornadas**, crie seus casos de uso de várias etapas: arraste e solte facilmente um evento de entrada ou uma atividade de público-alvo de leitura, adicione condições e envie mensagens personalizadas.

[Explorar o designer de jornada](using-the-journey-designer.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=pt-BR)

**Testar e otimizar**

Teste suas jornadas antes de publicar, monitore o desempenho e otimize o delivery com recursos avançados, como otimização de tempo de envio.

[Testar e publicar jornadas](testing-the-journey.md)
:::

::::

## Casos de uso e exemplos {#use-cases}

No designer de jornadas, profissionais de marketing podem enviar mensagens 1:1 acionadas em tempo real por qualquer canal quando um evento ocorre. Por exemplo, quando um(a) cliente assina um serviço, ele pode [acionar um email de boas-vindas](message-to-subscribers-uc.md), incentivando-o(a) a fazer logon no aplicativo pela primeira vez e definir suas preferências. Ações como concluir a compra, abrir o email e fazer logon no aplicativo podem ser usadas como incentivos para o progresso de clientes em suas jornadas.

O [designer de jornada](using-the-journey-designer.md) fornece [ações de canal integradas](journeys-message.md) que oferecem suporte a mensagens de saída, como emails, notificações por push e SMS/MMS, bem como canais de entrada, incluindo aplicativos móveis, sites e experiências baseadas em código criadas diretamente no Journey Optimizer. Você também pode usar sistemas de terceiros para enviar mensagens — o Journey Optimizer inclui [ações personalizadas](using-custom-actions.md) para permitir que esses sistemas sejam integrados ao jornada diretamente do designer do jornada.


:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=pt-BR)

**Saiba mais sobre casos de uso**

Explore casos de uso abrangentes e completos do jornada que demonstram implementações reais e práticas recomendadas.

[Descubra todos os casos de uso](jo-use-cases.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=pt-BR)

**Bem-vindo(a) aos novos assinantes**

Envie uma jornada de boas-vindas personalizada quando os clientes assinarem seu serviço, guiando-os pelas etapas de integração.

[Saiba mais](message-to-subscribers-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg?lang=pt-BR)

**Otimizar tempos de envio de email**

Use a otimização de tempo de envio baseada em IA para enviar emails quando houver maior probabilidade de cada cliente participar.

[Saiba mais](send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=pt-BR)

**Aumentar entregas**

Aumente gradualmente o volume de mensagens para aquecer a reputação de envio e evitar problemas de capacidade de delivery.

[Saiba mais](ramp-up-deliveries-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=pt-BR)

**Direcionar por dia da semana**

Envie conteúdo diferente com base no dia da semana em que os clientes entram na sua jornada.

[Saiba mais](weekday-email-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/question.svg?lang=pt-BR)

**Perguntas frequentes sobre o Jornada**

Encontre respostas para perguntas frequentes sobre a criação de jornadas, a solução de problemas e as práticas recomendadas.

[Exibir perguntas frequentes](journey-faq.md)
:::

::::



## Recursos de aprendizado {#learning-resources}

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=pt-BR)

**Criar e gerenciar jornadas**

Orientação passo a passo sobre design, teste, publicação e rastreamento de jornadas do cliente para criar campanhas onicanais personalizadas.

[Explorar criação de jornada](/help/rp_landing_pages/create-journey-landing-page.md) | [Saiba mais sobre o gerenciamento de jornadas](/help/rp_landing_pages/manage-journey-landing-page.md) | [Jornada etapas do fluxo de trabalho](journey.md#workflow)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=pt-BR)

**Jornada atividades**

Descubra como configurar e usar atividades como acionadores, etapas de decisão, gerenciamento de público-alvo e mensagens personalizadas em jornadas.

[Explorar atividades](/help/rp_landing_pages/about-journey-building-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=pt-BR)

**Expressões e condições**

Domine a criação de expressões para fluxos de trabalho dinâmicos, manipulação de dados e orquestração de jornada avançada usando ferramentas e sintaxe avançadas.

[Saiba mais sobre expressões](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bell.svg?lang=pt-BR)

**Solução de problemas e monitoramento**

Diagnostique e resolva problemas de execução de jornada com ferramentas, códigos de erro e práticas recomendadas para depuração e otimização.

[Manual de solução de problemas](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=pt-BR)

**visão geral do designer do Jornada**

Entenda a tela, a paleta e como projetar as jornadas do cliente usando a interface visual do jornada.

[Conheça o designer](using-the-journey-designer.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=pt-BR)

**Testar e publicar**

Teste suas jornadas minuciosamente antes de publicá-las para garantir que funcionem conforme o esperado e forneçam a experiência correta.

[Guia de testes](testing-the-journey.md)
:::

::::

### Tutorial em vídeo {#video}

Descubra os componentes de uma jornada e entenda os aspectos básicos da criação de uma jornada na tela.

>[!VIDEO](https://video.tv.adobe.com/v/3430346?captions=por_br&quality=12)

### Recursos adicionais

* **[Referência a códigos de erro](error-codes-reference.md)**: códigos de erro e etapas de solução de problemas da jornada
* **[Alertas](../reports/alerts.md)**: configurar alertas para monitoramento da jornada
* **[Solução de problemas](troubleshooting.md)**: problemas e soluções comuns da jornada
* **[Tutoriais do Jornada](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}** - Saiba mais sobre a criação de jornadas por meio de tutoriais em vídeo práticos
* **[medidas de proteção e limitações de Jornada](../start/guardrails.md)** - Verifique as medidas de proteção e as limitações ao usar [!DNL Adobe Journey Optimizer]

