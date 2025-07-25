---
solution: Journey Optimizer
product: journey optimizer
title: Introdução às campanhas orquestradas
description: Saiba como começar a usar as campanhas orquestradas
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 611dd06d-aa18-4fa3-a477-8a910cec21d8
source-git-commit: 0d6e3c082032b11b38f7d4b67da1e38756b5f101
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 16%

---

# Introdução às campanhas orquestradas {#orchestrated-camp}

>[!CONTEXTUALHELP]
>id="campaigns_overview_orchestrated"
>title="campaigns_overview_orchestrated"
>abstract="<b>Orquestração de campanha</b><br/>Dividir, combinar, enriquecer e manipular conjuntos de dados relacionais para definir seu público-alvo<br/><br/> <b>Aproveite dados de várias entidades</b><br/>Saiba como as campanhas orquestradas podem aproveitar os conjuntos de dados relacionais para enriquecer dados de segmentação e personalização<br/><br/><b>Segmentação ad-hoc e contagens exatas</b><br/>Crie seu segmento passo a passo com contagens exatas<br/><br/><b>Canais disponíveis</b><br/>Email, SMS, Notificações por push, Correspondência direta"

+++ Índice 

| Bem-vindo(a) às campanhas orquestradas | Lançar a sua primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| <b>[Introdução a campanhas orquestradas](gs-orchestrated-campaigns.md)</b><br/><br/>Criar e gerenciar Esquemas e Conjuntos de Dados relacionais:</br> <ul><li>[Introdução a Esquemas e Conjuntos de Dados](gs-schemas.md)</li><li>[Esquema manual](manual-schema.md)</li><li>[Esquema de carregamento de arquivo](file-upload-schema.md)</li><li>[Assimilar dados](ingest-data.md)</li></ul>[Acesse e gerencie campanhas orquestradas](access-manage-orchestrated-campaigns.md)<br/><br/>[Etapas principais para criar uma campanha orquestrada](gs-campaign-creation.md) | [Criar e programar a campanha](create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](orchestrate-activities.md)<br/><br/>[Iniciar e monitorar a campanha](start-monitor-campaigns.md)<br/><br/>[Geração de relatórios](reporting-campaigns.md) | [Trabalhar com o construtor de regras](orchestrated-rule-builder.md)<br/><br/>[Criar a sua primeira consulta](build-query.md)<br/><br/>[Editar expressões](edit-expressions.md)<br/><br/>[Redirecionamento](retarget.md) | [Introdução às atividades](activities/about-activities.md)<br/><br/>Atividades:<br/>[Associação](activities/and-join.md) - [Criar público-alvo](activities/build-audience.md) - [Mudar dimensão](activities/change-dimension.md) - [Atividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Desduplicação](activities/deduplication.md) - [Enriquecimento](activities/enrichment.md) - [Bifurcação](activities/fork.md) - [Reconciliação](activities/reconciliation.md) - [Salvar público-alvo](activities/save-audience.md) - [Divisão](activities/split.md) - [Aguardar](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

O conteúdo desta página não é final e pode estar sujeito a alterações.

>[!ENDSHADEBOX]

A Orquestração de Campanhas no [!DNL Adobe Journey Optimizer] possibilita campanhas de marketing sofisticadas e iniciadas pela marca em todos os canais, ajudando você a impulsionar o engajamento, a receita e a fidelidade do cliente em escala.

Embora o marketing entre canais seja essencial, campanhas orquestradas o tornam ininterrupto. Com uma interface visual do tipo arrastar e soltar, você pode projetar e automatizar fluxos de trabalho de marketing complexos, desde a segmentação até a entrega de mensagens, em vários canais. Tudo acontece em um ambiente intuitivo, criado para oferecer velocidade, controle e eficiência.

![](assets/canvas-example-diagram.png){zoomable="yes"}

## Principais recursos

A Orquestração de campanhas é construída em torno de quatro pilares principais:

<table style="table-layout:auto">
<tr style="border: 0;">
<td><img alt="Públicos-alvo sob demanda" src="assets/do-not-localize/icon-audience.svg" width="50px"></a></td><td><b>Públicos-alvo por demanda</b><br/>Consulte instantaneamente entre conjuntos de dados para criar segmentos de público-alvo usando qualquer combinação de tipos de dados e dimensões.</td></tr>
<tr style="border: 0;">
<td><img alt="Segmentação e envio de várias entidades" src="assets/do-not-localize/icon-entity.svg" width="50px"></a></td><td><b>Segmentação e envio de várias entidades</b><br/>Vá além das campanhas com base em pessoas; use entidades como catálogos de produtos, locais de lojas ou dados de serviço para direcionar com precisão.<br/><br/>
Suportar envio de vários níveis, em que uma mensagem é enviada por Perfil e por entidade secundária associada. Essas entidades secundárias podem incluir endereços de contato, reservas, assinaturas, contratos ou outros dados vinculados. Por exemplo, isso permite que campanhas sejam enviadas para todos os endereços conhecidos de um Perfil ou para cada reserva associada a esse Perfil.</td></tr>
<tr style="border: 0;">
<td><img alt="Visibilidade e precisão de pré-envio" src="assets/do-not-localize/icon-visibility.svg" width="50px"></a></td><td><b>Visibilidade e precisão de pré-envio</b><br/>Obtenha contagens exatas de segmentação e escopo completo da campanha antes do lançamento, garantindo precisão e confiança.</td></tr>
<tr style="border: 0;">
<td><img alt="Fluxos de trabalho de campanha em várias etapas" src="assets/do-not-localize/icon-multistep.svg" width="50px"></a></td><td><b>Fluxos de trabalho de campanha em várias etapas</b><br/>Crie campanhas em várias etapas, desde mensagens diárias até campanhas complexas, como promoções sazonais ou grandes lançamentos de produtos.</td></tr>
</table>

## Campanhas e jornadas orquestradas

Embora a visualização de campanhas orquestradas tenha semelhanças com as jornadas, ela resolve diferentes objetivos e casos de uso:

* **Jornadas** - 1 a 1 tela onde cada perfil percorre as diferentes etapas em seu próprio ritmo. O estado de cada cliente é mantido em seu contexto para acionar ações em tempo real.

* **Campanhas orquestradas** - Ao contrário do jornada, as campanhas orquestradas operam usando uma tela de lote que calcula segmentos. Todos os perfis são processados juntos ao mesmo tempo.

Ambas as telas são otimizadas para seus respectivos casos de uso: a tela de Jornada publica jornadas que tendem a permanecer por um período mais longo, enquanto a tela do Campaign é projetada para execuções iterativas e incrementais de uma campanha em lote.

## Pré-requisitos

Antes de trabalhar com Campanhas orquestradas, é essencial garantir que você tenha as permissões apropriadas. O acesso às campanhas Orquestradas é restrito aos usuários atribuídos a um **[!UICONTROL Perfil de Produto]** relevante, como o Administrador do Orchestrated Campaign, o Aprovador do Orchestrated Campaign, o Gerente do Orchestrated Campaign ou o Visualizador do Orchestrated Campaign.

Se não conseguir acessar as funcionalidades do Orchestrated campaign, entre em contato com o administrador para solicitar as permissões necessárias.

➡️ [Saiba mais sobre perfis de produtos relacionados a Campanhas Orquestradas](../administration/ootb-product-profiles.md)

## Vamos nos aprofundar um pouco mais

Agora que você entende o que são campanhas orquestradas, é hora de se aprofundar nessas seções de documentação para começar a trabalhar com o recurso.

<table><tr style="border: 0; text-align: center;">
<td>
<a href="gs-campaign-creation.md">
<img alt="Acessar e gerenciar fluxos de trabalho" src="assets/do-not-localize/workflow-access.jpeg">
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
