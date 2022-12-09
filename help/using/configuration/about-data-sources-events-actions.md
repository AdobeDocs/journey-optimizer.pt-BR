---
solution: Journey Optimizer
product: journey optimizer
title: Configurar jornadas
description: Saiba como configurar fontes de dados, eventos e ações
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: c144d44f-031f-4ca2-800e-d3878af400a5
source-git-commit: f04454860ebe597d3306e62b58de5f32e08342ee
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# Configurar jornadas {#configure-journeys}

>[!CONTEXTUALHELP]
>id="ajo_journey_configuration_dashboard"
>title="Sobre a configuração da jornada"
>abstract="Para enviar mensagens com jornadas, é necessário configurar as Fontes de dados, os Eventos e as Ações. As fontes de dados permitem definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas, por exemplo, em suas condições. Os eventos permitem acionar suas jornadas quando um evento é recebido. As ações personalizadas permitem conectar-se a um sistema de terceiros para enviar suas mensagens. Se estiver usando os recursos de mensagem incorporados do Journey Otimizer, não será necessário configurar uma ação."

Para enviar mensagens com jornadas, é necessário configurar **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** e **[!UICONTROL Actions]**.

![](assets/admin-menu.png)

## Fontes de dados {#data-sources}

A configuração da Fonte de Dados permite definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas. [Saiba mais](../../using/datasource/about-data-sources.md)

## Eventos {#events}

Os eventos permitem acionar suas jornadas de forma unitária para enviar mensagens, em tempo real, para o indivíduo que flui para a jornada.

Na configuração do evento, você configura os eventos esperados nas jornadas. Os dados de entrada dos eventos são normalizados de acordo com o Adobe Experience Data Model (XDM). Os eventos vêm das APIs de assimilação de fluxo para eventos autenticados e não autenticados (como eventos do SDK do Adobe Mobile). [Saiba mais](../../using/event/about-events.md)

## Ações {#actions}

Os recursos de mensagem do Journey Otimizer são incorporados: você só precisa adicionar uma atividade de ação de canal à jornada. Se você estiver usando um sistema de terceiros para enviar mensagens, é possível criar uma ação personalizada. [Saiba mais](../../using/action/action.md)

## Navegue pelos campos da Adobe Experience Platform {#friendly-names-display}

Ao definir [carga do evento](../event/about-creating.md#define-the-payload-fields), [carga do grupo de campos](../datasource/configure-data-sources.md#define-field-groups) e selecionar campos na [editor de expressão](../building-journeys/expression/expressionadvanced.md), o nome de exibição é exibido além do nome do campo. Essas informações são recuperadas da definição do schema no Modelo de dados de experiência.

Se descritores como &quot;xdm:alternativeDisplayInfo&quot; forem fornecidos durante a configuração de schemas, os nomes amigáveis substituirão os nomes de exibição. É especialmente útil ao trabalhar com &quot;eVars&quot; e campos genéricos. Você pode configurar descritores de nome amigáveis por meio de uma chamada de API. Para obter mais informações, consulte o [Guia do desenvolvedor do Registro de Schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html){target=&quot;_blank&quot;}.

![](assets/xdm-from-descriptors.png)

Se um nome amigável estiver disponível, o campo será exibido como `<friendly-name>(<name>)`. Se nenhum nome simples estiver disponível, o nome de exibição será exibido, por exemplo `<display-name>(<name>)`. Se nenhum deles estiver definido, somente o nome técnico do campo será exibido `<name>`.

>[!NOTE]
>
>Os nomes amigáveis não são recuperados ao selecionar campos de uma união de schemas.
