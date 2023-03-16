---
solution: Journey Optimizer
product: journey optimizer
title: Configurar uma notificação por push
description: Saiba como criar uma notificação por push no Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 2ebbcd7d-dcfc-4528-974d-6230fc0dca3d
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 4%

---

# Criar uma notificação por push {#create-push-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push"
>title="Criação de mensagens por push"
>abstract="Adicione sua mensagem de push e comece a personalizá-la com o editor de expressão."

## Criar a notificação por push em uma jornada ou campanha {#create}

Para criar uma notificação por push, siga as etapas abaixo:

>[!BEGINTABS]

>[!TAB Adicionar um push a uma Jornada]

1. Abra a jornada e arraste e solte uma atividade de Push da seção Ações da paleta.

   ![](assets/push_create_1.png)

1. Forneça informações básicas sobre a mensagem (rótulo, descrição, categoria) e escolha a superfície da mensagem a ser usada.

   ![](assets/push_create_2.png)

   >[!NOTE]
   >
   >Se estiver enviando uma notificação por push de uma jornada, você pode aproveitar o recurso de Otimização de tempo de envio da Adobe Journey Optimizer para prever o melhor momento para enviar a mensagem para maximizar o envolvimento com base nas taxas de abertura e clique do histórico. [Saiba como trabalhar com a Otimização de tempo de envio](../building-journeys/journeys-message.md#send-time-optimization)

   Para obter mais informações sobre como configurar uma jornada, consulte [esta página](../building-journeys/journey-gs.md)

1. Na tela de configuração da jornada, clique no botão **[!UICONTROL Editar conteúdo]** para configurar o conteúdo de push. [Criar uma notificação por push](design-push.md)

1. Após definir o conteúdo da mensagem, é possível usar perfis de teste para pré-visualizá-lo e testá-lo.

1. Quando o push estiver pronto, conclua a configuração do [jornada](../building-journeys/journey-gs.md) para enviá-lo.

   Para rastrear o comportamento dos recipients por meio de aberturas e/ou interações de push, verifique se as opções dedicadas na seção de rastreamento estão habilitadas na variável [atividade de email](../building-journeys/journeys-message.md).

>[!TAB Adicionar um push a uma campanha]

1. Crie uma nova campanha agendada ou acionada por API, selecione **[!UICONTROL Notificação por push]** como sua ação e escolha o **[!UICONTROL Superfície do aplicativo]** para usar. [Saiba mais sobre a configuração de push](push-configuration.md).

   ![](assets/push_create_3.png)

1. Clique em **[!UICONTROL Criar]**.

1. No **[!UICONTROL Propriedades]** edite o **[!UICONTROL Título]** e **[!UICONTROL Descrição]**.

   ![](assets/push_create_4.png)

1. Clique no botão **[!UICONTROL Seleção do público-alvo]** para definir o público-alvo a ser direcionado a partir da lista de segmentos disponíveis do Adobe Experience Platform. [Saiba mais](../segment/about-segments.md).

1. No **[!UICONTROL Namespace de identidade]** , escolha o namespace a ser usado para identificar os indivíduos do segmento selecionado. [Saiba mais](../event/about-creating.md#select-the-namespace).

   ![](assets/push_create_5.png)

1. As campanhas são projetadas para serem executadas em uma data específica ou em uma frequência recorrente. Saiba como configurar o **[!UICONTROL Agendar]** da sua campanha em [esta seção](../campaigns/create-campaign.md#schedule).

1. No **[!UICONTROL Acionadores de ação]** escolha o **[!UICONTROL Frequência]** da sua notificação por push:

   * Uma vez
   * Diariamente
   * Semanalmente
   * Mensalmente

1. Na tela de configuração da campanha, clique no botão **[!UICONTROL Editar conteúdo]** para configurar o conteúdo de push. [Criar uma notificação por push](design-push.md)

1. Após definir o conteúdo da mensagem, é possível usar perfis de teste para pré-visualizá-lo e testá-lo.

1. Quando o push estiver pronto, conclua a configuração do [campanha](../campaigns/create-campaign.md) para enviá-lo.

   Para rastrear o comportamento dos recipients por meio de aberturas e/ou interações de push, verifique se as opções dedicadas na seção de rastreamento estão habilitadas na variável [campanha](../campaigns/create-campaign.md).

>[!ENDTABS]

**Tópicos relacionados**

* [Configurar canal de push](push-gs.md)
* [Adicionar uma mensagem em uma jornada](../building-journeys/journeys-message.md)

## Modo de entrega rápida {#rapid-delivery}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_rapid_delivery"
>title="Modo de entrega rápida"
>abstract="O modo de entrega rápida permite que você execute o envio de mensagens de alta velocidade no canal de push para um tamanho de público-alvo inferior a 30M."

O modo de entrega rápida, anteriormente conhecido como modo Burst no jornada, é um [!DNL Journey Optimizer] que permite o envio muito rápido de mensagens de push em grandes volumes por meio de campanhas.

A entrega rápida é usada quando o atraso na entrega de mensagens é essencial para os negócios, quando você deseja enviar um alerta por push urgente em telefones celulares, por exemplo, uma notícia de última hora para os usuários que instalaram seu aplicativo de canal de notícias.

Para obter mais informações sobre desempenho ao usar o modo Rapid delivery, consulte [Descrição do produto Adobe Journey Optimizer](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer.html).

### Pré-requisitos {#prerequisites}

As mensagens de delivery rápidas vêm com os seguintes requisitos:

* A entrega rápida está disponível para **[!UICONTROL Programado]** somente campanhas e não está disponível para campanhas acionadas por API,
* Nenhuma personalização é permitida na mensagem de push,
* O público-alvo deve conter menos de 30 M perfis,
* Você pode executar até 5 campanhas simultaneamente usando o modo Rapid delivery .

### Ativar modo de entrega rápida

1. Criar uma campanha de notificação por push e ativar **[!UICONTROL Entrega rápida]** opção.

![](assets/create-campaign-burst.png)

1. Configure o conteúdo da mensagem e selecione o público-alvo a ser direcionado. [Saiba como criar uma campanha](#create)

   >[!IMPORTANT]
   >
   >Certifique-se de que o conteúdo da mensagem não inclua nenhuma personalização e que o público-alvo contenha menos de 30M perfis.

1. Revise e ative sua campanha como de costume. Observe que, no modo de teste, as mensagens não são enviadas por meio do modo Rapid delivery .