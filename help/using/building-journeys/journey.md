---
solution: Journey Optimizer
product: journey optimizer
title: Introdução a jornadas
description: Introdução a jornadas
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: jornada, descobrir, introdução
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
version: Journey Orchestration
source-git-commit: dd3d91266c0edea562f75ceb1f75974c7242ee1a
workflow-type: tm+mt
source-wordcount: '1108'
ht-degree: 34%

---


# Introdução a jornadas{#jo-general-principle}

As jornadas no Adobe Journey Optimizer permitem criar jornadas personalizadas e de várias etapas para o cliente que se adaptam em tempo real ao comportamento e às necessidades do seu público-alvo. Usando uma tela intuitiva de arrastar e soltar, você pode orquestrar mensagens e ações em vários canais, aproveitando dados contextuais e o direcionamento de público-alvo para obter o máximo impacto. Esteja você explorando acionadores em tempo real, gerenciando propriedades do jornada ou usando ferramentas avançadas como ações e expressões personalizadas, esta seção fornece um roteiro claro para ajudá-lo a projetar e refinar jornadas que proporcionem experiências relevantes e oportunas ao cliente.

Use o [!DNL Journey Optimizer] para criar casos de uso de orquestração em tempo real usando dados contextuais armazenados em eventos ou fontes de dados. É possível projetar cenários avançados em várias etapas com os seguintes recursos:

* Enviar **entrega unitária** em tempo real disparada quando um [evento](general-events.md) é recebido ou **em lote** usando [públicos-alvo](read-audience.md) da Adobe Experience Platform.

* Aproveite os **dados contextuais** de [eventos](../event/about-events.md), informações da Adobe Experience Platform ou dados de serviços de API de terceiros por meio de [fontes de dados](../datasource/about-data-sources.md).

* Use as **[ações integradas](journeys-message.md)** para enviar mensagens projetadas no [!DNL Journey Optimizer] ou crie **[ações personalizadas](using-custom-actions.md)** se estiver usando um sistema de terceiros para enviar mensagens.

* Com o **[designer do jornada](using-the-journey-designer.md)**, crie seus casos de uso em várias etapas: arraste e solte facilmente um evento de entrada ou uma [atividade de leitura de público-alvo](read-audience.md), adicione [condições](condition-activity.md) e envie mensagens personalizadas.

➡️ [Conheça o Journey Optimizer neste vídeo](#video)

## Visão geral de jornadas

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=pt-BR)

Introdução à criação de Jornadas

Orientação passo a passo sobre design, teste, publicação e rastreamento de jornadas do cliente para criar campanhas onicanais personalizadas.

[Criar a primeira jornada](journey-gs.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=pt-BR)

Journey Orchestration - Guia completo

Documentação abrangente que abrange todos os aspectos da criação, do gerenciamento e da otimização de jornadas no Adobe Journey Optimizer.

[Explorar o guia completo](journey-get-started.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=pt-BR)

Gerenciamento de Jornadas

Gerencie as jornadas do cliente com eficiência com ferramentas para filtragem, gerenciamento de perfil, fusos horários e técnicas de otimização.

[Saiba mais sobre o gerenciamento de jornada](/help/rp_landing_pages/manage-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=pt-BR)

Jornada atividades

Descubra como configurar e usar atividades como acionadores, etapas de decisão, gerenciamento de público-alvo e mensagens personalizadas em jornadas.

[Explorar atividades](/help/rp_landing_pages/about-journey-building-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=pt-BR)

Criação de expressões

Domine a criação de expressões para fluxos de trabalho dinâmicos, manipulação de dados e orquestração de jornada avançada usando ferramentas e sintaxe avançadas.

[Saiba mais sobre expressões](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=pt-BR)

Jornada casos de uso

Explore aplicativos reais do Adobe Journey Optimizer, incluindo mensagens multicanais e integração com sistemas externos.

[Descubra casos de uso](/help/rp_landing_pages/journey-use-cases-landing-page.md)
:::

::::

## O que você pode fazer com as jornadas?

No designer de jornadas, profissionais de marketing podem enviar mensagens 1:1 acionadas em tempo real por qualquer canal quando um evento ocorre. Por exemplo, quando um(a) cliente assina um serviço, ele pode [acionar um email de boas-vindas](message-to-subscribers-uc.md), incentivando-o(a) a fazer logon no aplicativo pela primeira vez e definir suas preferências. Ações como concluir a compra, abrir o email e fazer logon no aplicativo podem ser usadas como incentivos para o progresso de clientes em suas jornadas.

## Tipos de jornada

O Adobe Journey Optimizer é compatível com quatro tipos de jornada, cada um projetado para casos de uso e mecanismos de entrada diferentes. Escolha o tipo certo com base em como você deseja que os perfis entrem e avancem nas experiências do cliente.

>[!BEGINTABS]

>[!TAB jornadas unitárias]

As **jornadas unitárias** são acionadas individualmente por um evento quando ocorre uma ação específica, como uma compra, entrada no aplicativo ou envio de formulário. Os perfis entram na jornada, um de cada vez, em tempo real, quando o evento é recebido, tornando-a ideal para experiências personalizadas e orientadas por comportamento.

**Características-chave:**

* Entrada orientada por eventos e em tempo real
* Processamento de perfil individual
* Perfeito para mensagens transacionais e respostas imediatas
* Oferece suporte a dados contextuais do evento de acionamento

**Casos de uso:**

* Confirmação de pedido após compra
* Email de boas-vindas quando alguém assinar
* Abandono do carrinho acionado pelo comportamento de navegação
* Notificações de redefinição de senha

➡️ [Saiba mais sobre a configuração do evento](../event/about-events.md) | [Eventos gerais](general-events.md) | [Caso de uso de mensagem para assinantes](message-to-subscribers-uc.md)

>[!TAB Ler jornadas de Público-Alvo]

**Ler jornadas de público-alvo** comece com um público-alvo do Adobe Experience Platform e envie mensagens em lote para todos os perfis desse público-alvo. Esse tipo de jornada processa todo o público-alvo de uma só vez, tornando-o ideal para campanhas programadas e comunicações recorrentes.

**Características-chave:**

* Processamento em lote de segmentos de público-alvo
* Execução programada ou única
* Todos os perfis são inseridos simultaneamente
* Oferece suporte a comunicações em larga escala

**Casos de uso:**

* Boletins informativos mensais
* Campanhas promocionais para segmentar segmentos
* Anúncios de produtos para todos os clientes
* Campanhas de marketing sazonais

➡️ [Saiba mais sobre a Atividade Ler Público](read-audience.md) | [Introdução aos públicos-alvo](../audience/about-audiences.md) | [Caso de uso de mensagens multicanais](journeys-uc.md)

>[!TAB jornadas de qualificação de público-alvo]

**As jornadas de qualificação de público-alvo** são acionadas quando os perfis se qualificam para (ou saem de) um segmento de público-alvo específico. Os perfis entram na jornada individualmente, pois atendem aos critérios de público-alvo em tempo real, permitindo envolvimento imediato quando o comportamento do cliente muda.

**Características-chave:**

* Entrada baseada em qualificação em tempo real
* Monitoramento contínuo da associação de público
* Processamento de perfil individual conforme eles são qualificados
* Melhor com públicos de transmissão

**Casos de uso:**

* Notificações de atualização de nível do VIP
* Reengajamento quando os clientes se tornam inativos
* Mensagens de celebração da primeira compra
* Direcionamento geográfico quando os clientes se movem

➡️ [Saiba mais sobre a qualificação de público-alvo](audience-qualification-events.md) | [Atividade de condição](condition-activity.md) | [Criando definições de segmento](../audience/creating-a-segment-definition.md)

>[!TAB jornadas de eventos comerciais]

As **jornadas de eventos comerciais** são acionadas por eventos comerciais (como atualizações de estoque, alertas meteorológicos ou alterações de preço) que afetam vários perfis simultaneamente. Em vez de reagir a ações individuais do cliente, essas jornadas respondem a condições de negócios mais amplas ou a fatores externos.

**Características-chave:**

* Acionado por eventos de nível de negócios, não por ações individuais
* Afeta vários perfis de uma só vez
* Segmenta um público-alvo específico quando o evento ocorre
* Combina tempo orientado por eventos com direcionamento de público-alvo

**Casos de uso:**

* Alertas de baixo inventário para clientes interessados
* Anúncios de venda do Flash
* Promoções baseadas no clima
* Notificações de queda de preço
* Alertas de produtos devolvidos ao estoque

➡️ [Saiba mais sobre eventos comerciais](general-events.md) | [Configurar eventos comerciais](../event/about-creating-business.md) | [Gerenciamento de entradas](entry-management.md)

>[!ENDTABS]

## Jornada Designer{#journey-designer}

O [designer de jornadas](using-the-journey-designer.md) fornece tudo o que os profissionais de marketing e jornadas precisam para orquestrar jornadas de várias etapas do :1 entre canais. Isso inclui uma tela intuitiva com interface de arrastar e soltar para criar cada etapa da jornada, definir o público-alvo e incluir as mensagens, ofertas e conteúdo nos canais que os membros do público-alvo verão com base no comportamento, nos dados contextuais e nos eventos de negócios.

O designer de jornadas fornece tudo o que você precisa para criar experiências de várias etapas:

* **[Ações de canal integradas](journeys-message.md)** - Envie mensagens por email, notificações por push, SMS/MMS, no aplicativo, Web, experiências baseadas em código e muito mais, tudo isso diretamente no Journey Optimizer
* **[Ações personalizadas](using-custom-actions.md)** - Integre sistemas de terceiros para enviar mensagens ou acionar fluxos de trabalho em plataformas externas
* **[Atividades de orquestração](about-journey-activities.md)** - Adicione lógica, condições, tempos de espera e direcionamento de público-alvo para criar experiências de cliente sofisticadas
* **[Condições](condition-activity.md)** - Ramifique sua jornada com base em atributos de perfil, associação de público ou eventos em tempo real
* **[Expressões](expression/expressionadvanced.md)** - Crie lógica e personalização avançadas usando o editor de expressão

Saiba como usar o designer do jornada [nestes casos de uso completos](jo-use-cases.md).

>[!NOTE]
>
>As medidas de proteção e limitações da jornada estão detalhadas [nesta página](../start/guardrails.md)

## Vídeo tutorial {#video}

Descubra os componentes de uma jornada e entenda os aspectos básicos da criação de uma jornada na tela.

>[!VIDEO](https://video.tv.adobe.com/v/3424996?quality=12)

## Recursos adicionais {#additional-resources}

* **[Solução de problemas de Jornadas do cliente](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)** - Diagnostique e resolva problemas de execução de jornada com ferramentas, códigos de erro e práticas recomendadas para depuração e otimização
* **[Perguntas frequentes sobre jornadas](journey-faq.md)**: perguntas frequentes sobre jornadas
* **[Alertas de Jornada](../reports/alerts.md)** - Configure alertas para o monitoramento de jornadas e assine notificações para atualizações em tempo real
* **[Referência a códigos de erro](error-codes-reference.md)**: códigos de erro e etapas de solução de problemas da jornada
* **[Solução de problemas](troubleshooting.md)**: problemas e soluções comuns da jornada
* **[Tutoriais do Jornada (vídeos)](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}** - Saiba mais sobre a criação de jornadas por meio de tutoriais práticos em vídeo que abrangem recursos, funcionalidades e práticas recomendadas
