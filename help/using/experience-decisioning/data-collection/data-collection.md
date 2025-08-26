---
title: Coleção de dados
description: Saiba mais sobre a coleção de dados de feedback do Gestão de decisões
feature: Decision Management, Datasets
topic: Integrations
role: User, Data Engineer, Developer
level: Experienced
hide: true
hidefromtoc: true
exl-id: 32e3a5b9-0633-48df-95b5-c03536be23a1
source-git-commit: 58f4fdf8ec3cdb609efebf5b8713f6b770ef5414
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 1%

---

# Coleta de dados de gestão de decisão {#data-collection}

## Noções básicas sobre a coleta de dados

Você pode coletar comentários do Offer Decisioning no Adobe Experience Platform, incluindo quais ofertas são exibidas e como os usuários interagem com elas. Esses dados podem ser usados para:

* Compondo [relatórios de decisão](../cja-reporting.md);
* Usando regras de [limite](../items.md#capping);
* Compilando [modelos de IA](../ranking/ai-models.md) que podem ser usados como um método de classificação.

## Tipos de eventos

A forma como os dados são coletados varia de acordo com o tipo de evento que você deseja capturar.

### Eventos de decisão

Cada vez que a Decisão toma uma decisão, as informações relacionadas a esse evento de decisão são **automaticamente** enviadas para a Adobe Experience Platform. <!--TBC + link-->

### Eventos de impressão e clique

As impressões e os cliques da gestão de decisão são definidos da seguinte maneira:

* Um evento **impressão** ocorre quando uma oferta é exibida a um usuário.

* Um evento de **clique** é quando um usuário clica ou interage com uma oferta.

O feedback sobre impressões e cliques é capturado dependendo do canal [!DNL Journey Optimizer] que é usado.

**Os emails** criados por [!DNL Journey Optimizer] **automaticamente** rastreiam impressões e cliques.

No entanto, **a maioria dos canais** exige que os dados de impressões e cliques sejam enviados para o Adobe Experience Platform como um **evento de experiência**. Isso inclui:

* Páginas da Web que usam o [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=pt-BR){target="_blank"} para renderizar ofertas

* Aplicativos móveis que usam o [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html?lang=pt-BR){target="_blank"} para renderizar ofertas - [Saiba mais](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer-decisioning/#ab-sj-tracking-servers){target="_blank"}
* Quiosques
* Mensagens enviadas por aplicativos de terceiros
  <!--Mobile push notifications authored by [!DNL Journey Optimizer] - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer/api-reference/#handlenotificationresponse){target="_blank"}-->

>[!NOTE]
>
>Os canais que usam uma solicitação de API de decisão para receber ofertas precisam de feedback enviado como um evento de experiência. Em outras palavras, se a oferta precisar de instruções sobre como renderizar, você pode supor que deve enviar feedback como eventos de experiência.

### Eventos personalizados

Os comentários sobre eventos personalizados vinculados a uma oferta podem ser enviados para o Adobe Experience Platform de acordo com suas próprias preferências. Por exemplo, se uma oferta tiver vários botões, como *Interessado*, *Não interessado* etc., você poderá enviar esses eventos separadamente, mas eles também poderão ser enviados como eventos de experiência.

## Envio de dados de feedback

Para enviar dados de feedback, é necessário criar um conjunto de dados para coletar eventos e, para cada tipo de evento, definir um evento de experiência que será enviado para o Adobe Experience Platform.

* Saiba como criar um conjunto de dados em que os eventos de experiência serão coletados em [esta seção](create-dataset.md).

* Saiba como definir eventos de experiência para enviar dados de feedback em [esta seção](schema-requirement.md).
