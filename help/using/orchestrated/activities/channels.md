---
solution: Journey Optimizer
product: journey optimizer
title: Adicionar uma atividade de canal a uma campanha em várias etapas
description: Saiba como adicionar uma atividade de canal a uma campanha em várias etapas
exl-id: ffe1e77c-6c4f-4f23-9183-d715a4c7c402
version: Campaign Orchestration
source-git-commit: 2bdabace34546bd27c2e3c19a3aee3c8a3eae5f2
workflow-type: tm+mt
source-wordcount: '1126'
ht-degree: 57%

---


# Atividades do canal {#channel}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_email"
>title="Atividade de email"
>abstract="A atividade Email permite enviar emails na campanha Orquestrada para mensagens únicas e recorrentes. Ela serve para automatizar o processo de envio de emails a um público-alvo calculado na mesma campanha orquestrada. É possível combinar atividades canal em uma tela da campanha em várias etapas para criar campanhas entre canais que podem acionar ações com base no comportamento e nos dados do cliente."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_sms"
>title="Atividade de SMS"
>abstract="A atividade SMS permite enviar SMS em sua campanha Orquestrada para mensagens únicas e recorrentes. Ela serve para automatizar o processo de envio de SMS a um público-alvo calculado na mesma campanha orquestrada. É possível combinar atividades de canal na tela da campanha em várias etapas para criar campanhas entre canais que possam acionar ações com base no comportamento e nos dados do cliente."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push"
>title="Atividade de push"
>abstract="A atividade Push permite enviar notificações por push como parte da campanha orquestrada. Ele permite a entrega de campanhas orquestradas únicas e recorrentes, automatizando o envio de notificações por push para um destino predefinido na mesma campanha orquestrada. É possível combinar atividades de canal na tela da campanha para criar campanhas entre canais que podem acionar ações com base no comportamento e nos dados do cliente."

<!--
UNUSED IDs in BJ

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_ios"
>title="Push iOS activity"
>abstract="The Push iOS activity lets you send iOS Push notifications as part of your Orchestrated campaign. It enables the delivery of both one-time and recurring Orchestrated campaigns, automating the sending of iOS Push notifications to a predefined target within the same workflow. You can combine channel activities into the campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_android"
>title="Push Android activity"
>abstract="The Push Android activity lets you send Android Push notifications as part of your Orchestrated campaign. It enables the delivery of both one-time and recurring messages, automating the sending of Android Push notifications to a predefined target within the same Orchestrated campaign. You can combine channel activities into the Orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data."

-->

>[!CONTEXTUALHELP]
>id="ajo_orchestration_directmail"
>title="Atividade de correspondência direta"
>abstract="A Atividade correspondência direta facilita o envio de correspondência direta na campanha orquestrada, tanto para mensagens únicas quanto recorrentes. Ela serve para automatizar o processo de geração do arquivo de extração exigido pelos provedores de correspondência direta. É possível combinar atividades de canal na tela da campanha orquestrada para criar campanhas entre canais que podem acionar ações com base no comportamento e nos dados do cliente."

O [!DNL Adobe Journey Optimizer] permite automatizar e executar campanhas de marketing em vários canais: email, SMS e notificações por push. Você pode combinar essas atividades de canal na tela da campanha para criar campanhas orquestradas entre canais. Essas campanhas podem acionar ações com base no comportamento e nos dados do cliente.

Por exemplo:

* Envie uma série de boas-vindas por email, SMS e push.
* Envie um email de acompanhamento pós-compra.
* Envie saudações de aniversário personalizadas por SMS.

Usando atividades do canal, você pode criar campanhas abrangentes e personalizadas que envolvem clientes em vários pontos de contato e impulsionam conversões.

>[!CAUTION]
>
>Somente os canais SMS, Push e Email são compatíveis com campanhas orquestradas.

## Adicionar uma atividade de canal e definir suas propriedades {#add}

>[!PREREQUISITES]
>
>Antes de adicionar uma atividade de canal, defina o público-alvo usando uma atividade [Criar público-alvo](build-audience.md) ou [Ler público](read-audience.md).

1. Adicione uma atividade de canal à tela. As atividades de canal disponíveis são **[!UICONTROL Email]**, **[!UICONTROL SMS]** e **[!UICONTROL Push]**.

   ![imagem mostrando a tela com as atividades disponíveis](../assets/channel-add.png)

1. Selecione a atividade e clique em **[!UICONTROL Editar email]**, **[!UICONTROL Editar SMS]** ou **[!UICONTROL Editar push]**, dependendo do canal escolhido.

   ![imagem mostrando a tela com uma atividade de email](../assets/channel-edit.png)

1. Na guia **[!UICONTROL Propriedades]**, insira uma descrição e alterne para a guia **[!UICONTROL Ações]** para configurar a atividade.

## Definir a configuração e as configurações do canal {#configuration}

Use a guia **[!UICONTROL Ações]** para selecionar uma configuração de canal para a sua mensagem e definir configurações adicionais, como rastreamento, experimento de conteúdo ou conteúdo multilíngue.

1. **Selecionar uma configuração de canal**

   Uma configuração é definida por um [Administrador do sistema](../../start/path/administrator.md). Ela contém todos os parâmetros técnicos para enviar a mensagem, como parâmetros de cabeçalho, subdomínio, aplicativos móveis etc. [Saiba como definir configurações de canal](../../configuration/channel-surfaces.md)

   ![imagem mostrando a seção de ações](../assets/channel-actions.png)

1. **Aplicar regras de limitação**

   Na lista suspensa **[!UICONTROL Conjunto de regras]**, selecione um conjunto de regras de canal para aplicar regras de limitação à sua campanha. O uso de conjuntos de regras de canal permite definir o limite de frequência por tipo de comunicação para evitar sobrecarga de clientes com mensagens semelhantes. [Saiba como trabalhar com conjuntos de regras](../../conflict-prioritization/rule-sets.md)

1. **Rastrear engajamento** (Email e SMS)

   Use a seção de **[!UICONTROL Rastreamento de ações]** para acompanhar como os seus destinatários reagem às suas entregas de email ou SMS. Os resultados do rastreamento podem ser acessados no relatório da campanha após a execução da campanha. [Saiba mais sobre os relatórios da campanha](../../reports/campaign-global-report-cja.md)

1. **Habilitar o modo de entrega rápida** (push)

   O modo de entrega rápida é um complemento do [!DNL Journey Optimizer] que permite um envio muito rápido de mensagens por push em grandes volumes por meio das campanhas. A entrega rápida é usada quando o atraso na entrega da mensagem é essencial para os negócios. Por exemplo, você deseja enviar um alerta de push urgente em telefones celulares, como notícias de última hora para usuários que instalaram seu aplicativo de canal de notícias. Saiba como habilitar o modo de entrega rápida para notificações por push [nesta página](../../push/create-push.md#rapid-delivery).

   Para mais informações sobre desempenho ao usar o modo de entrega rápida, consulte a [descrição do produto Adobe Journey Optimizer](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

1. **Criar um experimento de conteúdo**

   Use a seção de **[!UICONTROL Experimento de conteúdo]** para definir vários tratamentos de entrega a fim de medir qual apresenta o melhor desempenho para o seu público-alvo. Clique no botão **[!UICONTROL Criar experimento]** e siga as etapas detalhadas nesta seção: [Criar um experimento de conteúdo](../../content-management/content-experiment.md).

1. **Adicionar conteúdo multilíngue**

   Use a seção **[!UICONTROL Idiomas]** para criar conteúdo em vários idiomas dentro da sua campanha. Para isso, clique no botão **[!UICONTROL Adicionar idiomas]** e selecione as **[!UICONTROL Configurações de idioma]** desejadas. Informações detalhadas sobre como configurar e usar recursos multilíngues estão disponíveis nesta seção: [Introdução ao conteúdo multilíngue](../../content-management/multilingual-gs.md).

   ![imagem mostrando a seção de experimento de conteúdo](../assets/channel-experiment.png)

Quando a atividade do seu canal for configurada, selecione a guia **[!UICONTROL Conteúdo]** para definir seu conteúdo.

## Definição do conteúdo {#content}

Alterne para a guia **[!UICONTROL Conteúdo]** para criar a sua mensagem. As etapas do processo variam de acordo com o canal selecionado. Confira as etapas detalhadas para criar o conteúdo da sua mensagem nas páginas a seguir.

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;" >
<td><a href="../../email/create-email.md"><img alt="email" src="../../channels/assets/do-not-localize/email.png"></a><br/><a href="../../email/create-email.md"><strong>Criar um email</strong></a></td>
<td><a href="../../sms/create-sms.md"><img alt="SMS" src="../../channels/assets/do-not-localize/sms.png"></a><br/><a href="../../sms/create-sms.md"><strong>Criar um SMS</strong></a></td>
<td><a href="../../push/create-push.md"><img alt="push" src="../../channels/assets/do-not-localize/push.png"></a><a href="../../push/create-push.md"><strong>Criar uma notificação por push</strong></a></td>
</tr></table>

## Adicionar personalização

O Personalization em campanhas orquestradas funciona de forma semelhante a outras campanhas ou jornadas do **[!UICONTROL Journey Optimizer]**. No entanto, há algumas diferenças principais específicas para a tela orquestrada.

Ao acessar o editor de personalização por meio de uma campanha Orquestrada, duas pastas principais contêm atributos disponíveis para personalização detalhados abaixo.

* **[!UICONTROL Atributos do perfil]**

  Esta pasta inclui todos os dados relacionados ao perfil de [!DNL Adobe Experience Platform]. Esses são atributos padrão, como nome, endereço de email, localização ou quaisquer outras características capturadas no perfil do usuário.

* **[!UICONTROL Atributos do público-alvo]** (específicos para campanhas orquestradas)

  Essa pasta é exclusiva das Campanhas orquestradas. Ele contém atributos calculados diretamente na tela da campanha. Ele contém duas subpastas:

   * **`<Targeting dimension>`** (por exemplo, &quot;Recipients&quot;, &quot;Purchases&quot;): contém todos os atributos relacionados à dimensão direcionada pela campanha.

   * **`Enrichment`**: Inclui dados adicionados por meio de atividades de **[!UICONTROL Enriquecimento]** na tela. Isso permite personalizar mensagens com base em conjuntos de dados externos ou em lógica adicional incorporada durante a orquestração. [Saiba como usar uma atividade de Enriquecimento](../activities/enrichment.md)

Para obter uma visão geral detalhada de como usar o editor de personalização, consulte [Introdução à personalização](../../personalization/personalize.md).

## Verificar e testar o conteúdo

Depois que o conteúdo for criado, use o botão **[!UICONTROL Simular conteúdo]** para visualizar e testar o seu conteúdo com perfis de teste ou dados de entrada de amostra carregados de um arquivo CSV/JSON ou adicionados manualmente. [Saiba mais](../../content-management/preview-test.md)

![imagem mostrando o botão de simular conteúdo](../assets/channel-simulate.png)

## Próximas etapas {#next}

Quando o conteúdo da mensagem estiver pronto, navegue de volta para a campanha Orquestrada usando a seta **[!UICONTROL Voltar]**. Em seguida, você pode concluir a orquestração de atividades na tela e publicar a campanha para iniciar o envio das mensagens. [Saiba como iniciar e monitorar campanhas orquestradas](../start-monitor-campaigns.md)

![imagem mostrando o botão de voltar](../assets/channel-back.png)

<!--
## Examples {#cross-channel-workflow-sample}

Here is a cross-channel Orchestrated campaign example with a segmentation and two deliveries. The Orchestrated campaign targets all customers who live in Paris and who are interested in coffee machines. Among this population, an email is sent to the regular customers and an SMS is sent to the VIP clients.

![](../assets/workflow-channel-example.png)

<!--
description, which use case you can perform (common other activities that you can link before of after the activity)

how to add and configure the activity

example of a configured activity within a workflow
The Email delivery activity allows you to configure the sending an email in a workflow. 

-->

<!--You can also create a recurring Orchestrated campaign to send a personalized SMS every first day of the month at 8 PM to all customers living in Paris.

![](../assets/workflow-channel-example2.png)-->

<!-- Scheduled emails available?

This can be a single send email and sent just once, or it can be a recurring email.
* Single send emails are standard emails, sent once.
* Recurring emails allow you to send the same email multiple times to different targets over a defined period. You can aggregate the deliveries per period in order to get reports that correspond to your needs.

When linked to a scheduler, you can define recurring emails.
Email recipients are defined upstream of the activity in the same workflow, via an Audience targeting activity.

-->


<!--The message preparation is triggered according to the workflow execution parameters. From the message dashboard, you can select whether to request or not a manual confirmation to send the message (required by default). You can start the workflow manually or place a scheduler activity in the workflow to automate execution.-->

