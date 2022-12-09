---
solution: Journey Optimizer
product: journey optimizer
title: Sobre fontes de dados
description: Saiba como configurar uma fonte de dados
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
exl-id: e0cb261f-7cf7-42de-8e56-576492e3b5cc
source-git-commit: 0b19af568b33d29f4b35deeab6def17919cfe824
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 0%

---

# Sobre fontes de dados {#about-data-sources}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_list"
>title="Sobre fontes de dados"
>abstract="A configuração da fonte de dados é sempre executada por um usuário técnico. A configuração da fonte de dados permite definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas, para: definição de condição, parâmetro e dados de personalização em ações, definição de espera personalizada, definição de fuso horário."

A configuração da fonte de dados permite definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas, para:

* [definição de condição](../building-journeys/condition-activity.md)
* parâmetros e dados de personalização em [ações](../action/action.md)
* [definição de espera personalizada](../building-journeys/wait-activity.md#custom)
* [definição de fuso horário](../building-journeys/timezone-management.md)

➡️ [Descubra este recurso no vídeo](#video)

Essa configuração não é necessária se suas jornadas utilizarem somente os dados locais provenientes de uma carga útil do evento. Por exemplo, se sua jornada for composta por um evento seguido por uma atividade de ação de canal que usa somente os dados do evento, não será necessário configurar uma fonte de dados.

Há dois tipos de fontes de dados:

* A fonte de dados pré-configurada da Adobe Experience Platform que define a conexão com o Serviço de perfil do cliente em tempo real. Essa é uma fonte de dados integrada. Consulte [esta página](../datasource/adobe-experience-platform-data-source.md).
* As fontes de dados externas que permitem definir uma conexão com sistemas externos. Essas são as que você pode criar. Consulte [esta página](../datasource/external-data-sources.md).

Para cada fonte de dados, você define as informações a serem recuperadas usando grupos de campos. Grupos de campos são conjuntos de campos que podem ser recuperados de uma fonte de dados. Consulte [esta página](../datasource/configure-data-sources.md#define-field-groups).

>[!NOTE]
>
>As relações de esquema não são suportadas em fontes de dados.

Para obter mais informações sobre como configurar uma fonte de dados da Adobe Experience Platform e uma fonte de dados externa, e como localizar e usar dados em uma jornada, assista a isso [vídeo tutorial](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/journey-configuration/configure-data-sources.html){target=&quot;_blank&quot;}.

## Vídeo tutorial {#video}

Entenda o que é uma fonte de dados e saiba como configurar a Experience Platform e fontes de dados externas.

>[!VIDEO](https://video.tv.adobe.com/v/334256?quality=12)

