---
solution: Journey Optimizer
product: journey optimizer
title: Criar a primeira jornada
description: Etapas principais para criar sua primeira jornada com o Adobe Journey Optimizer
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: jornada, primeiro, iniciar, início rápido, público-alvo, evento, ação
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: 99099cb6b705cb5a7b97652154c42f0565fdfdb9
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 33%

---

# Criar a primeira jornada {#jo-quick-start}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="Criar jornadas"
>abstract="Use o **Adobe Journey Optimizer** para criar casos de uso de orquestração em tempo real, aproveitando dados contextuais armazenados em eventos ou fontes de dados."

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Jornadas"
>abstract="Crie jornadas do cliente para fornecer experiências personalizadas e contextuais. O Journey Optimizer permite criar casos de uso de orquestração em tempo real usando dados contextuais armazenados em eventos ou fontes de dados. A guia **Visão geral** exibe um painel com as métricas principais relacionadas às suas jornadas. A guia **Procurar** exibe a lista de jornadas existentes."


O Adobe Journey Optimizer inclui uma tela de orquestração omnicanal que permite aos profissionais de marketing harmonizar o alcance do marketing com o engajamento individual com clientes. A interface permite arrastar e soltar facilmente as atividades da paleta na tela para criar a jornada.

![](assets/journey38.png)

As principais etapas para criar uma jornada são as seguintes:

![](assets/journey-creation-process.png)

➡️ [Descubra este recurso no vídeo](#video)

A interface do usuário do jornada está detalhada em [esta página](journey-ui.md).


## Pré-requisitos {#start-prerequisites}

Para enviar mensagens com jornadas, os seguintes pré-requisitos são necessários:

1. **Configurar um evento**: se quiser acionar as jornadas de forma unitária quando um evento for recebido, será necessário configurar um evento. Você define as informações esperadas e como processá-las. Esta etapa é executada por um **usuário técnico**. [Leia mais](../event/about-events.md).

   ![](assets/jo-event7bis.png)

1. **Criar um público-alvo**: sua jornada também pode ouvir públicos-alvo da Adobe Experience Platform para enviar mensagens em lote para um conjunto especificado de perfis. Para isso, você precisa criar públicos. [Leia mais](../audience/about-audiences.md).

   ![](assets/segment2.png)

1. **Configurar a fonte de dados**: você pode definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas, por exemplo, em suas condições. Uma fonte de dados integrada da Adobe Experience Platform também é configurada no momento do provisionamento. Esta etapa não é necessária se você usar somente os dados dos eventos em sua jornada. Esta etapa é executada por um **usuário técnico**. [Leia mais](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **Configurar uma ação**: se você estiver usando um sistema de terceiros para enviar mensagens, poderá criar uma ação personalizada. Saiba mais nesta [seção](../action/action.md). Esta etapa é executada por um **usuário técnico**. Se você estiver usando os recursos de mensagem incorporados do Journey Optimizer, basta adicionar uma ação de canal à jornada e projetar o conteúdo.

   ![](assets/custom2.png)



Como engenheiro de dados, as etapas para configurar suas jornadas, incluindo Fontes de dados, Eventos e Ações são detalhadas [nesta seção](../configuration/about-data-sources-events-actions.md).


>[!NOTE]
>
>Medidas de proteção e limitações da jornada estão detalhadas [nesta página](../start/guardrails.md)

## Criar uma jornada de várias etapas {#jo-build}

Para criar uma jornada de várias etapas, siga estas etapas:

1. Na seção de menu GERENCIAMENTO de JORNADAS, clique em **[!UICONTROL Jornadas]**.

1. Clique no botão **[!UICONTROL Criar Jornada]** para criar uma nova jornada.

1. Edite o painel de configuração da jornada para definir o nome da jornada e definir suas propriedades. Saiba como definir as propriedades da sua jornada [nesta página](journey-properties.md).

   ![](assets/jo-properties.png)

Você pode então começar a projetar sua jornada.

## Projetar a jornada {#jo-design}

O designer de jornada omnicanal ajuda a criar jornadas em várias etapas com públicos-alvo direcionados, atualizações com base em interações de clientes ou empresas em tempo real e mensagens omnicanal usando uma interface intuitiva de arrastar e soltar.

![](assets/journey38.png)

1. Comece arrastando e soltando um evento ou uma atividade **Ler público-alvo** da paleta na tela. Para saber mais sobre design do jornada, consulte [esta seção](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. Arraste e solte as próximas etapas que o indivíduo seguirá. Por exemplo, é possível adicionar uma condição seguida por uma ação de canal. Para saber mais sobre atividades, consulte [esta seção](about-journey-activities.md).

## Testar a jornada {#jo-test}

Depois de criar a jornada, você pode testá-la antes de publicar. O Journey Optimizer oferece o &quot;Modo de teste&quot; como uma maneira de exibir perfis de teste conforme eles se movem ao longo da jornada, detectando possíveis erros antes da ativação. A execução de testes rápidos permite verificar se as jornadas funcionam corretamente para que você possa publicá-las com confiança.

Saiba mais nesta [seção](testing-the-journey.md)

## Publicar a jornada {#jo-pub}

Você deve publicar uma jornada para ativá-la e disponibilizá-la para que novos perfis a insiram. Antes de publicar sua jornada, verifique se ela é válida e se não há erros. Não é possível publicar uma jornada com erros. Saiba mais sobre a publicação do jornada nesta [seção](publishing-the-journey.md).

![](assets/jo-journeyuc2_32bis.png)

Após a publicação, é possível monitorar a jornada usando as ferramentas de relatório dedicadas para medir a eficiência da jornada.

![](assets/jo-dynamic_report_journey_12.png)

Saiba mais sobre relatórios do jornada nesta [seção](../reports/live-report.md).

Observe que você pode duplicar uma jornada existente ou criar uma nova versão de uma jornada. Saiba mais em [esta página](journey-ui.md)