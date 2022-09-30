---
title: Trabalhar com o Customer Journey Analytics
description: Introdução ao Customer Journey Analytics
feature: Reporting
topic: Content Management
role: User
level: Beginner
source-git-commit: bf4857f63b44d557304ef05e490fe6659f0ad888
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 9%

---

# Trabalhar com o [!DNL Customer Journey Analytics] {#cja-ajo}

![](assets/cja.png)

Depois de criar a jornada em [!DNL Journey Optimizer], é possível importar os dados do cliente para o [!DNL Customer Journey Analytics] para iniciar relatórios e entender o impacto de cada interação que um cliente tem com suas jornadas.

➡️ [Customer Journey Analytics do Discover](https://docs.adobe.com/content/help/pt-BR/experience-cloud/user-guides/home.translate.html){target=&quot;_blank&quot;}

Antes de usar [!DNL Customer Journey Analytics] para suas jornadas, você deve primeiro configurar essa integração:

1. [Criar uma conexão](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=pt-BR) em [!DNL Customer Journey Analytics] com o **[!UICONTROL Conjunto de dados]** você deseja enviar para a plataforma.

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
