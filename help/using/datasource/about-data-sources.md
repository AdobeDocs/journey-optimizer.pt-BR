---
title: Sobre fontes de dados
description: Saiba como configurar uma fonte de dados
feature: Fontes de dados
topic: Administração
role: Admin
level: Intermediate
source-git-commit: d69779418d50fdc4b75cc777b27a62392d1634a0
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 72%

---

# Sobre fontes de dados {#concept_s1s_dqt_52b}

>[!CONTEXTUALHELP]
>id="jo_datasources"
>title="Sobre fontes de dados"
>abstract="A configuração da fonte de dados é sempre executada por um usuário técnico. A configuração da fonte de dados permite definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas para: definição de condição, parâmetro e dados de personalização em ações, definição de espera personalizada e definição de fuso horário personalizado."

A configuração da fonte de dados permite definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas, para:

* [definição de condição](../building-journeys/condition-activity.md)
* parâmetros e dados de personalização em [ações](../action/action.md)
* [definição de espera personalizada](../building-journeys/wait-activity.md#custom)
* [definição de fuso horário](../building-journeys/timezone-management.md)

Essa configuração não é necessária se suas jornadas só usarem os dados locais provenientes de uma carga útil do evento. Por exemplo, se a jornada for composta de um evento seguido por uma atividade de mensagem que usa somente os dados do evento, não será necessário configurar uma fonte de dados.

Há dois tipos de fontes de dados:

* A fonte de dados pré-configurada da Adobe Experience Platform que define a conexão com o Serviço de perfil do cliente em tempo real. Essa fonte de dados é integrada. Consulte [esta página](../datasource/adobe-experience-platform-data-source.md).
* As fontes de dados externas que permitem definir uma conexão com sistemas externos. Essas são as que você pode criar. Consulte [esta página](../datasource/external-data-sources.md).

Para cada fonte de dados, você define as informações que serão recuperadas usando grupos de campos. Grupos de campos são conjuntos de campos que podem ser recuperados de uma fonte de dados. Consulte [esta página](../datasource/configure-data-sources.md#define-field-groups).

>[!NOTE]
>
>As relações de esquema agora são suportadas em fontes de dados.

Para obter mais informações sobre como configurar uma Fonte de Dados do Adobe Experience Platform e uma fonte de dados externa e como localizar e usar dados em uma jornada, assista a este [vídeo tutorial](https://experienceleague.adobe.com/docs/journey-orchestration-learn/tutorials/configure-data-sources.html){target=&quot;_blank&quot;}.
