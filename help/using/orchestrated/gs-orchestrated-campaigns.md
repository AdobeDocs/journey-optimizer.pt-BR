---
solution: Journey Optimizer
product: journey optimizer
title: Introdução às campanhas orquestradas
description: Saiba como começar a usar as campanhas orquestradas
short-description: Descubra os principais recursos e casos de uso de campanhas orquestradas.
exl-id: 611dd06d-aa18-4fa3-a477-8a910cec21d8
version: Campaign Orchestration
source-git-commit: 97f9c32435667fecb950892ed6f6531085055e59
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 100%

---


# Introdução às campanhas orquestradas {#orchestrated-camp}

>[!CONTEXTUALHELP]
>id="campaigns_overview_orchestrated"
>title="campaigns_overview_orchestrated"
>abstract="<b>Orquestração de campanha</b><br/>Dividir, combinar, enriquecer e manipular conjuntos de dados relacionais para definir o público-alvo<br/><br/> <b>Aproveite dados de várias entidades</b><br/>Saiba como as campanhas orquestradas podem aproveitar os conjuntos de dados relacionais no enriquecimento de dados para segmentação e personalização<br/><br/><b>Segmentação ad hoc e contagens exatas</b><br/>Crie seu segmento passo a passo com contagens exatas<br/><br/><b>Canais disponíveis</b><br/>Email, SMS, notificações por push"

A orquestração de campanhas no [!DNL Adobe Journey Optimizer] viabiliza campanhas de marketing sofisticadas e iniciadas pela marca em vários canais, ajudando a impulsionar o engajamento, a receita e a fidelidade do cliente em grande escala.

>[!IMPORTANT]
>
>Para acessar a Orquestração de campanha, sua licença deve incluir o pacote **Journey Optimizer – Campanhas e jornadas** ou **Journey Optimizer – Campanhas**. Entre em contato com o representante da Adobe para confirmar sua licença e atualizá-la, se necessário.

Embora o marketing entre canais seja essencial, as campanhas orquestradas permitem que ele flua melhor. Com uma interface visual do tipo arrastar e soltar, você pode projetar e automatizar fluxos de trabalho de marketing complexos, desde a segmentação até a entrega de mensagens, em vários canais. Tudo acontece em um ambiente intuitivo, criado para proporcionar velocidade, controle e eficiência.

![](assets/canvas-example-diagram.png){zoomable="yes"}

➡️ [Descubra campanhas orquestradas nesse vídeo](#video-oc)

## Principais recursos

A Orquestração de campanhas é construída em torno de quatro pilares principais:

<table style="table-layout:auto">
<tr style="border: 0;">
<td><img alt="Públicos-alvo sob demanda" src="assets/do-not-localize/icon-audience.svg" width="150px"></a></td><td><b>Públicos-alvo sob demanda</b><br/>Consulte instantaneamente os conjuntos de dados para criar segmentos de público-alvo usando qualquer combinação de tipos de dados e dimensões.</td></tr>
<tr style="border: 0;">
<td><img alt="Segmentação e envio de várias entidades" src="assets/do-not-localize/icon-entity.svg" width="150px"></a></td><td><b>Segmentação e envio de várias entidades</b><br/>Vá além das campanhas com base em pessoas: use entidades como catálogos de produtos, locais de armazenamento ou dados de serviço para direcionar com precisão.<br/><br/>
Dá suporte ao envio de vários níveis, em que uma mensagem é enviada por perfil e por entidade secundária associada. Essas entidades secundárias podem incluir endereços de contato, reservas, assinaturas, contratos ou outros dados vinculados. Por exemplo, isso permite que campanhas sejam enviadas para todos os endereços conhecidos de um perfil ou para cada reserva associada a esse perfil.</td></tr>
<tr style="border: 0;">
<td><img alt="Visibilidade e precisão de pré-envio" src="assets/do-not-localize/icon-visibility.svg" width="150px"></a></td><td><b>Visibilidade e precisão de pré-envio</b><br/>Obtenha contagens exatas de segmentação e o escopo completo da campanha antes do lançamento, garantindo precisão e confiança.</td></tr>
<tr style="border: 0;">
<td><img alt="Fluxos de trabalho da campanha em várias etapas" src="assets/do-not-localize/icon-multistep.svg" width="150px"></a></td><td><b>Fluxos de trabalho da campanha em várias etapas</b><br/>Crie campanhas em várias etapas, desde mensagens diárias até campanhas complexas, como promoções sazonais ou grandes lançamentos de produtos.</td></tr>
</table>


>[!NOTE]
>
>Os canais com suporte são: [Email](../email/get-started-email.md), [SMS/MMS/RCS](../sms/get-started-sms.md), [Notificações por push](../push/get-started-push.md).
>
>Os canais disponíveis variam com base no modelo de licenciamento e nos complementos.

## Campanhas orquestradas e jornadas

Embora a visualização de campanhas orquestradas tenha semelhanças com as jornadas, ela tem diferentes objetivos e casos de uso:

* **Jornadas** - tela 1 para 1 onde cada perfil percorre as diferentes etapas em seu próprio ritmo. O estado de cada cliente é mantido em seu contexto para iniciar ações em tempo real.

* **Campanhas orquestradas** - Ao contrário de jornadas, as campanhas orquestradas operam usando uma tela em lote que calcula segmentos. Todos os perfis são processados juntos e ao mesmo tempo.

Ambas as telas são otimizadas para seus respectivos casos de uso: a tela de jornada publica jornadas que tendem a permanecer por um período mais longo, enquanto a tela de campanha é projetada para execuções iterativas e incrementais de uma campanha em lote.

## O que há dentro de uma campanha orquestrada? {#gs-ms-campaign-inside}

A tela da campanha orquestrada é uma representação do que deve acontecer. Ela descreve as várias tarefas a serem executadas e como elas estão vinculadas.

![imagem mostrando a tela de uma campanha orquestrada](assets/canvas-example.png)

Cada campanha orquestrada contém:

* **Atividades**: uma atividade é uma tarefa a ser executada. As [várias atividades](activities/about-activities.md) são representadas na tela por ícones. Cada atividade tem propriedades específicas e outras propriedades que são comuns a todas as atividades.

  Na tela de uma campanha orquestrada, uma determinada atividade pode gerar várias tarefas, principalmente quando há um ciclo ou ações recorrentes.

* **Transições**: as transições vinculam uma atividade de origem a uma atividade de destino e definem sua sequência.

* **Tabelas de trabalho**: as tabelas de trabalho contêm todas as informações transportadas pela transição. Cada campanha orquestrada usa várias tabelas de trabalho. Os dados transmitidos nessas tabelas podem ser usados durante todo o ciclo de vida da campanha orquestrada.


## Vídeo de introdução {#video-oc}

Saiba mais sobre os principais conceitos e recursos disponíveis com campanhas orquestradas.


>[!VIDEO](https://video.tv.adobe.com/v/3471538/?learn=on&enablevpops)


## Vamos nos aprofundar um pouco mais

Agora que você entende o que são campanhas orquestradas, é hora de se aprofundar nestas seções da documentação para começar a trabalhar com o recurso.

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
