---
title: Sobre fontes de dados
description: Saiba como configurar uma fonte de dados
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
exl-id: e0cb261f-7cf7-42de-8e56-576492e3b5cc
source-git-commit: d9f7c64358be3c3355337ba0db12e5b8c17bba4c
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 74%

---

# Sobre fontes de dados {#about-data-sources}

>[!CONTEXTUALHELP]
>id="jo_datasources"
>title="Sobre fontes de dados"
>abstract="A configuração da fonte de dados é sempre executada por um usuário técnico. A configuração da fonte de dados permite definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas para: definição de condição, parâmetro e dados de personalização em ações, definição de espera personalizada e definição de fuso horário personalizado."

A configuração da fonte de dados permite definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas, para:

* [definição de condição](../building-journeys/condition-activity.md)
* parâmetros e dados de personalização em [ações](../action/action.md)
* [definição de espera personalizada](../building-journeys/wait-activity.md#custom)
* [definição de fuso horário](../building-journeys/timezone-management.md)

➡️ [Descubra este recurso no vídeo](#video)

Essa configuração não é necessária se suas jornadas só usarem os dados locais provenientes de uma carga útil do evento. Por exemplo, se a jornada for composta de um evento seguido por uma atividade de mensagem que usa somente os dados do evento, não será necessário configurar uma fonte de dados.

Há dois tipos de fontes de dados:

* A fonte de dados pré-configurada da Adobe Experience Platform que define a conexão com o Serviço de perfil do cliente em tempo real. Essa fonte de dados é integrada. Consulte [esta página](../datasource/adobe-experience-platform-data-source.md).
* As fontes de dados externas que permitem definir uma conexão com sistemas externos. Essas são as que você pode criar. Consulte [esta página](../datasource/external-data-sources.md).

Para cada fonte de dados, você define as informações que serão recuperadas usando grupos de campos. Grupos de campos são conjuntos de campos que podem ser recuperados de uma fonte de dados. Consulte [esta página](../datasource/configure-data-sources.md#define-field-groups).

>[!NOTE]
>
>As relações de esquema agora são suportadas em fontes de dados.

Para obter mais informações sobre como configurar uma fonte de dados da Adobe Experience Platform e uma fonte de dados externa e como localizar e usar dados em uma jornada, assista a isso [vídeo tutorial](https://experienceleague.adobe.com/docs/journey-orchestration-learn/tutorials/configure-data-sources.html){target=&quot;_blank&quot;}.

## Vídeo tutorial {#video}

Entenda o que é uma fonte de dados e saiba como configurar fontes de dados da Experience Platform e externas.

>[!VIDEO](https://video.tv.adobe.com/v/334256?quality=12)

