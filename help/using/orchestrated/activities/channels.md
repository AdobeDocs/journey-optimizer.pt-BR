---
solution: Journey Optimizer
product: journey optimizer
title: Adicionar uma atividade de canal em uma campanha multistep
description: Saiba como adicionar uma atividade de canal em uma campanha multietapas
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: ffe1e77c-6c4f-4f23-9183-d715a4c7c402
source-git-commit: 5872e192c849b7a7909f0b50caa1331b15490d79
workflow-type: tm+mt
source-wordcount: '968'
ht-degree: 44%

---

# Atividades do canal {#channel}

+++ Sumário

| Bem-vindo às campanhas orquestradas | Iniciar sua primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](../gs-orchestrated-campaigns.md)<br/><br/>[Etapas de configuração](../configuration-steps.md)<br/><br/>[Etapas principais para a criação de campanhas orquestradas](../gs-campaign-creation.md) | [Criar uma campanha orquestrada](../create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](../orchestrate-activities.md)<br/><br/>[Enviar mensagens com campanhas orquestradas](../send-messages.md)<br/><br/>[Iniciar e monitorar a campanha](../start-monitor-campaigns.md)<br/><br/>[Relatórios](../reporting-campaigns.md) | [Trabalhar com o Query Modeler](../orchestrated-rule-builder.md)<br/><br/>[Criar sua primeira consulta](../build-query.md)<br/><br/>[Editar expressões](../edit-expressions.md) | [Introdução às atividades](about-activities.md)<br/><br/>Atividades:<br/>[And-join](and-join.md) - [Criar público](build-audience.md) - [Alterar dimensão](change-dimension.md) - [Combinar](combine.md) - [Eliminação de Duplicação](deduplication.md) - [Enriquecimento](enrichment.md) - [Bifurcação](fork.md) - [Reconciliação](reconciliation.md) - [Divisão](split.md) - [Espera](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

O Adobe Journey Optimizer permite automatizar e executar campanhas de marketing em canais de entrada e saída. Você pode combinar atividades de canal na tela de campanha orquestrada para criar campanhas orquestradas entre canais que podem acionar ações com base no comportamento do cliente e nos dados. Os canais com suporte estão listados em [esta página](../../channels/gs-channels.md).

Por exemplo, você pode criar uma campanha de email de boas-vindas que inclui uma série de mensagens em diferentes canais, como email, SMS, push e correspondência direta. Também é possível enviar um email de acompanhamento depois que alguém concluir uma compra ou enviar uma mensagem de aniversário personalizada para um cliente por SMS.

Usando atividades do canal, você pode criar campanhas abrangentes e personalizadas que envolvem clientes em vários pontos de contato e impulsionam conversões.

## Pré-requisitos {#channel-activity-prereq}

Comece a criar sua campanha orquestrada com as atividades relevantes:

* Antes de inserir uma atividade de canal, é necessário definir o público-alvo. O público-alvo é o principal alvo do delivery: os perfis que recebem as mensagens.

* Para enviar uma entrega recorrente, inicie sua campanha orquestrada com uma atividade **Scheduler**. Você também pode usar uma atividade **Scheduler** para entregas únicas e únicas para definir a data de contato para essa entrega. Essa data de contato também pode ser definida nas configurações de delivery.

## Configurar a atividade canal {#create-a-delivery-in-a-workflow}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_email"
>title="Atividade email"
>abstract="A Atividade email permite enviar emails na campanha em várias etapas, tanto mensagens únicas quanto recorrentes. Ela serve para automatizar o processo de envio de emails para um destino calculado na mesma campanha em várias etapas. É possível combinar atividades canal em uma tela da campanha em várias etapas para criar campanhas entre canais que podem acionar ações com base no comportamento e nos dados do cliente."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_sms"
>title="Atividade de SMS"
>abstract="A Atividade SMS permite enviar mensagens SMS na campanha em várias etapas, tanto mensagens únicas como recorrentes. Ela serve para automatizar o processo de envio de SMS a um destino calculado na mesma campanha em várias etapas. É possível combinar atividades canal na tela da campanha em várias etapas para criar campanhas entre canais que podem acionar ações com base no comportamento e nos dados do cliente."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_ios"
>title="Atividade push para iOS"
>abstract="A Atividade push para iOS permite enviar notificações por push do iOS como parte da campanha em várias etapas. Ela permite a entrega de campanhas com várias etapas únicas e recorrentes, automatizando o envio de notificações por push para iOS a um destino predefinido no mesmo fluxo de trabalho. É possível combinar atividades do canal na tela do fluxo de trabalho para criar fluxos de trabalho entre canais que podem acionar ações com base no comportamento e nos dados de clientes."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_android"
>title="Atividade push para Android"
>abstract="A Atividade push para Android permite enviar notificações por push do Android como parte da campanha em várias etapas. Ela permite a entrega de mensagens únicas e recorrentes, automatizando o envio de notificações por push para Android a um destino predefinido na mesma campanha em várias etapas. É possível combinar atividades canal na tela da campanha em várias etapas para criar campanhas entre canais que podem acionar ações com base no comportamento e nos dados do cliente."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_directmail"
>title="Atividade correspondência direta"
>abstract="A Atividade correspondência direta facilita o envio de correspondência direta na campanha em várias etapas para mensagens únicas e recorrentes. Ela serve para automatizar o processo de geração do arquivo de extração exigido pelos provedores de correspondência direta. É possível combinar atividades canal na tela da campanha em várias etapas para criar campanhas entre canais que podem acionar ações com base no comportamento e nos dados do cliente."

Para configurar um delivery no contexto de uma campanha orquestrada, siga as etapas abaixo:

1. Adicione uma atividade de canal: **[!UICONTROL Email]**, **[!UICONTROL SMS]**, **[!UICONTROL Notificação por push (Android)]**, **[!UICONTROL Notificação por push (iOS)]** ou **[!UICONTROL Correspondência direta]**.

1. Selecione o **Tipo de entrega**: única ou recorrente.

   * Uma **Entrega única** é uma entrega única, enviada apenas uma vez, por exemplo, um email Black Friday.
   * Uma **entrega recorrente** é enviada várias vezes com base em sua frequência de execução. Cada vez que a campanha orquestrada é executada, o público é recalculado e o delivery é enviado ao público atualizado, com o conteúdo atualizado. Pode ser um informativo semanal ou um email de aniversário recorrente, por exemplo.

1. Selecione um **Modelo** da entrega. Os modelos são configurações de entrega pré-definidas, específicas para um canal. Um modelo integrado está disponível para cada canal e é preenchido previamente por padrão.

   ![](../assets/delivery-activity-in-wf.png)

   Você pode selecionar o modelo no painel esquerdo da configuração de atividade do canal. Se o público-alvo selecionado anteriormente não for compatível com o canal, não será possível selecionar um modelo. Para resolver isso, atualize a atividade **Criar público-alvo** para selecionar um público-alvo com o target mapping correto.

1. Clique em **Criar entrega**. Você pode então definir as configurações de mensagem e o conteúdo da mesma maneira que cria um delivery independente. Também é possível testar e simular o conteúdo.

1. Volte para o fluxo de trabalho. Para continuar o fluxo de trabalho, alterne a opção **Generate an outbound transition** para adicionar uma transição após a atividade do canal.

1. Clique em **Iniciar** para iniciar sua campanha orquestrada.

   Por padrão, iniciar uma campanha orquestrada aciona a etapa de preparação da mensagem, sem enviar imediatamente a mensagem.

1. Abra a atividade do canal para confirmar o envio com o botão **Revisar e enviar**.

1. No painel de entrega, clique em **Enviar**.

## Exemplos {#cross-channel-workflow-sample}

Este é um exemplo de campanha orquestrada entre canais com uma segmentação e duas entregas. A campanha orquestrada tem como alvo todos os clientes que vivem em Paris e que estão interessados em máquinas de café. Entre essa população, um email é enviado aos clientes regulares e um SMS é enviado aos clientes VIP.

![](../assets/workflow-channel-example.png)

<!--
description, which use case you can perform (common other activities that you can link before of after the activity)

how to add and configure the activity

example of a configured activity within a workflow
The Email delivery activity allows you to configure the sending an email in a workflow. 

-->

Você também pode criar uma campanha orquestrada recorrente para enviar um SMS personalizado todos os primeiros dias do mês, às 20h, para todos os clientes que moram em Paris.

![](../assets/workflow-channel-example2.png)

<!-- Scheduled emails available?

This can be a single send email and sent just once, or it can be a recurring email.
* Single send emails are standard emails, sent once.
* Recurring emails allow you to send the same email multiple times to different targets over a defined period. You can aggregate the deliveries per period in order to get reports that correspond to your needs.

When linked to a scheduler, you can define recurring emails.
Email recipients are defined upstream of the activity in the same workflow, via an Audience targeting activity.

-->


<!--The message preparation is triggered according to the workflow execution parameters. From the message dashboard, you can select whether to request or not a manual confirmation to send the message (required by default). You can start the workflow manually or place a scheduler activity in the workflow to automate execution.-->
