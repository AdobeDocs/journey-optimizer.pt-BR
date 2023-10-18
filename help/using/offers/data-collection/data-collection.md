---
title: Coleção de dados
description: Saiba mais sobre a coleção de dados de feedback do Gestão de decisões
feature: Decision Management, Datasets
topic: Integrations
role: User, Data Engineer, Developer
level: Experienced
exl-id: 278cb255-439c-4ce8-ab59-07df79774b98
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 3%

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

**Emails** criado por [!DNL Journey Optimizer] **automaticamente** rastrear impressões e cliques.

No entanto, **maioria dos canais** exigir que os dados de impressões e cliques sejam enviados para o Adobe Experience Platform como um **evento de experiência**. Isso inclui:

* Páginas da Web que usam o [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=pt-BR){target="_blank"} para renderizar ofertas

* Aplicativos móveis que usam o [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"} to render offers - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer-decisioning/#ab-sj-tracking-servers){target="_blank"}
* Quiosques
* Mensagens enviadas por aplicativos de terceiros
  <!--Mobile push notifications authored by [!DNL Journey Optimizer] - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer/api-reference/#handlenotificationresponse){target="_blank"}-->

>[!NOTE]
>
>Os canais que usam uma solicitação de API de decisão para receber ofertas precisam de feedback enviado como um evento de experiência. Em outras palavras, se a oferta precisar de instruções sobre como renderizar, você pode supor que deve enviar feedback como eventos de experiência.

### Eventos personalizados

Os comentários sobre eventos personalizados vinculados a uma oferta podem ser enviados para o Adobe Experience Platform de acordo com suas próprias preferências. Por exemplo, se uma oferta tiver vários botões, como *Interesse*, *Não está interessado*, etc., convém enviar esses eventos separadamente, mas eles também podem ser enviados como eventos de experiência.

## Envio de dados de feedback

Para enviar dados de feedback, é necessário criar um conjunto de dados para coletar eventos e, para cada tipo de evento, definir um evento de experiência que será enviado para o Adobe Experience Platform.

* Saiba como criar um conjunto de dados em que os eventos de experiência serão coletados [nesta seção](create-dataset.md).

* Saiba como definir eventos de experiência para enviar dados de feedback no [nesta seção](schema-requirement.md).
