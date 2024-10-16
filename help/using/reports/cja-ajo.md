---
solution: Journey Optimizer
product: journey optimizer
title: Trabalhar com o Customer Journey Analytics
description: Introdução ao Customer Journey Analytics
feature: Reporting, Integrations
topic: Content Management
role: User
level: Beginner
exl-id: 5349b0cf-da4e-458c-89be-c75a38e4721a
source-git-commit: 47482adb84e05fe41eb1c50479a8b50e00469ec4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Configurar manualmente o [!DNL Customer Journey Analytics] {#cja-ajo}

A integração do [!DNL Journey Optimizer] com o [!DNL Customer Journey Analytics] fornece uma visão holística de todas as suas jornadas com distribuição automatizada de relatórios e visualizações personalizadas dos dados.

A seção a seguir descreve como utilizar manualmente os dados gerados pela Journey Optimizer para uma análise detalhada no Customer Journey Analytics. Observe que essa integração pode ser configurada automaticamente. [Saiba mais](report-gs-cja.md)

![](assets/cja.png)

Depois de criar sua jornada no [!DNL Journey Optimizer], você pode importar os dados do cliente para o [!DNL Customer Journey Analytics] para iniciar os relatórios e entender o impacto de cada interação que um cliente tem com suas jornadas.

➡️ [Customer Journey Analytics de Descoberta](https://experienceleague.adobe.com/en/docs/analytics-platform/using/integrations/ajo#manually-configure-a-data-view-to-be-used-with-journey-optimizer){target="_blank"}

>[!NOTE]
>
>Além dessa integração, você também pode exportar o conteúdo dos conjuntos de dados do Adobe Journey Optimizer para locais de armazenamento na nuvem e usar essas informações para fins de relatório ou análise. [Saiba como exportar conjuntos de dados para locais de armazenamento na nuvem](../data/export-datasets.md)
>
>Observe que o recurso de exportação de conjuntos de dados está atualmente na versão beta e disponível para todos os usuários do Adobe Journey Optimizer. Entre em contato com seu representante da Adobe para obter acesso aos destinos, caso ainda não o tenha.

Antes de usar o [!DNL Customer Journey Analytics] para suas jornadas, você deve primeiro configurar esta integração:

1. [Crie uma conexão](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html) em [!DNL Customer Journey Analytics] com o **[!UICONTROL Conjunto de Dados]** que você deseja enviar para a Adobe Experience Platform.

   O seguinte [!DNL Journey Optimizer] pode ser configurado:
   * [Evento de Etapa de Jornada](../data/datasets-query-examples.md#journey-step-event): permite ver quem entra nas jornadas e até que ponto elas chegam.
   * [Conjuntos de dados de Rastreamento/Feedback de Mensagens](../data/datasets-query-examples.md#message-feedback-event-dataset): permite exibir informações de entrega sobre suas mensagens enviadas por meio de [!DNL Journey Optimizer].
   * [Conjuntos de dados de entidade e Jornada](../data/datasets-query-examples.md#entity-dataset): permite pesquisar nomes amigáveis e usá-los em seus relatórios.

1. [Crie uma visualização de dados](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=pt-BR) para configurar as dimensões e métricas que deseja usar no relatório.

   Você pode criar métricas específicas do Journey Optimizer para refletir melhor os dados da sua jornada. [Saiba mais](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics)

O uso de [!DNL Journey Optimizer] com [!DNL Customer Journey Analytics] pode levar a alguma discrepância nos dados do relatório causada por:

* **Os dados de sincronização [!DNL Journey Optimizer] e [!DNL Customer Journey Analytics] do Azure Data Lake Storage (ADLS) para relatórios.**

  O tempo de processamento dos dados recebidos pode ser um pouco diferente entre os produtos. Por isso, os dados podem não corresponder ao exibir relatórios de uma determinada data para o dia atual. Para reduzir a discrepância, use intervalos de datas, exceto o dia atual.

* **Em [!DNL Journey Optimizer] relatórios, a métrica Enviado também inclui a métrica Repetir.**

  **[!UICONTROL Tentativas]** não serão incluídas na métrica **[!UICONTROL Enviadas]** em [!DNL Customer Journey Analytics]. Isso fará com que as métricas [!DNL Customer Journey Analytics] **[!UICONTROL Enviadas]** mostrem valores menores que [!DNL Journey Optimizer]. No entanto, os dados de nova tentativa são convertidos para a métrica **[!UICONTROL Mensagens enviadas com êxito]** ou **[!UICONTROL Rejeições]**.
Para reduzir a discrepância, use intervalos de datas de uma semana atrás ou até mesmo mais tarde.

* **Os relatórios estão sendo fornecidos por uma fonte de dados diferente.**

  Isso pode levar a discrepâncias de dados entre 1 e 2% entre produtos.
