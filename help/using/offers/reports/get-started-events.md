---
title: Introdução aos eventos de Gerenciamento de decisão
description: Saiba como criar relatórios do Gestão de decisões no Adobe Experience Platform.
feature: Offers
topic: Integrations
role: User
level: Beginner
exl-id: 51830c63-fa88-47e7-8605-192297fcf6b8
source-git-commit: b06b545d377fcd1ffe6ed218badeb94c1bb85ef2
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 56%

---

# Introdução aos eventos da Gestão de decisões {#monitor-offer-events}

Cada vez que a Gestão de decisões toma uma decisão para determinado perfil, as informações relacionadas a esses eventos são automaticamente enviadas para a Adobe Experience Platform.

Isso permite exportar esses dados para analisá-los no seu próprio sistema de relatórios. Você também pode aproveitar o Adobe Experience Platform [Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=pt-BR) em combinação com outras ferramentas para fins de análise e relatório aprimorados.

Os conjuntos de dados contendo eventos de Gestão de decisão podem ser acessados no Adobe Experience Platform **[!UICONTROL Conjuntos de dados]** menu. Um conjunto de dados é criado automaticamente no provisionamento para cada uma de suas instâncias.

![](../assets/events-datasets-list.png)

Esses conjuntos de dados são baseados na variável **[!UICONTROL ODE DecisionEvents]** esquema, que contém todos os campos XDM necessários para enviar informações da Gestão de decisões para a Adobe Experience Platform.

>[!NOTE]
>
>Observe que os conjuntos de dados do ODE DecisionEvents são **conjuntos de dados que não são de perfil**, o que significa que eles não podem ser assimilados no Experience Platform para uso pelo perfil do cliente em tempo real.

**Tópicos relacionados:**

* [Informações importantes sobre eventos da Gestão de decisões](../reports/key-information.md)
* [Acessar campos XDM de eventos](../reports/xdm-fields.md)
