---
title: Administração e configurações
description: Saiba mais sobre administração e diretrizes de configurações
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Configurações do aplicativo
topic: Administração
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 50%

---

# Configurar jornadas

Para enviar mensagens com o jornada, você precisa configurar **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** e **[!UICONTROL Actions]**.

![](../assets/admin-menu.png)

## Fontes de dados

A configuração da Fonte de Dados permite definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas. [Saiba mais](../../using/datasource/about-data-sources.md)

## Eventos

Os eventos permitem acionar as jornadas de forma unitária para enviar mensagens, em tempo real, ao indivíduo que flui para a jornada.

Na configuração do evento, configure os eventos esperados nas jornadas. Os dados de entrada dos eventos são normalizados de acordo com o Adobe Experience Data Model (XDM). Os eventos vêm das APIs de assimilação de streaming para eventos autenticados e não autenticados (como eventos do Adobe Mobile SDK). [Saiba mais](../../using/event/about-events.md)

## Ações

Os recursos de mensagem do Journey Optimizer são incorporados: você só precisa criar o conteúdo e publicar a mensagem. Se você estiver usando um sistema de terceiros para enviar mensagens, é possível criar uma ação personalizada. [Saiba mais](../../using/action/action.md)

## Procurar nos campos da Adobe Experience Platform {#friendly-names-display}

Ao definir [carga útil do evento](../event/about-creating.md#define-the-payload-fields), [carga útil do grupo de campos](../datasource/configure-data-sources.md#define-field-groups) e selecionar campos no [editor de expressão](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/expressionadvanced.html?lang=pt-BR){target=&quot;_blank&quot;}, o nome de exibição é exibido além do nome do campo. Essas informações são recuperadas a partir da definição do schema no modelo de dados de experiência.

Se descritores como &quot;xdm:alternateDisplayInfo&quot; forem fornecidos durante a configuração de schemas, os nomes de usuário simples substituirão os nomes de exibição. É especialmente útil ao trabalhar com &quot;eVars&quot; e campos genéricos. Você pode configurar descritores de nome amigáveis por meio de uma chamada de API. Para obter mais informações, consulte o [Guia do desenvolvedor do Registro de Schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=pt-BR){target=&quot;_blank&quot;}.

![](../assets/xdm-from-descriptors.png)

Se um nome simples estiver disponível, o campo será exibido como `<friendly-name>(<name>)`. Se nenhum nome simples estiver disponível, o nome de exibição será exibido, por exemplo `<display-name>(<name>)`. Se nenhum deles estiver definido, somente o nome técnico do campo será exibido `<name>`.

>[!NOTE]
>
>Os nomes simples não são recuperados ao selecionar campos de uma união de schemas.