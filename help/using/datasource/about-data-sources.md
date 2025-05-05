---
solution: Journey Optimizer
product: journey optimizer
title: Introdução a fontes de dados
description: Saiba como começar a usar fontes de dados
feature: Journeys, Data Sources
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: dados, origem, jornada, plataforma
exl-id: e0cb261f-7cf7-42de-8e56-576492e3b5cc
source-git-commit: d498f32a42b13bfdee20f32a589dd31c77d88fa8
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 52%

---

# Introdução a fontes de dados {#about-data-sources}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_list"
>title="Sobre fontes de dados"
>abstract="A configuração da fonte de dados é sempre executada por um usuário técnico. A configuração da fonte de dados permite definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas para: definição de condição, parâmetro e dados de personalização em ações, definição de espera personalizada e definição de fuso horário personalizado."

A configuração da fonte de dados permite definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas, para:

* [definição de condição](../building-journeys/condition-activity.md)
* parâmetros e dados de personalização em [ações](../action/action.md)
* [definição de espera personalizada](../building-journeys/wait-activity.md#custom)
* [definição de fuso horário](../building-journeys/timezone-management.md)

➡️ [Descubra este recurso no vídeo](#video)

Essa configuração não é necessária se suas jornadas só usarem os dados locais provenientes de uma carga útil do evento. Por exemplo, se sua jornada for composta por um evento seguido por uma atividade de ação de canal que usa apenas dados do evento, não será necessário configurar uma fonte de dados.

Há dois tipos de fontes de dados:

* A fonte de dados do Adobe Experience Platform **pré-configurada** que define a conexão com o Serviço de Perfil do Cliente em Tempo Real. Essa fonte de dados é integrada. Consulte [esta página](../datasource/adobe-experience-platform-data-source.md).
* As fontes de dados **externas** que permitem definir uma conexão com sistemas externos. Essas são as que você pode criar. Consulte [esta página](../datasource/external-data-sources.md).

>[!NOTE]
>
>Como as respostas agora são compatíveis, você deve usar ações personalizadas em vez de fontes de dados para casos de uso de fontes de dados externas. Para obter mais informações sobre respostas, consulte esta [seção](../action/action-response.md)

Para cada fonte de dados, você define as informações que serão recuperadas usando grupos de campos. Grupos de campos são conjuntos de campos que podem ser recuperados de uma fonte de dados. Consulte [esta página](../datasource/configure-data-sources.md#define-field-groups).

>[!NOTE]
>
>Não há suporte para relações de esquema em fontes de dados.

Para obter mais informações sobre como configurar uma Adobe Experience Platform Data Source e uma fonte de dados externa e como localizar e usar dados em uma jornada, assista a este [tutorial em vídeo](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/journey-configuration/configure-data-sources.html?lang=pt-BR){target="_blank"}.

## Vídeo tutorial {#video}

Entenda o que é uma fonte de dados e saiba como configurar fontes de dados da Experience Platform e externas.

>[!VIDEO](https://video.tv.adobe.com/v/334256?quality=12)

