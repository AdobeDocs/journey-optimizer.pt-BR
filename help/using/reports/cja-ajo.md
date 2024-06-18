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
source-git-commit: c2f2dde40385f56ea86be15a5857fa9e5e2e2fed
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 6%

---

# Trabalhar com [!DNL Customer Journey Analytics] {#cja-ajo}


[!DNL Journey Optimizer] integração com [!DNL Customer Journey Analytics] O fornece uma visualização integral de todas as suas jornadas com distribuição automatizada de relatórios e visualizações personalizadas dos dados.

![](assets/cja.png)

Depois de criar a jornada no [!DNL Journey Optimizer], você pode importar os dados do cliente para o [!DNL Customer Journey Analytics] para iniciar relatórios e entender o impacto de cada interação que um cliente tem com suas jornadas.

➡️ [Descubra o Customer Journey Analytics](https://docs.adobe.com/content/help/pt-BR/experience-cloud/user-guides/home.translate.html){target="_blank"}

>[!NOTE]
>
>Além dessa integração, você também pode exportar o conteúdo dos conjuntos de dados do Adobe Journey Optimizer para locais de armazenamento na nuvem e usar essas informações para fins de relatório ou análise. [Saiba como exportar conjuntos de dados para locais de armazenamento na nuvem](../data/export-datasets.md)
>
>Observe que o recurso de exportação de conjuntos de dados está atualmente na versão beta e disponível para todos os usuários do Adobe Journey Optimizer. Entre em contato com seu representante da Adobe para obter acesso aos destinos, caso ainda não o tenha.

Antes de usar [!DNL Customer Journey Analytics] para suas jornadas, você deve primeiro configurar essa integração:

1. [Criar uma conexão](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html) in [!DNL Customer Journey Analytics] com o **[!UICONTROL Conjunto de dados]** que deseja enviar para o Adobe Experience Platform.

   As seguintes [!DNL Journey Optimizer] pode ser configurado:
   * [Jornada evento de etapa](../data/datasets-query-examples.md#journey-step-event): permite visualizar quem entra nas jornadas e até que ponto elas chegam.
   * [Conjuntos de dados de Feedback/Rastreamento de mensagens](../data/datasets-query-examples.md#message-feedback-event-dataset): permite exibir informações de delivery sobre suas mensagens enviadas pelo [!DNL Journey Optimizer].
   * [Entidade e conjuntos de dados de Jornada](../data/datasets-query-examples.md#entity-dataset): permite pesquisar nomes amigáveis e usá-los em seus relatórios.

1. [Criar uma visualização de dados](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=pt-BR) para configurar as dimensões e métricas que deseja usar no relatório.

   Você pode criar métricas específicas do Journey Optimizer para refletir melhor os dados da sua jornada. [Saiba mais](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics)

Usar [!DNL Journey Optimizer] com [!DNL Customer Journey Analytics] pode levar a alguma discrepância nos dados de relatórios causada por:

* **Ambos [!DNL Journey Optimizer] e [!DNL Customer Journey Analytics] sincronizar dados do Azure Data Lake Storage (ADLS) para relatórios.**

  O tempo de processamento dos dados recebidos pode ser um pouco diferente entre os produtos. Por isso, os dados podem não corresponder ao exibir relatórios de uma determinada data para o dia atual. Para reduzir a discrepância, use intervalos de datas, exceto o dia atual.

* **Entrada [!DNL Journey Optimizer] Relatórios, a métrica Enviado também inclui a métrica Repetir.**

  **[!UICONTROL Tentativas]** não serão incluídos em **[!UICONTROL Enviado]** métrica em [!DNL Customer Journey Analytics]. Isso causará [!DNL Customer Journey Analytics] **[!UICONTROL Enviado]** métricas para mostrar valores menores que [!DNL Journey Optimizer]. No entanto, os dados de nova tentativa são convertidos para o **[!UICONTROL Mensagens enviadas com sucesso]** ou **[!UICONTROL Rejeições]** métrica.
Para reduzir a discrepância, use intervalos de datas de uma semana atrás ou até mesmo mais tarde.

* **Os relatórios estão sendo distribuídos a partir de uma fonte de dados diferente.**

  Isso pode levar a discrepâncias de dados entre 1 e 2% entre produtos.
