---
solution: Journey Optimizer
product: journey optimizer
title: Crie a primeira jornada
description: Etapas principais para criar sua primeira jornada com o  [!DNL Adobe Journey Optimizer]
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: jornada, primeiro, iniciar, início rápido, público-alvo, evento, ação
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
version: Journey Orchestration
source-git-commit: e7586f50e9f806b7dccb6d88998c43a89feb392b
workflow-type: tm+mt
source-wordcount: '1215'
ht-degree: 10%

---

# Crie a primeira jornada {#jo-quick-start}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="Criar jornadas"
>abstract="Use o **[!DNL Adobe Journey Optimizer]** para criar casos de uso de orquestração em tempo real, aproveitando dados contextuais armazenados em eventos ou fontes de dados."

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Jornadas"
>abstract="Crie jornadas do cliente para fornecer experiências personalizadas e contextuais. O Journey Optimizer permite criar casos de uso de orquestração em tempo real usando dados contextuais armazenados em eventos ou fontes de dados. A guia **Visão geral** exibe um painel com as métricas principais relacionadas às suas jornadas. A guia **Procurar** exibe a lista de jornadas existentes."

[!DNL Adobe Journey Optimizer] inclui uma tela de orquestração omnicanal que permite aos profissionais de marketing harmonizar o alcance de marketing com o envolvimento individual do cliente. A interface de usuário do permite arrastar e soltar facilmente as atividades da paleta na tela para criar sua jornada. A interface do usuário do jornada está detalhada em [esta página](journey-ui.md).

![amostra da tela de jornada](assets/journey38.png)

As principais etapas para criar uma jornada são detalhadas nesta página. Elas são simplificadas da seguinte maneira:

![etapas de criação de jornadas: criar, projetar, testar e publicar](assets/journey-creation-process.png)

Neste guia, você deverá:

* Definir um ponto de entrada de jornada — um segmento de público ou um evento em tempo real
* Adicione ações de mensagem em canais — email, push, SMS, no aplicativo, Web, experiência baseada em código, cartão de conteúdo e muito mais. [Ver canais com suporte](journey-action.md)
* Testar sua jornada com perfis de teste antes da ativação
* Publicar a jornada e monitorar o desempenho

Crie jornadas de várias etapas para o cliente e inicie em tempo real uma sequência de interações, ofertas e mensagens entre canais. Essa abordagem garante que os clientes estejam envolvidos nos momentos ideais com base em suas ações e sinais de negócios relevantes.

<!--
>[!TIP]
>
>Not sure whether to use a journey or a campaign? [Learn how to choose the right approach](../start/journeys-vs-campaigns.md).
-->

## Antes de começar {#prerequisites}

O que é necessário configurar antes de criar depende de como a jornada é acionada. A maioria das jornadas começa em um destes dois pontos de entrada:

* **Entrada baseada em público-alvo** — A jornada é executada para um conjunto definido de perfis em um horário agendado. [Crie um público-alvo](../audience/about-audiences.md) no Adobe Experience Platform antes de criar sua jornada. Esse é o ponto de partida recomendado se você for novo no Journey Optimizer.

* **Entrada baseada em eventos** — A jornada é acionada em tempo real quando um indivíduo executa uma ação, como uma compra ou uma inscrição. [Configure um evento](../event/about-events.md) para definir o gatilho e os dados que ele transporta.

Os seguintes elementos são opcionais, mas podem ser obrigatórios, dependendo do seu caso de uso:

* **Fonte de dados** — Para enriquecer as condições de jornada ou a personalização com dados de um sistema externo, configure uma [fonte de dados](../datasource/about-data-sources.md).

* **Ação personalizada** — Se você entregar mensagens por meio de um sistema de terceiros em vez dos canais internos, configure uma [ação personalizada](../action/action.md).

>[!NOTE]
>
>* Se você for um engenheiro de dados responsável pela configuração técnica (eventos, fontes de dados e ações), consulte [esta seção](../configuration/about-data-sources-events-actions.md).
>
>* As medidas de proteção e limitações de jornada estão detalhadas em [esta página](../start/guardrails.md).

## Criar uma jornada {#jo-build}

Para criar uma jornada de várias etapas, siga estas etapas:

1. Na seção de menu GERENCIAMENTO de JORNADAS, clique em **[!UICONTROL Jornadas]**.

1. Clique no botão **[!UICONTROL Criar Jornada]** para criar uma nova jornada.

1. Edite o painel de configuração da jornada para definir o nome da jornada e definir suas propriedades. Saiba como definir as propriedades da sua jornada [nesta página](journey-properties.md).

   >[!TIP]
   >
   >**Que tipo de jornada devo escolher?** Se você é novo no Journey Optimizer, comece com uma jornada baseada em público-alvo usando uma atividade **[!UICONTROL Ler público-alvo]** — ela não requer configuração prévia de evento e é a maneira mais fácil de se familiarizar com a tela. Para experiências acionadas por eventos em tempo real (por exemplo, reagir a uma compra ou ao envio de um formulário), configure um evento primeiro e use uma entrada baseada em eventos. Pronto para aprofundar? [Descubra todos os tipos de jornadas e suas regras de entrada](entry-management.md#types-of-journeys).

   ![Painel de propriedades do Jornada com opções de configuração e definições](assets/jo-properties.png)

Você pode então começar a projetar sua jornada.

## Projetar a jornada {#jo-design}

O designer de jornadas permite criar jornadas de várias etapas usando uma interface intuitiva de arrastar e soltar. As atividades na paleta esquerda são organizadas em três categorias: **Eventos**, **Orquestração** e **Ações**. Para obter uma visão geral completa da tela e seus controles, consulte [esta página](using-the-journey-designer.md).

![Interface do designer de Jornadas com a paleta e a tela de atividades](assets/journey38.png)

Siga estas etapas para criar sua jornada:

1. **Adicionar um ponto de entrada** — Arraste um evento ou uma atividade **[!UICONTROL Ler Público]** da paleta para a tela. Isso define como os perfis entram na jornada: individualmente em tempo real (baseado em eventos) ou de uma só vez de um público-alvo definido (baseado em público-alvo).

   ![Ler configuração de atividade de público-alvo para selecionar público-alvo](assets/read-segment.png)

1. **Adicionar ações de mensagem** — Na seção **[!UICONTROL Ações]** da paleta, arraste uma ação de canal para a tela para enviar mensagens para perfis que fluem pela jornada. As ações estão disponíveis para email, notificações por push, SMS e muito mais.

1. **Adicionar atividades de orquestração** — Use uma atividade **[!UICONTROL Condition]** para ramificar a jornada em vários caminhos com base em atributos ou comportamento de perfil. Use uma atividade **[!UICONTROL Wait]** para introduzir um atraso de tempo entre as etapas.

>[!TIP]
>
>Para jornadas com várias fases ou muitos pontos de contato, considere dividir o fluxo de ponta a ponta em sub-jornadas menores conectadas à atividade **[!UICONTROL Jump]**. Isso reduz a complexidade e facilita o teste independente de cada subjornada. Saiba mais em [Estratégia de design: subjornadas de tamanho reduzido](jump.md#jump-strategy).

## Testar a jornada {#jo-test}

Depois de criar a jornada, teste-a antes de publicar. A Journey Optimizer oferece um **Modo de teste** como uma maneira de exibir perfis de teste conforme eles se movem ao longo da jornada, detectando possíveis erros antes da ativação. A execução de testes rápidos garante que as jornadas funcionem corretamente para que você possa publicá-las com confiança. Saiba como testar sua jornada [nesta seção](testing-the-journey.md)

Você também pode executar sua jornada em **Dry run**. O teste de simulação da jornada é um modo de publicação especial no Adobe Journey Optimizer que permite aos profissionais de jornada o teste de uma jornada usando dados de produção reais, sem entrar em contato com clientes reais ou atualizar informações de perfil. Esse recurso ajuda os profissionais de jornada a ganhar confiança no design da jornada e no direcionamento de público-alvo antes de publicá-la ao vivo. Saiba como publicar uma jornada no modo de Execução em Seco [nesta seção](journey-dry-run.md).

## Publicar a jornada {#jo-pub}

Você deve publicar uma jornada para ativá-la e disponibilizá-la para que novos perfis a insiram. Antes de publicar sua jornada, verifique se ela é válida e se não há erros. Não é possível publicar uma jornada com erros. Saiba mais sobre a publicação do jornada nesta [seção](publish-journey.md).

![Conclua o fluxo de jornadas com público-alvo, condições e ações](assets/jo-journeyuc2_32bis.png)

Após a publicação, é possível monitorar a jornada usando as ferramentas de relatório dedicadas para medir a eficiência da jornada.

![Relatório de análise de Jornada mostrando métricas e estatísticas de desempenho](assets/jo-dynamic_report_journey_12.png)

Saiba mais sobre relatórios do jornada nesta [seção](../reports/live-report.md).

## Casos de uso comuns {#use-cases}

Não tem certeza de onde começar? Estes são três cenários típicos em que as jornadas agregam mais valor:

<table style="table-layout:fixed">
  <tr style="border: 0;">
    <td>
      <a href="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding" target="_blank">
        <img src="../assets/do-not-localize/icon-quick-start.svg" width="35px">
      </a>
      <div><strong>Série de boas-vindas</strong><br/>Integre automaticamente novos usuários com uma sequência de mensagens após a inscrição, guiando-os por meio de seu produto ou serviço.</div>
    </td>
    <td>
      <a href="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart" target="_blank">
        <img src="../assets/do-not-localize/icon-campaign.svg" width="35px">
      </a>
      <div><strong>Abandono do carrinho</strong><br/>Reative os clientes que saíram sem concluir uma compra enviando um lembrete em tempo hábil com conteúdo personalizado.</div>
    </td>
    <td>
      <a href="jo-use-cases.md">
        <img src="../assets/do-not-localize/icon-content.svg" width="35px">
      </a>
      <div><strong>Reengajamento</strong><br/>Conquiste usuários inativos com ofertas ou atualizações direcionadas com base em seu último comportamento conhecido.</div>
    </td>
  </tr>
  <tr style="border: 0;">
    <td align="center"><a href="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding" target="_blank"><img src="../assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart" target="_blank"><img src="../assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="jo-use-cases.md"><img src="../assets/do-not-localize/learn-more-button.svg"></a></td>
  </tr>
</table>

## Recursos adicionais

* **[Tipos de Jornada e entrada de perfil](entry-management.md)** - Entenda todos os tipos de jornada (evento unitário, evento comercial, público-alvo de leitura, qualificação de público-alvo) e como os perfis entram, entram novamente e fluem pelas jornadas.
* **[visão geral do designer do Jornada](using-the-journey-designer.md)** - Domine a interface da tela do jornada para projetar e organizar jornadas do cliente.
* **[Atividades de Jornada](about-journey-activities.md)** - Descubra todas as atividades disponíveis, incluindo eventos, ações e componentes de orquestração.
* **[Testando jornadas](testing-the-journey.md)** - Saiba como testar suas jornadas usando o modo de teste antes de publicar na produção.
* **[jornadas de Publicação](publish-journey.md)** - Entenda o processo de publicação do jornada e como gerenciar jornadas ativas.
* **[Relatórios de Jornadas](report-journey.md)** - Acompanhe e analise o desempenho da jornada com métricas e insights detalhados.
* **[jornadas de Solução de Problemas](troubleshooting.md)** - Encontre soluções para problemas comuns de jornada e práticas recomendadas para depuração.
* **[tutoriais do Jornada](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/journeys/introduction-to-building-a-journey){target="_blank"}** - Explore tutoriais em vídeo passo a passo sobre a criação de jornadas e práticas recomendadas.

