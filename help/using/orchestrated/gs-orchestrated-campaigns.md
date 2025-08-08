---
solution: Journey Optimizer
product: journey optimizer
title: Introdução às campanhas orquestradas
description: Saiba como começar com campanhas orquestradas
short-description: Descubra recursos e casos de uso da chave de campanha orquestrada.
exl-id: 611dd06d-aa18-4fa3-a477-8a910cec21d8
source-git-commit: 86bd6a100644a0f50aa9e18fd7023dec11c05bfe
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 24%

---


# Introdução às campanhas orquestradas {#orchestrated-camp}

>[!CONTEXTUALHELP]
>id="campaigns_overview_orchestrated"
>title="campaigns_overview_orchestrated"
>abstract="<b>Orquestração de campanha</b><br/>Dividir, combinar, enriquecer e manipular conjuntos de dados relacionais para definir o público-alvo<br/><br/> <b>Aproveite dados multientidade</b><br/>Saiba como as campanhas orquestradas podem aproveitar os conjuntos de dados relacionais no enriquecimento de dados para segmentação e personalização<br/><br/><b>Segmentação ad-hoc e contagens exatas</b><br/>Crie seu segmento passo a passo com contagens exatas<br/><br/><b>Canais disponíveis</b><br/>Email, SMS, Notificações por push, Correspondência direta"

A Orquestração de Campanhas no [!DNL Adobe Journey Optimizer] possibilita campanhas de marketing sofisticadas e iniciadas pela marca em todos os canais, ajudando você a impulsionar o engajamento, a receita e a fidelidade do cliente em escala.

Embora o marketing entre canais seja essencial, as campanhas orquestradas o tornam ininterrupto. Com uma interface visual do tipo arrastar e soltar, você pode projetar e automatizar fluxos de trabalho de marketing complexos, desde a segmentação até a entrega de mensagens, em vários canais. Tudo acontece em um ambiente intuitivo, criado para oferecer velocidade, controle e eficiência.

![](assets/canvas-example-diagram.png){zoomable="yes"}

## Principais recursos

A Orquestração de campanhas é construída em torno de quatro pilares principais:

<table style="table-layout:auto">
<tr style="border: 0;">
<td><img alt="Públicos-alvo sob demanda" src="assets/do-not-localize/icon-audience.svg" width="150px"></a></td><td><b>Públicos-alvo por demanda</b><br/>Consulte instantaneamente entre conjuntos de dados para criar segmentos de público-alvo usando qualquer combinação de tipos de dados e dimensões.</td></tr>
<tr style="border: 0;">
<td><img alt="Segmentação e envio de várias entidades" src="assets/do-not-localize/icon-entity.svg" width="150px"></a></td><td><b>Segmentação e envio de várias entidades</b><br/>Vá além das campanhas com base em pessoas; use entidades como catálogos de produtos, locais de lojas ou dados de serviço para direcionar com precisão.<br/><br/>
Suportar envio de vários níveis, em que uma mensagem é enviada por Perfil e por entidade secundária associada. Essas entidades secundárias podem incluir endereços de contato, reservas, assinaturas, contratos ou outros dados vinculados. Por exemplo, isso permite que campanhas sejam enviadas para todos os endereços conhecidos de um Perfil ou para cada reserva associada a esse Perfil.</td></tr>
<tr style="border: 0;">
<td><img alt="Visibilidade e precisão de pré-envio" src="assets/do-not-localize/icon-visibility.svg" width="150px"></a></td><td><b>Visibilidade e precisão de pré-envio</b><br/>Obtenha contagens exatas de segmentação e escopo completo da campanha antes do lançamento, garantindo precisão e confiança.</td></tr>
<tr style="border: 0;">
<td><img alt="Fluxos de trabalho de campanha em várias etapas" src="assets/do-not-localize/icon-multistep.svg" width="150px"></a></td><td><b>Fluxos de trabalho de campanha em várias etapas</b><br/>Crie campanhas em várias etapas, desde mensagens diárias até campanhas complexas, como promoções sazonais ou grandes lançamentos de produtos.</td></tr>
</table>

## Campanhas e jornadas orquestradas

Embora a visualização Campanhas orquestradas tenha semelhanças com as jornadas, ela resolve diferentes objetivos e casos de uso:

* **Jornadas** - 1 a 1 tela onde cada perfil percorre as diferentes etapas em seu próprio ritmo. O estado de cada cliente é mantido em seu contexto para acionar ações em tempo real.

* **Campanhas orquestradas** - Ao contrário do jornada, as campanhas orquestradas operam usando uma tela de lote que calcula segmentos. Todos os perfis são processados juntos ao mesmo tempo.

Ambas as telas são otimizadas para seus respectivos casos de uso: a tela de Jornada publica jornadas que tendem a permanecer por um período mais longo, enquanto a tela do Campaign é projetada para execuções iterativas e incrementais de uma campanha em lote.

## O que há dentro de uma campanha orquestrada? {#gs-ms-campaign-inside}

A tela de campanha orquestrada é uma representação do que deveria acontecer. Ele descreve as várias tarefas a serem executadas e como elas estão vinculadas.

![imagem mostrando uma tela de campanha orquestrada](assets/canvas-example.png)

Cada campanha Orquestrada contém:

* **Atividades**: uma atividade é uma tarefa a ser executada. As várias atividades são representadas no diagrama por ícones. Cada atividade tem propriedades específicas e outras propriedades que são comuns a todas as atividades.

  Em um diagrama de campanha Orquestrado, uma determinada atividade pode produzir várias tarefas, principalmente quando há um loop ou ações recorrentes.

* **Transições**: as transições vinculam uma atividade de origem a uma atividade de destino e definem sua sequência.

* **Tabelas de trabalho**: as tabelas de trabalho contêm todas as informações transportadas pela transição. Cada campanha Orquestrada usa várias tabelas de trabalho. Os dados transmitidos nessas tabelas podem ser usados durante o ciclo de vida da campanha Orquestrada.

## Vamos nos aprofundar um pouco mais

Agora que você entende o que são campanhas orquestradas, é hora de se aprofundar nessas seções de documentação para começar a trabalhar com o recurso.

<table><tr style="border: 0; text-align: center;">
<td>
<a href="gs-campaign-creation.md">
<img alt="Acessar e gerenciar campanhas" src="assets/do-not-localize/workflow-access.jpeg">
</a>
<div>
<a href="gs-campaign-creation.md"><strong>Etapas de configuração</strong></a>
</div>
<p>
</td>
<td>
<a href="create-orchestrated-campaign.md">
<img alt="Lead" src="assets/do-not-localize/workflow-create.jpeg">
</a>
<div><a href="create-orchestrated-campaign.md"><strong>Criar uma campanha orquestrada</strong>
</div>
<p>
</td>
<td>
<a href="activities/about-activities.md">
<img alt="Pouco frequente" src="assets/do-not-localize/workflow-activities.jpeg">
</a>
<div>
<a href="activities/about-activities.md"><strong>Trabalhar com atividades</strong></a>
</div>
<p></td>
</tr></table>
