---
solution: Journey Optimizer
product: journey optimizer
title: Adicionar uma atividade de canal em uma campanha multistep
description: Saiba como adicionar uma atividade de canal em uma campanha multietapas
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: ffe1e77c-6c4f-4f23-9183-d715a4c7c402
source-git-commit: cfb09467809a69516c34d52be3f41e7a1abdb7c3
workflow-type: tm+mt
source-wordcount: '985'
ht-degree: 17%

---

# Atividades do canal {#channel}

+++ Sumário

| Bem-vindo às campanhas orquestradas | Lançar a primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](../gs-orchestrated-campaigns.md)<br/><br/>[Etapas de configuração](../configuration-steps.md)<br/><br/>[Etapas principais para a criação de campanhas orquestradas](../gs-campaign-creation.md) | [Criar uma campanha orquestrada](../create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](../orchestrate-activities.md)<br/><br/><br/>[Iniciar e monitorar a campanha](../start-monitor-campaigns.md)<br/><br/>[Relatórios](../reporting-campaigns.md) | [Trabalhar com o Query Modeler](../orchestrated-rule-builder.md)<br/><br/>[Criar sua primeira consulta](../build-query.md)<br/><br/>[Editar expressões](../edit-expressions.md) | [Introdução às atividades](about-activities.md)<br/><br/>Atividades:<br/>[And-join](and-join.md) - [Criar público](build-audience.md) - [Alterar dimensão](change-dimension.md) - **[Atividades de canal](channels.md)** - [Combinar](combine.md) - [Eliminação de Duplicação](deduplication.md) - [Enriquecimento](enrichment.md) - [Bifurcação](fork.md) - [Reconciliação](reconciliation.md) - [Divisão](split.md) - [Aguardar](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

O [!DNL Adobe Journey Optimizer] permite automatizar e executar campanhas de marketing em canais. Você pode combinar atividades de canal na tela de campanha orquestrada para criar campanhas orquestradas entre canais que podem acionar ações com base no comportamento do cliente e nos dados.

Por exemplo, você pode criar uma campanha de email de boas-vindas que inclui uma série de mensagens em diferentes canais, como email, SMS e push. Também é possível enviar um email de acompanhamento depois que alguém concluir uma compra ou enviar uma mensagem de aniversário personalizada para um cliente por SMS.

Usando atividades de canal, você pode criar campanhas abrangentes e personalizadas que envolvem clientes em vários pontos de contato e geram conversões. Os canais compatíveis são Email, SMS e Push.

## Pré-requisitos {#channel-activity-prereq}

Comece a criar sua campanha orquestrada com as atividades relevantes:

* Antes de inserir uma atividade de canal, é necessário definir o público-alvo. O público-alvo é o principal alvo do delivery: os perfis que recebem as mensagens. [Saiba como usar a atividade Criar público-alvo](build-audience.md)

* Para enviar uma entrega recorrente, inicie sua campanha orquestrada com uma atividade **[!UICONTROL Scheduler]**. Você também pode usar uma atividade **[!UICONTROL Scheduler]** para entregas únicas e únicas para definir a data de contato para essa entrega. Essa data de contato também pode ser definida nas configurações de delivery. [Saiba como agendar uma campanha orquestrada](../create-orchestrated-campaign.md#schedule)

## Configurar a atividade canal {#create-a-delivery-in-a-workflow}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_email"
>title="Atividade email"
>abstract="A atividade Email permite enviar emails em sua campanha orquestrada, tanto para mensagens únicas quanto recorrentes. Ele serve para automatizar o processo de envio de emails para um público-alvo calculado na mesma campanha orquestrada. É possível combinar atividades canal em uma tela da campanha em várias etapas para criar campanhas entre canais que podem acionar ações com base no comportamento e nos dados do cliente."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_sms"
>title="Atividade de SMS"
>abstract="A atividade de SMS permite enviar SMS em sua campanha orquestrada, para mensagens recorrentes e únicas. Ele serve para automatizar o processo de envio de SMS para um público-alvo calculado na mesma campanha orquestrada. É possível combinar atividades canal na tela da campanha em várias etapas para criar campanhas entre canais que podem acionar ações com base no comportamento e nos dados do cliente."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push"
>title="Atividade de push"
>abstract="A atividade Push permite enviar notificações por push como parte da campanha orquestrada. Ela permite a entrega de campanhas orquestradas únicas e recorrentes, automatizando o envio de notificações por push para um público-alvo predefinido na mesma campanha orquestrada. Você pode combinar atividades de canal na tela da campanha para criar campanhas entre canais que podem acionar ações com base no comportamento e nos dados do cliente."

<!--
UNUSED IDs in BJ

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_ios"
>title="Push iOS activity"
>abstract="The Push iOS activity let you send iOS Push notifications as part of your orchestrated campaign. It enables the delivery of both one-time and recurring orchestrated campaigns, automating the sending iOS Push notifications to a predefined target within the same workflow. You can combine channel activities into the campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_android"
>title="Push Android activity"
>abstract="The Push Android activity ket you send Android Push notifications as part of your orchestrated campaign. It enables the delivery of both one-time and recurring messages, automating the sending Android Push notifications to a predefined target within the same orchestrated campaign. You can combine channel activities into the orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data."

-->

>[!CONTEXTUALHELP]
>id="ajo_orchestration_directmail"
>title="Atividade correspondência direta"
>abstract="A atividade de correspondência direta facilita o envio de correspondência direta dentro da campanha orquestrada, para mensagens recorrentes e únicas. Ela serve para automatizar o processo de geração do arquivo de extração exigido pelos provedores de correspondência direta. Você pode combinar atividades de canal na tela de campanha orquestrada para criar campanhas entre canais que podem acionar ações com base no comportamento do cliente e nos dados."

Para configurar um delivery no contexto de uma campanha orquestrada, siga as etapas abaixo.

### Adicionar uma atividade de canal e definir suas propriedades {#add}

1. Adicione uma atividade de canal na tela. As atividades de canal disponíveis são **[!UICONTROL Email]**, **[!UICONTROL SMS]** e **[!UICONTROL Push]**.

   ![imagem mostrando a tela com atividades disponíveis](../assets/channel-add.png)

1. Selecione a atividade adicionada e clique no botão **[!UICONTROL Editar email]**, **[!UICONTROL Editar SMS]** ou **[!UICONTROL Editar push]**, dependendo do canal escolhido.

   ![imagem mostrando a tela com uma atividade Email](../assets/channel-edit.png)

1. Na guia **[!UICONTROL Propriedades]**, insira uma descrição para a campanha.

### Definir as configurações do canal {#configuration}

1. Selecione a guia **[!UICONTROL Ações]** e escolha a configuração de canal a ser usada para a mensagem.

   Uma configuração foi definida por um [Administrador do Sistema](../../start/path/administrator.md). Ela contém todos os parâmetros técnicos para enviar a mensagem, como parâmetros de cabeçalho, subdomínio, aplicativos móveis etc. [Saiba como definir configurações de canal](../../configuration/channel-surfaces.md).

1. Para email e SMS, use as opções de rastreamento para monitorar como os recipients reagem aos deliveries de email ou SMS.

   Os resultados do rastreamento podem ser acessados no relatório da campanha após a execução da campanha. [Saiba mais sobre relatórios de campanha](../../reports/campaign-global-report-cja.md)

1. Para notificações por push, use a opção **[!UICONTROL Modo de entrega rápida]** para enviar mensagens em alta velocidade em um canal de push para um público-alvo de tamanho inferior a 30 milhões.

   O modo de entrega rápida é um complemento do **[!DNL Journey Optimizer]** que permite o envio muito rápido de mensagens por push em grandes volumes. [Saiba mais](../../push/create-push.md#rapid-delivery)

1. A seção **[!UICONTROL Experimento de conteúdo]** permite definir vários tratamentos de entrega para medir qual deles tem melhor desempenho para o público-alvo.

   Para fazer isso, clique no botão **[!UICONTROL Criar experimento]** e siga as etapas detalhadas nesta seção: [Criar recursos de experimentação de conteúdo](../../content-management/content-experiment.md).

1. A seção **[!UICONTROL Languages]** permite que você crie conteúdo em vários idiomas dentro da campanha.

   Para fazer isso, clique no botão **[!UICONTROL Adicionar idiomas]** e selecione as **[!UICONTROL configurações de idioma]** desejadas. Informações detalhadas sobre como configurar e usar recursos multilíngues estão disponíveis nesta seção: [Introdução a conteúdo multilíngue](../../content-management/multilingual-gs.md)

### Definição do conteúdo {#content}

Selecione a guia **[!UICONTROL Content]** para definir o conteúdo da mensagem. O processo de criação de conteúdo depende do canal selecionado.

Saiba mais sobre as etapas detalhadas para criar o conteúdo da mensagem nas seguintes páginas:

<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../../email/create-email.md"><img alt="email" src="../../channels/assets/do-not-localize/email.png"></a>
<div align="center"><a href="../../email/create-email.md"><strong>Email</strong></a></div></td>
<td><a href="../../sms/create-sms.md"><img alt="SMS" src="../../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><a href="../../sms/create-sms.md"><strong>SMS</strong></a></div></td>
<td><a href="../../push/create-push.md"><img alt="push" src="../../channels/assets/do-not-localize/push.png"></a>
<div align="center"><a href="../../push/create-push.md"><strong>Notificação por push</strong></a></div></td>
</tr></table>

Depois que o conteúdo for definido, use o botão **[!UICONTROL Simular conteúdo]** para visualizar e testar o conteúdo com perfis de teste ou dados de entrada de amostra carregados de um arquivo CSV/JSON ou adicionados manualmente. [Saiba mais](../../content-management/preview-test.md)

## Próximas etapas {#next}

Volte para sua campanha orquestrada usando a seta **[!UICONTROL Voltar]**.

![imagem mostrando o botão Voltar](../assets/channel-back.png)

Agora é possível concluir a orquestração de atividades na tela e publicar a campanha para iniciar o envio das mensagens. [Saiba como iniciar e monitorar campanhas orquestradas](../start-monitor-campaigns.md)

<!--
## Examples {#cross-channel-workflow-sample}

Here is a cross-channel orchestrated campaign example with a segmentation and two deliveries. The orchestrated campaign targets all customers who live in Paris and who are interested in coffee machines. Among this population, an email is sent to the regular customers and an SMS is sent to the VIP clients.

![](../assets/workflow-channel-example.png)

<!--
description, which use case you can perform (common other activities that you can link before of after the activity)

how to add and configure the activity

example of a configured activity within a workflow
The Email delivery activity allows you to configure the sending an email in a workflow. 

-->

<!--You can also create a recurring orchestrated campaign to send a personalized SMS every first day of the month at 8 PM to all customers living in Paris.

![](../assets/workflow-channel-example2.png)-->

<!-- Scheduled emails available?

This can be a single send email and sent just once, or it can be a recurring email.
* Single send emails are standard emails, sent once.
* Recurring emails allow you to send the same email multiple times to different targets over a defined period. You can aggregate the deliveries per period in order to get reports that correspond to your needs.

When linked to a scheduler, you can define recurring emails.
Email recipients are defined upstream of the activity in the same workflow, via an Audience targeting activity.

-->


<!--The message preparation is triggered according to the workflow execution parameters. From the message dashboard, you can select whether to request or not a manual confirmation to send the message (required by default). You can start the workflow manually or place a scheduler activity in the workflow to automate execution.-->
