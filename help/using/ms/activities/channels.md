---
solution: Journey Optimizer
product: journey optimizer
title: Adicionar uma atividade de canal em uma campanha multistep
description: Saiba como adicionar uma atividade de canal em uma campanha multietapas
hide: true
hidefromtoc: true
exl-id: ffe1e77c-6c4f-4f23-9183-d715a4c7c402
source-git-commit: 040c8387c73f9d867840225ddff6cf940cc96ac5
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 18%

---

# Atividades do canal {#channel}

O Adobe Journey Optimizer permite automatizar e executar campanhas de marketing em canais de entrada e saída. Você pode combinar atividades de canal na tela de campanha de várias etapas para criar campanhas entre canais com várias etapas, que podem acionar ações com base no comportamento e nos dados do cliente. Os canais com suporte estão listados em [esta página](../../channels/gs-channels.md).

Por exemplo, você pode criar uma campanha de email de boas-vindas que inclui uma série de mensagens em diferentes canais, como email, SMS, push e correspondência direta. Também é possível enviar um email de acompanhamento depois que alguém concluir uma compra ou enviar uma mensagem de aniversário personalizada para um cliente por SMS.

Usando atividades do canal, você pode criar campanhas abrangentes e personalizadas que envolvem clientes em vários pontos de contato e impulsionam conversões.

## Pré-requisitos {#channel-activity-prereq}

Comece a criar sua campanha em várias etapas com as atividades relevantes:

* Antes de inserir uma atividade de canal, é necessário definir o público-alvo. O público-alvo é o principal alvo do delivery: os perfis que recebem as mensagens.

* Para enviar uma entrega recorrente, inicie sua campanha em várias etapas com uma atividade **Scheduler**. Você também pode usar uma atividade **Scheduler** para entregas únicas e únicas para definir a data de contato para essa entrega. Essa data de contato também pode ser definida nas configurações de delivery. Consulte [esta seção](scheduler.md).

## Configurar uma atividade de canal {#create-a-delivery-in-a-workflow}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_email"
>title="Atividade Email"
>abstract="A atividade Email permite enviar emails em sua campanha em várias etapas, tanto para mensagens únicas quanto para mensagens recorrentes. Ele serve para automatizar o processo de envio de emails para um público-alvo calculado na mesma campanha em várias etapas. Você pode combinar atividades de canal em uma tela de campanha em várias etapas para criar campanhas entre canais que podem acionar ações com base no comportamento e nos dados do cliente."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_sms"
>title="Atividade de SMS"
>abstract="A atividade SMS permite enviar SMS em sua campanha em várias etapas, para mensagens únicas e recorrentes. Ele serve para automatizar o processo de envio de SMS para um público-alvo calculado na mesma campanha em várias etapas. Você pode combinar atividades de canal na tela de campanha em várias etapas para criar campanhas entre canais que podem acionar ações com base no comportamento e nos dados do cliente."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_ios"
>title="Atividade push para iOS"
>abstract="A atividade Push iOS permite enviar notificações por push do iOS como parte de sua campanha em várias etapas. Ela permite a entrega de campanhas únicas e recorrentes em várias etapas, automatizando o envio de notificações por push do iOS para um público-alvo predefinido no mesmo fluxo de trabalho. É possível combinar atividades do canal na tela do fluxo de trabalho para criar fluxos de trabalho entre canais que podem acionar ações com base no comportamento e nos dados de clientes."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_android"
>title="Atividade push para Android"
>abstract="A atividade de push do Android permite enviar notificações por push do Android como parte de sua campanha em várias etapas. Ele permite a entrega de mensagens únicas e recorrentes, automatizando o envio de notificações por push do Android para um público-alvo predefinido na mesma campanha multietapas. Você pode combinar atividades de canal na tela de campanha em várias etapas para criar campanhas entre canais que podem acionar ações com base no comportamento e nos dados do cliente."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_directmail"
>title="Atividade Correspondência direta"
>abstract="A atividade Correspondência direta facilita o envio de correspondência direta na campanha em várias etapas, para mensagens únicas e recorrentes. Ela serve para automatizar o processo de geração do arquivo de extração exigido pelos provedores de correspondência direta. Você pode combinar atividades de canal na tela de campanha em várias etapas para criar campanhas entre canais que podem acionar ações com base no comportamento e nos dados do cliente."

Para configurar um delivery no contexto de uma campanha em várias etapas, siga as etapas abaixo:

1. Adicione uma atividade de canal: **[!UICONTROL Email]**, **[!UICONTROL SMS]**, **[!UICONTROL Notificação por push (Android)]**, **[!UICONTROL Notificação por push (iOS)]** ou **[!UICONTROL Correspondência direta]**.

1. Selecione o **Tipo de entrega**: única ou recorrente.

   * Uma **Entrega única** é uma entrega única, enviada apenas uma vez, por exemplo, um email Black Friday.
   * Uma **entrega recorrente** é enviada várias vezes com base em sua frequência de execução definida em uma [atividade do agendador](scheduler.md). Cada vez que a campanha com várias etapas é executada, o público-alvo é recalculado e o delivery é enviado ao público atualizado, com o conteúdo atualizado. Pode ser um informativo semanal ou um email de aniversário recorrente, por exemplo.

1. Selecione um **Modelo** da entrega. Os modelos são configurações de entrega pré-definidas, específicas para um canal. Um modelo integrado está disponível para cada canal e é preenchido previamente por padrão.

   ![](../assets/delivery-activity-in-wf.png)

   Você pode selecionar o modelo no painel esquerdo da configuração de atividade do canal. Se o público-alvo selecionado anteriormente não for compatível com o canal, não será possível selecionar um modelo. Para resolver isso, atualize a atividade **Criar público-alvo** para selecionar um público-alvo com o target mapping correto.

1. Clique em **Criar entrega**. Você pode então definir as configurações de mensagem e o conteúdo da mesma maneira que cria um delivery independente. Também é possível testar e simular o conteúdo.

1. Volte para o fluxo de trabalho. Para continuar o fluxo de trabalho, alterne a opção **Generate an outbound transition** para adicionar uma transição após a atividade do canal.

1. Clique em **Iniciar** para iniciar sua campanha em várias etapas.

   Por padrão, iniciar uma campanha em várias etapas aciona a etapa de preparação da mensagem, sem enviar imediatamente a mensagem.

1. Abra a atividade do canal para confirmar o envio com o botão **Revisar e enviar**.

1. No painel de entrega, clique em **Enviar**.

## Exemplos {#cross-channel-workflow-sample}

Este é um exemplo de campanha em várias etapas entre canais com uma segmentação e dois deliveries. A campanha em várias etapas é direcionada a todos os clientes que vivem em Paris e que estão interessados em máquinas de café. Entre essa população, um email é enviado aos clientes regulares e um SMS é enviado aos clientes VIP.

![](../assets/workflow-channel-example.png)

<!--
description, which use case you can perform (common other activities that you can link before of after the activity)

how to add and configure the activity

example of a configured activity within a workflow
The Email delivery activity allows you to configure the sending an email in a workflow. 

-->

Você também pode criar uma campanha recorrente em várias etapas para enviar um SMS personalizado todos os primeiros dias do mês às 20h para todos os clientes que moram em Paris.

![](../assets/workflow-channel-example2.png)

<!-- Scheduled emails available?

This can be a single send email and sent just once, or it can be a recurring email.
* Single send emails are standard emails, sent once.
* Recurring emails allow you to send the same email multiple times to different targets over a defined period. You can aggregate the deliveries per period in order to get reports that correspond to your needs.

When linked to a scheduler, you can define recurring emails.
Email recipients are defined upstream of the activity in the same workflow, via an Audience targeting activity.

-->


<!--The message preparation is triggered according to the workflow execution parameters. From the message dashboard, you can select whether to request or not a manual confirmation to send the message (required by default). You can start the workflow manually or place a scheduler activity in the workflow to automate execution.-->
