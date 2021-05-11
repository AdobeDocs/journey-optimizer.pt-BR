---
title: Introdução aos eventos de Gerenciamento de decisões
description: Saiba como criar relatórios de Gerenciamento de decisões no Adobe Experience Platform.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 47%

---

# Introdução aos eventos de Gerenciamento de decisões {#monitor-offer-events}

Sempre que o Gerenciamento de decisões tomar um determinado perfil, as informações relacionadas a esses eventos são automaticamente enviadas para a Adobe Experience Platform.

Isso permite exportar esses dados para analisá-los no seu próprio sistema de relatórios. Você também pode aproveitar o Adobe Experience Platform [Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=pt-BR) em combinação com outras ferramentas para fins de análise e relatório aprimorados.

Os conjuntos de dados que contêm eventos de Gerenciamento de decisões podem ser acessados no menu Adobe Experience Platform **[!UICONTROL Datasets]** . Um conjunto de dados é criado automaticamente no provisionamento para cada uma de suas instâncias.

![](../assets/events-datasets-list.png)

Esses conjuntos de dados são baseados no esquema **[!UICONTROL ODE DecisionEvents]**, que contém todos os campos XDM necessários para enviar informações do Gerenciamento de decisão para a Adobe Experience Platform.

>[!NOTE]
>
>Observe que os conjuntos de dados do ODE DecisionEvents são **conjuntos de dados que não são de perfil**, o que significa que eles não podem ser assimilados no Experience Platform para uso pelo perfil do cliente em tempo real.

**Tópicos relacionados:**

* [Informações-chave sobre eventos do Gerenciamento de decisões](../reports/key-information.md)
* [Acessar campos XDM de eventos](../reports/xdm-fields.md)
