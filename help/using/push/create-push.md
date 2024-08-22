---
solution: Journey Optimizer
product: journey optimizer
title: Configurar uma notificação por push
description: Saiba como criar uma notificação por push no Journey Optimizer
feature: Push
topic: Content Management
role: User
level: Beginner
exl-id: 2ebbcd7d-dcfc-4528-974d-6230fc0dca3d
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 10%

---

# Criar uma notificação por push {#create-push-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push"
>title="Criação de mensagens por push"
>abstract="Adicione sua mensagem por push e comece a personalizá-la com o editor de personalização."

## Criar a notificação por push em uma jornada ou campanha {#create}

Para criar uma notificação por push, siga as etapas abaixo:

>[!BEGINTABS]

>[!TAB Adicionar um push a uma Jornada]

1. Abra a jornada e arraste e solte uma atividade de push da seção Ações da paleta.

   ![](assets/push_create_1.png)

1. Forneça informações básicas sobre a mensagem (rótulo, descrição, categoria) e escolha a configuração de mensagem a ser usada.

   ![](assets/push_create_2.png)

   >[!NOTE]
   >
   >Se você estiver enviando uma notificação por push de uma jornada, poderá aproveitar o recurso de Otimização de hora de envio da Adobe Journey Optimizer para prever o melhor momento para enviar a mensagem e maximizar o engajamento com base no histórico de taxas de abertura e de cliques. [Saiba como trabalhar com a Otimização de Tempo de Envio](../building-journeys/journeys-message.md#send-time-optimization)

   Para obter mais informações sobre como configurar uma jornada, consulte [esta página](../building-journeys/journey-gs.md)

1. Na tela de configuração da jornada, clique no botão **[!UICONTROL Editar conteúdo]** para configurar o conteúdo de push. [Criar uma notificação por push](design-push.md)

1. Depois que o conteúdo da mensagem for definido, você poderá usar perfis de teste para visualizar seu conteúdo.

1. Quando o push estiver pronto, conclua a configuração da [jornada](../building-journeys/journey-gs.md) para enviá-lo.

   Para acompanhar o comportamento de seus destinatários por meio de aberturas e/ou interações por push, verifique se as opções dedicadas na seção de rastreamento estão habilitadas na [atividade de email](../building-journeys/journeys-message.md).

>[!TAB Adicionar uma notificação por push a uma campanha]

1. Acesse o menu **[!UICONTROL Campanhas]** e clique em **[!UICONTROL Criar campanha]**.

1. Selecione o tipo de campanha que deseja executar

   * **Agendado - Marketing**: execute a campanha imediatamente ou em uma data especificada. As campanhas programadas são destinadas ao envio de mensagens de marketing. Eles são configurados e executados na interface do usuário do.

   * **Acionado por API - Marketing/Transacional**: execute a campanha usando uma chamada de API. As campanhas acionadas por API destinam-se ao envio de mensagens de marketing ou transacionais, ou seja, mensagens enviadas após uma ação executada por um indivíduo: redefinição de senha, compra de carrinho etc.

1. Na seção **[!UICONTROL Propriedades]**, edite o **[!UICONTROL Título]** e a **[!UICONTROL Descrição]** da sua campanha.

1. Clique no botão **[!UICONTROL Selecionar público-alvo]** para definir o público-alvo a ser direcionado na lista de públicos-alvo disponíveis do Adobe Experience Platform. [Saiba mais](../audience/about-audiences.md).

1. No campo **[!UICONTROL Namespace de identidade]**, escolha o namespace a ser usado para identificar os indivíduos do público selecionado. [Saiba mais](../event/about-creating.md#select-the-namespace).

1. Na seção **[!UICONTROL Actions]**, escolha a **[!UICONTROL Notificação por push]** e selecione ou crie uma nova configuração.

   Saiba mais sobre a configuração de push em [esta página](push-configuration.md).

   ![](assets/push_create_3.png)

1. Clique em **[!UICONTROL Criar experimento]** para começar a configurar seu experimento de conteúdo e criar tratamentos para medir seu desempenho e identificar a melhor opção para seu público-alvo. [Saiba mais](../content-management/content-experiment.md)

1. As campanhas são projetadas para serem executadas em uma data específica ou em uma frequência recorrente. Saiba como configurar o **[!UICONTROL Cronograma]** da sua campanha no [nesta seção](../campaigns/create-campaign.md#schedule).

1. No menu **[!UICONTROL Acionadores de ação]**, escolha a **[!UICONTROL Frequência]** da sua notificação por push:

   * Uma vez
   * Diariamente
   * Semanal
   * Mensal

1. Na tela de configuração da campanha, clique no botão **[!UICONTROL Editar conteúdo]** para configurar o conteúdo de push. [Criar uma notificação por push](design-push.md)

1. Depois que o conteúdo da mensagem for definido, você poderá usar perfis de teste para visualizar seu conteúdo.

1. Quando o push estiver pronto, conclua a configuração da sua [campanha](../campaigns/create-campaign.md) para enviá-lo.

   Para acompanhar o comportamento de seus destinatários por meio de aberturas e/ou interações por push, verifique se as opções dedicadas na seção de rastreamento estão habilitadas na [campanha](../campaigns/create-campaign.md).

>[!ENDTABS]

**Tópicos relacionados**

* [Configurar canal por push](push-gs.md)
* [Adicionar uma mensagem em uma jornada](../building-journeys/journeys-message.md)

## Modo de entrega rápida {#rapid-delivery}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_rapid_delivery"
>title="Modo de entrega rápida"
>abstract="O modo de entrega rápida permite que você execute o envio de mensagens de alta velocidade no canal de push para um tamanho de público inferior a 30 milhões."

O modo de entrega rápida é um complemento do [!DNL Journey Optimizer] que permite o envio muito rápido de mensagens por push em grandes volumes por meio de campanhas.

A entrega rápida é usada quando o atraso na entrega da mensagem é essencial para os negócios, quando você deseja enviar um alerta de push urgente em telefones celulares, por exemplo, notícias de última hora para usuários que instalaram seu aplicativo de canal de notícias.

Para obter mais informações sobre desempenho ao usar o modo de entrega rápida, consulte a [descrição do produto Adobe Journey Optimizer](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer.html).

### Pré-requisitos {#prerequisites}

As mensagens de delivery rápido vêm com os seguintes requisitos:

* A entrega rápida está disponível somente para campanhas **[!UICONTROL Agendadas]** e não está disponível para campanhas acionadas por API,
* Nenhuma personalização é permitida na mensagem de push,
* O público-alvo deve conter menos de 30 milhões de perfis,
* Você pode executar até 5 campanhas simultaneamente usando o modo de entrega rápida.

### Ativar modo de entrega rápida

1. Crie uma campanha de notificação por push e alterne para a opção **[!UICONTROL Entrega rápida]**.

   ![](assets/create-campaign-burst.png)

1. Configure o conteúdo da mensagem e selecione o público-alvo a ser direcionado. [Saiba como criar uma campanha](#create)

   >[!IMPORTANT]
   >
   >Verifique se o conteúdo da mensagem não inclui personalização e se o público-alvo contém menos de 30 milhões de perfis.

1. Revise e ative sua campanha como de costume. Observe que, no modo de teste, as mensagens não são enviadas pelo modo de delivery rápido.