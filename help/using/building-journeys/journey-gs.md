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
source-git-commit: fa46397b87ae3a81cd016d95afd3e09bb002cfaa
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 25%

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

O Adobe Journey Optimizer inclui uma tela de orquestração omnicanal que permite aos profissionais de marketing harmonizar o alcance do marketing com o engajamento individual com clientes. A interface de usuário do permite arrastar e soltar facilmente as atividades da paleta na tela para criar sua jornada. A interface do usuário do jornada está detalhada em [esta página](journey-ui.md).

![amostra da tela de jornada](assets/journey38.png)


As principais etapas para criar uma jornada são detalhadas nesta página. Elas são simplificadas da seguinte maneira:

![etapas de criação de jornadas: criar, projetar, testar e publicar](assets/journey-creation-process.png)


Crie jornadas de várias etapas para o cliente e inicie em tempo real uma sequência de interações, ofertas e mensagens entre canais. Essa abordagem garante que os clientes estejam envolvidos nos momentos ideais com base em suas ações e sinais de negócios relevantes. Os públicos-alvo são definidos com base no comportamento, nos dados contextuais e nos eventos comerciais. Os pré-requisitos dependem do seu caso de uso e do [tipo de jornada](entry-management.md#types-of-journeys) que você está criando.

Antes de começar a criar a jornada, verifique se as etapas de configuração relevantes foram concluídas:

* Se quiser acionar suas jornadas individualmente quando um evento for recebido, **configure um evento**. Defina as informações esperadas e como processá-las. [Leia mais](../event/about-events.md).

<!--   ![](assets/jo-event7bis.png)  -->

* Sua jornada também pode ouvir os públicos-alvo da Adobe Experience Platform para enviar mensagens em lotes para um conjunto especificado de perfis. Para isso, **crie públicos-alvo**. [Leia mais](../audience/about-audiences.md).

<!--   ![](assets/segment2.png)  -->

* Defina uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas, por exemplo, em suas condições. Esta conexão depende de uma **fonte de dados**. [Leia mais](../datasource/about-data-sources.md).

<!--   ![](assets/jo-datasource.png)  -->

* O Journey Optimizer vem com [recursos de mensagem](../building-journeys/journeys-message.md) incorporados. Se você estiver usando um sistema de terceiros para enviar mensagens, poderá **criar uma ação personalizada**. Saiba mais nesta [seção](../action/action.md).

<!--    ![](assets/custom2.png)  -->


Como engenheiro de dados, as etapas para configurar suas jornadas, incluindo Fontes de dados, Eventos e Ações são detalhadas [nesta seção](../configuration/about-data-sources-events-actions.md).


>[!NOTE]
>
>As medidas de proteção e limitações da jornada estão detalhadas [nesta página](../start/guardrails.md)

## Criar uma jornada {#jo-build}

Para criar uma jornada de várias etapas, siga estas etapas:

1. Na seção de menu GERENCIAMENTO de JORNADAS, clique em **[!UICONTROL Jornadas]**.

1. Clique no botão **[!UICONTROL Criar Jornada]** para criar uma nova jornada.

1. Edite o painel de configuração da jornada para definir o nome da jornada e definir suas propriedades. Saiba como definir as propriedades da sua jornada [nesta página](journey-properties.md).

   ![](assets/jo-properties.png)

Você pode então começar a projetar sua jornada.

## Projetar a jornada {#jo-design}

O designer de jornada omnicanal ajuda a criar jornadas em várias etapas com públicos-alvo direcionados, atualizações com base em interações de clientes ou negócios em tempo real e mensagens omnicanal usando uma interface intuitiva de arrastar e soltar.

![](assets/journey38.png)

1. Comece arrastando e soltando um evento ou uma atividade **Ler público-alvo** da paleta na tela. Para saber mais sobre design do jornada, consulte [esta seção](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. Comece arrastando e soltando um evento ou uma atividade **Ler público-alvo** da paleta na tela. Para saber mais sobre design do jornada, consulte [esta seção](using-the-journey-designer.md).

## Testar a jornada {#jo-test}

Depois de criar a jornada, teste-a antes de publicar. A Journey Optimizer oferece um **Modo de teste** como uma maneira de exibir perfis de teste conforme eles se movem ao longo da jornada, detectando possíveis erros antes da ativação. A execução de testes rápidos garante que as jornadas funcionem corretamente para que você possa publicá-las com confiança. Saiba como testar sua jornada [nesta seção](testing-the-journey.md)

Você também pode executar sua jornada em **Dry run**. A execução de prática de jornada é um modo especial de publicação no Adobe Journey Optimizer que permite aos profissionais de jornada o teste de uma jornada usando dados de produção reais sem entrar em contato com clientes do mundo real ou atualizar informações de perfil. Esse recurso ajuda os profissionais de jornada a ganhar confiança no design da jornada e no direcionamento de público-alvo antes de publicá-la ao vivo. Saiba como publicar uma jornada no modo de Execução em Seco [nesta seção](journey-dry-run.md).

## Publicar a jornada {#jo-pub}

Você deve publicar uma jornada para ativá-la e disponibilizá-la para que novos perfis a insiram. Antes de publicar sua jornada, verifique se ela é válida e se não há erros. Não é possível publicar uma jornada com erros. Saiba mais sobre a publicação do jornada nesta [seção](publishing-the-journey.md).

![](assets/jo-journeyuc2_32bis.png)

Após a publicação, é possível monitorar a jornada usando as ferramentas de relatório dedicadas para medir a eficiência da jornada.

![](assets/jo-dynamic_report_journey_12.png)

Saiba mais sobre relatórios do jornada nesta [seção](../reports/live-report.md).

>[!NOTE]
>
>Se você precisar modificar uma jornada do **live**, [crie uma nova versão](journey-ui.md#journey-versions) da jornada.
