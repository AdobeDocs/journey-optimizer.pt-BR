---
solution: Journey Optimizer
product: journey optimizer
title: Configurar jornadas
description: Saiba como configurar Fontes de dados, Eventos e Ações
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: configuração, jornada, painel, fontes de dados, eventos, ações
exl-id: c144d44f-031f-4ca2-800e-d3878af400a5
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 65%

---

# Configurar jornadas {#configure-journeys}

>[!CONTEXTUALHELP]
>id="ajo_journey_configuration_dashboard"
>title="Sobre a configuração de jornada"
>abstract="Para enviar mensagens com jornadas, é necessário configurar as Fontes de dados, os Eventos e as Ações. As fontes de dados permitem definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas, por exemplo, em suas condições. Os eventos permitem acionar as jornadas quando um evento é recebido. As ações personalizadas permitem conectar-se a um sistema de terceiros para enviar mensagens. Se estiver usando recursos de mensagem integrada do Journey Optimizer, não será necessário configurar uma ação."

Para enviar mensagens com jornadas, você precisa configurar as **[!UICONTROL Fontes de Dados]**, os **[!UICONTROL Eventos]** e as **[!UICONTROL Ações]**.

![](assets/admin-menu.png)

## Fontes de dados {#data-sources}

A configuração do Data Source permite definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas. [Saiba mais](../../using/datasource/about-data-sources.md)

## Eventos {#events}

Os Eventos permitem acionar as jornadas de forma unitária para enviar mensagens, em tempo real, ao indivíduo que flui para a jornada.

Na configuração do evento, configure os eventos esperados nas jornadas. Os dados de entrada dos eventos são padronizados de acordo com o Adobe Experience Data Model (XDM). Os eventos vêm das APIs de ingestão de streaming para eventos autenticados e não autenticados (como eventos do SDK móvel da Adobe). [Saiba mais](../../using/event/about-events.md)

## Ações {#actions}

Os recursos de mensagem do Journey Optimizer são incorporados: basta adicionar uma atividade de ação de canal à jornada. Se você estiver usando um sistema de terceiros para enviar mensagens, poderá criar uma ação personalizada. [Saiba mais](../../using/action/action.md)

## Navegar pelos campos do Adobe Experience Platform {#friendly-names-display}

Ao definir a [carga útil do evento](../event/about-creating.md#define-the-payload-fields), [carga útil do grupo de campo](../datasource/configure-data-sources.md#define-field-groups) e selecionar campos no [editor de expressões](../building-journeys/expression/expressionadvanced.md), o nome de exibição é exibido além do nome do campo. Essas informações são recuperadas a partir da definição do schema no modelo de dados de experiência.

Se descritores como &quot;xdm:alternateDisplayInfo&quot; forem fornecidos durante a configuração de schemas, os nomes de usuário simples substituirão os nomes de exibição. É especialmente útil ao trabalhar com &quot;eVars&quot; e campos genéricos. Você pode configurar descritores de nome amigáveis por meio de uma chamada de API. Para obter mais informações, consulte o [guia do desenvolvedor do Registro de Esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=pt-BR){target="_blank"}.

![](assets/xdm-from-descriptors.png)

Se um nome simples estiver disponível, o campo será exibido como `<friendly-name>(<name>)`. Se nenhum nome simples estiver disponível, o nome de exibição será exibido, por exemplo `<display-name>(<name>)`. Se nenhum deles estiver definido, somente o nome técnico do campo será exibido `<name>`.

>[!NOTE]
>
>Os nomes simples não são recuperados ao selecionar campos de uma união de schemas.
