---
title: Coleta de dados
description: Saiba mais sobre a coleta de dados de feedback do Gerenciamento de decisões
feature: Offers
topic: Integrations
role: User
level: Intermediate
source-git-commit: d690e066e5a6ec51b0cc86f9e4f375e72cd7f661
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 2%

---

# Coleta de dados da gestão de decisões {#data-collection}

## Como entender a coleta de dados

Você pode coletar comentários do offer decisioning no Adobe Experience Platform, incluindo quais ofertas são exibidas e como os usuários interagem com elas. Esses dados podem ser usados para:
* Composição [Relatórios de gestão de decisões](../reports/get-started-events.md);
* Usando [limite de frequência](../offer-library/add-constraints.md#capping) regras;
* Construção [Modelos de IA](../ranking/create-ranking-strategies.md) que pode ser usado como um método de classificação.

## Tipos de eventos

A maneira como os dados são coletados varia de acordo com o tipo de evento que você deseja capturar.

### Eventos de decisão

Sempre que a gerência de decisão tomar uma decisão, as informações relacionadas a esse evento de decisão serão **automaticamente** enviado ao Adobe Experience Platform para todos os canais. [Saiba mais](../reports/get-started-events.md)

### Eventos de impressão e clique

As impressões e os cliques do gerenciamento de decisões são definidos da seguinte maneira:

* Um **impressão** é quando uma oferta é exibida para um usuário.

* A **click** é quando um usuário clica ou interage com uma oferta.

O feedback sobre impressões e cliques é capturado dependendo do [!DNL Journey Optimizer] canal usado.

1. Por um lado, alguns canais **automaticamente** rastrear impressões e cliques. São as seguintes:

   * Emails criados por [!DNL Journey Optimizer]
   * Notificações por push em dispositivos móveis criadas por [!DNL Journey Optimizer]

   <!--If Adobe renders the offer visually to the end user on the channel, you can assume that Adobe will auto-send in the feedback.-->

1. Por outro lado, alguns canais exigem que os dados de impressões e cliques sejam enviados para o Adobe Experience Platform como um **evento de experiência**.

   Todos os canais que usam uma solicitação de API de decisão para receber ofertas precisam que o feedback seja enviado como um evento de experiência. Isso inclui:

   * Páginas da Web usando o [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=pt-BR){target="_blank"} para renderizar ofertas
   * Aplicativos para dispositivos móveis que usam o [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"} para renderizar ofertas
   * Quiosque
   * Mensagens enviadas por aplicativos de terceiros

   >[!NOTE]
   >
   >Se a oferta precisar de instruções sobre como renderizar, você pode assumir que deve enviar feedback como eventos de experiência.

### Eventos personalizados

Os comentários sobre eventos personalizados vinculados a uma oferta podem ser enviados para o Adobe Experience Platform de acordo com suas próprias preferências. Por exemplo, se uma oferta tiver vários botões, como *Interessado*, *Não interessado*, etc., você pode enviar esses eventos separadamente, mas eles também podem ser enviados como eventos de experiência. <!--Not sure to get that part. How feedback is collected in the first case, i.e. when events are sent in separately? Does it mean the customer just handles it the wau he wants?-->

## Envio de dados de feedback

Para enviar dados de feedback, é necessário criar um conjunto de dados para coletar eventos e, para cada tipo de evento, definir um evento de experiência que será enviado para o Adobe Experience Platform.

* Saiba como criar um conjunto de dados no qual os eventos de experiência serão coletados [esta seção](create-dataset.md).

* Saiba como definir eventos de experiência para enviar dados de feedback em [esta seção](schema-requirement.md).

