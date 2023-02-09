---
solution: Journey Optimizer
product: journey optimizer
title: Trabalhar com o Customer Journey Analytics
description: Introdução ao Customer Journey Analytics
feature: Reporting
topic: Content Management
role: User
level: Beginner
exl-id: 5349b0cf-da4e-458c-89be-c75a38e4721a
source-git-commit: 928ad6822efbe95c0ddf5456531d92be8b4bed75
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 8%

---

# Trabalhar com o [!DNL Customer Journey Analytics] {#cja-ajo}


[!DNL Journey Optimizer] integração com [!DNL Customer Journey Analytics] O fornece uma visualização holística de todas as jornadas com distribuição automatizada de relatórios e visualizações personalizadas dos dados.

![](assets/cja.png)

Depois de criar a jornada em [!DNL Journey Optimizer], é possível importar os dados do cliente para o [!DNL Customer Journey Analytics] para iniciar relatórios e entender o impacto de cada interação que um cliente tem com suas jornadas.

➡️ [Customer Journey Analytics do Discover](https://docs.adobe.com/content/help/pt-BR/experience-cloud/user-guides/home.translate.html){target="_blank"}

Antes de usar [!DNL Customer Journey Analytics] para suas jornadas, você deve primeiro configurar essa integração:

1. [Criar uma conexão](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=pt-BR) em [!DNL Customer Journey Analytics] com o **[!UICONTROL Conjunto de dados]** você deseja enviar para o Adobe Experience Platform.

   O seguinte [!DNL Journey Optimizer] pode ser configurado:
   * [Evento de etapa de Jornada](../data/datasets-query-examples.md#journey-step-event): permite visualizar quem entra em suas jornadas e até que ponto elas chegam.
   * [Conjuntos de dados de feedback/rastreamento de mensagens](../data/datasets-query-examples.md#message-feedback-event-dataset): permite exibir informações do delivery sobre as mensagens enviadas por [!DNL Journey Optimizer].
   * [Conjuntos de dados de entidade e Jornada](../data/datasets-query-examples.md#entity-dataset): O permite pesquisar nomes amigáveis e usá-los no relatório.

1. [Criar uma visualização de dados](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=pt-BR) para configurar as dimensões e métricas que deseja usar no relatório.

   Você pode criar métricas específicas do Journey Optimizer para refletir melhor seus dados de jornadas. [Saiba mais](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics)


Usando [!DNL Journey Optimizer] com [!DNL Customer Journey Analytics] pode levar a alguma discrepância nos dados de relatório causada por:

* **Ambos [!DNL Journey Optimizer] e [!DNL Customer Journey Analytics] sincronizar dados do Armazenamento Azure Data Lake (ADLS) para relatórios.**

   O tempo de processamento dos dados recebidos pode ser um pouco diferente entre os produtos. Devido a isso, os dados podem não corresponder ao exibir relatórios de uma determinada data para o dia atual. Para reduzir a discrepância, use intervalos de datas excluindo o dia atual.

* **Em [!DNL Journey Optimizer] Relatórios, Métrica enviada também inclui Métrica de nova tentativa.**

   **[!UICONTROL Tentativas]** não será incluído em **[!UICONTROL Enviado]** em [!DNL Customer Journey Analytics]. Isso causará [!DNL Customer Journey Analytics] **[!UICONTROL Enviado]** métricas para mostrar valores mais baixos que [!DNL Journey Optimizer]. No entanto, os dados de nova tentativa são convertidos para o **[!UICONTROL Mensagens enviadas com êxito]** ou **[!UICONTROL Rejeições]** métrica.
Para reduzir a discrepância, use intervalos de datas de uma semana atrás ou até mesmo posterior.

* **Os relatórios estão sendo veiculados a partir de uma fonte de dados diferente.**

   Isso pode levar a discrepâncias de dados de 1 a 2% entre produtos.
