---
title: Coleta de dados
description: Saiba mais sobre a coleção de dados de feedback do Gestão de decisões
feature: Offers
topic: Integrations
role: User
level: Intermediate
source-git-commit: b06b545d377fcd1ffe6ed218badeb94c1bb85ef2
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 1%

---

# Coleta de dados de gestão de decisão {#data-collection}

## Noções básicas sobre a coleta de dados

Você pode coletar comentários do offer decisioning no Adobe Experience Platform, incluindo quais ofertas são exibidas e como os usuários interagem com elas. Esses dados podem ser usados para:
* Composição [Relatórios de gestão de decisão](../reports/get-started-events.md);
* Usar [limite de frequência](../offer-library/add-constraints.md#capping) regras;
* Criação [Modelos de IA](../ranking/create-ranking-strategies.md) que pode ser usado como um método de classificação.

## Tipos de eventos

A forma como os dados são coletados varia de acordo com o tipo de evento que você deseja capturar.

### Eventos de decisão

Cada vez que a Gestão de decisões toma uma decisão, as informações relacionadas a esse evento de decisão são **automaticamente** enviado à Adobe Experience Platform para todos os canais. [Saiba mais](../reports/get-started-events.md)

### Eventos de impressão e clique

As impressões e os cliques da gestão de decisão são definidos da seguinte maneira:

* Um **impressão** evento é quando uma oferta é exibida a um usuário.

* A **click** evento é quando um usuário clica ou interage com uma oferta.

O feedback sobre impressões e cliques é capturado, dependendo da [!DNL Journey Optimizer] que é usado.

1. Por um lado, alguns canais **automaticamente** rastrear impressões e cliques. Elas são as seguintes:

   * Emails criados por [!DNL Journey Optimizer]
   * Notificações por push para dispositivos móveis criadas por [!DNL Journey Optimizer]
   * Aplicativos móveis que usam o [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"} ou SDK móvel<!--TBC--> para renderizar ofertas <!--need more info + link-->

   >[!NOTE]
   >
   >Se o Adobe renderizar a oferta visualmente para o usuário final no canal, você pode supor que o Adobe enviará automaticamente o feedback.

1. Por outro lado, alguns canais exigem que os dados de impressões e cliques sejam enviados para o Adobe Experience Platform como um **evento de experiência**.

   Exceto aplicativos móveis que usam o [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"} ou SDK móvel<!--TBC-->, todos os canais que usam uma solicitação de API de decisão para receber ofertas precisam de feedback enviado como um evento de experiência. Isso inclui:

   * Páginas da Web
   * Quiosques
   * Mensagens enviadas por aplicativos de terceiros

   >[!NOTE]
   >
   >Se a oferta precisar de instruções sobre como renderizar, você pode supor que deve enviar feedback como eventos de experiência.

### Eventos personalizados

Os comentários sobre eventos personalizados vinculados a uma oferta podem ser enviados para o Adobe Experience Platform de acordo com suas próprias preferências. Por exemplo, se uma oferta tiver vários botões, como *Interesse*, *Não está interessado*, etc., convém enviar esses eventos separadamente, mas eles também podem ser enviados como eventos de experiência. <!--Not sure to get that part. How feedback is collected in the first case, i.e. when events are sent in separately? Does it mean the customer just handles it the wau he wants?-->

## Envio de dados de feedback

Para enviar dados de feedback, é necessário criar um conjunto de dados para coletar eventos e, para cada tipo de evento, definir um evento de experiência que será enviado para o Adobe Experience Platform.

* Saiba como criar um conjunto de dados em que os eventos de experiência serão coletados [nesta seção](create-dataset.md).

* Saiba como definir eventos de experiência para enviar dados de feedback no [nesta seção](schema-requirement.md).

